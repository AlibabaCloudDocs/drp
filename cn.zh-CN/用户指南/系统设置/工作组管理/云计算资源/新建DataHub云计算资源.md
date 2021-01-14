# 新建DataHub云计算资源

本章节为您介绍如何新建DataHub云计算资源。

1.  您已经购买DataHub并开始使用，详情请参见[开始使用](https://help.aliyun.com/document_detail/158783.html?spm=a2c4g.11186623.6.555.5ade506dMvEnmy)。
2.  您已经创建项目，详细请参考[创建项目](https://help.aliyun.com/document_detail/158785.html?spm=a2c4g.11186623.6.556.57321cd9DH9G8d)。
3.  您已经新建Topic，详细请参见[创建Topic](https://help.aliyun.com/document_detail/158792.html?spm=a2c4g.11186623.6.561.43aa7cefPMa80P)。

添加云计算资源为使用数据资源平台做数据支撑。

1.  登录[数据资源平台控制台](https://dataq.console.aliyun.com)。

2.  在页面右上角单击**账号** \> **系统设置** \> **工作组管理**。

3.  在**工作组管理**页面，单击目标工作组**操作**列下的**云计算资源** \> **新建云计算资源**。

4.  在**新建云计算资源**页面，填写云计算资源的相关信息，单击**确定**。

    |参数名称|说明|
    |----|--|
    |**云计算资源标识**|自定义的 DataHub 计算资源标识。|
    |**资源存储类型**|单击下拉框选择您的云计算资源类型为 **DataHub**。|
    |**project**|DataHub项目名称。|
    |**Endpoint**|DataHub计算资源所在的服务地址。可以通过以下步骤进行获取：     1.  [登录DataHub控制台](https://dhsnext.console.aliyun.com/)。
    2.  选择左上角色DataHub所在的区域。
    3.  在**概览**页面的**常用信息**的外网\(互联网\)地址。 |
    |**VPC Endpoint**|DataHub计算资源所在的私网服务地址。可以通过以下步骤进行获取：     1.  [登录DataHub控制台](https://dhsnext.console.aliyun.com/)。
    2.  选择左上角色DataHub所在的区域。
    3.  在**概览**页面的**常用信息**的经典\(私网\)地址。 |
    |**Access Key ID**|访问 ID。进入[阿里云管理控制台首页](https://home.console.aliyun.com/)，将鼠标悬停至用户头像，单击 **AccessKey 管理**，即可查询您的 **Access Key ID** 信息。|
    |**Access Key Secret**|访问密钥。进入[阿里云管理控制台首页](https://home.console.aliyun.com/)，将鼠标悬停至用户头像，单击 **AccessKey 管理**，即可查询您的 **Access Key Secret**信息。|
    |**描述**|可选项，DataHub计算资源的描述。|
    |**是否校验连通性**|可选项，选择是否校验云资源的连通性。|

5.  在**云计算资源**列表查看新建的云计算资源。


