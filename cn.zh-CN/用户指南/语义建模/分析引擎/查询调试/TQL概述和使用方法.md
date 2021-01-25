# TQL概述和使用方法

TQL\(tag querylanguage\)整合分析提供的基于OLP的标签查询语言，实现基于标签的分析查询。屏蔽了物理模型和存储，使用户更容易的使用标签用于分析查询。兼容SQL ANSIC SELECT标准。

TQL只有select查询，语法定义如下:

```
SELECT [distinct] entityCode.tagCode, ...
FROM entityCode
where SQL_WHERE_CONDITION
group by SQL_GROUP_EXPR
[having SQL_HAVING_EXPR]
order by SQL_ORDER_EXPR
limit LIMIT, OFFSET
```

标签一般定义为:entity.tag

关系一般定义为:link.entity.tag

## 简单查询

标签select的列不支持select \*,TQL的查询语法兼容标准的SQL查询语法。

1.  简单select

    ```
    select user.age from user where user.id > 0;
    ```

2.  group by

    ```
    select count(user.category),user.category from user 
    group by user.category
    ```

3.  window函数

    ```
    select count(user.category) over
    ( partition by user.category order by user.age) from user
    ```

4.  使用变量

    ```
    select user.age from user where user.age > ${age, number}
    ```


## TQL使用举例

比如:

```
select user.name, user.gender from user where user.gender = 'man'
```

比如上句查询语句，通过将'man' 设定为一个参数。

```
select user.name, user.gender from user where user.gender = ${gender, string, 'man'}'
```

上面的变量有以下几层含义：

-   $\{...\}：在语法上，$符号后面的内容用\{\}包裹，代表着此处是一个变量;
-   gender：代表此变量的名字为gender;
-   string：代表次变量的类型为string,可支持string,bool,number,tag三种，如果是tag，则为标签变量;
-   'man'：代表了默认值，当调用api时，没有传入参数则会默认设置为'man'。

特别的，类型和默认值都可以省略，比如:

```
${gender, string}           ---> ok
${gender}                   ---> ok
${gender,'man'}             ---> ok
${}                         ---> error
${gender, string, bad, bad} ---> error
```

## 普通变量

定义：$\{VAR\_NAME\[,TYPE, DEFAULT\_VALUE\]\}

替换查询变量

```
-- 变量名为name,类型为string，默认是jack
select user.name from user where user.name = ${name, string, 'jack'}
-- 不设置默认值，如果调用api的时候不指定name的值，查询会报错
select user.name from user where user.name = ${name, string}
```

替换select列表中的标签

```
-- 变量可以是查询列表中的column值，即标签的值
select user.name, ${name} from user where user.name = 'jack' 
-- 可以设置默认值, 注意并没有引号
select user.name, ${name, user.gender} from user where user.name = 'jack' 
-- 设置的类型会被忽略,效果和上一条一样
select user.name, ${name, string, user.gender} from user where user.name = 'jack'
```

替换order by，group by，limit等

```
-- 设置group by的变量
select user.name, user.gender from user where user.name = 'jack' group by ${g_var, user.name} 
-- 设置order by的变量
select user.name, user.gender from user where user.name = 'jack' order by ${o_var} 
-- 设置limit的变量
select user.name, user.gender from user where user.name = 'jack' limit ${l_var, 1000}
```

替换order by，group by，limit等

```
-- 设置group by的变量
select user.name, user.gender from user where user.name = 'jack' group by ${g_var, user.name} 
-- 设置order by的变量
select user.name, user.gender from user where user.name = 'jack' order by ${o_var} 
-- 设置limit的变量
select user.name, user.gender from user where user.name = 'jack' limit ${l_var, 1000}
```

## 函数变量

变量除了可以替换查询条件中的字符串，数字等，同时也可以替换函数。

定义：$FUNC\_NAME\{ARGS...\}

只有函数

```
-- 替代的函数参数名为m_func，并在函数中写入了一个user.age作为参数
-- m_func传入max，则解析为 max(user.age)
-- m_func传入min，则解析为 min(use.age)
select $m_func{user.age}, user.gender from user
```

## 使用限制

1.  变量只能是数字，下划线，字母组成，只能以字母开头，不区分大小写。
2.  变量的长度最多为199字符。
3.  变量不能是sql的任何关键字。
4.  变量的值是字符串，比如 where user.gender ='man', 变量记为 $\{gender, string, 'man'\}。
5.  变量的传值会被转义，不能使用sql关键字，或者if，case when等条件语句，函数变量的值中不允许有空格。

/\[a-zA-Z\]\[\\w\]\{0,199\}/

