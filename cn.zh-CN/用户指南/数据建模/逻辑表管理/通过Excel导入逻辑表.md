通过Excel导入逻辑表 
=================================

支持用户通过导入标准格式或者Visual Paradigm格式的Excel文件方式，快速批量创建逻辑表。

前提条件
----

根据导入模板准备要导入的数据。

操作步骤 
-------------------------

1. 登录[数据资源平台控制台](https://dataq.console.aliyun.com)。

   

2. 在页面左上角，单击![工作台](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/4682213261/p280916.png)图标，选择 **研发工作台** 。

   

3. 在顶部菜单栏，单击 **资产加工** 。

   

4. 在左侧导航栏，选择![数据建模.png](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/4960303261/p268674.png) **数据建模** **\>** **数据模型设计** 。

   

5. 在数据模型下，选择需要的目录，单击![目录](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/5682213261/p280932.png)。

   

6. 在该目录右侧页面，单击 **导入** **\>** **Excel导入** 。![excel导入](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1032043261/p283197.png)

   

7. 在 **Excel导入逻辑表** 对话框，选择导入文件的格式、类型。![导入逻辑表](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/2716043261/p283198.png)

   1. 选择导入文件的格式。

      * **标准格式** ：待导入文件的格式，当选择该值时，主要针对模型目录、模型关系、模型列表等信息的导入。

        
      
      * **Visual Paradigm格式** ：待导入文件的格式，当选择该值时，需要通过Visual Paradigm工具建立逻辑表，将导出的VP格式文件进行导入。

        
      

      
      **说明**

      * 文件格式选择标准模式，导入的文件支持逻辑表和质量规则。

        
      
      * 文件格式选择Visual Paradigm格式，导入的文件仅支持逻辑表。

        
      

      
      
   
   2. 选择导入的文件类型。

      * **逻辑表** ：当选择该值时，表示当前导入的是标准格式的excel逻辑表。根据模型目录列表、目录模型关系和模型列表信息导入逻辑表。

        
      
      * **质量规则** ：当选择该值时，表示当前导入的是excel格式的质量规则。根据模型规则、字段规则和自定义规则信息导入逻辑表的规则。

        
      

      
   
   3. （可选）单击 **下载模板** ，下载模板文件，并根据不同模板填写逻辑表数据信息或者质量规则。

      
   

   

8. 导入准备好的文件。

   * 单击 **点击区域** ，选择本地文件上传。

     
   
   * 将本地文档直接拖拽至导入区域。

     
   
   <group data-tag="info" id="info-x3i-2lo-z84" class="info">
   **说明**

   选择文件时，请注意导入的是逻辑表模板还是规则模板。
   </group>

   

9. 单击 **确定** 。界面提示导入成功后刷新页面，可在模型目录 对应的右侧列表页面查看导入的逻辑表。![导入结果](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/7923293261/p283211.png)

   



