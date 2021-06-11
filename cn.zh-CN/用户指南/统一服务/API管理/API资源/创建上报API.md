# 创建上报API

本文介绍如何通过创建数据表的方式生成API。

-   新建工作组。
-   新建云计算资源。
-   新建应用。
-   已创建组织机构，并成为一个组织机构的成员。

1.  登录[数据资源平台控制台](https://dataq.console.aliyun.com)。

2.  在菜单栏左上角，单击**![菜单](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/6504337061/p188771.png)** \> **研发工作台**。

3.  在顶部菜单栏单击**资产加工**，并在左侧导航栏选择**![统一服务](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0702579161/p268584.png)** \> **API管理** \> **API资源**。

4.  在API资源页面，单击页面右上角的**创建API** \> **上报API**。

5.  设置API基础信息。输入API的名称、选择所属应用、选择调用认证方式和输入描述等信息后，单击**下一步**。

    ![008](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0663133261/p282016.png)

6.  配置API参数。

    1.  选择云计算资源类型和云计算资源。

    2.  单击目标数据表后面的**创建**，在弹出的创建表页面，填写表名和字段信息，操作完成后，单击**确定**。

        ![创建](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/6683666161/p207481.png)

    3.  在请求参数区域，选中字段参数。

        ![canshu](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/4492213261/p280901.png)

    4.  选择是否需要**自动添加上报时间戳**。

    5.  选择覆盖或丢弃**主键重复数据处理策略**后，单击**下一步**。

7.  API测试。单击**开始测试**，核对测试结果无误后，单击**下一步**。

    ![009](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0663133261/p282019.png)

8.  查看返回内容。查看返回示例， 单击**下一步**。

    ![010](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0663133261/p282023.png)

9.  配置流量控制参数。填写API最大调用次数，选择超时配置，单击**完成**。

    ![14253](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/4492213261/p280907.png)


新建的API可在API资源列表查看。

