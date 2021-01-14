# 新建PostgreSQL云计算资源

本章节为您介绍如何新建PostgreSQL云计算资源。

您已经购买PostgreSQL云计算资源，并完成PostgreSQL快速入门，详细操作参见：[PostgreSQL快速入门](https://help.aliyun.com/document_detail/26151.html?spm=a2c4g.11174283.6.1008.4af65b83bFTBCX)。

添加PostgreSQL云计算资源为使用数据资源平台做数据支撑。

1.  登录[数据资源平台控制台](https://dataq.console.aliyun.com)。

2.  在页面右上角单击**账号** \> **系统设置** \> **工作组管理**。

3.  在**工作组管理**页面，单击目标工作组**操作**列下的**云计算资源** \> **新建云计算资源**。

4.  在**新建云计算资源**页面，填写云计算资源的相关信息，单击**确定**。

    |参数名称|说明|
    |----|--|
    |**云计算资源标识**|自定义的 PostgreSQL计算资源标识。|
    |**资源存储类型**|单击下拉框选择您的云计算资源类型为 **PostgreSQL**。|
    |**域名**|PostgreSQL的实例的外网地址。您可以通过以下步骤获取：    1.  [登录PostgreSQL控制台](https://rdsnext.console.aliyun.com/rdsList/cn-hangzhou/basic)。
    2.  单击左侧导航栏**实例列表**，在页面左上角，选择实例所在地域。
    3.  找到目标实例，单击**实例ID/名称**。
    4.  单击基本信息栏的**网络类型**后的**查看连接详情**中，即可查看 PostgreSQL 实例的外网地址和端口信息。 |
    |**库名**|查看PostgreSQL数据库的名称，具体详见：[查看数据库](https://help.aliyun.com/document_detail/26156.html?spm=a2c4g.11174283.6.1011.5b495b83nZuVpR)。|
    |**端口**|PostgreSQL实例的外网端口。|
    |**登录用户名**|登录数据库的账号。可[登录PostgreSQL控制台](https://rdsnext.console.aliyun.com/rdsList/cn-hangzhou/basic)，单击左侧导航栏的**账号管理**进行查看。|
    |**登录密码**|登录数据库的密码。如果忘记密码，可[登录PostgreSQL控制台](https://rdsnext.console.aliyun.com/rdsList/cn-hangzhou/basic)，单击左侧导航栏的**账号管理**进行[重置密码](https://help.aliyun.com/document_detail/96814.html?spm=a2c4g.11174283.6.1052.4af65b839hwr4h)操作。|
    |**描述**|可选项，PostgreSQL云计算资源的描述。|
    |**是否校验连通性**|可选项，选择是否校验云计算资源的连通性。|


