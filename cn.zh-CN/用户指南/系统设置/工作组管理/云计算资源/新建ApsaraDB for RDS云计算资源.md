新建ApsaraDB for RDS云计算资源 
============================================

通过新建ApsaraDB for RDS云计算资源，为使用数据资源平台做数据支撑。

前提条件 
-------------------------

* 您已经购买ApsaraDB for RDS云计算资源，并完成RDS快速入门。

  * [创建RDS MySQL实例](https://help.aliyun.com/document_detail/26117.html?spm=a2c4g.11174283.6.665.18535b83HC4Fz1)。

    
  
  * [设置IP白名单](/cn.zh-CN/RDS MySQL 数据库/快速入门/设置白名单/设置IP白名单.md)。

    
  
  * [申请外网地址](https://help.aliyun.com/document_detail/26128.html?spm=a2c4g.11186623.2.34.708540a8dzSOaO)。

    
  
  * [创建账号和数据库](https://help.aliyun.com/document_detail/87038.html?spm=a2c4g.11186623.2.35.708540a8dzSOaO)。

    
  
  * [连接MySQL实例](https://help.aliyun.com/document_detail/26138.html?spm=a2c4g.11186623.6.669.303238f8gRrN8t)。

    
  
  * 在RDS数据库建表和插入语句，详细参见[准备数据](/cn.zh-CN/最佳实践/准备工作/准备数据.md)。

    
  

  

* 已创建工作组，具体操作请参见[创建工作组](/cn.zh-CN/用户指南/系统设置/工作组管理/创建工作组.md)。

  




操作步骤 
-------------------------

1. 登录[数据资源平台控制台](https://dataq.console.aliyun.com)。

   

2. 在页面右上角单击账号名称，选择 **系统设置** 。

   

3. 在左侧导航栏，单击 **工作组管理** 。

   

4. 在工作组列表 **操作** 列中，单击目标工作组的 **云计算资源** 。

   

5. 在 **云计算资源** 页面，单击 **新建** **云计算资源** 。

   

6. 在 **新建** **云计算资源** 对话框中，配置云计算资源信息。

   

   |     参数名称     |                                                                                                                                                                                                                                    说明                                                                                                                                                                                                                                     |
   |--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | **云计算资源标识**  | 自定义的ApsaraDB for RDS计算资源的标识。                                                                                                                                                                                                                                                                                                                                                                                                                                              |
   | **资源存储类型**   | 单击下拉框选择您的云计算资源类型为 **ApsaraDB for RDS** ，单击后面的![白名单](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/2847900161/p211240.png)查看白名单列表。                                                                                                                                                                                                                                                                                                                |
   | **是否为VPC资源** | 默认选否。                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
   | **域名**       | ApsaraDB for RDS实例的外网地址。您可以通过以下步骤进行获取：  1. [登录RDS管理控制台](https://rds.console.aliyun.com/?spm=a2c4g.11186623.2.40.708540a8dzSOaO)。   2. 单击左侧导航栏 **实例列表** ，在页面左上角，选择实例所在地域。   3. 找到目标实例，单击实例 ID/名称。   4. 单击基本信息栏的 **网络类型** 后的 **查看连接详情** 中，即可查看 RDS 实例的外网地址和端口信息。    |
   | **库名**       | ApsaraDB for RDS 的数据库名称。可[登录RDS管理控制台](https://rdsnext.console.aliyun.com/detail/rm-bp1f7x6016jt756p6/basicInfo?spm=5176.19907444.0.0.64b11450Ea7NOm&region=cn-hangzhou&DedicatedHostGroupId=)，单击左侧导航栏的 **数据库管理** 进行查看。                                                                                                                                                                                                                                 |
   | **端口**       | RDS 实例的外网端口。                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
   | **登录用户名**    | 登录数据库的账号。可[登录RDS管理控制台](https://rdsnext.console.aliyun.com/detail/rm-bp1f7x6016jt756p6/basicInfo?spm=5176.19907444.0.0.64b11450Ea7NOm&region=cn-hangzhou&DedicatedHostGroupId=)，单击左侧导航栏的 **账号管理** 进行查看。                                                                                                                                                                                                                                                 |
   | **登录密码**     | 登录数据库的密码。如果忘记密码，可[登录RDS管理控制台](https://rdsnext.console.aliyun.com/detail/rm-bp1f7x6016jt756p6/basicInfo?spm=5176.19907444.0.0.64b11450Ea7NOm&region=cn-hangzhou&DedicatedHostGroupId=)，单击左侧导航栏的 **账号管理** 进行[重置密码](https://help.aliyun.com/document_detail/96100.html?spm=a2c4g.11186623.2.44.708540a8dzSOaO)操作。                                                                                                                      |
   | **日志模型**     | * 无：无日志。   * binlog：有日志。                                                                                                                                                                                                                                                                                                                                                               |
   | **描述**       | 可选项，RDS计算资源的描述。                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
   | **是否校验连通性**  | 默认选择"是"，用于新建资源的连通性测试。                                                                                                                                                                                                                                                                                                                                                                                                                                                     |

   

7. 配置完成后，单击 **确定** 。

   



