---
layout: post
title: JavaScript常用DOM总结
tags: [JS]
---
学**JavaScript**有一段时间了，今天就来总结一下其中常用的**DOM**

    node.nodeName

返回该节点的名字，若是元素节点则返回元素名字，若是属性节点则返回属性名字，若是文本节点则返回 *#text* 字符串

    node.nodeType

返回节点属性，1为元素节点，2为属性节点，3为文本节点，8为注释节点

    node.nodeValue

返回节点的值，若是元素节点则返回 *null*，若是属性节点则返回属性值，若是文本节点则返回文本内容，也可设置节点值：nodeValue = *value*

    node.childNodes

返回一个包含给定元素节点的全部子元素的数组，包括元素节点、属性节点、文本节点

    node.firstChild

返回某一节点的第一个子节点

    node.lastChild

返回某一节点的最后一个子节点

    node.parentNode

返回某一节点的父节点，永远是元素节点（除 *document* 节点返回 *null* 外）

    node.nextSibling

返回某一节点的下一兄弟节点

    node.previousSibling

返回某一节点的前一兄弟节点

    element.hasChildNodes

返回 *true* 则表示该元素有子节点，反之则返回 *false*

    element.innerHTML

获得元素的内容，或设置元素内容：innerHTML = *value*

    object.getElementById(id)

返回一个有着该 *id* 的元素节点

    object.getElementsByTagName(tagName)

返回一个有着该 *tagName* 的元素节点数组

    object.getAttribute(att)

只能被一元素节点对象调用，返回该属性值

    object.setAttribute(att,value)

只能被一元素节点对象调用，设置该属性值，或添加新属性值

    document.createElement(element)

创建元素节点，返回一个指向新增节点的指针

    document.createTextNode(text)

创建文本节点，返回一个指向新增节点的指针

    parent.appendChild(child)

将子节点添加到父节点上，可用来挪动节点，返回一个指向子节点的指针

    parentElement.insertBefore(newElement,targetElement)

将 *newElement* 插入到 *parentElement* 中的 *targetElement* 之前，可用来挪动节点，返回一个指向子节点的指针

    node.cloneNode(boolean)

复制一个节点，如果参数为 *true* ，则也复制其子节点，反之则不复制子节点，返回一个指向新节点的指针

    element.remove(node)

从元素中删除某节点，包括其子节点，返回一个指向删除节点的指针

    parentElement.replaceChild(newChild,oldChild)

替换父元素中的节点，也可挪动节点，返回一个指向旧节点的指针

    element.style.property

获得或修改 *property* 的值(只能获取内嵌样式，且 *property* 需用 **Camel** 记法)

    element.className

获得或修改某一元素的 *class* 值

    setTimeOut("function",interval)

设定时间间隔 *interval* (毫秒)后执行 *function* (带括号)， *variable* = setTimeOut(...)

    clearTimeOut(variable)

取消对 *setTimeOut()* 的设定
    
    setInterval("function",interval)

设定时间间隔 *interval* 后反复执行 *function*

    clearInterval(variable)

取消对 *setInterval()* 的设定

    parseInt(string)

提取 *string* 中最前面的整数

    parseFloat(string)

提取 *string* 中最前面的浮点数

######检查浏览器是否支持该方法
{% highlight javascript %}
    if(!document.getElementById){
	return false;
    }
{% endhighlight %}

