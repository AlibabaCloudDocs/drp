# 向导模式创建数据API

本文介绍如何使用向导模式创建数据API。

-   新建工作组。
-   新建云计算资源。
-   新建应用。
-   准备好要创建API的数据库数据。

以下以RDS云数据库创建API为例：

1.  登录[数据资源平台控制台](https://dataq.console.aliyun.com)。

2.  在菜单栏左上角，单击**![菜单](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/6504337061/p188771.png)** \> **研发工作台** \> **资产加工**。

3.  单击**![统一服务](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0702579161/p268584.png)** \> **API管理** \> **API资源**。

4.  在API资源页面，单击**创建API** \> **数据API**。

5.  设置API基础信息：输入API的名称、选择所属应用和输入描述等信息后，单击**下一步**。

    ![API基础信息](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/5618030061/p140485.png)

6.  进行API参数配置。

    1.  选择云计算资源类型、云计算资源和源数据表。

    2.  将新建模式选为"向导模式”。

    3.  在**返回参数**区域，选中全部字段，在**请求参数**区域，单击**请求参数**，填写请求参数说明、条件和默认值等。

    4.  单击**下一步**。

7.  进行API测试：单击**开始测试**，核对返回内容无误后，单击**下一步**。

    ![API测试](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/5618030061/p140491.png)

8.  在返回内容页面：查看返回示例， 单击**下一步**。

    ![返回结果](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/5618030061/p140492.png)

9.  在流量控制页面：填写API最大调用次数，选择超时配置，单击**完成**。

    ![流量控制](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/5618030061/p140493.png)


新建的API可在API资源列表查看。

