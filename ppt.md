title: grid基础
speaker: xuejr
plugins:
    - echarts

<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">

# grid基础 {.text-landing.text-shadow}

By xuejr {.text-intro}

[:fa-github: Github](https://github.com/xuejianrong/grid){.button.ghost}

<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
:::{.font-1}
1. 概念：网格容器、网格项、网格线、网格轨道、网格单元、网格区域、fr
2. 网格容器的属性
3. 函数：repeat、fit-content、minmax
4. 网格项的属性
:::

<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
### 网格容器、网格项
``` html
<div class="container"> // 网格容器
    <div class="item">one</div> // 网格项
    <div class="item">two</div>
    <div class="item">three</div>
    <div class="item">four</div>
</div>
```
``` css
.container {
    display: grid;
}
```
<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
### 网格线、网格轨道
<p>网格轨道：相邻两条网格线之间的轨道</p>
<img src="/grid_line.png" style="margin-top: 40px;">

<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
### 网格单元
<img src="/grid_cell.png" style="margin-top: 40px;">

<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
### 网格区域
<img src="/grid_area.png" style="margin-top: 40px;">

<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
### 单位fr
<p>剩余空间分配</p>

<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
## 网格容器中的属性
- `grid-template-columns: <track-size> | <[line-name]> <track-size> ...`
- `grid-template-rows: <track-size> | <[line-name]> <track-size> ...`
- `track-size`\: `<length> | <percentage> | <flex> | max-content | min-content | minmax(min, max)`
<p>定义网格线的名字和网格轨道的宽度</p>
  
[示例](/grid-template.html){.button.ghost}

<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
## 网格容器中的属性
- `grid-template-areas: <area-name> | none`
<p>通常使用`.`代表`none`，表示该网格单元是空的</p>
[示例](/grid-template2.html){.button.ghost}


<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
## 网格容器中的属性
### grid-template
<p>所简写属性：`grid-template-rows`、`grid-template-columns`与`grid-template-areas`</p>
[MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template){.button.ghost}

<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
## 网格容器中的属性
- `grid-gap: <row-gap> <column-gap>?`
<p>网格间隙，所简写属性：`grid-column-gap`和`grid-row-gap`。不能单独设置其中一个间隙</p>
- `grid-column-gap`
- grid-row-gap

<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
## 网格容器中的属性
### items
<p>定义 **网格项** 相对于网格单元的布局方式</p>
- `justify-items: stretch | center | start | end;`
- `align-items: stretch | center | start | end;`
- `place-items: <'align-items'> <'justify-items'>?`

[示例](/place-items.html){.button.ghost}

<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
## 网格容器中的属性
### content
<p>定义 **网格单元** 在网格容器中的布局</p>
- `justify-content: stretch | start | center | end | space-between | space-around | space-evenly;`
- `align-content: stretch | start | center | end | space-between | space-around | space-evenly;`
- `place-content: <'align-content'> <'justify-content'>?`

[示例](/place-content.html){.button.ghost}

<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
## 网格容器中的属性
### grid-auto
- 指定隐式网格轨道的大小
  - `grid-auto-columns`
  - `grid-auto-rows`
- `grid-auto-flow`网格排列方式
  
[MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-auto-flow){.button.ghost}

<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
## css函数
### 1.`repeat(repeat, value)`
<p>使用在`grid-template-rows`或者`grid-template-columns`中</p>
#### `repeat`重复次数
- \<number\> 整数
- \<auto-fill\> 以网格项为准自动填充
- \<auto-fit\> 以网格容器为准自动填充
#### `value`取值，除了正常尺寸之外，还有
- `max-content`表示网格轨道长度自适应最大的那个单元格
- `min-content`

[示例](/repeat.html){.button.ghost}

<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
## css函数
### 2.`fit-content`内容适配
<p>使用在`grid-template-rows`或者`grid-template-columns`中</p>

[示例](/fit-content.html){.button.ghost}

<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
## css函数
### 3.`minmax(最小值, 最大值)`
#### `value`取值，除了正常尺寸之外，还有
`max-content`和
`min-content`
<p></p>

[普通示例](css-function.html){.button.ghost}

[结合repeat的auto-fill和auto-fit的示例](https://codepen.io/xboxyan/pen/zYYgYdL?editors=1100){.button.ghost}

<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
## 网格项上的属性
### `start-end`
- `grid-column-start: <number> | <name> | span | <number> | span <name> | auto`
- `grid-column-end: <number> | <name> | span | <number> | span <name> | auto`
- `grid-row-start: <number> | <name> | span | <number> | span <name> | auto`
- `grid-row-end: <number> | <name> | span | <number> | span <name> | auto`
- `grid-column: <start-line> / <end-line> | <start-line> / span <value>`
- `grid-row: <start-line> / <end-line> | <start-line> / span <value>`
### 注意点
- 没有声明`grid-column-end`和`grid-row-end`，网格跨越一个轨道
- 网格项可以重叠，使用z-index来控制堆叠顺序
- 如果设置了`place-items`，`start-end`会不生效，[例子](/place-items.html)

[示例](/start-end.html){.button.ghost}

<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
## 网格项上的属性
- `grid-area: <name> | <row-start> / <column-start> / <row-end> / <column-end>`
- name\:结合`grid-template-areas`使用
- 另一种是`start-end`的缩写

[name示例](/grid-area.html){.button.ghost}

<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
## 网格项上的属性
### self
- `justify-self: <start> | <end> | <center> | <stretch>`
- `align-self: <start> | <end> | <center> | <stretch>`


<slide class="bg-black-blue aligncenter" image="https://source.unsplash.com/C1HhAQrbykQ/ .dark">
## flex属性
- `flex: 1 0 100px;`是什么意思？这样子写有什么意义？
<p></p>

[flex示例](/flex-attrbute.html){.button.ghost}

<style>
p {
    margin: 20px 0;
}
.wrap {
    width: 900px;
}
.font-1 li {
    font-size: 30px;
    line-height: 2em;
    text-align: left;
}
code[class*=language-], pre[class*=language-] {
    color: #fff;
    text-shadow: none;
}
</style>