---
title: "CSS语法"
date: 2020-05-20T16:46:52+08:00
slug: 7aad209b
draft: false
---

## 编码格式

`@charset` 必须写在最顶部

```css
@charset "UTF-8";
```

## 引入其他文件

`@import` 是引入其他 CSS文件

```css
@import url(style.css);
```

## 媒体查询

```css
@media (min-width: 100px) and (max-width: 200px){
    body {
        属性: 值;
    }
}
```

## PDF样式

在 `@media print` 中的值只会在PDF格式下生效

```css
@media print {
  body {
     background: red;
  }
}
```

> 注意 ：`@charset` 和 `@import` 结尾必须加分号

**查找 CSS 样式**

搜索 CSS tricks 加关键词

**CSS 案例**

CSS 案例参考：https://cn.365psd.com/

## 变量

以设置字体变量为例：

```css
/* 声明变量 */
:root {
    --font-size: 14px;
}
/* 使用变量 */
p {
    font-size: var(--font-size);
}
```

> :root 表示作用域，可以改为 html，或上面案例中的 p 标签