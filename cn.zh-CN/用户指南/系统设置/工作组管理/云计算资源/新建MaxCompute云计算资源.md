新建MaxCompute云计算资源 
======================================

通过新建MaxCompute云计算资源，为使用数据资源平台做数据支撑。

前提条件 
-------------------------

* 您已经购买MaxCompute云计算资源。

  

* 在添加MaxCompute云计算资源之前，您需要开通MaxCompute产品权限并创建项目。 

  
  * 开通MaxCompute方法参见[开通MaxCompute和DataWorks](/cn.zh-CN/准备工作/开通MaxCompute.md)。

    
  
  * 创建MaxCompute项目方法参见[创建MaxCompute项目](/cn.zh-CN/准备工作/创建MaxCompute项目.md)。

    
  

  

  

* 如果您需要将MaxCompute中的数据接入数据资源平台，还需要在MaxCompute项目中完成数据表的创建和数据导入。 

  
  * 在MaxCompute数据库建表和插入语句，详细参见[准备数据](/cn.zh-CN/最佳实践/准备工作/准备数据.md)。

    
  
  * 创建MaxCompute数据表方法参见[创建表](/cn.zh-CN/快速入门/通过MaxCompute客户端使用MaxCompute/创建表.md)。

    
  
  * 数据导入MaxCompute数据表方法参见[导入数据](/cn.zh-CN/快速入门/通过MaxCompute客户端使用MaxCompute/导入数据.md)。

    
  

  

  

* 已创建工作组，具体操作请参见[创建工作组](/cn.zh-CN/用户指南/系统设置/工作组管理/创建工作组.md)。

  




操作步骤 
-------------------------

1. 登录[数据资源平台控制台](https://dataq.console.aliyun.com)。

   

2. 在页面右上角单击账号名称，选择 **系统设置** 。

   

3. 在左侧导航栏，单击 **工作组管理** 。

   

4. 在工作组列表 **操作** 列中，单击目标工作组的 **云计算资源** 。

   

5. 在 **云计算资源** 页面，单击 **新建** **云计算资源** 。

   

6. 在 **新建** **云计算资源** 对话框中，配置云计算资源信息。

   

   |       参数名称        |                                                                    说明                                                                     |
   |-------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
   | 云计算资源标识           | 自定义的MaxCompute计算资源标识。                                                                                                                     |
   | 资源存储类型            | 单击下拉框选择您的云计算资源类型为 **MaxCompute** 。                                                                                                        |
   | 是否为VPC资源          | 默认选择否。                                                                                                                                    |
   | project           | MaxCompute项目名称。                                                                                                                           |
   | Endpoint          | MaxCompute计算资源所在的服务地址，即您 MaxCompute项目所在的区域，详细请参考[Endpoint](/cn.zh-CN/准备工作/配置Endpoint.md)。                              |
   | Access Key ID     | 访问 ID。进入[阿里云管理控制台首页](https://home.console.aliyun.com/)，将鼠标悬停至用户头像，单击 **AccessKey 管理** ，即可查询您的 **Access Key ID** 信息。    |
   | Access Key Secret | 访问密钥。进入[阿里云管理控制台首页](https://home.console.aliyun.com/)，将鼠标悬停至用户头像，单击 **AccessKey 管理** ，即可查询您的 **Access Key Secret** 信息。 |
   | 描述                | 可选项，MaxCompute计算资源的描述。                                                                                                                    |
   | 是否校验连通性           | 可选项，选择是否校验云资源的连通性。                                                                                                                        |

   

7. 配置完成后，单击 **确定** 。

   



