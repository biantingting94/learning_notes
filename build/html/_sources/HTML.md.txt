###1、特殊字符

1. &nbsp；—表示一个空格
2. &lt；表示一个<
3. &gt；表示一个>
4. &copy；表示版权
5. &yen；表示￥

###2、文本样式

1. \<b> ：加粗
2. \<i>： 斜体
3. \<u>：下划线
4. \<s>：删除线
5. \<sup>：上标
6. \<sub>：下标

###3、标题元素\<h>

字体加粗；上下文之间有垂直空白间距

### 4、段落元素\<p>

默认换行；段落之间产生垂直间距

###5、分割线（水平线）

\<hr>

属性：

   	1. size 水平高度，像素px或者百分比%
   	2. width 宽度
   	3. align 对齐方式，默认居中
   	4. color 颜色

### 6、预格式化——保留HTML代码中的回车和空格

\<pre>\</pre>

### 7、分区元素

#### 7.1、块级元素——独占一行

块分区——用于页面布局

标题、段落、div

#### 7.2、行内元素——多个元素在同一行

行分区——用于处理同一行文本的不同样式

文本元素：b i u s sup sub a span img 

#### 7.3、行内块元素——表单控件

### 8、图片img

jpg：压缩图片；图片模糊

gif：动画

png：背景透明（logo图标） 

width和height属性，只修改其中一个属性值，另一个值会等比缩放

###9、链接a

#####语法：

target：网页打开方式

- \_self：当前标签页打开，默认值
- \__blank：新的标签页中打开

#####表现形式：href

- 资源下载：url链接到rar或者zip
- 发送电子邮件：\<a href="mailto:xxx.163.com">\</a>
- 返回到页面顶部：href=“#”
- 链接到JavaScript：\<a href="javascript:js脚本">\</a>

#####锚点：跳转到指定位置

- 定义：

  - a标记的name名称：\<a name="锚点名称">\</a>
  - 其他标签使用id属性

- 跳转到锚点：

  当前页面：\<a href="#锚点名称">本页\</a>

  其他页面：\<a href="url#锚点名称">其他页面\</a>

###10、表格table

- 行：tr，在行中插入列

- 列：td

####2、属性：

  **table：**

- 宽度：width

- 高度：height

- align：对齐方式，left、center、right

- border：边框宽度

- cellpadding：单元格内边距

- cellspacing：单元格外边距

- bgcolor：背景颜色

**tr：**行

- align：行内容水平对齐，left、center、right
- valign：行内容垂直对齐，top、middle、bottom
- bgcolor：当前行的背景颜色

**td：**单元格

- width
- height
- align
- valign
- bgcolor
- colspan：跨列
- rowspan：跨行

  设置宽高后，对齐方式才能生效

#### 3、可选标记

- 表格标题：caption，位于table下的第一个子元素
- 行/列的标题：th，取代td

#### 4、复杂应用

1. 行分组：
   1. 表头行：thead，表格最上面一行
   2. 表尾行：tfoot，表格最后一行
   3. 表主体：tbody，将若干行放在tbody中，统一管理
2. 不规则表格
   1. 跨列：colspan，删除被合并的单元格，横向合并
   2. 跨行：rowspan，纵向合并

### 11、列表

1. 作用：从上到下（从左到右）显示所有数据

2. 组成：列表类型+列表项

   1. 有序列表：ol——li

      1. type：指定列表项标识的类型
      2. start：指定第一个元素的起始编号

   2. 无序列表：ul——li

      1. type：指定列表项标识的类型

   3. 定义列表：

      1. dl：表示定义列表
      2. dt：要解释的名词
      3. dd：对名词的解释内容，会有空格

     ·常用于图文混排
###12、结构标记，取代div，都是块级元素

1. \<header>\</header>：定义网页或者某部分的头部
2. \<nav>\</nav>：导航链接
3. \<section>\</section>：网页主体内容
4. \<aside>\</aside>：页面的侧边栏
5. \<footer>\</footer>：页面底部
6. \<article>\</article>：定义文字性内容

### 13、表单form

#### 13.1、属性

1. action：定义服务器处理程序的地址url
2. method：指定表单是数据的提交方式
   1. get（默认）：显示提交；数据限制2kb；需要从服务器获取数据时显示
   2. post：隐式提交；无数据限制；传递数据给服务器
3. enctype：指定表单数据的编码格式
   1. 默认值：任意字符
   2. multipart/form-data：允许提交文件
   3. text/plain 普通字符

#### 13.2、表单控件

1. **input**

   1. type：控件类型

      1. 文本框和密码框：type="text"   type="password"

         属性：

         1. maxlength：输入的最大字符数
         2. readonly：只读，无属性值，可以提交
         3. placeholder：占位符，默认显示的文本

      2. 按钮

         1. 提交按钮：type="submit"，将表单中的数据提交给服务器
         2. 重置按钮：type=“reset”，将表单中的内容恢复到初始化的状态
         3. 普通按钮：type=“button”
         4. value：按钮上的文字

      3. 单选框、复选框

         1. name：定义控件名称，**用于分组**。单选按钮需定义name属性
         2. checked，设置默认被选中，无属性值

      4. 隐藏域和文件选项框

         1. 隐藏域：type=“hidden”，想提交给服务器，但是不想展示给用户
         2. 文件选项框：type=“file”，method=“post”，enctype="multipart/form-data"

   2. **name**：控件名称，服务器端使用

   3. **value**：控件的值，显示在页面中

   4. **disabled**：                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   禁用控件，不能提交到服务器，没有属性值 

2. textarea：多行文本，换行符不能使用

   1. cols：指定文本域的列数（英文字符个数，中文减半）
   2. rows：默认显示的行数，超过rows范围出现滚动条

3. select—选项框

   1. size：显示选项的数量，默认为1。取值大于1，元素为滚动条，否则为下拉列表
   2. multiple：设置多选，没有值。只有滚动列表支持

   option—选项的值

   1. value：选项的值
   2. selected：设置被选中

4. 其他

   1. label元素：关联文本与表单控件

      语法:\<label>\</label>

      属性：用for关联表单控件的id值，用于选中表单控件

      如：\<label for="uname">姓名\</label>

      ​	<input type="text" id="uname">点击文字“姓名”可以关联到输入框

   2. 为控件分组：fieldset

      语法：\<fieldset>\</fieldset>为控件分组——自动为组内信息加外边框

      ​	    \<legend>\</legend>为分组指定标题

   3. 浮动框架：iframe

         作用：从一个网页引入另一个网页的内容 

         属性：

         ​	src：引入的文件地址

         ​	frameborder：框架边框

#### 13.3、新表单控件

1. 电子邮件：email
2. 搜索：search
3. URL路径：url
4. 电话号码类型：tel 在移动端使用，显示拨号键盘
5. 数字类型：number
   1. value：控件值
   2. min：最小值
   3. max：最大值
   4. step：步长
6. 范围类型：range，提供滑块组件，允许选择指定范围的值
7. 颜色类型：color
8. 日期类型：date
9. 周类型：week
10. 月份类型：month
      

  ​    

  ​    



   

​      


​      

   