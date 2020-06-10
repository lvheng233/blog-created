---
title: "LocalStorage 的使用"
categories:
  - 前端
tags:
  - HTTP
  - LocalStorage
date: 2020-05-22T19:43:52+08:00
draft: false
---

## 判断key(值名称)是否存在

```js
let _key = localStorage.hasOwnProperty('key')
```


## 获取

```js
// 从 localStorage 中获取名为 "key" 的值
let JsonData = localStorage.getItem("key")
// 将获取到的值由字符串转换为 JSON 格式
let data  = JSON.parse(JsonData)
```

## 存储

```js
let data = { type: 1 }
// 将 data 转换为字符串格式
let stringData = JSON.stringify(data)
// 存储到 localStorage 中并命名为 "key"
localStorage.setItem("key", stringData)
```

