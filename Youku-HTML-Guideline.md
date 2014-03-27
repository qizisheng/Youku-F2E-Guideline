#Youku HTML Gideline

##1.文件规范

* DTD(doctype)统一用HTML5 文档声明 
	
			<!doctype html>

* 文件字符集格式统一为utf-8编码

			<meta charset="utf-8" />
	
##2.书写规范

* 元素必须正确嵌套并在结束处标明注释


		<div class="content">
			<div class="carousel">
			</div><!-- carousel -->
		</div><!-- content -->


* 元素必须关闭标签
* 表签名、属性名、必须用小写字母且不能简写（id除外）
* 给所有属性赋值
