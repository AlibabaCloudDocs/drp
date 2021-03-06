新建Object Storage Service云计算资源 
==================================================

添加OSS云计算资源为使用数据资源平台做数据支撑。

前提条件 
-------------------------

* 您已经购买OSS云计算资源，并完成OSS快速入门，具体操作请参见[OSS快速入门](https://help.aliyun.com/document_detail/31883.html?spm=a2c4g.11186623.6.610.418b7a7412s755)。

  

* 已创建工作组，具体操作请参见[创建工作组](/cn.zh-CN/用户指南/系统设置/工作组管理/创建工作组.md)。

  




操作步骤 
-------------------------

1. 登录[数据资源平台控制台](https://dataq.console.aliyun.com)。

   

2. 在页面右上角单击账号名称，选择 **系统设置** 。

   

3. 在左侧导航栏，单击 **工作组管理** 。

   

4. 在工作组列表 **操作** 列中，单击目标工作组的 **云计算资源** 。

   

5. 在 **云计算资源** 页面，单击 **新建** **云计算资源** 。

   

6. 在 **新建** **云计算资源** 对话框中，配置云计算资源信息。

   

   |           参数名称            |                                                                                                                                                                                                      说明                                                                                                                                                                                                      |
   |---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | **云计算资源标识**               | 自定义的 OSS 云计算资源标识。                                                                                                                                                                                                                                                                                                                                                                                            |
   | **资源存储类型**                | 单击下拉框选择您的云计算资源类型为 **Object Storage Service** 。                                                                                                                                                                                                                                                                                                                                                               |
   | **Endpoint**              | OSS的Endpoint。您可以通过以下步骤进行获取： 1. 登录[OSS控制台](https://oss.console.aliyun.com/bucket/oss-cn-beijing/test20200112/overview)。   2. 单击 **某条Bucket信息** 。   3. 在左侧导航栏，单击 **概览** ，在访问域名中查看外网访问Endpoint。                                                             |
   | **bucket**                | OSS的bucket名称。您可以通过以下步骤进行获取： 1. 登录[OSS控制台](https://oss.console.aliyun.com/bucket/oss-cn-beijing/test20200112/overview)。   2. 单击 **Bucket列表** ，然后单击 **创建Bucket** 。   3. 在 **创建Bucke** 面板，按如下说明配置必要参数。   4. 单击 **确定** 。    |
   | **Access Key ID**         | 访问 ID。进入[阿里云管理控制台首页](https://home.console.aliyun.com)，将鼠标悬停至用户头像，单击 **AccessKey 管理** ，即可查询您的 **Access Key ID** 信息。                                                                                                                                                                                                                                                                           |
   | **Access** **Key Secret** | 访问密钥。进入[阿里云管理控制台首页](https://home.console.aliyun.com)，将鼠标悬停至用户头像，单击 **AccessKey 管理** ，即可查询您的 **Access Key Secret** 信息。                                                                                                                                                                                                                                                                        |
   | **描述**                    | 可选项，OSS云计算资源的描述。                                                                                                                                                                                                                                                                                                                                                                                             |
   | **是否校验连通性**               | 可选项，选择是否校验云资源的连通性。                                                                                                                                                                                                                                                                                                                                                                                           |

   

7. 配置完成后，单击 **确定** 。

   



