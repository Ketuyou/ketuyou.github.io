---
layout: post
title: 关于垂直居中
category : css
---
### 单行文字垂直居中

```html
<div class="demo">我们来看看这行文字是不是垂直居中。</div>
```
```css
.demo{ line-height:28px; height:28px;}
```

<!--break-->

### 父元素高度固定多行文字垂直居中（模拟表格）

```html
<div class="demo">
 <p>我们来看看这段文字是不是垂直居中我们来看看这段文字是不是垂直居中我们来看看这段文字是不是垂直居中我们来看看这段文字是不是垂直居中我们来看看这段文字是不是垂直居中。</p>
</div>
```
```css
.demo{ display:table-cell; width:400px; height:300px; vertical-align:middle;}
.demo p{width:100%; margin: auto; }
```
*注意：这种方法不适合IE6、7*

### 多行文字垂直居中（文字块垂直居中）

```html
<div class="demo">
 <p>我们来看看这段文字是不是垂直居中我们来看看这段文字是不是垂直居中我们来看看这段文字是不是垂直居中我们来看看这段文字是不是垂直居中我们来看看这段文字是不是垂直居中。</p>
</div>
```
```css
.demo{
	width: 200px;
	height:200px;
	position: absolute;
	left: 50%;
	top:50%;
	margin-left: -100px;
	margin-top: -100px;
}
```
*这种方法多用于在页面中间垂直水平居中*
