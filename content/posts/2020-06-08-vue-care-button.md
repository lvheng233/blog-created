---
title: "Vue造轮子笔记「一」"
date: 2020-06-08T18:12:45+08:00
draft: false
---

这是第一章，主要记录第一个轮子，Button 按钮的制作过程

## 选择一个开源许可证

首先将项目放到 GitHub 后需要选择一个开源许可证

第一步，在项目的Code下选择「Create new file」

第二步，在输入框中输入"LICENSE"，点击右侧的按钮提示「Choose a license template」

第三步，在新页面中选择「MIT License」

第四步，接下来一直点绿色的按钮即可~

> 注：最好选择MIT许可，MIT的开源性最高

初始化包管理

运行

```sh
npm init
```

它会问你如下问题：

```sh
# 你的包的名字叫什么：care
package name: (a-vue-care) care
# 当前版本：0.0.1
version: (1.0.0) 0.0.1
# 描述：这是一个基于Vue的UI框架
description: 这是一个基于Vue的UI框架
# 入口（可直接回车）
entry point: (index.js)
# 用什么测试，不使用，回车
test command:
# 仓库，括号中有默认值，直接回车
git repository: (https://github.com/ChenNing02/care.git)
# 关键字：vue,ui
keywords: vue,ui
# 作者：bravchen
author: bravchen
# 选择ISC：MIT
license: (ISC) MIT
# 检查你的配置
About to write to E:\Project\GitHub\a-vue-care\package.json:

{
  "name": "care",
  "version": "0.0.1",
  "description": "这是一个基于Vue的UI框架",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/ChenNing02/care.git"
  },
  "keywords": [
    "vue",
    "ui"
  ],
  "author": "bravchen",
  "license": "MIT",
  "bugs": {
    "url": "https://github.com/ChenNing02/care/issues"
  },
  "homepage": "https://github.com/ChenNing02/care#readme"
}

# 是这样吗？yes回车或直接回车
Is this OK? (yes)
```

安装Vue

```sh
npm i vue
```

创建一个index.html文件，在文件中引入vue

```html
<!DOCTYPE html>
<html lang="zh-Hans">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>care-UI</title>
</head>
<body>
    <script src="./node_modules/vue/dist/vue.min.js"></script>
</body>
</html>
```

> 注：html 标签要添加语言设置(`<html lang="zh-Hans">`)

安装开发者模式的 parcel（将普通安装中的 `-g` 改为 `-D`）

```sh
npm install -D parcel-bundler
```

> `-D` 表示给开发者使用的版本

将button组件分离后，运行 parcel

```sh
./node_modules/.bin/parcel index.html
# 或
npx parcel index.html
```

> `npx parcel` 表示在当前目录中寻找 parcel

运行后报错，需要给 Parcel 在 package.json 中添加以下配置，以运行完整版 vue

```json
{
  // ...
  "alias": {
    "vue" : "./node_modules/vue/dist/vue.common.js"
  }
}
```

> 在Vue的官方文档中有说明：[https://cn.vuejs.org/v2/guide/installation.html#运行时-编译器-vs-只包含运行时](https://cn.vuejs.org/v2/guide/installation.html#运行时-编译器-vs-只包含运行时)

再次运行时添加 `--no-cache` ，表示禁止使用之前的缓存

```sh
./node_modules/.bin/parcel index.html --no-cache
# 或
npx parcel index.html --no-cache
```

