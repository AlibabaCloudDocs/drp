# Java SDK {#concept_jdd_wp5_hhb .concept}

## 概览 {#section_ucc_tbh_jhb .section}

该SDK为AIMaster算法模型管理Java版，主要提供了模型的上传、下载、查询、删除、版本控制等功能

## 运行环境 {#section_vcc_tbh_jhb .section}

Java Version 1.8

## Maven坐标 {#section_ekj_7vp_ud7 .section}

``` {#codeblock_787_plu_2iz}
<dependency>
  <groupId>com.aliyun.asap</groupId>
  <artifactId>alg-model-sdk</artifactId>
  <version>1.0.0-SNAPSHOT</version>
</dependency>
```

## 使用样例 {#section_fuz_xcm_6yb .section}

``` {#codeblock_cok_evf_zix}
import com.alibaba.cosmo.remote.http.HttpRawResultHandler;
import com.aliyun.asap.AlgModelManager;
import com.aliyun.asap.model.AlgModel;
import com.aliyun.dtboost.asap.sdk.model.Enums;
import com.aliyun.dtboost.asap.sdk.model.alg.model.AlgModelInfo;
import com.google.gson.JsonArray;
import com.google.gson.JsonElement;
import com.google.gson.JsonObject;
import com.google.gson.JsonParser;
import org.junit.Test;
import java.io.File;
import java.io.FileNotFoundException;
import java.util.List;

public class AlgModelTest {

    protected final static String endPoint = "http://10.125.25.106";
    protected final static String tenant = "dtboost";
    protected final static String userid = "1696462764375572";
    protected final static String accessId = "xxx";
    protected final static String accessKey = "xxx";
    protected final static String algCode = "example_agl_4_model";
    protected final static String algVersion = "1.1.0";
    protected final static Integer timeout = 5*60;

    //构建算法模型管理器
/   //timeout:模型超时时间设置(单位秒)，默认10分钟
    private AlgModelManager getAlgModelManager() {
        return new AlgModelManager(endPoint, tenant, userid, accessId, accessKey, algCode, algVersion, timeout);
    }

    //上传模型文件
    @Test
    public void addModelTest() {

        File file = new File("/.../test.xml");
        AlgModel algModel = new AlgModel();
        algModel.setModelName("page_sql_1");
        algModel.setModelVersion("1.0.0");
     //自定义类型：Enums.AlgModelFileType.CUSTOMIZED
        //true:模型已存在时强制更新
        long save = getAlgModelManager().save(file, algModel, Enums.AlgModelFileType.PMML, true);
        System.out.println(">>>>>>>>>>>" + save);
    }

    //通过模型名称查询该模型名称下的所有版本的模型文件信息
    @Test
    public void listAlgModelsByNameTest() {
        List<AlgModelInfo> algModels = getAlgModelManager().listAlgModelsByName("page_sql_1");
        for (AlgModelInfo algModel : algModels) {
            System.out.println(">>>>>>>>>>>" + algModel);
        }
    }

    //通过模型名称 + 模型版本查询模型详细信息
    @Test
    public void getAlgModelTest() {
        AlgModel algModel = new AlgModel();
        algModel.setModelName("page_sql_1");
        algModel.setModelVersion("1.0.0");
        AlgModelInfo algModel1 = getAlgModelManager().getAlgModel(algModel);
        System.out.println(">>>>>>>>>>>" + algModel1);
    }

    //通过模型名称 + 模型版本删除模型
    @Test
    public void deleteAlgModelTest() {
        AlgModel algModel = new AlgModel();
        algModel.setModelName("page_sql_1");
        algModel.setModelVersion("1.0.0");
        boolean b = getAlgModelManager().delAlgModel(algModel);
        System.out.println(">>>>>>>>>>>" + b);
    }

    //通过模型ID下载模型文件
    @Test
    public void getModelFileByModelIdTest() {
        Long modelId = 21L;
        try {
            HttpRawResultHandler.FileHandler fileHandler = new HttpRawResultHandler.FileHandler("/Users/kongsh/MyGit/alg-model-sdk/src/test/resources/test1.xml");
            getAlgModelManager().getModelFileByModelId(modelId, fileHandler);
        } catch (FileNotFoundException e) {
            e.printStackTrace();
        }
    }

    //通过模型名称 + 模型版本下载模型文件
    @Test
    public void getModelFileTest() {
        AlgModel algModel = new AlgModel();
        algModel.setModelName("page_sql_1");
        algModel.setModelVersion("1.0.0");
        try {
            HttpRawResultHandler.FileHandler fileHandler = new HttpRawResultHandler.FileHandler("/Users/kongsh/MyGit/alg-model-sdk/src/test/resources/test2.xml");
            getAlgModelManager().getModelFile(algModel,fileHandler);
        } catch (FileNotFoundException e) {
            e.printStackTrace();
        }
    }
}
```

