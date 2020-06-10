---
title: 'table 表格'
date: 2020-06-06T15:16:34+08:00
draft: true
---

## 使用

```html
<table>
    <caption>
        Council budget (in £) 2018
    </caption>
    <thead>
        <tr>
            <th>Items</th>
            <th scope="col">Expenditure</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th scope="row">Donuts</th>
            <td>3,000</td>
        </tr>
        <tr>
            <th scope="row">Stationery</th>
            <td>18,000</td>
        </tr>
    </tbody>
</table>
```

## 标签

### 标题

`<caption>`，表格的标题，它常常作为 `<table>` 的第一个子元素出现。

### colgroup

`<colgroup>`标签用来定义表中的一组列表。

**可用属性**

span 正整数，指示该<colgroup>元素跨越的连续列数。如果不存在，则默认值为1。

**案例**

设置单列颜色

```html
<table>
    <colgroup>
        <col />
        <col style="background-color: orange" />
    </colgroup>
    <tr>
        <th>Data 1</th>
        <th>Data 2</th>
    </tr>
    <tr>
        <td>Calcutta</td>
        <td>Orange</td>
    </tr>
    <tr>
        <td>Robots</td>
        <td>Jazz</td>
    </tr>
</table>
```

设置所有表格颜色

```html
<colgroup>
    <col style="background-color: orange" span="2">
</colgroup>
```

## 属性

### 内边框合并

```css
table {
    border-collapse: collapse;
}
```

### 列合并：

```js
<th colspan="2">The table header</th>
// colspan 的最大值为 1000
```

### 行合并：

```js
<th rowspan="2">The table header</th>
// rowspan 的最大值为 65534
```

scope 属性在 `HTML5` 标准中已废弃，尽量不使用
