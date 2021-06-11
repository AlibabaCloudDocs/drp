# SQL模式创建数据API

本章节介绍如何用SQL模式创建数据API。

-   已创建工作组。
-   已创建云计算资源。
-   已创建应用。
-   已创建组织机构，并成为一个组织机构的成员。
-   已准备好需创建API的数据库数据。
-   不是所有的云计算资源类型都支持SQL模式创建数据API，具体请以界面展示为准。

1.  登录[数据资源平台控制台](https://dataq.console.aliyun.com)。

2.  在菜单栏左上角，单击**![菜单](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/6504337061/p188771.png)** \> **研发工作台**。

3.  在顶部菜单栏单击**资产加工**，并在左侧导航栏选择**![统一服务](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0702579161/p268584.png)** \> **API管理** \> **API资源**。

4.  在API资源页面，单击页面右上角的**创建API** \> **数据API**。

5.  设置API基础信息。输入API的名称、选择所属应用、选择调用认证方式和输入描述等信息后，单击**下一步**。

    ![004](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/9762133261/p282003.png)

6.  配置API参数。选择云计算资源类型、云计算资源，**新建模式**选择“SQL模式”，输入SQL代码，单击**语法检查及格式化**，语法或数据格式无错误提示后，单击**下一步**。

    ![SQL](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/3496579161/p268661.png)

7.  API测试。单击**开始测试**，查看返回内容，单击**下一步**。

    ![API测试](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1492213261/p280798.png)

8.  查看返回内容。核对信息无误后，单击**下一步**。

    ![返回信息](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/3496579161/p268664.png)

9.  配置流量控制参数。填写API最大调用次数，选择超时配置，单击**完成**。

    ![流量控制](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1492213261/p280799.png)


新建的API在API资源列表可查看。

