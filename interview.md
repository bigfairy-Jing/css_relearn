1. css 样式(选择器)优先级

- 计算权重确定
- !important
- 内联样式
- 后写的优先级高

2. 雪碧图的作用

- 减少 HTTP 请求数，提高页面加载性能
- 有一些情况下可以减少图片大小

3. 自定义字体的使用场景

- 宣传/品牌/banner 等固体文案
- 字体图标

4. base64 使用

- 减少 HTTP 请求
- 适用小图片
- 体积会增大三分之一大概

5.  伪元素和伪类的区别

- 伪元素 :after :before

- 伪类 :active :focus :hover :link :visited : first-child :lang

6. 如何美化 checkbox

- label[for]和 id
- 隐藏原生的 input
- :checked 　+ label

7. 如何产生不占空间的边框

- box-shadow
- outline (outline （轮廓）是绘制于元素周围的一条线，位于边框边缘的外围，可起到突出元素的作用。)

8. 如何实现 ios 图标的圆角

- clip-path (svg 图片)

9. 如何实现半圆，扇形等圆形

- border-radius 组合 （有无边框 边框粗细 圆角半径 ）

10. css 动画的实现方式有几种

- transition
- keyframes(animation) 关键帧动画 逐帧动画

11. 过渡动画和关键帧动画的区别

- 过渡动画需要有状态变化
- 关键帧动画不需要状态变化
- 关键帧动画可以控制的更加精细

12. css 动画的性能

- 性能不坏
- 部分情况下优于 JS
- 但 JS 可以做得更好
- 部分高危害属性 box-shadow
