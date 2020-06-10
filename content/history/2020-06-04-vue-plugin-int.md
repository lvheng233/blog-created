---
title: "Vue插件安装"
date: 2020-06-04T13:36:42+08:00
draft: false
---

## 创建项目

```sh
# 指定目录下创建
vue create demo
# 当前目录下创建
vue create .
```

分析
```sh
? Please pick a preset: Manually select features
? Check the features needed for your project:
 (*) Babel
 ( ) TypeScript
 ( ) Progressive Web App (PWA) Support
 (*) Router
 (*) Vuex
 (*) CSS Pre-processors
 (*) Linter / Formatter
>( ) Unit Testing
 ( ) E2E Testing

? Use history mode for router? (Requires proper server setup for index fallback in production) (Y/n)

? Pick a linter / formatter config: (Use arrow keys)
> ESLint with error prevention only
  ESLint + Airbnb config
  ESLint + Standard config
  ESLint + Prettier

? Pick additional lint features: (Press <space> to select, <a> to toggle all, <i> to invert selection)
>(*) Lint on save
 ( ) Lint and fix on commit
```





## Sass 安装

安装sass的依赖包

```sh
npm install --save-dev sass-loader
# sass-loader 依赖于 node-sass
npm install --save-dev node-sass
```

vue 中使用

```js
new webpack.ProvidePlugin({
  Vue: ['vue/dist/vue.esm.js', 'default']
});
```