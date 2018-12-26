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
    * [2.1 CSS 基础](#21-css-基础)
        * [2.1.1 CSS 基本规则](#211-css-基本规则)
        * [2.1.2 选择器](#212-选择器)
            * [2.1.2.1 选择器的分类](#2121-选择器的分类)
            * [2.1.2.2 选择器的权重](#2122-选择器的权重)
    * [2.2 CSS 布局](#22-css-布局)
        * [2.2.1 非布局样式](#221-非布局样式)
            * [2.2.1.1 文字 - 字体](#2211-文字---字体)


## 1. HTML

[h5o - HTML 大纲算法工具](http://h5o.github.io)

### 1.1 HTML 常见元素

#### 1.1.1 head 元素

head 元素 不会在页面上留下直接的内容，主要为页面相关资源及信息描述。  

* 声明 - [meta](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/meta)
    * `<meta charset='utf-8'>` - `charset`表示页面使用的字符集
    * `<mate name='viewport' content='width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no‘>` - 控制缩放（此属性对多端适配非常有用）
        * `name='viewport'` - 视口，表示页面显示的范围
        * `width=device-width` - 显示宽度，`device-width` - 此处为设备宽度
        * `initial-scale=1.0` - 默认缩放，此处为1
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

* 块级元素 - div / section（文章、文字） / article（文章） / aside（侧边栏、广告） / nav（菜单、导航） / header（头部） / footer（尾部） / i（icon 图标）
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
        * `a[href]` - 链接地址
        * `a[target]` - 指定在哪里打开链接，`_self`(默认)在当前窗口打开；`_blank`新窗口打开
    * img
        * `img[src]` - 图片地址
        * `img[alt]` - 替换资源，图片不可用时使用

> 延伸：  
> [HTML 参考
](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference) | [HTML5
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

## 2. [CSS](https://developer.mozilla.org/zh-CN/docs/Web/CSS)

> CSS：层叠样式表（Cascading Style Sheet）  
[CSS](https://developer.mozilla.org/zh-CN/docs/Glossary/CSS) | 
[CSS 参考
](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference)
[CSS 教程
](https://developer.mozilla.org/zh-CN/docs/Learn/CSS) | 
[CSS 文档
](https://developer.mozilla.org/zh-CN/docs/Web/CSS)

### 2.1 CSS 基础

#### 2.1.1 CSS 基本规则

```text
选择器 {
    属性(Property): 值(Value);
    ...
}
```

> 值后面的分号(`;`)可以不加，但建议为每一行加上分号

#### 2.1.2 [选择器](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Introduction_to_CSS/Selectors)

* 匹配 HTML 元素
* 有不同的匹配规则
* 多个选择器可叠加

##### 2.1.2.1 [选择器的分类](https://developer.mozilla.org/zh-CN/search?q=选择器&topic=api&topic=css&topic=canvas&topic=html&topic=http&topic=js&topic=svg&topic=standards&topic=webdev&topic=webext&topic=webgl&topic=apps&topic=mobile)

1. 元素选择器 - a
2. [伪元素](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Pseudo-elements)选择器 - ::before
3. 类选择器 - .class-name
4. 属性选择器 - [Property-name=Property-value]
5. [伪类](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)选择器 - :hover
6. ID 选择器 - #id-name
7. 否定选择器 - :not(...)
8. 通用选择器 - * (匹配所有元素)
9. [组合选择器](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Introduction_to_CSS/Combinators_and_multiple_selectors)

##### 2.1.2.2 [选择器的权重](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Specificity)

按先后顺序，同一级别下权重相同，不同级别下数值越小权重越高：

1. ID 选择器
2. 类 属性 伪类
3. 元素 伪元素
4. 其它

> 在同一元素被多个选择器选中时，浏览器会优先应用优先级较低的选择器的样式，再应用优先级高的选择器的样式，如果设定了重复的样式，则会使用优先级高的选择器的样式。

属性生效的其它规则：

* !important 优先级最高（除了另一个!important，谁不可覆盖）
* 内联样式 优先级高（高于 ID 选择器）
* 相同权重 后写的生效

### 2.2 CSS [布局](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/CSS_layout)

#### 2.2.1 非布局样式

* 文字 - [字体](#2211-文字---字体)、字重、颜色、大小、行高
* 盒子 - 背景、边框
* 页面 - 滚动、换行
* 装饰性样式 - 粗体、斜体、下划线
* 其它

##### 2.2.1.1 文字 - 字体

* 字体族（使用字体族时不要加引号）  
    serif(衬线字体)、sans-serif(非衬线字体)、monospace(等宽字体)、cursive(手写体)、fantasy(花体)
* 多字体（fallback）  
* 网络字体、自定义字体  
* iconfont  

> 在声明字体时先写平台独有的字体再加字体族是一个好的习惯
> ```css
> font-family: "PingFang SC", "Microsoft Yahei", monospace;
> ```
> 由于苹果用户在安装Office后也会有 `Microsoft Yahei`，但 `Microsoft Yahei` 在Mac上的效果不如 `PingFang SC` 因此将 `PingFang SC` 在前面

### 2.4 CSS 效果

### 2.5 CSS 动画

### 2.6 预处理器

### 2.7 CSS 工程化
