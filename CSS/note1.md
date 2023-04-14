

# css单位

html只有一种单位：px像素（默认，可以不写）

css没有默认单位，必须写

1、绝对单位

1 in=2.54cm=25.4mm=72pt=6pc。

各种单位的含义：

in：英寸Inches (1 英寸 = 2.54 厘米)

cm：厘米Centimeters

mm：毫米Millimeters

pt：点Points，或者叫英镑 (1点 = 1/72英寸)

pc：皮卡Picas (1 皮卡 = 12 点)

2、相对单位

px：像素 

em：印刷单位相当于12个点 

%：百分比，相对周围的文字的大小

# font

	p{
		font-size: 50px; 		/*字体大小*/
		line-height: 30px;      /*行高*/
		font-family: 幼圆,黑体; 	/*字体类型：如果没有幼圆就显示黑体，没有黑体就显示默认*/
		font-style: italic ;		/*italic表示斜体，normal表示不倾斜*/
		font-weight: bold;	/*粗体*/
		font-variant: small-caps;  /*小写变大写*/
	}

# RGBA
background-color: rgba(0, 0, 255, 0.3);
// 红 绿 蓝 透明度

	#000   黑
	#fff   白
	#f00   红
	#222   深灰
	#333   灰
	#ccc   浅灰

# HSLA
background-color: hsla(240,50%,50%,0.4);

H 色调，取值范围 0~360。0或360表示红色、120表示绿色、240表示蓝色

S 饱和度，取值范围 0%~100%。值越大，越鲜艳。

L 亮度，取值范围 0%~100%。亮度最大时为白色，最小时为黑色。

A 透明度，取值范围 0~1。


透明度：opacity 
background: tansparent;

# background
	
	background:red url(1.jpg) 
	no-repeat 100px 100px fixed;

等价于~

	background-color:red;
	background-image:url(1.jpg);
	background-repeat:no-repeat;
	background-position:100px 100px;
	background-attachment:fixed;

# 裁剪
clip-path

/* 裁剪出圆形区域 */

	clip-path: circle(50px at 100px 100px);

	transition: clip-path .4s;


# html & css
	HTML 的缺陷：

	不能够适应多种设备
	要求浏览器必须智能化足够庞大
	数据和显示没有分开
	功能不够强大

	CSS 优点：

	使数据和显示分开
	降低网络流量
	使整个网站视觉效果一致
	使开发效率提高了（耦合性降低，一个人负责写 html，一个人负责写 css）