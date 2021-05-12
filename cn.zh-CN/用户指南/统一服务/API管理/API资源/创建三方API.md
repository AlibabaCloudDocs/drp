# 创建三方API

本章节介绍如何创建三方API。

-   已创建工作组。
-   已创建云计算资源。
-   已创建应用。

1.  登录[数据资源平台控制台](https://dataq.console.aliyun.com)。

2.  在菜单栏左上角，单击**![菜单](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/6504337061/p188771.png)** \> **研发工作台** \> **资产加工**。

3.  单击**![统一服务](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0702579161/p268584.png)** \> **API管理** \> **API资源**。

4.  在API资源页面，单击**创建API** \> **三方API**。

5.  在API基础信息页面：输入API的名称、选择所属应用和输入描述等信息后，单击**下一步**。

    ![API基础信息](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0500731061/p140503.png)

6.  API参数配置：选择工作组，填写API提供商URL，选择ContentType和请求方式，在请求参数\{body\}里面写入参数，单击**下一步**。

    ![BODY](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0500731061/p140504.png)

    **说明：** 请求参数来自于注册的API提供商的URL的请求参数。

7.  在API测试页面：单击**开始测试**，查看返回内容，单击**下一步**。

    ![CESHI ](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0500731061/p140505.png)

8.  在返回内容页面：单击**下一步**。

    ![内容查看](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0500731061/p140507.png)

9.  在流量控制页面：填写API调用次数，选择超时配置后，单击**完成**。

    ![流量控制](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1500731061/p140509.png)


新建的API可在API资源列表查看。

