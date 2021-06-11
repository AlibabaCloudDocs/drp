# 创建三方API

本章节介绍如何创建三方API。

-   已创建工作组。
-   已创建应用。
-   已创建组织机构，并成为一个组织机构的成员。
-   已准备好需创建API的数据库数据。

1.  登录[数据资源平台控制台](https://dataq.console.aliyun.com)。

2.  在菜单栏左上角，单击**![菜单](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/6504337061/p188771.png)** \> **研发工作台**。

3.  在顶部菜单栏单击**资产加工**，并在左侧导航栏选择**![统一服务](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0702579161/p268584.png)** \> **API管理** \> **API资源**。

4.  在API资源页面，单击页面右上角的**创建API** \> **三方API**。

5.  设置API基础信息。输入API的名称、选择所属应用、选择调用认证方式和输入描述等信息后，单击**下一步**。

    ![005](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/5523133261/p282006.png)

6.  配置API参数。选择工作组，填写API提供商URL，选择ContentType和请求方式，在请求参数\{body\}里面写入参数，单击**下一步**。

    ![API参数配置](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/2492213261/p280831.png)

    **说明：** 请求参数来自于注册的API提供商的URL的请求参数。

7.  API测试。单击**开始测试**，查看返回内容后，单击**下一步**。

    ![006](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/6523133261/p282010.png)

8.  查看返回内容。单击**下一步**。

    ![007](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/6523133261/p282012.png)

9.  配置流量控制参数。填写API最大调用次数，选择超时配置后，单击**完成**。

    ![流程控制](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/3492213261/p280821.png)


新建的API可在API资源列表查看。

