#Youku CSS Gideline

> 部分less or sass的代码规范也做参考

## 1. CSS支持标准 

（注：根据2014年4月数据整理）

*  A级－交互和视觉完全符全设计的要求
*  B级－视觉上允许有所差异，但不破坏页面的整体效果
*  C级－可忽略设计上的细节，但不防碍功能使用

> 详情请参考Youku Graded OS Browser Support 文档


##2. Youku Cake CSS 框架(Core核心库、Atom元件、Kit组件、Extend扩充组件)

 * 主站全局CSS文件 - cake.css (压缩合并后文件 包含 cake.less、atom.less、kit.less、extend.less)
 * Cake 核心模块 - core.css （包含reset、栅格、文字排版、颜色) - /style/core.less
   * 基础变量 /style/core/base.less
   * 基础环境 /style/core/reset.less
   * 栅格布局 /style/core/layout.less
   * 文字 /style/core/font.less
   * 颜色 /style/core/color.less
 * Cake 元件模块（持续更新）- /style/atom.less
   * 通用模块容器 /style/atom/mod.less
   * 按钮  /style/atom/btn.less
 * Cake 组件模块（持续更新）- /style/kit.less
   * 视频 /style/kit/video.less
   * 分页 /style/kit/pagination.css

##3. CSS文件的目录管理

所有的CSS分为两大类：核心库和业务类。

 * 通用的CSS文件，放在如下目录中：
<table width="300" style="margin-left:60px;">
<tbody><tr><td> 核心库 </td><td style="text-align: left"> /css/core 
</td></tr><tr><td> 通用UI元素样式库 </td><td style="text-align: left"> /css/atom
</td></tr><tr><td> 交互组件相关样式库 </td><td style="text-align: left"> /css/ui
</td></tr></tbody></table>

 * 业务类的CSS是指和具体产品（如付费、分成）相关的文件，放在如下目录中：
<table width="200" style="margin-left:60px;">
<tbody><tr><td> 播放页 </td><td style="text-align: left"> /style/play/ 
</td></tr><tr><td> 付费 </td><td style="text-align: left"> /style/pay/ 
</td></tr><tr><td> 分成 </td><td style="text-align: left"> /style/share/ 
</td></tr><tr><td> 明星 </td><td style="text-align: left"> /style/star/ 
</td></tr><tr><td> 指数 </td><td style="text-align: left"> /style/vr/ 
</td></tr><tr><td> CMS </td><td style="text-align: left"> /style/cms/ 
</td></tr><tr><td style="text-align: center">  ...  </td><td style="text-align: left"> /style/产品名称 
</td></tr></tbody></table>

 * 外联CSS文件适用于全站级和产品级通用的大文件。
 * 内联CSS文件适用于在一个或几个页面共用的CSS。
 * CSS(外联和内联)必须放在head里
 
##4. 代码和模块化的组织 

* 使用和完善现有CSS库
* 单个CSS文件避免过大
* CSS文件嵌套不要超过一层
* 以组件为单位组织代码段。
* 制定一致的注释规范。
* 使用一致的空白符将代码分隔成块，这样利于扫描较大的文档。
* 开发中，应尽量按功能分解大文件，实现模块化的文件组织。
* 如果使用了多个 CSS 文件，将其按照组件而非页面的形式分拆，因为页面会被重组，而组件只会被移动。

##5. 不要轻易改动全站级CSS和通用CSS库。改动后，要经过全面测试

##6. CSS书写规范（部分包含Less & Sass）

 * 用两个空格来代替制表符（tab） -- 这是唯一能保证在所有环境下获得一致展现的方法。
 * 选择器分组时，将单独的选择器单独放在一行
 * 绝对不要在CSS中使用"*"选择符
 * 为了代码的易读性，在每个声明块的左花括号前添加一个空格。
 * 声明块的右花括号应当单独成行。
 * 避免直接定义标签的样式。 
 * 每条声明语句的 : 后应该插入一个空格。
 * 为了获得更准确的错误报告，每条声明都应该独占一行。
 * 所有声明语句都应当以分号结尾。最后一条声明语句后面的分号是可选的，但是，如果省略这个分号，你的代码可能更易出错。
 * 对于以逗号分隔的属性值，每个逗号后面都应该插入一个空格（例如，`box-shadow`）。
 * 不要在 `rgb()`、`rgba()`、`hsl()`、`hsla()` 或 `rect()` 值的内部的逗号后面插入空格。这样利于从多个属性值（既加逗号也加空格）中区分多个颜色值（只加逗号，不加空格）。
 * 对于属性值或颜色参数，省略小于 1 的小数前面的 0 （例如，`.5` 代替 `0.5`；`-.5px` 代替 `-0.5px`）。
 * 十六进制值应该全部小写，例如，`#fff`。在扫描文档时，小写字符易于分辨，因为他们的形式更易于区分。尽量使用简写形式的十六进制值，例如，用 `#fff` 代替 `#ffffff`。
 * 选择器中的属性添加双引号，例如，`input[type="text"]`。只有在某些情况下是可选的，但是，为了代码的一致性，建议都加上双引号。
 * 避免为 0 值指定单位，例如，用 `margin: 0;` 代替 `margin: 0px;`。
 * 兼容多个浏览器时，将标准规则声明写在后面
 * 当使用特定厂商的带有前缀的属性时，通过缩进的方式，让每个属性的值在垂直方向对其，这样便于多行编辑。
 * 简写形式的属性声明
 * 声明书写顺序
	* Positioning
	* Box model
	* Typographic
	* Visual
 
			/* Bad CSS */
			.selector, .selector-secondary, .selector[type=text],div {
        		border-radius: 4px;
        		top:0;right:0;left:0;bottom:0;
        		z-index:100;
        		left:10px;width:100px;height:100px;
  				-webkit-border-radius: 4px;
      			-moz-border-radius: 4px;
 				padding:15px;margin:0px 0px 15px;
 				background-color:rgba(0, 0, 0, 0.5);
 				position:absolute;
 				box-shadow:0px 1px 2px #CCC,inset 0 1px 0 #FFFFFF
				font: normal 13px "Helvetica Neue", sans-serif;
				line-height: 1.5;
				color: #333;
				text-align: center;
				_width:110px;
			}
			
			/* Good CSS */
			.selector,
			.selector-secondary,
			.selector[type="text"] {
			
				/* Positioning */
				position: absolute;
				top: 0;
				right: 0;
				bottom: 0;
				left: 0;
				z-index: 100;
				
				/* Box-model */
				display: block;
				float: right;
				width: 100px;
				height: 100px;
				padding: 15px;
				margin-bottom: 15px;
				
				/* Typography */
				font: normal 13px "Helvetica Neue", sans-serif;
				line-height: 1.5;
				color: #333;
				text-align: center;
				
				/* Visual */
				background-color: #fff;
				border: 1px solid #e5e5e5;
  				-webkit-border-radius: 4px;
      			   -moz-border-radius: 4px;
        			    border-radius: 4px;

				/* Misc */
				opacity: 0.9;
				
				/* Hack 可单独创建文件 */
				_width:110px;
				width:110px/9;
			}
* 单行规则声明,`只包含一条声明`

		.span1 { width: 60px; }
		.span2 { width: 140px; }
		.span3 { width: 220px; }

* id和Class命名规则
	* id是用来标识具体模块，命名必须具体且唯一，由前缀和名字组成。不要滥用ID。如： #yk-video-list、#group-member-list等。采用驼峰写法 `videoList`
	* class 名称中只能出现小写字符和破折号（dashe）（不是下划线，也不是驼峰命名法）。破折号应当用于相关 class 的命名（类似于命名空间）（例如，`.btn` 和 `.btn-danger`）。
	* 避免过度任意的简写。`.btn` 代表 button，但是 `.s` 不能表达任何意思。
	* class 名称应当尽可能短，并且意义明确。
	* 使用`js-*`的class来表示行为（与样式相对）,不要将这些class包含到css文件中
	* 使用有意义的名称。使用有组织的或目的明确的名称，不要使用表现形式（`left`）的名称。
		
			推荐使用的class名：
		
			表示状态 : .on, .active, .selected, .hili 
			表示位置 : .first, .last, .main, .side 
			表示结构 : .hd, .bd, .ft, .col, .section 
			通用元素 : .tb, .frm, .nav, .list, .item, .tag, .pic, .info 
		
* 媒体查询（Media query）的位置
> 将媒体查询放在尽可能相关规则的附近。不要将他们打包放在一个单一样式文件中或者放在文档底部。如果你把他们分开了，将来只会被大家遗忘。下面给出一个典型的实例。

		.element { ... }
		.element-avatar { ... }
		.element-selected { ... }

		@media (min-width: 480px) {
		.element { ...}
		.element-avatar { ... }
		.element-selected { ... }
		}	

* Less 和 Sass 中的嵌套
> 避免非必要的嵌套。这是因为虽然你可以使用嵌套，但是并不意味着应该使用嵌套。只有在必须将样式限制在父元素内（也就是后代选择器），并且存在多个需要嵌套的元素时才使用嵌套。

		// Without nesting
		.table > thead > tr > th { … }
		.table > thead > tr > td { … }

		// With nesting
		.table > thead > tr {
		  > th { … }
		  > td { … }
		}


##7.  注释书写形式

> 注释内容单行控制在40个中文或80个英文字符宽。注释的格式：

* 多行注释(文件级)

		/************************************************************
		*
		*	@name 		:	文件或组件名字
		*	@desc 		:	文件或组件介绍
		*	@author		:	作者
		*	@require	:	依赖less
		*	@date		:	修改时间
		*
		************************************************************>

* 单行注释（模块级）

		/* mod: video */ 		 

 * 规则分类放在一起。通用规则在具体业务规则的前面。如：

		/* layout */
		...
		/* mod */
		...
		/* nav */
		...
		/* mod: slider */
		...


##9. 避免滥用CSS Hack

推荐使用下面的：

区别属性：
<table width="300" style="margin-left:60px;">
<tbody><tr><td> IE6 </td><td style="text-align:left;"> _property:value 
</td></tr><tr><td> IE6/7 </td><td style="text-align:left;"> *property:value 
</td></tr><tr><td> IE6/7/8/9 </td><td style="text-align:left;"> property:value\9 
</td></tr></tbody></table>
区别规则：
<table width="70%" style="margin-left:60px;">
<tbody><tr><td> IE6 </td><td style="text-align:left;"> * html selector { ... } 
</td></tr><tr><td> IE7 </td><td style="text-align:left;"> *:first-child+html selector { ... } 
</td></tr><tr><td> 非IE6 </td><td style="text-align:left;"> html&gt;body selector { ... } 
</td></tr><tr><td> firefox only </td><td style="text-align:left;"> @-moz-document url-prefix() { ... } 
</td></tr><tr><td> saf3+/chrome1+ </td><td style="text-align:left;"> @media all and (-webkit-min-device-pixel-ratio:0) { ... } 
</td></tr><tr><td> opera only </td><td style="text-align:left;"> @media all and (-webkit-min-device-pixel-ratio:10000),not all and (-webkit-min-device-pixel-ratio:0) { ... } 
</td></tr><tr><td> iPhone/mobile webkit </td><td style="text-align:left;"> @media screen and (max-device-width: 480px) { ... } 
</td></tr></tbody></table>


##10. 使用after或overflow的方式清浮动，不要在html里增加多余的标签

##11. 避免使用低效的选择器

	body > * {...}
	ul > li > a {...}
	#footer > h3 {...}
	ul#top_blue_nav {...}
	#searbar span.submit a { ... }
	.target #target-node { ... }

##12. 避免使用filter

##13. 避免在标签上直接写样式。如:

	<div style="margin-bottom:30px;">

##14. 避免在CSS中使用expression

##15. 避免在CSS中使用@import

##16. 尽量不要在CSS中使用!important


