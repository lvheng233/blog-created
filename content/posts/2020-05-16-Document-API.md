---
title: Document API
categories:
  - 前端
tags:
  - JavaScript
slug: a0000001
date: 2020-05-16 22:22:05
---

## Class 类名添加与删除

当点击 id 为 xxx 的元素时，如果 id 为 yyy 元素存在 active 的 class 样式就删除该 class 名，不存在就添加该 class 名

```js
xxx.onclick = function(){
    yyy.classList.toggle('active')
}
```

案例链接：https://jsbin.com/xoxelaj/1/edit?html,css,js,output

## String

### 获取某一个索引对应的字符 (`String.prototype.charAt()`)

```js
var str = 'wobuzaiyi'
// 获取某一个索引对应的字符
str.charAt(0) // "w"
// 获取某一个索引对应的字符的编码 -- String.prototype.charCodeAt()
str.charCodeAt(0) // 119 -- "w"对应的字符编码
```

### 去掉字符串两边的空格 (`String.prototype.trim()`)

```js
'   username   '.trim() // "username"
```

### 字符串拼接 (`Array.prototype.concat()`)

```js
var s1 = 'Hello'
var s2 = 'World'
s1.concat(s2) // "HelloWorld"
```

### 截取字符串 (`Array.prototype.slice()`)

从索引为 0 开始截取至索引为 2 不包括索引为 2

```js
'Hello'.slice(0, 2) // He
```

### 字符串生成 a 标签

```js
var str = 'wobuzaiyi'
str.anchor() // "<a name="undefined">wobuzaiyi</a>"
```

## Number

```js
// 获取 100 的 16 进制
(100).toString(16) // "64"
```

## Boolean

在 boolean 中 new Boolean() 与普通的布尔值可能会有所不同，如下：

```js
var b1 = false
var b2 = new Boolean(false)
if(b1){ console.log('我是b1') } 
if(b2){ console.log('我是b2') } // 由于b2是一个对象，所以它还是会执行
// 我是b2
```