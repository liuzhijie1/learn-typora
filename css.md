# CSS

###### 响应式和自适应的区别

响应式布局和自适应布局是现代网页设计中常用的倆种技术，他们都是为了用户在不同设备上的浏览体验，以下是这2者的区别
**响应式布局**：通过使用流式布局和媒体查询，使网页能够根据不同的屏幕尺寸自动调整布局和内容，响应式布局设计允许页面元素在任何设置上灵活变化，以适应不同的视口大小
**自适应布局**：为不同类别的设备创建多个静态布局，当检测到设备的分辨率时，网站会加载相应的布局，而不是动态调整。自适应设计通常需要为每种设备设计特定的页面
**总体而言**：响应式布局更为灵活，可以适应各种屏幕尺寸，而自适应布局在某些情况下可以提供更可控的设计选择，选择那种布局方式取决于项目需求、预算和目标用户群体

###### 移动端怎么适配 =》 响应式布局和自适应  =》 实现响应式的方式有哪些

1. 使用媒体查询

``` css
body {
  font-size: 20px;
}
@media screen and (max-width: 600px) {
  body {
    font-size: 14px;
  }
}
@media screen and (min-width: 1200px) {
  body {
    font-size: 18px
  }
}
```

2. 使用百分比单位
3. 使用视窗单位
4. 使用 REM 单位
5. 使用 Flexbox 或 Grid布局

###### rem单位是怎么计算的？

rem 单位是CSS中的一种相对单位，他相当于文档的根元素\<html\> 的字体大小来计算长度，rem单位的主要有点在于它提供了一种全局的相对尺寸，使得整个页面的布局可以统一缩放

###### CSS inherited proprtyies cheatsheet

```css
border-collapse
border-spacing
caption-side
color
cursor
direction
empty-cells
font-family
font-size
font-style
font-variant
font-weight
font-size-adjust
font-stretch
font
letter-spacing
line-height
list-style-image
list-style-position
list-style-type
list-style
orphans
quotes
tab-size
text-align
text-align-last
text-decoration-color
text-indent
text-justify
text-shadow
text-transform
visibility
white-space
widows
word-break
word-spacing
word-wrap
```

###### window.devicePixelRatio 的含义

它代表了物理像素和CSS像素之间的比值，在不同的显示设备，所对应的值也是不一样的。

