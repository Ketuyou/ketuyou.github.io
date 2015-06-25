---
layout: post
title: 事件冒泡与事件捕获
category : js
---
### 事件冒泡
微软提出了名为事件冒泡(event bubbling)的事件流。事件冒泡可以形象地比喻为把一颗石头投入水中，泡泡会一直从水底冒出水面。也就是说，事件会从最内层的元素开始发生，一直向上传播，直到document对象。

<!-- break -->

### 事件捕获
网景提出另一种事件流名为事件捕获(event capturing)。与事件冒泡相反，事件会从最外层开始发生，直到最具体的元素。
### addEventListener的第三个参数
“DOM2级事件”中规定的事件流同时支持了事件捕获阶段和事件冒泡阶段，而作为开发者，我们可以选择事件处理函数在哪一个阶段被调用。

addEventListener方法用来为一个特定的元素绑定一个事件处理函数，是JavaScript中的常用方法。addEventListener有三个参数：

element.addEventListener(event, function, useCapture)
第一个参数是需要绑定的事件，第二个参数是触发事件后要执行的函数。而第三个参数默认值是false，表示在事件冒泡的阶段调用事件处理函数，如果参数为true，则表示在事件捕获阶段调用处理函数。现代浏览器里参照w3c规范，采用了这两种方式并行的方式，简单的来说就是先捕获，再冒泡。
[举例](http://www.w3schools.com/jsref/tryit.asp?filename=tryjsref_element_addeventlistener_capture)
### 事件代理
对于事件代理来说，在事件捕获或者事件冒泡阶段处理并没有明显的优劣之分，但是由于事件冒泡的事件流模型被所有主流的浏览器兼容，从兼容性角度来说最好还是使用事件冒泡模型。

