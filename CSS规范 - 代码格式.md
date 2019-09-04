## CSS规范 - 代码格式(测试）1

#### 根据属性的重要性按顺序书写
 
单个样式规则下的属性在书写时，应按功能进行分组，并以 Positioning Model > Box Model > Typographic > Visual 的顺序书写，提高代码的可读性。
- 如果包含 content 属性，应放在最前面；

- Positioning Model 布局方式、位置，相关属性包括：position / top / right / bottom / left / z-index / display / float / …

- Box Model 盒模型，相关属性包括：width / height / padding / margin / border / overflow / …

- Typographic 文本排版，相关属性包括：font / line-height / text-align / word-wrap / …

- Visual 视觉外观，相关属性包括：color / background / list-style / transform / animation / transition / …

Positioning 处在第一位，因为他可以使一个元素脱离正常文本流，并且覆盖盒模型相关的样式。盒模型紧跟其后，因为他决定了一个组件的大小和位置。其他属性只在组件内部起作用或者不会对前面两种情况的结果产生影响，所以他们排在后面。

#### 注释格式：/* 注释文字 */

对选择器的注释统一写在被注释对象的上一行，对属性及值的注释写于分号后。

注释内容两端需空格，已确保即使在编码错误的情况下也可以正确解析样式。

在必要的情况下，可以使用块状注释，块状注释保持统一的缩进对齐。

原则上每个系列的样式都需要有一个注释，言简意赅的表明名称、用途、注意事项等。
```
/* 块状注释文字
 * 块状注释文字
 * 块状注释文字
 */
.m-list{width:500px;}
.m-list li{height:20px;line-height:20px;/* 这里是对line-height的一个注释 */overflow:hidden;}
.m-list li a{color:#333;}
/* 单行注释文字 */
.m-list li em{color:#666;}
```

#### 选择器顺序
请综合考虑以下顺序依据：

- 从大到小（以选择器的范围为准）
- 从低到高（以等级上的高低为准）
- 从先到后（以结构上的先后为准）
- 从父到子（以结构上的嵌套为准）

以下仅为简单示范：
```
/* 从大到小 */
.m-list p{margin:0;padding:0;}
.m-list p.part{margin:1px;padding:1px;}
/* 从低到高 */
.m-logo a{color:#f00;}
.m-logo a:hover{color:#fff;}
/* 从先到后 */
.g-hd{height:60px;}
.g-bd{height:60px;}
.g-ft{height:60px;}
/* 从父到子 */
.m-list{width:300px;}
.m-list .itm{float:left;}
```

#### 清晰的CSS模块
用“注释”来说明每一个模块对于较大的CSS文件来说显得尤为重要。