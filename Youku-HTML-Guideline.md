#Youku HTML Gideline

##1.文件规范

* DTD(doctype)统一用HTML5 文档声明 
	
			<!doctype html>

* 文件字符集格式统一为utf-8编码

			<meta charset="utf-8" />
			
* 必须添加注释
	* 页面级别 

			<!------------------------------------------------------------
			|
			|	@name 		:	文件或组件名字
			|	@desc 		:	文件或组件介绍
			|	@author		:	作者
			|	@require	:	依赖样式
			|	@date		:	修改时间
			|
			-------------------------------------------------------------->
	* 模块级
		
			<!-- 模块名字 -->
			
* html扩展名为`.html`

	
##2.书写规范

* 表签名、属性名、必须用小写字母且不能简写 `禁止用拼音命名`（id除外,id可采用驼峰写法 i.e. toolBarItem）

* 代码排版用`tab` or `4个空格` 模块间隔要用一空行间隔

* 避免将样式写入标签

		<div style="background:red;width:100px;height:50px;"></div>
 	
* 元素必须正确嵌套并在结束处标明注释

		<div class="content">
			<div class="carousel">
			</div><!-- carousel -->
		</div><!-- content -->

* 元素必须关闭标签 包括自闭合标签 i.e. `<hr />` as `<hr>`, `<br />` as `<br>` and `<img />` as `<img>`,`<meta />` as `<meta>`.

* 给所有属性赋值

		<input disabled="disabled" checked="checked" />
		
* 给所有`<img />`标签增加`title`和`alt`属性赋值

		<img src="" alt="视频标题" title="视频标题" />
		
* 合理使用标签嵌套(内联元素不允许嵌套块级元素)

* table表格只承载数据不能应用于布局
		
* ARIA roles 为模块的功能设定

		<nav class="nav" role="navigation">
			<ul>
				<li>...</li>
				<li>...</li>
			</ul>
		</div><!-- navigation -->

		<div class="spacer" role="separator"></div>
