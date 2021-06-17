# 通过DDL新建逻辑表

可以通过新建DDL的方式创建逻辑表。

已存新建模型和目录。

当前支持通过DDL在MaxCompute、Hive数据源上创建逻辑表。

## 操作步骤

1.  登录[数据资源平台控制台](https://dataq.console.aliyun.com)。

2.  在页面左上角，单击![工作台](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/4682213261/p280916.png)图标，选择**研发工作台**。

3.  在顶部菜单栏，单击**资产加工**。

4.  在左侧导航栏，选择**![数据建模.png](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/4960303261/p268674.png)数据建模** \> **数据模型设计**。

5.  在数据模型下，选择需要的目录，单击**![目录](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/5682213261/p280932.png)**。

6.  在目录右侧页面，单击**DDL新建**。

    ![ddl新建](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/6682213261/p281157.png)

7.  在**通过DDL新建**面板，选择云计算资源，并输入DDL语句，单击**确定**。

    **说明：**

    -   DDL语句中逻辑表名称不能已存在。
    -   仅支持MAXComputer和Hive云计算资源通过DDL方式创建逻辑表。
    ![DDL新建](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/7648559951/p132263.jpg)

    创建完成以后，可以在数据模型对应目录下的右侧页面查看已创建的逻辑表。

    ![逻辑表](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/3475183261/p283698.png)

    在逻辑表列表页面，单击操作列的**详情**，进入逻辑表详情页面，即可在**逻辑表详情**页签的配置信息的**字段信息**区域框，查看创建的逻辑表中包含的字段。

    ![创建完成](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/4475183261/p283676.png)


