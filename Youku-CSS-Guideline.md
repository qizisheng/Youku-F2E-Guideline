#Youku CSS Gideline
-------------------------------------------------------


## 1. CSS支持标准 

（注：根据2014年3月数据整理）

*  A级－交互和视觉完全符全设计的要求
*  B级－视觉上允许有所差异，但不破坏页面的整体效果
*  C级－可忽略设计上的细节，但不防碍功能使用

###PC端

<table width="100%"
    <tbody>
        <tr>
            <th> </th>
            <th style="background:#f5f5f5"> WinXP </th>
            <th style="background:#f5f5f5"> Win7 </th>
            <th style="background:#f5f5f5"> OS X </th>
        </tr>
        <tr>
            <td> IE10+ </td>
            <td> B  </td>
            <td> B </td>
            <td> </td>
        </tr>
        <tr>
            <td> IE9 </td>
            <td> B  </td>
            <td> B </td>
            <td> </td>
        </tr>
        <tr>
            <td> IE8 </td>
            <td> A  </td>
            <td> A </td>
            <td> </td>
        </tr>
        <tr>
            <td> IE7 </td>
            <td> B  </td>
            <td> B </td>
            <td> </td>
        </tr>
        <tr>
            <td> IE6 </td>
            <td> B  </td>
            <td> B </td>
            <td> </td>
        </tr>
        <tr>
            <td> Chrome30+ </td>
            <td> A  </td>
            <td> A </td>
            <td> A </td>
        </tr>
        <tr>
            <td> Chrome20- </td>
            <td> B  </td>
            <td> B </td>
            <td> B </td>
        </tr>
        <tr>
            <td> Firefox10 </td>
            <td> A </td>
            <td> A </td>
            <td> A </td>
        </tr>
        <tr>
            <td> Firefox9 </td>
            <td> A  </td>
            <td> A </td>
            <td> A </td>
        </tr>
        <tr>
            <td> Safari </td>
            <td> B  </td>
            <td> B </td>
            <td> B </td>
        </tr>
        <tr>
            <td> Opera </td>
            <td> C  </td>
            <td> C </td>
            <td> C </td>
        </tr>
    </tbody>
</table>


###移动端




##2. Youku Cake CSS 框架(Core核心库、Atom元件、Kit组件、Extend扩充组件)
---------------------
 * 2-1. 主站全局CSS文件 - cake.css (压缩合并后文件 包含 cake.less、atom.less、kit.less、extend.less)
 * 2-2. Cake 核心模块 - core.css （包含reset、栅格、文字排版、颜色) - /style/core.less
   * core-01. 基础变量 /style/core/base.less
   * core-02. 基础环境 /style/core/reset.less
   * core-03. 栅格布局 /style/core/layout.less
   * core-04. 文字 /style/core/font.less
   * core-05. 颜色 /style/core/color.less
 * 2-3. Cake 元件模块（持续更新）- /style/atom.less
   * atom-01. 通用模块容器 /style/atom/mod.less
   * atom-02. 按钮  /style/atom/btn.less
 * 2-4. Cake 组件模块（持续更新）- /style/kit.less
   * kit-01. 视频 /style/kit/video.less
   * kit-02. 分页 /style/kit/pagination.css

3. CSS文件的目录管理
---------------------
所有的CSS分为两大类：核心库和业务类。

 * 3-1. 通用的CSS文件，放在如下目录中：
<table width="300" style="margin-left:60px;">
<tbody><tr><td> 核心库 </td><td style="text-align: left"> /css/core 
</td></tr><tr><td> 通用UI元素样式库 </td><td style="text-align: left"> /css/atom
</td></tr><tr><td> 交互组件相关样式库 </td><td style="text-align: left"> /css/ui
</td></tr></tbody></table>

 * 3-2. 业务类的CSS是指和具体产品（如付费、分成）相关的文件，放在如下目录中：
<table width="200" style="margin-left:60px;">
<tbody><tr><td> 播放页 </td><td style="text-align: left"> /style/play/ 
</td></tr><tr><td> 付费 </td><td style="text-align: left"> /style/pay/ 
</td></tr><tr><td> 分成 </td><td style="text-align: left"> /style/share/ 
</td></tr><tr><td> 明星 </td><td style="text-align: left"> /style/star/ 
</td></tr><tr><td> 指数 </td><td style="text-align: left"> /style/vr/ 
</td></tr><tr><td> CMS </td><td style="text-align: left"> /style/cms/ 
</td></tr><tr><td style="text-align: center">  ...  </td><td style="text-align: left"> /style/产品名称 
</td></tr></tbody></table>

 * 3-3. 外联CSS文件适用于全站级和产品级通用的大文件。
 * 3-4. 内联CSS文件适用于在一个或几个页面共用的CSS。

4. CSS的模块化组织 
---------------------

开发中，应尽量按功能分解大文件，实现模块化的文件组织。

 * 使用和完善现有CSS库（见2-4）。
 * 单个CSS文件避免过大（建议少于300行）。
 * CSS文件嵌套不要超过一层

5. 不要轻易改动全站级CSS和通用CSS库。改动后，要经过全面测试
---------------------------------------------------------

6. 单条CSS规则的书写格式要求
---------------------

 * 6-1. 单行形式适用于直接写在页面中和长文件的情况。声明写在一行。需要在“{"和"}”前后加空格。
（注：在很长的文件中，单行形式有利于检索选择器）

```css
    .selector { property:value;property:value; }
```

简短规则声明（1或2个）也适用单行形式。

```css
    .selector { property:value; }
```

 * 6-2. 格式化书写形式。适用于不是很长的模块文件或CSS3语法。冒号后加空格。

```css
    .selector { 
        property: value;
        property: value; 
    }
```

CSS3兼容书写形式和对齐方式：

```css
    .selector { 
      -webkit-box-shadow: 0 0 5px rgba(200, 200,200, 0.8);
         -moz-box-shadow: 0 0 5px rgba(200, 200,200, 0.8);
              box-shadow: 0 0 5px rgba(200, 200,200, 0.8);
    }
```

CSS3中逗号分隔的长属性值：

```css
    .selector {
        box-shadow:
            1px 1px 1px #000,
            2px 2px 1px 1px #ccc inset;
        background-image:
            linear-gradient(#fff, #ccc),
            linear-gradient(#f3c, #4ec);
    }
```

 * 6-3. 多个(>2)selector每个占一行：

```css
    .selector1,
    .selector2,
    .selector3 { ... }
```

 * 6-4. 规则声明的顺序：定位、盒模型（width/height/padding/border/margin）、行高、字体/字号/颜色、背景、CSS3效果等

 * 6-5. 兼容多个浏览器时，将标准规则声明写在后面，如：

```css
    -webkit-border-radius: 4px;
       -moz-border-radius: 4px;
            border-radius: 4px;
```


7.  注释书写形式
--------------
 * 7-1. 注释内容单行控制在40个中文或80个英文字符宽。注释的格式：

```css
     /* 
      * mod     : video 
      * author  : guohuimin@youku.com 
      * 描述内容
      */
```

SCSS中支持单行注释

```css
    // mod: video
```

 * 7-2. 规则分类放在一起。通用规则在具体业务规则的前面。如：

```css
    /* layout */
    ...
    /* mod */
    ...
    /* nav */
    ...
    /* mod: slider */
    ...
```

8. ID和Class命名。命名不要用缩写(除一些公认的缩写，见8-4)，单词间用"-"做为连接符
-----------------------------------------------------------------------
 * 8-1. ID是用来标识具体模块，命名必须具体且唯一，由前缀和名字组成。不要滥用ID。如： #db-video-list、#group-member-list等。
 * 8-2. Class是用来标识某一类型的对象，命名简洁表意清楚。如：.list。
 * 8-3. 命名示例：

坏：

```css
    #rec
    .gray-link
    .broadsmr
    .pl
```   

好：

```css
    #db-nav-main
    .infobox
    .item
```

 * 8-4. 推荐使用的class名：
<table width="400" style="margin-left:60px;">
<tbody><tr><td> 表示状态 </td><td style="text-align:left;"> .on, .active, .selected, .hili 
</td></tr><tr><td> 表示位置 </td><td style="text-align:left;"> .first, .last, .main, .side 
</td></tr><tr><td> 表示结构 </td><td style="text-align:left;"> .hd, .bd, .ft, .col, .section 
</td></tr><tr><td> 通用元素</td><td style="text-align:left;"> .tb, .frm, .nav, .list, .item, .tag, .pic, .info 
</td></tr></tbody></table>


9. 避免滥用CSS Hack
-----------------------
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
注意：SCSS会自动转换一些不标准CSS写法，会破坏CSS Hack。


10. 使用after或overflow的方式清浮动，不要在html里增加多余的标签
--------------------------------------------------------

11. CSS必须放在head里
--------------------

12. 避免使用低效的选择器
---------------------
如：

```css
    body > * {...}
    ul > li > a {...}
    #footer > h3 {...}
    ul#top_blue_nav {...}
    #searbar span.submit a { ... }
    .target #target-node { ... }
```

13. 避免使用filter
--------------------

14. 避免直接定义标签的样式。如: div { ... } 
---------------------------

15. 避免在标签上直接写样式。如:&lt; div style="margin-bottom:30px;"&gt;
-----------------------------------------------------------

16. 避免在CSS中使用expression
---------------------------

17. 避免在CSS中使用@import
---------------------------

18. 尽量不要在CSS中使用!important
-----------------------------

19. 绝对不要在CSS中使用"*"选择符
----------------------------
