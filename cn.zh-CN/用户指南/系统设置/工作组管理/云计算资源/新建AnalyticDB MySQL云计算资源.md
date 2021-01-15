# 新建AnalyticDB MySQL云计算资源

本章节为您介绍如何新建AnalyticDB MySQL云计算资源。

-   [创建集群](https://help.aliyun.com/document_detail/122234.html?spm=a2c4g.11186623.6.589.173d152fzd8Vx3)。
-   [创建数据库账号](https://help.aliyun.com/document_detail/122280.html?spm=a2c4g.11186623.6.590.7a6b4ecbFdXbrd)。
-   [设置白名单](https://help.aliyun.com/document_detail/122244.html?spm=a2c4g.11186623.6.591.439e7c78PCC26X)。
-   [连接集群](https://help.aliyun.com/document_detail/122512.html?spm=a2c4g.11186623.6.592.6d9d1ad941ffwj)。
-   [创建数据库](https://help.aliyun.com/document_detail/135654.html?spm=a2c4g.11186623.6.593.781c6b32maAPNw)。
-   [导入数据](https://help.aliyun.com/document_detail/188324.html?spm=a2c4g.11186623.6.594.5c7c7c1dfdWZvS)。
-   [申请公网地址](https://help.aliyun.com/document_detail/122252.html?spm=a2c4g.11186623.6.598.1ee62206qajuIF)。

添加云计算资源为使用数据资源平台做数据支撑。

1.  登录[数据资源平台控制台](https://dataq.console.aliyun.com)。

2.  在页面右上角单击**账号** \> **系统设置** \> **工作组管理**。

3.  在**工作组管理**页面，单击目标工作组**操作**列下的**云计算资源** \> **新建云计算资源**。

4.  在**新建云计算资源**对话框，填写云计算资源的相关信息。

    |参数名称|说明|
    |----|--|
    |**云计算资源标识**|自定义的AnalyticDB MySQL云计算资源的标识。|
    |**资源存储类型**|单击下拉框选择您的云计算资源类型为 **AnalyticDB MySQL**，单击后面的**![白名单](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/2847900161/p211240.png)**查看白名单列表。|
    |**是否为VPC资源**|默认选否。|
    |**域名**|AnalyticDB MySQL集群的公网地址。您可以通过以下步骤进行获取：     1.  [登录ADB控制台](https://ads.console.aliyun.com/)。
    2.  单击左侧导航栏**集群列表**，在页面左上角，选择集群所在地域。
    3.  找到目标集群，单击**集群 ID/集群描述**。
    4.  查看网络信息下的公网地址。 |
    |**库名**|AnalyticDB MySQL的数据库名称。请参见[查看数据库](https://help.aliyun.com/document_detail/135654.html?spm=a2c4g.11186623.6.593.2cc77c78SkD6HO)。|
    |**端口**|ADB 集群的公网端口。|
    |**登录用户名**|登录数据库的账号。您可以通过以下步骤进行获取：     1.  [登录ADB控制台](https://ads.console.aliyun.com/)。
    2.  单击左侧导航栏**集群列表**，在页面左上角，选择集群所在地域。
    3.  找到目标集群，单击**集群 ID/集群描述**。
    4.  单击左侧导航栏的**账号管理**信息查看账号。 |
    |**登录密码**|登录数据库的密码。您可以通过以下步骤进行获取：     1.  [登录ADB控制台](https://ads.console.aliyun.com/)。
    2.  单击左侧导航栏**集群列表**，在页面左上角，选择集群所在地域。
    3.  找到目标集群，单击**集群 ID/集群描述**。
    4.  单击左侧导航栏的**数据库管理**信息查看
如您忘记密码，可[重置账号密码](https://help.aliyun.com/document_detail/122659.html?spm=a2c4g.11174283.6.661.1e289abd3wqx7d)。|
    |**描述**|可选项，ADB云计算资源的描述。|
    |**是否校验连通性**|默认选择”是“，用于新建资源的连通性测试。|

5.  在**云计算资源**列表查看新建的云计算资源。


