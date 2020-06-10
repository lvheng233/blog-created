---
title: "常用的HTML5标签"
date: 2020-05-27T08:33:39+08:00
slug: dd3e7bbd
draft: false
---


## `<canvas>` 画布绘制长方形

Html

```html
<canvas id="canvas"></canvas>
```

JavaScript

`Document.getElementById()` 方法获取HTML `<canvas>` 元素的引用。接着，`HTMLCanvasElement.getContext()` 方法获取这个元素的context——图像稍后将在此被渲染。

由 `CanvasRenderingContext2D` 接口完成实际的绘制。`fillStyle` 属性让长方形变成绿色。`fillRect()` 方法将它的左上角放在(10, 10)，把它的大小设置成宽150高100。

```js
const canvas = document.getElementById('canvas');
// 获取 canvas 的 2d 上下文
const ctx = canvas.getContext('2d');

ctx.fillStyle = 'green';
ctx.fillRect(10, 10, 150, 100);
```

## `<video>` 的常用属性

src：视频的地址

autoplay：设置自动播放（默认值为false）

poster：视频的封面

```html
<!-- Simple video example -->
<video src="videofile.ogg" autoplay poster="posterimage.jpg">
    抱歉，您的浏览器不支持内嵌视频，不过不用担心，你可以 <a href="videofile.ogg">下载</a>
    并用你喜欢的播放器观看!
</video>

<!-- Video with subtitles -->
<video src="foo.ogg">
    <!-- 设置视频字幕 -->
    <track kind="subtitles" src="foo.en.vtt" srclang="en" label="English">
    <track kind="subtitles" src="foo.sv.vtt" srclang="sv" label="Svenska">
</video>
```

## `<audio>` 的常用属性

src：可选属性，设置播放地址。你可以在audio元素中使用 `<source>` 元素来替代该属性指定嵌入的音频。

controls：显示控制面板。如果设置了该属性，浏览器将提供一个包含声音，播放进度，播放暂停的控制面板，让用户可以控制音频的播放。

volume：播放的音量。值从0.0 (无声) 到 1.0 (最大声).

loop：循环播放

autoplay：设置自动播放（默认值为false）

muted：是否静音（默认值为false）

HTML `<audio>` 元素用于在文档中表示音频内容。 `<audio>` 元素可以包含多个音频资源， 这些音频资源可以使用 src 属性或者`<source>` 元素来进行描述； 浏览器将会选择最合适的一个来使用。

## `<section>` 的使用

表示一个包含在 HTML 文档中的独立部分，它没有更具体的语义元素来表示，一般来说会有包含一个标题。有点类似于 div。