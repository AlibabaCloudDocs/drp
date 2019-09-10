# Python SDK {#concept_msd_nbh_jhb .concept}

## 概览 {#section_lpq_qbh_jhb .section}

该SDK为AIMaster算法模型管理Python版，主要提供了模型的上传、下载、查询、删除、版本控制等功能

**特别说明：**

如果是使用zerg-standalone算法来训练模型且在登记算法的时候勾选了“产出模型”， 在zerg-standalone算法启动的时候的启动Shell脚本的输入参数`$1`中包含了AlgModelManager初始化需要的信息，可以直接将`$1`传给Python脚本， 在Python脚本中用`sys.argv[1]`获取的值作为AlgModelManager的构造函数入参即可完成初始化。

## 运行环境 {#section_mpq_qbh_jhb .section}

Python 3.6

## 安装说明 {#section_npq_qbh_jhb .section}

1.  联系产品团队获取 SDK 对应的 EGG 文件：alg\_model\_sdk-2.0.0-py3.6.egg.zip

2.  通过 easy\_install 安装：

    `cd <your_project_dir>`

    `export PYTHONPATH=$(pwd)/lib:${PYTHONPATH}`

    `easy_install --install-dir=$(pwd)/lib alg_model_sdk-2.0.0-py3.6.egg`


## 使用样例 {#section_qpq_qbh_jhb .section}

说明：如果是本地测试，初始化AlgModelManager时需要的用户相关信息（tenant，user\_id，access\_id， access\_key\)可以在AIMaster右上角的用户信息里拿到：

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/155560/156809752346990_zh-CN.png)

实例代码：

``` {#codeblock_mrz_09r_jdu}
from alg_model_sdk import AlgModelManager, ModelType, AlgModel

end_point = 'http://10.125.25.106'
tenant = 'dtboost'
user_id = '1696462764375572'
access_id = '******'
access_key = '******'
alg_code = 'example_agl_4_model'
alg_version = '1.1.0'

# 构建算法模型管理器

# algModelManager = AlgModelManager(end_point, tenant, user_id, access_id, access_key, alg_code, alg_version)
#{
#    "_alg_model_params":{
#        "endPoint":"http://10.125.25.106",  AIMaster相应环境的endPoint
#        "tenant":"dtboost",                               AIMaster用户信息中的tenantCode
#        "userId":"1696462764375572",                      AIMaster用户信息中的userId
#        "accessId":"******",                              AIMaster用户信息中的accessKeyId
#        "accessKey":"******",                             AIMaster用户信息中的accessKeySecret
#        "algCode":"example_agl_4_model",                  产出模型的算法code
#        "algVersion":"1.1.0"                              产出模型的算法版本
#    }
#}
args = '{"_alg_model_params":{"endPoint":"http://10.125.25.106","tenant":"dtboost","userId":"1696462764375572","accessId":"******","accessKey":"******","algCode":"example_agl_4_model","algVersion":"1.1.0"}}'
algModelManager = AlgModelManager.get_alg_model_manager(args)

# 上传模型文件
model_file_path = 'example.pmml'
# PMML类型：        ModelType.PMML
# H5类型：          ModelType.H5
# TENSORFLOW类型：  ModelType.TENSORFLOW
# 自定义类型：       ModelType.CUSTOMIZED
alg_model = AlgModel('example_model', '1.0.0', ModelType.PMML, 'This is a example model')
model_id = algModelManager.save(model_file_path, alg_model, 'true')
print("model_id: " + str(model_id) + "\r\n")

# 通过模型名称 + 模型版本查询模型详细信息
model_name = 'example_model'
model_version = '1.0.0'
model_info = algModelManager.get_alg_model(model_name, model_version)
print("model_info: " + str(model_info) + "\r\n")

# 通过模型名称查询该模型名称下的所有版本的模型文件信息
model_name = 'example_model'
model_list = algModelManager.list_alg_models_by_name(model_name)
print("model_list: " + str(model_list) + "\r\n")

# 通过模型ID下载模型文件
model_data = algModelManager.download_alg_model_by_id(model_id)
print("model_data: " + str(model_data) + "\r\n")

# 通过模型名称 + 模型版本下载模型文件
model_data = algModelManager.download_alg_model_by_name('example_model', '1.0.0')
print("model_data: " + str(model_data) + "\r\n")

# 通过模型名称 + 模型版本删除模型
model_name = 'example_model'
model_version = '1.0.0'
ret = algModelManager.del_alg_model(model_name, model_version)
print("Delete model return value: " + str(ret) + "\r\n")
```

SDK 2.0新增功能

``` {#codeblock_lfl_0w3_15z}
# 模型超时时间设置（单位是秒），默认是10分钟，比如修改为5分钟
algModelManager.timeout = 5 * 60

# 模型保存支持模型训练算法版本、特征预处理参数、特征预处理函数、预测后处理函数
def test_save_model_with_model_data_version_and_post_handle_fun(self):
    model_file_path = 'test.pmml'
    alg_model = AlgModel('test_model_1', '1.0.0', ModelType.PMML, 'This is a test model',
                         model_data_version='2.0.0', post_handle_function='def abc(): print("hello")')
    r = self.algModelManager.save(model_file_path, alg_model, 'true')
    model = self.algModelManager.get_alg_model('test_model_1', '1.0.0', '2.0.0')
    print(r)
    print(model)
# 通过模型名称下载模型到本地文件
def test_download_alg_model_by_name_2_file(self):
    file = '/home/admin/aimaster/model/test_model.pmml'
    self.algModelManager.download_alg_model_by_name_2_file(file,
                                                           'test_model', '1.0.0')
    print(os.path.exists(file))
    with open(file, 'r') as f:
        print(f.readlines())
    file = 'test_model.pmml'
    self.algModelManager.download_alg_model_by_name_2_file(file,
                                                           'test_model', '1.0.0')
    print(os.path.exists(file))
    with open(file, 'r') as f:
        print(f.readlines())
    file = ''
    self.algModelManager.download_alg_model_by_name_2_file(file,
                                                           'test_model', '1.0.0')
    print(os.path.exists(file))
    with open(file, 'r') as f:
        print(f.readlines())

# 通过模型ID下载模型到本地文件
def test_download_alg_model_by_id_2_file(self):
    model_id = 213
    file = '/home/admin/aimaster/model/test_model.pmml'
    self.algModelManager.download_alg_model_by_id_2_file(file, model_id)
    print(os.path.exists(file))
    with open(file, 'r') as f:
        print(f.readlines())
```

