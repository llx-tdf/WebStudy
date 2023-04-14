# css书写方式

1.行内样式：在某个特定的标签里采用 style 属性。范围只针对此标签。

    <p style="color:white;background-color:red">我不会就这样轻易的狗带</p>


2.内嵌样式（内联样式）：在页面的 head 标签里里采用\<style\>标签。范围针对此页面。

    <style type="text/css">
        p {
            font-weight: bold;
            font-style: italic;
            color: red;
        }
    </style>

    <body>
        <p>洗白白</p>
        <p style="color:blue">你懂得</p>
</body>


3.外链样式：引入外部样式表 CSS 文件。这种引入方式又分为两种：

    3.1 采用<link>标签。
    例如：<link rel = "stylesheet" type = "text/css" href = "a.css"></link>

    3.2 采用 import 导入，必须写在<style>标签中，并且是第一句。
    然后用类似于@import url(a.css) ;这种方式导入。

    
# 选择器

    高级选择器：

    后代选择器：用空格隔开
    交集选择器：选择器之间紧密相连
    并集选择器（分组选择器）：用逗号隔开
    伪类选择器


# 伪类

同一个标签，根据其不同的种状态，有不同的样式。

- 静态伪类选择器：只能用于超链接的样式
    - :link 超链接点击之前
    - :visited 超链接被访问过之后 
- 动态伪类选择器：针对所有标签都适用的样式
    - :hover “悬停”：鼠标放到标签上的时候
    - :active “激活”： 鼠标点击标签，但是不松手时。
    - :focus 是某个标签获得焦点时的样式（比如某个输入框获得焦点）

# 超链接

- :link “链接”：超链接点击之前
- :visited “访问过的”：链接被访问过之后
- :hover “悬停”：鼠标放到标签上的时候
- :active “激活”： 鼠标点击标签，但是不松手时。

    <style type="text/css">
	/*让超链接点击之前是红色*/
	a:link{
		color:red;
	}

	/*让超链接点击之后是绿色*/
	a:visited{
		color:orange;
	}

	/*鼠标悬停，放到标签上的时候*/
	a:hover{
		color:green;
	}

	/*鼠标点击链接，但是不松手的时候*/
	a:active{
		color:black;
	}
    </style>

在css中，这四种状态必须按照固定的顺序写：

a:link 、a:visited 、a:hover 、a:active

# 盒子

一个盒子中主要的属性就5个：width、height、padding、border、margin。如下：

- width和height：内容的宽度、高度（不是盒子的宽度、高度）。
- padding：内边距。
- border：边框。
- margin：外边距。

padding：上 右 下 左
         上  右和左  下
         上和下  左和右

# CSS盒模型和IE盒模型的区别：

在 标准盒子模型中，width 和 height 指的是内容区域的宽度和高度。增加内边距、边框和外边距不会影响内容区域的尺寸，但是会增加元素框的总尺寸。

IE盒子模型中，width 和 height 指的是内容区域+border+padding的宽度和高度。

# 浮动
所有标签，浮动之后，不区分行内、块级了。

标准流中的文字不会被浮动的盒子遮挡住。

关于浮动我们要强调一点，浮动这个东西，为避免混乱，我们在初期一定要遵循一个原则：永远不是一个东西单独浮动，<b>浮动都是一起浮动，要浮动，大家都浮动<b>。

# 收缩
一个浮动的元素，如果没有设置width，那么将自动收缩为内容的宽度（这点非常像行内元素）。



