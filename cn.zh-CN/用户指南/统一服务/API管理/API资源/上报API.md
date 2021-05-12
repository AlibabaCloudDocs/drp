# 上报API

本文介绍如何通过创建数据表的方式生成API。

-   新建工作组。
-   新建云计算资源。
-   新建应用。

1.  登录[数据资源平台控制台](https://dataq.console.aliyun.com)。

2.  在菜单栏左上角，单击**![菜单](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/6504337061/p188771.png)** \> **研发工作台** \> **资产加工**。

3.  单击**![统一服务](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0702579161/p268584.png)** \> **API管理** \> **API资源**。

4.  在API资源页面，单击**创建API** \> **上报API**。

5.  进入API基础信息页面，输入API的名称、选择所属应用和输入描述等信息后，单击**下一步**。

    ![API基础信息](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/5618030061/p140485.png)

6.  进入API参数配置页面，配置PAI参数。

    1.  选择云计算资源类型和云计算资源。

    2.  单击目标数据表后面的**创建**，在弹出的创建表页面，填写表名和字段信息，操作完成后，单击**确定**。

        ![创建](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/6683666161/p207481.png)

    3.  在请求参数区域，选中字段参数。

        ![请求参数](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/6683666161/p207483.png)

    4.  选择是否需要**自动添加上报时间戳**。

    5.  选择覆盖或丢弃**主键重复数据处理策略**后，单击**下一步**。

7.  进入API测试页面，单击**开始测试**，核对测试结果无误后，单击**下一步**。

    ![API测试](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/6683666161/p207484.png)

8.  进入返回内容页面，查看返回示例， 单击**下一步**。

    ![查看返回示例](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/6683666161/p207485.png)

9.  进入流量控制页面，填写API最大调用次数，选择超时配置，单击**完成**。

    ![流量控制](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/6683666161/p207486.png)


新建的API可在API资源列表查看。

