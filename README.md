# Web Base(Web 基础)

本仓库包含部分 HTML 知识及全面详实的 CSS 知识。便于开发中的快速查询。

> 前置知识：对 HTML5、CSS3 有一定了解。  
> 说明：本仓库的名词并不专业严谨，只求便于理解。  

# 目录（Contents）

* [1. HTML](#1-html)
    * [1.1 HTML 常见元素](#11-html-常见元素)
        * [1.1.1 head 元素](#111-head-元素)
        * [1.1.2 body 元素](#112-body-元素)
    * [1.2 HTML 元素分类](#12-html-元素分类)
    * [1.3 HTML 元素嵌套关系](#13-html-元素嵌套关系)
    * [1.4 HTML 元素的默认样式](#14-html-元素的默认样式)
* [2. CSS](#2-css)

## 1. HTML

[h5o - HTML 大纲算法工具](http://h5o.github.io)

### 1.1 HTML 常见元素

#### 1.1.1 head 元素

head 元素 不会在页面上留下直接的内容，主要为页面相关资源及信息描述。  

* 声明 - [meta](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/meta)
    * `<meta charset='utf-8'>` - `charset`表示页面使用的字符集
    * `<mate name='viewport' content='width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no‘>` - 控制缩放（此属性对多端适配非常有用）
        * `name='viewport'` - 视口，表示页面显示的范围
        * `width=device-width` - 显示宽度，`device-width` - 此处为设备宽度
        * `initial-scale=1.0` - 默认缩放，此处为1
        * `maximum-scale=1.0` - 最大缩放，此处为1
        * `user-scalable=no` - 用户缩放，此处为不允许用户缩放
* 标题 - [title](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/title)
* 样式 - [style](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/style)
* 链接 - [link](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/link)
* 脚本 - [script](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/script)
* 制定基础路径 - [base](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/base)`<base href="" />`（较少使用，设置此标签则表示本页面中所有链接都基于此路径）

#### 1.1.2 body 元素

body 元素 的内容会直接出现在页面上。

> 括号中的内容为对应标签在 HTML5 中的语义，更多内容可访问：  
https://developer.mozilla.org/zh-CN/docs/Glossary/语义#语义化元素

* 块级元素 - div / section（文章、文字） / article（文章） / aside（侧边栏、广告） / nav（菜单、导航） / header（头部） / footer（尾部） / i（icon 图标）
* 段落元素 - p
* 行内元素 - span / label / em（强调 - 斜体） / strong（强调 - 粗体）
* 表格元素 - [table](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/table) / thead / tbody / tr / td / th
    * td
        * `colspan` - 跨列
        * `rowspan` - 跨行
* 列表元素 - ul / ol / li / dt / dd
* 表单元素 - form / [input](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/Input) / [select](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/select) / [textarea](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/textarea) / [button](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/button)
    * placeholder - 表单的默认显示（提示）内容
    * [form](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/form)
        * `target` - 表单提交的地址
        * `method` - 表单提交的方式（GET/POST）
        * `enctype` - (POST请求时)提交时使用的编码格式
    * button
        * `type` - 按钮类型
            * `button`普通按钮
            * `submit`提交按钮（form中生效），`input` 中 `type='submit'` 与此作用相同
            * `reset`重置按钮（form中生效）
* 链接 - a / img
    * [a](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/a)
        * `a[href]` - 链接地址
        * `a[target]` - 指定在哪里打开链接，`_self`(默认)在当前窗口打开；`_blank`新窗口打开
    * img
        * `img[src]` - 图片地址
        * `img[alt]` - 替换资源，图片不可用时使用

> 延伸：  
> [HTML 元素参考
](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element) | [HTML5
](https://developer.mozilla.org/zh-CN/docs/Web/Guide/HTML/HTML5) | [HTML表单指南
](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Forms) | [SEO(语义
)](https://developer.mozilla.org/zh-CN/docs/Glossary/语义)


### 1.2 HTML 元素分类

按默认样式分类： 块级 block、行内 inline、inline-block

按内容分类：
https://www.w3.org/TR/html5/dom.html#kinds-of-content


### 1.3 HTML 元素嵌套关系

* 块级元素可以包含行内元素
* 块级元素不一定能包含块级
* 行内元素一般不能包含块级元素

> 延伸：[Text-level semantics](https://www.w3.org/TR/html5/textlevel-semantics.html) | [22 Transitional Document Type Definition](https://www.w3.org/TR/1999/REC-html401-19991224/sgml/loosedtd.html) | [Allowed nesting of elements in HTML 4 (and XHTML 1.0)](http://jkorpela.fi/html/nesting.html)

### 1.4 HTML 元素的默认样式

浏览器会自动为一些元素加默认样式。

[CSS Reset](https://cssreset.com)  
[CSS Tools: Reset CSS](https://meyerweb.com/eric/tools/css/reset/)  
[YUI CSS Reset](https://cssreset.com/scripts/yahoo-css-reset-yui-3/)

CSS Reset 重置默认样式
[normalize.css](http://necolas.github.io/normalize.css/) | 
[Github](https://github.com/necolas/normalize.css/)

## 2. CSS