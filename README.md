# androidNotes
<a name="_ac"></a>
1.web基础<br/>br换行标签，<p>p段落标签</p>  水平分割线hr<hr>    
指数标记sup  5<sup>3</sup>  <h1>h1标签自带加粗换行效果</h1>
<br/>font标签<font size="7">红色</font>,size的取值范围1-7，7最大<br/>
<b>b加粗</b>
<br/>转移字符&nbsp;nbsp
<br/>lt表示<   a&lt;b
<br/>gt表示>   a&gt;b;但是如果是比较数字1<2，那么不需要转义 <br/>
无需列表   
爱好<ul type="circle">
 <li>a</li>
  <li>b</li>
   <li>c</li>
</ul>
</br>
有序列表      
爱好<ol>
 <li>a</li>
  <li>b</li>
   <li>c</li>
</ol>

<br/>
图形标记:title是指鼠标移动图形上的提示，alt是图片加载不到时显示的文字,border是图形的边框 
<br/>
超链接a: <a href="https://www.baidu.com/" target="_blank">超链接</a>
<br/>
下载链接: <a href="thunder://***************" target="_blank">点击下载</a>
<br/>
定义锚点，使用锚点: <a name="_abc"></a>   <br/> <hr><a href="#_ac">点击回到锚点</a>
<br/>
绘制表格:<table><tr><th>姓名</th><th>年龄</th></tr><tr><td>tom</td><td>18</td></tr><tr><td>Jerry</td><td>21</td></tr></table>
表格的边框由自身外围边框加上每个单元格的边框构成，cellpadding是指内容距离单元格边框的距离,cellspacing是指单元格之间的间距,th是表头标签，与td一样，但是具有加粗和剧中的效果<br/>
frameset框架集合，用frameset时不需要body,frame没一个子页面,指定rows时，效果为竖着排列<frameset rows="30%,70%"><frame src="https://www.baidu.com/"/><frameset cols><frame src="https://www.baidu.com/"/><frame src="https://www.baidu.com/"/></frameset></frameset>
<br/>
如果想在a页面有个超链接，但是想在b中打开，那么在a中指定超链接时<a href="xxxxx" target="_dd">在b中打开</a>  <br/>并在指明框架页面时<frame src="b页面" name="_dd"/>

<br/>
表单，放在body内，用<form action="#提交服务器" method="get">  
用户名：<input type="text" name="username"/><!--健名-->disabled属性为yes时，提交的表单中没有username，readonly是不能修改，但是还可以提交
<input type="submit" value="提交"/>
</form>表示范围,<br/>
radio单选框
<br/>多选框checkbox提交时，如果有多个选项，会产生多个键值对
<br/>下拉选,不是input类型，而是select标签修饰
<select name="edu">
<option value="bk">本科</option>
<option value="zk">专科</option>
<option value="ss">硕士</option>
</select>
<br/>
文本域：<textarea rows="10" cols="">
<br/>
文件上传<input type="file" name="file"/>
<br/>
隐藏域
<input type="hidden" name="haha" value="heihei"/>在表单上看不到却可以提交   
meta标签是告诉浏览器用什么样的方式去解码0101这些数据<br/>
<meta http-equiv="Content-Type" content="text/html;charset=utf-8">  <br/>
3s后自动刷新到baidu
<meta http-equiv="Refresh" content="3;url=http://www.baidu.com">

html注释<!--注释内容-->

2.CSS：cascade style sheet层叠样式表   
结合方式1：
所有的html标签都有style属性，给标签添加style属性 <p stype="color:red;"></p> ，style是css属性<br/>
结合方式2:
在heade中添加style<br/>
<head>
<style type="text/css">
p {
 color:red; 
}
</style>
</head>
<br/>
结合方式3:
创建.css文件,在里面写
p{
color:red;
}
，然后在需要引用css文件的html文件的head里，添加<link rel="stylesheet" type="text/css" href="p.css引用的"> 

css语法
选择器{
  样式属性键:样式属性值;
  样式属性键:样式属性值1 样式属性值2 样式属性值3;/*   这里是css中的注释,一个键存在多个值的情况下，值用空格隔开  */
}

选择器类型

标签选择器
a{
 键:值
}

id选择器
#one{
 键:值
}
引用时<a id="one"></a>指明标签id，同时要保证id的使用在同一个页面中唯一

类选择器
.one{
 键:值
}
引用时<a class="one">************</a>，类选择器可以多次引用

伪类选择器
选择标签的某个状态，需要配合其他选择器使用
状态种类:
l  未访问过的
v  访问过
h  悬浮鼠标放在上面
a  激活，点击
a:link{
 color:green;
}
a:visited{
 color:black;
}
a:hover{
color:white
}
a:active{
color:pink
}
还可以将前三种选择器组合起来

样式设置背景图片
background-image:url("mn.jpg");
默认情况下，图片会重复铺满整个页面，为了禁用图片重复，一张图片铺满，可以设置
background-repeat:no-repeat;
background-attachment:fixed;背景跟着屏幕滚动

div块级标签，占据范围是若干整行， span行内标签，占据的是一行单中的一部分

块内标签：div p ul li ol ..
行内标签: span a font b(加粗)  ..

盒子的构成由块
padding：内边距，
margin：外边距,
padding:
1个值，上下左右
2个值，第一个上下，第二个左右
3个值，1上，2左右，3下

3.javascript
结合方式1:在head里面
<head>
<script type="text/javascript">
alert("haha")
</script>

结合方式2:
<script type="text/javascript" src="hello.js"></script>，但是script标签中，不能再输写js代码

</head>
