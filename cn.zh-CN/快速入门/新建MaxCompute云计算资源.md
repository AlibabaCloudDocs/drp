# 新建MaxCompute云计算资源

本文为您介绍在数据资源平台配置MaxCompute云计算资源，便于之后对相应云计算资源下ods\_base\_yhkh表的数据进行ETL开发。

在新建MaxCompute云计算资源之前，您需要开通MaxCompute产品权限并创建项目。

-   开通MaxCompute方法参见[开通MaxCompute](https://help.aliyun.com/document_detail/58226.html?spm=a2c4g.11186623.6.589.2b2e7ae21OMcMt)。
-   创建MaxCompute项目方法参见[创建项目空间](https://help.aliyun.com/document_detail/27815.html?spm=a2c4g.11186623.6.590.747019a4L3S8wj)。

1.  登录[数据资源平台控制台](https://dataq.console.aliyun.com)。

2.  在页面右上角单击**账号** \> **系统设置** \> **工作组管理**。

3.  在**工作组管理**页面，单击目标工作组**操作**列下的**云计算资源** \> **新建云计算资源**。

4.  在**新建云计算资源**页面，填写云计算资源的相关信息，单击**确定**。

    |参数名称|说明|
    |----|--|
    |**云计算资源标识**|自定义的 MaxCompute 计算资源标识。|
    |**资源存储类型**|单击下拉框选择您的云计算资源类型为 **MaxCompute**。|
    |**是否为VPC资源**|默认选择否**经典网络**，如果选择是为**专有网络**。|
    |**project**|MaxCompute 项目名称。|
    |**Endpoint**|MaxCompute 计算资源所在的服务地址，即您 MaxCompute 项目所在的区域，详细请参考[配置Endpoint](https://help.aliyun.com/document_detail/34951.html?spm=a2c4g.11174283.6.593.600a590eJNd3vH)。|
    |**Access Key ID**|访问 ID。进入[阿里云管理控制台首页](https://home.console.aliyun.com)，将鼠标悬停至用户头像，单击 **AccessKey 管理**，即可查询您的 **Access Key ID** 信息。|
    |**Access Key Secret**|访问密钥。进入[阿里云管理控制台首页](https://home.console.aliyun.com)，将鼠标悬停至用户头像，单击 **AccessKey 管理**，即可查询您的 **Access Key Secret**信息。|
    |**描述**|可选项，MaxCompute 计算资源的描述。|
    |**是否校验连通性**|可选项，选择是否校验云资源的连通性。|

5.  在云计算资源列表查看新建的云计算资源，单击**检测**，可以手动检测该云计算资源的通性。


