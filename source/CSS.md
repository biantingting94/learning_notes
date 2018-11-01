##选择器
###基础选择器
1. 通用选择器
2. 元素选择器
3. 类选择器：类名不能包含特殊符号，除了_,- 
   1. 多类选择器：一个元素同时引用多个类选择器
   2. **分类选择器：**将元素和类选择器联合使用 
      元素.类名{样式声明}——表示引用该类的元素
4. id选择器
5. **群组选择器：选定多个元素**
   选择器1,选择器2,选择器3,...{样式声明}
6. **后代选择器：**通过后代关系选择指定的元素-多级嵌套
   选择器1 选择器2 选择器3{样式声明}
7. 子代选择器：仅一级嵌套
   选择器1>选择器2{样式声明}
8. 伪类：匹配元素不同状态
   1. 链接
      1. link 未访问
      2. visited 已访问
   2. 动态
      1. hover 悬停
      2. active 激活/点击时（超链接、文本框、密码框）
      3. focus 获取焦点（文本框和密码框）

###选择器优先级
元素：1
类：10
伪类：10
ID：100
内联：1000
**权值相加**
**！important**：添加到属性值后面，与属性值空格隔开，优先使用当前样式，可以覆盖行内样式

##尺寸与边框
### 尺寸
####尺寸单位
1. px
2. em：相对于父元素乘以倍数
3. rem：跟相对
####尺寸属性
1. 宽度
   1. width
   2. min-width：最小宽度
   3. max-width：最大宽度
2. 高度
   1. height
   2. min-height：最小高度
   3. max-height：最大高度
3. 设置元素尺寸
   行内块：大部分的表单控件（单选框和复选框不支持设置宽高）
4. 内容溢出：纵向溢出 overflow，overflow-x，overflow-y
    visible、auto、hidden、scroll	
####颜色

1.  英文单词
2.  rgb(r,g,b)
3. rgba(r,g,b,alpha)alpha表示透明度，0-1之间的小数，值越大，不透明度越高
4. \#rrggbb,缩写#rgb

###边框
1. border：宽度 样式 颜色
   颜色可以设置透明度rgb(0,0,0,0)，最后一个0表示完全透明
   取消边框：border:0或者border:none;

2. 指定方向：border-left

3. 单属性：border-width:100px;border-style:dashed;

4. 特定边的样式：border-bottom-color:red;

5. **圆角：border-radius:10px;或者border-radius:10%;**

   单脚设置：

   	border-top-left-radius:			border-top-right-radius:
   	border-bottom-left-radius: 		border-bottom-right-radius:

6. **边框阴影：box-shadow：水平偏移 垂直偏移 [模糊距离 阴影大小 阴影颜色 内阴影]**

   h-shadow：阴影在水平方向的偏移，必须。取值为正，向右偏移；取值为负，向左偏移

   v-shadow：阴影在垂直方向的偏移，必须。取值为正，向下偏移；取值为负，阴影向上偏移

   blur：可选，阴影的模糊距离，取值越大，模糊效果越明显，px

   spread：可选，阴影大小，指定在基础阴影上扩充出来的大小，px

   color：可选，阴影颜色

   inset：可选，将默认的外阴影改为内阴影

   **box-shadow: 0 0 30px 10px red inset;**内阴影；无偏移

7. **轮廓：边框的边框，在边框外围的线**

   outline：宽度 样式 颜色

   取消轮廓：outline:0/none；

##边距

### 外边距-margin

1. 取值

   1. % 百分比，以父级的宽高为基数
   2. auto，控制块级元素水平居中，0 auto

2. 自带外间距的元素

   body、h、p、ul、ol、dl、dd、pre——重置边距：margin：0

3. **特殊效果**

   1. 两个元素的上下外边距会合并，取值大的那个
   2. 外边距溢出——某些情况下，给子元素设置的外边距会作用到父元素上
      1. 父元素没有上边框
      2. 为子元素设置上外边距时
   3. 解决溢出：
      1. 增加上边框—对父元素的高度有影响
      2. 使用父元素的上内边距取代子元素的上外边距—对父元素的高度有影响
      3. 在父元素的第一个子元素位置处增加空元素table
   4. 行内/行内块元素的垂直外边距：
      1. 行内元素：垂直外边距无效，img除外
      2. 行内块：设置垂直外边距时整行元素都会改变

### 内边距-padding

改变计算方式，属性：box-sizing—指定盒模型的计算方式

取值：

1. content-box：默认的计算方式	宽度=左右边框+左右外边距+左右内边距

2. border-box：元素的尺寸会包含border以及padding的值，width就是实际占地大小

   box-sizing:border-box;

##背景-background

background-color	默认从边框处开始填充

###背景图片

1. background-image:url(1.jpg);
2. **背景图片平铺：background-repeat**   默认横向纵向都平铺，背景图片显示在背景颜色上方
   1. no-repeat 不平铺	图片较小时，元素内部有空白
   2. repeat-x 仅水平平铺
   3. repext-y 仅垂直平铺
3. **背景图片尺寸：background-size**，
   1. 大小：原图像等比缩放，等于原图像
   2. 百分比：元素本身的百分比，等于原图像
   3. cover：将背景图等比放大,直到覆盖元素所有区域，可能只显示图片的某个部分
   4. contain：将背景图等比放大/缩小，直到背景图碰到元素的某个边缘，等于原图像
4. 

## body
body属性：
text：修饰body内的所有文本，其他元素没有text属性
bgcolor：背景颜色设置，仅body可以
### 浮动
.clearfix{
	content:'';
	display:block;
	clear:both;

}

## 图片

本身是行内元素，但是支持设置宽高