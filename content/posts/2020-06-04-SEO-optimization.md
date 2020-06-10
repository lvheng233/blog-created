---
title: "SEO优化"
date: 2020-06-04T17:42:29+08:00
draft: false
---

## 什么是SEO

SEO 就是搜索引擎优化

搜索引擎会根据页面默认显示的内容来获取页面的关键字（页面默认不会显示包括JS创建的内容），比如：

h1 是页面主要内容的标题

description 是页面的描述

keyword 是页面的关键字

以淘宝网为例：

```html
<head>
    <!-- 页面名称 -->
    <title>淘宝网 - 淘！我喜欢</title>
    <!-- 描述 -->
    <meta name="description" content="淘宝网 - 亚洲较大的...">
    <!-- 关键词 -->
    <meta name="keyword" content="淘宝,掏宝,网上购物...">
</head>
<body>
    <h1>
        <a href="//www.taobao.com" role="img" class="logo-bd clearfix">淘宝网</a>
    </h1>
</body>
```

## 拓展：什么是ssr

ssr 就是不要用客户端的 JS 渲染内容，而是用服务端的 JS 渲染内容。
