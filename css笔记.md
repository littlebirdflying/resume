css的3中引入方式
内联 style属性
sytle标签
外部文件 css link
@import url(./b.css);
第四种引入方式
除了divhespan，其他元素都有样式

**给所有子元素添加float left
子元素浮动，父元素添加clearfix**
子类选择器 父>子

开发者工具
 style所有样式
 computed计算出来的样式，平时看这个

 没设置a display:block前 li 和a 不一样高

 color可以继承

 同级元素样式相同 可以写在父元素上，前提是可继承
 span和span之间有空格，是因为代码里有回车


 一个块级元素的高度是由什么决定的？
 由内容决定的，**div高度由其内部文档流元素的高度总和决定（特别重要）**
 文档流：
 内联元素从左往右。
 文档内元素的流动方向，内联元素从左往右流动，如果流动遇到阻碍，就换行继续流动。
 块级元素从上往下。
 如果是块级元素，从上往下，每一个块级元素占一行，如果还有就另起一行。
 如果span有border，并在流的过程中被截断了，border不会出现两个。
 如果span里是英文，遇到阻碍，则不会换行。通过属性word-break:break-all;中文为主就用break-all值，要是英文多就用break-word值。
 一个内联元素的高度是有什么决定的？
 基本上不可测，当font-size比较小时，可以通过line-height控制内敛元素的高度。

 建议行高，默认行高是1.4倍的字体大小，建议行高根据字体不同也会不同，
 字体是基线对齐。
 不同高度的内联元素在一起，行高有最高的决定。

更多，搜索 方应杭 css line height

设置height会有无穷无尽的bug

设置postion:fixed之后，脱离文档流，原先父元素高度会减小，内容收缩，通过添加width:100%解决

实际工作中尽量不使用height和width的px值，当内容变化了，高度就变了，可能会有很多bug。
写width:100%，如果元素有margin和padding，导致和超过屏幕宽，而出bug

max-width当窗口小于设定值时，可以自适应

设置垂直居中时，不用固定width,设置padding和line-height，能避免很多bug

如何用css画一个三角形,更多资源，搜 css tricks shape
span里不能放div，放了会有bug
span加个display:block，就是div了

第二个脱离文档流的情况，position:absolute;

float元素默认会收缩
chrome调整大小时，按shift可以快点儿
span display:inline-block，设置margin不合并

什么是空标签 meta input
伪类，所有非空标签都有伪类
伪元素选不中
absolute自动变block了
::before必须有content才能显示，before和after是装逼用的
relative不好的地方

利用margin的负值，调位置
a的donwload强制下载
内联元素的左右padding是有用的，上下padding没用
内联元素或inline-block元素居中，给父元素加tac

box-shadow生成器
动画查文档
小技巧：如果爸爸高度设置好，子元素可以height:100%;
box-sizing: border-box;width算border和padding
利用float和伪类nth:child(even)，实现li的布局
使用inline-block的两个bug
一旦使用它，必须加vertical-align: top;不然下面有空隙
-中划线只用来做结构
