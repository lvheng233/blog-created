---
title: "简单类型和对象的区别"
categories:
  - 前端
tags:
  - JavaScript
date: 2020-05-26T14:47:31+08:00
draft: false
---

普通的变量 1 和 `new Number(1)` 的区别

```js
var n1 = 1
console.log(n1) // 1
var n2 = new Number(1)
console.log(n2) // Number {1} 原型：__proto__: Number
```

上面两个变量都可以使用 `.toString()` 方法转换为字符串

```js
n1.toString() // "1"
n2.toString() // "1"
```

但是显然 `var n1 = 1` 的方式更简洁。

> 那么为什么会有两种方式声明呢，主要是JavaScript的发明人的老板要求 JS的语法要长得像 Java。所以这个语法的实际用处并不大

它们的区别：

简单类型 `var n1 = 1` 并不存在 `.toString()` 方法，但是当你调用该方法时，会临时生成一个对象 使得它有 `new Number(1)` 的功能。在你使用后该对象就会被立即销毁。

声明一个普通变量，给它添加一个属性，但你会发现它并没有该属性，如下：

```js
var n = 1
n.xxx = 2
console.log(n.xxx) // undefined
```

其他的如 String 也是同理

```js
var str1 = 'wobuzaiyi'
var str2 = new String('wobuzaiyi')
console.log(str1) // "wobuzaiyi"  普通字符串
console.log(str2) // String {"wobuzaiyi"} 原型：__proto__: String
```