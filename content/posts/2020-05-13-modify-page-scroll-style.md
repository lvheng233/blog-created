---
title: 修改页面滚动条样式
categories:
  - 前端
tags:
  - CSS
abbrlink: 912887466
date: 2020-05-13 14:26:41
---

虽然之前修改过滚动条，但一直没做笔记，每次都是用过就忘了，于是决定记录一下~

## 关于滚动条的三个伪类选择器

```css
element::-webkit-scrollbar // 滚动条整体样式
element::-webkit-scrollbar-track // 滚动条内部滑轨
element::-webkit-scrollbar-thumb // 滚动条内部滑块
```

## 自定义所有元素滚动条样式

```css
*::-webkit-scrollbar {
    /* 滚动条整体样式 */
    width: 8px; /* 定义纵向滚动条宽度 */
    height: 8px; /* 定义横向滚动条高度 */
}

*::-webkit-scrollbar-thumb {
    /* 滚动条内部滑块 */
    border-radius: 8px;
    background-color: hsla(220, 4%, 58%, 0.3);
    transition: background-color 0.3s;
}

*::-webkit-scrollbar-thumb:hover {
    /* 鼠标悬停滚动条内部滑块 */
    background: #bbb;
}

*::-webkit-scrollbar-track {
    /* 滚动条内部轨道 */
    background: #ededed;
}
```

> 本文内容摘自：https://juejin.im/post/5d24984d518825453a25a8b4