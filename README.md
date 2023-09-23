# 网页制作

## 准备工作

### 项目目录

* images文件夹：存放固定图片素材
* uploads文件夹：存放非固定使用的图片素材
* css文件夹：存放CSS文件
  * base.css：基础公共样式
  * index.css：首页CSS样式
* index.html：首页HTML文件

#### 基础公共样式

* 清除默认样式，例如内外边距、项目符号
* 设置通用样式，例如文字样式

#### 默认样式代码

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

li {
    list-style: none;
}

body {
    font: 14px/1.5 "Microsoft Yahei","Hiragino Sans GB", "Heiti SC", "WenQuanYi Micro Hei",sans-serif;
    color: #333;
}

a {
    text-decoration: none;
    color: #333;
}

.wrapper {
    margin: 0 auto;
    width: 1200px;
}
```

## 网页制作思路

### 布局思路

先整体后局部，从外到内，从上到下，从左到右

### CSS实现思路

1. 画盒子，调整盒子范围->宽高背景色
2. 调整盒子位置->flex布局，内外边距
3. 控制图片、文字内容样式

## 制作网页

### header区域

通栏：宽度与浏览器窗口相同的盒子

标签结构：通栏>**版心**>logo+导航+搜索+用户

版心display:flex

#### logo

功能：

* 单击跳转首页
* 搜索引擎优化

实现方法：

* 标签结构：h1>a>网站名称(搜索关键字)
* CSS：
  ```css
  .logo a {
      display: block;
      width: 195px;
      height: 41px;
      background-image: url(../images/logo.png);
      font-size: 0;
  }
  ```

#### nav

功能：

* 单击跳转页面

实现方法：

* 标签结构：ul>li*3>a
* CSS思路
  * li 设置 margin-right
  * a 设置 左右padding

#### search

* 标签结构：.search>input+a/button
* div.search标签flex布局，侧轴居中，input标签flex：1

#### user

* 标签结构：.user>a>img+span
* 图片、文字垂直方向居中

### banner区域

结构：通栏banner>版心>.left+.right

#### left

* 标签结构：.left>ul>li*9>a
* 默认状态：背景图白色右箭头
* 悬停状态：背景图蓝色右箭头

#### right

* 标签结构：.right>h3+.content

### 精品推荐

* 标签结构：.recommend>h3+ul+a.modify
* flex布局

### 精品课程

* 标签结构:.hd+.bd
* 盒子模型

#### hd

* 标签结构：.hd>h3+a.more
* a.more设置箭头背景图

#### bd

* 课程卡片各个区域样式复用
* 标签结构：.bd>ul>li>a
* flex布局

### 学科课程

* 标签结构：.hd(复用)+.bd

#### 标题

* 标签结构:h3+ul+a.more

#### 内容

* 标签结构：.left+.right>.top+.bottom

### 版权区域footer

* 标签结构：通栏>版心>.left+.right>dl
