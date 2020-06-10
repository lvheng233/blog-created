---
title: "JS 拖曳事件总结"
categories:
  - 前端
tags:
  - JavaScript
date: 2020-06-01T19:17:59+08:00
draft: false
---

## 常用的三个事件

### mousedown

当指针(鼠标)在元素上按下时触发

### mousemove

当指针(鼠标)在元素上移动时触发

### mouseup

当指针(鼠标)在元素上抬起时触发

### 使用案例

```js
demo.onmousedown = function(){
    console.log('鼠标已按下')
}
demo.addEventListener('mousedown', function(e){
    console.log('鼠标已按下')
})
```

