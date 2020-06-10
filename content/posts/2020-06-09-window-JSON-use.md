---
title: "window.JSON的使用"
date: 2020-06-09T18:31:00+08:00
draft: false
---

## JSON.parse

作用：将符合JSON语法的字符串转换成JS对应的数据类型

JSON字符串 => JS 数据

注意事项：由于JSON只有6种类型，所以转成的数据也只有6种，如果不符合JSON的语法，则直接抛出一个Error对象，大部分时候我们用try catch捕获这个错误，如下：

```js
let object
try {
    object = JSON.parse(`{'name':'frank'}`)
}catch(error){
    console.log('出错了，错误详情是')
    console.log(error)
    object = {'name': 'no name'}
}
```

语法

```js
JSON.parse(value)
```

## JSON.stringify

作用：JSON.parse的逆运算

JS 数据 => JSON字符串

由于JS数据类型比JSON多，所以未必会转换成功，假如你在要转换的数据中加入了函数，那么很可能会报错，或者被浏览器忽略掉

语法

```js
JSON.stringify(value)
```