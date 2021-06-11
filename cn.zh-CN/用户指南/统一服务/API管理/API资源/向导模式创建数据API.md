# 向导模式创建数据API

本文介绍如何使用向导模式创建数据API。

-   已创建工作组。
-   已创建云计算资源。
-   已创建应用。
-   已创建组织机构，并成为一个组织机构的成员。
-   已准备好需创建API的数据库数据。

以下以RDS云数据库创建API为例。

1.  登录[数据资源平台控制台](https://dataq.console.aliyun.com)。

2.  在菜单栏左上角，单击**![菜单](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/6504337061/p188771.png)** \> **研发工作台**。

3.  在顶部菜单栏单击**资产加工**，并在左侧导航栏选择**![统一服务](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0702579161/p268584.png)** \> **API管理** \> **API资源**。

4.  在API资源页面，单击页面右上角的**创建API** \> **数据API**。

5.  设置API基础信息。输入API的名称、选择所属应用、选择调用认证方式和输入描述等信息后，单击**下一步**。

    ![001](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/7431133261/p281996.png)

6.  配置API参数。

    1.  选择云计算资源类型、云计算资源和源数据表。

    2.  将**新建模式**选为“向导模式”。

    3.  在**返回参数**区域，选中全部字段，在**请求参数**区域，单击**请求参数**，填写请求参数字段名称、条件和默认值等。

        ![请求参数](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0492213261/p280805.png)

    4.  单击**下一步**。

7.  API测试。单击**开始测试**，核对返回内容无误后，单击**下一步**。

    ![002](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/7431133261/p281997.png)

8.  查看返回内容。查看返回示例，单击**下一步**。

    ![003](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/7431133261/p281998.png)

9.  配置流量控制参数。填写API最大调用次数，选择超时配置，单击**完成**。

    ![流量控制](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0492213261/p280807.png)


新建的API可在API资源列表查看。

