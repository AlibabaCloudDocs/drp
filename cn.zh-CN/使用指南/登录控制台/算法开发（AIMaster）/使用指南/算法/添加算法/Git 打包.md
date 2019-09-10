# Git 打包 {#concept_185761 .concept}

在添加 Zerg-standalone（Java、Python）、Zerg-Service 2.0（Java、Python）类型的算法时，支持本地上传和 Git 打包两种方式上传算法文件。本节向您介绍如何以 Git 打包的方式上传算法文件。

## 前提条件 {#section_dua_gu4_tpd .section}

算法文件是在 Git 库中开发的。

## 操作步骤 {#section_ukr_xu4_olx .section}

以添加 Zerg-Service 2.0类型的算法为例：

1.  添加 Zerg-Service 2.0 类型的算法时，在算法资源界面选择**Git 打包**方式上传算法文件。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/159897/156809739244735_zh-CN.png)

    **说明：** 确保目标项目授予**dtboost-autobuild@alibaba-inc.com** 账号至少 **reporter** 权限。

2.  单击**配置打包信息**，在弹出的对话框中设置 Git 库的相关信息。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/159897/156809739344736_zh-CN.png)

    **说明：** **项目地址**和**项目分支**为必填项，**项目地址**必须是一个合法的 Git 地址。

3.  完成上述参数配置后，单击**打包**，则开始打包项目文件。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/159897/156809739344737_zh-CN.png)

    打包过程中，您可在**打包日志**中查看实时的打包日志。当**打包**变为**确定**或日志中显示**Package pushing success!**时，说明打包已完成。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/159897/156809739344738_zh-CN.png)

4.  打包完成后，单击**确定**，则打包的算法文件显示在算法资源界面中。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/159897/156809739344739_zh-CN.png)

    **说明：** 如果需要本地保存算法文件，则您可单击**下载**，下载算法文件到本地。

5.  上传算法文件完成并且设置好其他参数后，单击**下一步**即可。

