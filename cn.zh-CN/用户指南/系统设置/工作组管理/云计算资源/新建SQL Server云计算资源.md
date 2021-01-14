# 新建SQL Server云计算资源

本章节为您介绍如何新建SQL Server云计算资源。

您已经购买RDS SQL Server云计算资源，并完成SQL Server快速入门，详细操作参见：[RDS SQL Server快速入门](https://help.aliyun.com/document_detail/53729.html?spm=a2c4g.11186623.6.875.3d5e48b1uMeLE8)

1.  登录[数据资源平台控制台](https://dataq.console.aliyun.com)。

2.  在页面右上角单击**账号** \> **系统设置** \> **工作组管理**。

3.  在**工作组管理**页面，单击目标工作组**操作**列下的**云计算资源** \> **新建云计算资源**。

4.  在**新建云计算资源**页面，填写云计算资源的相关信息，单击**确定**。

    |参数名称|说明|
    |----|--|
    |**云计算资源标识**|自定义的SQL Server的标识。|
    |**资源存储类型**|单击下拉框选择您的云计算资源类型为 **SQL Server**，单击后面的**![白名单](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/2847900161/p211240.png)**查看白名单列表。|
    |**是否为VPC资源**|默认选否。|
    |**域名**|SQL Server集群的公网地址。您可以通过以下步骤进行获取：     1.  [登录SQL Server控制台。](https://rdsnext.console.aliyun.com/rdsList/cn-hangzhou/basic)。
    2.  单击左侧导航栏**集群列表**，在页面左上角，选择集群所在地域。
    3.  找到目标集群，单击**集群 ID/集群描述**。
    4.  单击基本信息栏的**网络类型**后的**查看连接详情**中，即可查看 SQL Server 实例的外网地址和端口信息。 |
    |**库名**|SQL Server的数据库名称。请参见[查看数据库](https://help.aliyun.com/document_detail/95698.html?spm=a2c4g.11186623.6.946.69546b56yGPLTv)。|
    |**端口**|SQL Server集群的公网端口。|
    |**登录用户名**|登录数据库的账号。您可以通过以下步骤进行获取：     1.  [登录SQL Server控制台。](https://rdsnext.console.aliyun.com/rdsList/cn-hangzhou/basic)。
    2.  单击左侧导航栏**集群列表**，在页面左上角，选择集群所在地域。
    3.  找到目标集群，单击**集群 ID/集群描述**。
    4.  单击左侧导航栏的**账号管理**信息查看账号。 |
    |**登录密码**|登录数据库的密码。如果忘记密码，可[登录SQL Server控制台。](https://rdsnext.console.aliyun.com/rdsList/cn-hangzhou/basic)，单击左侧导航栏的**账号管理**进行[重置密码](https://help.aliyun.com/document_detail/95691.html?spm=a2c4g.11186623.6.939.2a2848b1t2Bolw)操作。|
    |**描述**|可选项，SQL Server云计算资源的描述。|
    |**是否校验连通性**|默认选择”是“，用于新建资源的连通性测试。|


