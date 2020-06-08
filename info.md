css learn >>>>>

该仓库主要用于 css 记录,好用的 css 方式记录. 以及对之前所知道的 css 知识进行整理

###html 常见元素
####head
meta title style script base

####body
div/section/acticle/aside/header footer

p span em strong table thead tbody tr td ul ol li dl dt dd

a from input select textarea button

<!-- 指定一个基础路径 -->
<base href="/">
<a href="1"> 这里点击一个a标签  跳转的就是 /a

### html 重要属性

a -> href target

img -> src alt(Alternate) src 不显示的时候替换资源

table td[colspan,rowspan]

form[target method enctype]

input [type,value]

button[type]

select>option[value]

label[for]

##

section 区块

aside 不是很重要的区域

footer 底部

{
http://h5o.github.io/
H5o 可以查看大纲
}

html 版本
html4 html4.1
xhtml
html5

html5 新增 section article nav 导航 aside 不太重要

表单增强 日期 时间 搜索 表单验证 placeholder 自动聚焦

###语义
header/footer 头尾
section/arcticle 区域
nav 导航
aside 不重要的内容(侧边栏)
em(默认斜体)/strong(粗体) 强调
i(图标)/icon

###html 元素分类 ######按照默认样式分
block  
 iniline  
 inline-block

### html 嵌套关系

块级元素可以包含行内元素

块级元素不一定能包含块级元素

行内元素一般不能包含块级元素(a 元素可以包含 div)

### html 默认样式

默认样式意义

css reset

### 某些问题

doctype 意义 让浏览器标准模式渲染 让浏览器知道元素的合法性

html xhtml html5 html 属于 sgml xhtml 属于 xml ,是 html 进行 xml 严格化的结果 ,html5 不输入 sgml 也不属于 xml,比较宽松

html5 有哪些变化 新语义化元素 表单增强 新的 API(离线,音视频,图形,实时通信,本地存储,设备能力(定位,加速器,偏移....)) 分类和嵌套变更

em 和 i 区别 em 是语义化标签,表强调 i 纯样式,表斜体

语义化意义 开发者容易理解 (搜索 读屏软件(盲人使用的)) 有助于 SEO semantic microdata(语义化标记);

哪些元素可以自闭合

input img br hr meta link

html dom

property attribute \$0.value attribute 是死的 property 是活的

## 选择器

浏览器解析方式会从右往左解析的，所以最后一层最好是一个存在的 class

##选择器:

- 元素选择器 a{}

- 伪元素选择器 ::before

- 类元素选择器 .link {}

- 属性选择器 [type=radio]{}

- 伪类选择器 :hover

- ID 选择器

- 组合选择器 [type=checkbox] + label{}

- 否定选择器 :not(.link){}

- 通配选择器 \*

ID 选择器 100

类属性 伪类 10

元素 伪元素 +1

其他选择器 0

### 计算一个不进位的数字 所以十个类选择器没有一个 id 选择器优先级高

!important 优先级最高

元素属性 优先级高

相同权重 后写的生效

### 非布局样式

字体 字重 颜色 大小 行高

背景 边框

滚动 换行

粗体 斜体 下划线

其他

## 文字折行

- overflow-wrap(word-wrap) 通用换行控制  
  -是否保留单词 保留单词单词不换行 不保留 单词换行
- word-break 针对多字节文字
  —中文句子也是单词
- white-space 空白处是否断行

## 滚动

visible hidden scroll auto

## 背景

###背景

背景颜色

渐变色背景

多背景叠加

背景图片和雪碧图（雪碧图）

base64 和 性能优化

多分辨率适配

####设置背景的方式（hsl）

background-color: #fff;
background-color: rgba(0, 0, 0, 0.6);
background-color: hsl(0, 100%, 10%);
background:url('图片地址');
//渐变
background: linear-gradient(to right, red, green);
background: linear-gradient(0, red, green);
background: linear-gradient(45deg, red, green);

#### 多背景的叠加

#### 背景图片属性

background: red url('./bg.png');
background-repeat: no-repeat;
background-position: 20px 30px;
background-size: 100px 50px;

雪碧图背景 一张图片多张雪碧图

#####base64
//转换 base64 图片方式，找一个网站转换成 base64 格式

图片转 base64 图片体积会增大 1/3

把一张图片转换成 base64 图片，节省 http 请求数量，
同样有一个缺点就是体积会增大，图片本身体积会增大 1/3，css 文件会变得很大，所以一般这种场景我们只会适合比较小的图标
base64 传输性能，增大体积开销，增大解码开销
所以 base64 一般用在小图标或者 loading 小的

## 行高

###行高
行高构成：inline box 的高度会决定行高的高度

行高相关现象和方案

行高的调整

### line-height 会撑起外层 box 的高度，但是并不会改变自己撑起的高度

一行元素的高度，是由行高最高的那个决定

### 字体默认是沿着基线对齐的也就是 x 字母的底部对齐

- 设置 vertical-align:middle 沿着中间对齐

- 设置 vertical-align:top 沿着顶部对齐（顶线对齐）

- 设置 vertical-align: bottom 沿着底线对齐

- 设置 vertical-align: 某个 px 会根据 baseline 变化对应 px

### 图片下面有空隙，因为图片会按照 inline 去排版，然后就会沿着基线对齐，会留着空隙、 baseline 与底线会有偏差的

解决方式：vertical-align:bottom 或者 display:block

##边框

- 边框的属性：线型 大小 颜色

- 边框的背景图

- 边框的衔接（三角形）

##字体

- 字体族
  serif 衬线字体，字体周围有 wanwangougou （宋体）
  sans-serif 非衬线字体 （黑体）
  monospace 等宽字体（代码编程）
  cursive 轴写体 （）
  fantasy 花体

* 多字体 fallback

* 网络字体 自定义字体

* iconfont //实际上这里是用字体的 before 伪元素

自定义字体方式

```
@font-face {
font-family:'IF';
src:url('./IndieFlower.ttf'); //远程字体，可考虑字体
}
.class-name{
font-family:IF
}
```

## 装饰性属性以及其他

- 字重 font-weight (bold:700 normal:400 默认 100-900 (bolder 和 lighter 都是不确定，根据父级大小确定))
- 斜体 font-style：itaatic
- 下划线 text-decoration
- 指针 cursor

## CSS Hack （在一部分浏览器生效的 css 写法被称为 css hack）

hack 不合法但是生效的写法 主要用于区分不同的浏览器

- 替代方案： 特性检测

* 替代方案： 针对性加 class

标准属性写在前面 hack 写在后面

## float

- 脱离文档流，但是不脱离字体流
- 形成块（BFC），位置尽量靠左右

1. 对兄弟的影响

- 上面贴非 float 元素
- 旁边贴 float 元素
- 不影响其他块级元素的位置
- 影响其他块级元素内部文本

2. 对父级元素的影响

- 从布局上“消失”
- 高度塌陷

```
.container2::after{
  content:' ';
  clear:both;
  display:block;
  visibility:hidden;
  height:0;
}
```

## inline-block 布局

- 像文本一样排 block 元素
- 没有清除浮动等问题
- 需要处理间隙

## 响应式设计和布局

# 效果属性

- box-shadow
- text-shadow
- border-radius
- background
- clip-path

## box-shadow

> 语法 **box-shadow: h-shadow v-shadow blur spread color inset;**

1. h-shadow 必需。水平阴影的位置。允许负值。
2. v-shadow 必需。垂直阴影的位置。允许负值。
3. blur 可选。模糊距离。
4. spread 可选。阴影的尺寸
5. color 可选。阴影的颜色。请参阅 CSS 颜色值。
6. inset 可选。将外部阴影 (outset) 改为内部阴影。

- 营造层次感
- 充当没有宽度的边框
- 特殊效果

## text-shadow

> 语法 text-shadow: h-shadow v-shadow blur color;

1. h-shadow 必需。水平阴影的位置。允许负值。
2. v-shadow 必需。垂直阴影的位置。允许负值。
3. blur 可选。模糊的距离。
4. color 可选。阴影的颜色。参阅 CSS 颜色值。

## border-radius

> 每个都有两个参数 水平和垂直方向

1. border-top-left-radius
2. border-top-right-radius
3. border-bottom-left-radius
4. border-bottom-right-raidus

- 圆角矩形 圆形 半圆/扇形 一些奇奇怪怪的角角

## clip-path

- 对容器进行裁剪 之外的隐藏 之内的显示
- 常见的几何图形
- 自定义路径

<!-- 但是兼容性会有很多的问题，所以用不用要考虑一下 -->

## transform 3d

- translate
- scale
- skew
- rotate

```
//transform-style: preseve-3d 3d透视样式效果
//给元素加上 perspective:500px 值越大表示观看的地方离盒子的距离
```

## transform 跟动画是没有关系的,只是给元素进行位置变化不要搞混

- 近大远小

## z-index 其实是 z 轴的顺序,

## background

### cover 覆盖整个容器 contain 包含这个图片的

- 纹理 图案
- 渐变
- 雪碧图动画 背景图排到一起，然后设置 transition：background-position

## 动画

> 动画的原理：

1. 视觉暂留作用
2. 画面逐渐变化

#### 动画类型

1. transition 补间动画
2. keyframe 关键帧动画
3. 逐帧动画

###### 补间动画

- 位置-平移(left right margin transform)
- 方位-旋转(transform)
- 大小-缩放(transform)
- 透明度(opacity)
- 其他 - 线性变换(transform)

###### 关键帧动画

> @keyframes

##### 逐帧动画

> A-->B-->C

- 适用于无法补间计算的动画 资源较大 使用 steps()
- 使用面积不大,使用循环,时长不大

## CSS 预处理器

- 基于 CSS 的另一种语言
- 通过工具编译成 CSS
- 添加了很多 CSS 不具备的特性

* less 使用 node 写的 sass 用 ruby 写的

### less 函数

- lighten(颜色,百分比)
- 可以计算 12px + 12px

```
//mixmin
.block(@fontSize){
  font-size:@fontSize;
  border:1px solid @ccc;
  border-radius:4px;
}
//extend
.block{
  font-size:12px;
  border:1px solid @ccc;
  border-radius:4px;
}
.container:extend(.block){

}
.container{
  &:extend(.block )
}
//loop 递归循环
.gen-col(@n) when (@n > 0){
  .col-@{n}{
    width:1000px/12*@n
  }
  .gen-col(@n-1);
}
.gen-col(12)

//sass 循环
@for $i from 1 through 12{
  .col-#{$i}{
    width:1000px/12$i;
  }
}

```

## CSS 预处理器框架

- sass-compass
- less-lesshat/EST
- 提供现成的 mixin
- 类似 JS 类库 封装常用功能

## Bootstrap （css 框架） （3.0 使用 less 4.0 之后用了 sass）

## webpack 和 css

- css-loader 将 css 变成 js
- style-loader 将 js 样式插入 head
- ExtractTextPLUgin 将 CSS 从 JS 中提取
- css modules 解决 CSS 命名冲突问题

* less-loader sass-loader 各类预处理器
* postcss-loadder postCss 处理

## 如何解决 css 模块化的问题

- less sass 等 css 预处理器
- postcss 插件(post-import/precss 等)
- webpack 处理 css(css-loader + style-loader)

## postCss 作用

- autoprefixer cssnext precss 等兼容性处理
- import 模块合并
- css 语法检查 兼容性处理
- 压缩文件

## css modules

- 解决类名冲突问题

## 为什么使用 js 来引用,加载 css

- js 作为入口,管理资源有天然优势
- 将组件的结构样式行为封装到一起,增加内聚
- 可以做更多处理
