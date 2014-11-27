preview v1.1.0
=======

纯浏览器端的图片预览组件<br/>
支持IE5.5~IE11、Chrome、FF、Safari和Opera<br/>

**Usage**<br/>
````
<input type="file" id="icon1" accept="image/jpeg"/>&nbsp;<button onclick="pv1.reset()">重置</button>
<div class="preview" id="pv1"></div>
<input type="file" id="icon2" accept="image/jpeg"/>&nbsp;<button onclick="pv2.reset()">重置</button>
<div class="preview" id="pv2"></div>
<script type="text/javascript" src="./preview.js"></script>
<script type="text/javascript">
  var get = function(id){
  	return document.getElementById(id);
  };
  var pv1 = new Preview(get('icon1'), get('pv1'));
  var pv2 = Preview(get('pv2'), get('icon2'));
</script>
````

**v1.1.0**<br/>
1. 图片预览实例添加`reset()`方法，用于重置组件；<br/>
2. `Preview构造函数`入参由原来的顺序设置fileEl,previewEl改为无序设置。

**v.1.0**<br/>
全局重构

**v.0.5**<br/>
IE10+通过window.URL.createObjectURL替代FileReader，缩短Data URI Scheme长度从而提高性能。

**v0.4**<br/>
新增上传文件MIME类型筛选。默认值为`image/*`,通过input的accept属性值设置。<br/>

**v0.3**<br/>
修复FF3.0不支持`FileReader`的bug。<br/>

**v0.2**<br/>
修复IE11下当`document.documentMode < 10`时无法预览图片的bug。<br/>

**v0.1**<br/>
通过滤镜和`FileReader`实现图片预览功能。<br/>
 
