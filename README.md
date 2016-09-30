# webNotes
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
<input type="button" onclick="close();" />   //close为script中的方法名
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

在javascript中,var是弱类型(变量的类型是可以改变的，可以赋值1,"a",false)

js中每行语句的结束使用;，也可以不使用

声明变量是，可以不加var，作用范围为全局，加var，作用范围在代码块中

js中的变量分类:原始类型(基本数据类型),对象类型(引用类型)
原始类型种类:
number,不区分整形，小数
string,"hello"和'world'都是字符串类型，不区分单引号双引号
boolean,
null,对象数据类型的占位符
undefined,null的衍生值，通常是系统自动赋值,比如当创建一个变量，但是没有初始化 

js中typeof＝>返回原始类型的类型,不适用于对象类型

typeof(null)返回的是object类型

var c="1234"
c= +c;此时，c变成数字类型，因为例子中+是数学运算符，

number==>boolean，除了+0,-0，NAN(其他未知数,用来表示错误的数字 ),其他都是true 
NaN,not a number，比如var n =+"abc"，此时就是NaN

sting==>boolean，字符串不为空，就是true，
null==>boolean,相当于false
undefined==>boolean,false
Object＝>true，只要对象存在，那么就是true


+"1"的结果为1

var a = "1"+1,==>输出"11"，只要有字符串存在,+就是拼接作用,但是其他数学运算符，字符串会自动转换为数字

"2">1,true,"2"=>2

"2">"1",true，字符串的比较是比较assci码

2==true,在比较的时候，是将boolean类型转换成数字类型,此结果为false

0==null，null转换成数字相当于NaN，所以为false
null==undefine,true
NaN==NaN，false,凡是NaN参与的，除了!  !=，其他全是false

===在比较时包括类型本身

Object是所有对象的父类
toString(),
n
function对象
function func(){
 alert("hello");
}

function对象的创建
var fun2 = function(a,b){
 return(a+b);
};


var fun3 = new Function("alert('helloe3')");
fun2.length==>打印的是fun2的参数个数
fun2.toString===>打印函数的定义 

fun2(1,2,3,5);//3,只用前两个
fun2();//NaN

js中的函数在调用时，只看函数名称，不看参数

arguments.length;//参数的个数。argrments是参数的封装,实际传递的参数个数

如果一个寒暑没有返回值，但是采用alert(fun()),那么打印的结果是undefined

超链接标签也可以使用javascript协议
<a href="javaScript:alert('haha');"> 点我</a>

<a href="javaScript:fun2(1,2);">点我</a>,函数fun2有返回值，默认情况下，会跳转到新的页面显示结果。如果想避免这样的结果，那么就使用void拦截返回的结果
<a href="havaScript:void(fun2(1,2);)">点我</a>

下面的0，起到了覆盖标签原有的功能,
<a href="javaScript:void(0)" onclick="alert('haha')">哈哈</a>

js中5个原始类型，有3个包装类，Number  String  Boolean ,原始类型可以直接调用包装类型的属性函数

String
创建:var str = new String(1);

"abc" instanceof String  ==>false，instalceof只用于判断对象是否是指定类型,"abc"是原始类型

Global全局对象:全局对象是与定义的对象，作为javaScript的全局函数和全局属性的占位符 。使用时不需要创建

decodeURI()解码某个编码的URI,将中文转成16进制
encodeURI()，把字符串编码为URI，将16进制转成中文

decodeURIComponent()解码某个编码的URI,除了英文,.,数字,其他的都转成16进制
encodeURIComponent()，把字符串编码为URI,与上面相反

parseInt   转换成整数
parseFloat 转换成浮点数

将字符串转换成数字的方法:
var str = "123";
var num1 = parseInt(str);从左到右依次转换，转换到遇到不能转换的字符为止,比如parseInt("123a")===>123
var num2 = +str;
var num3 = new Number(str);

判断一个值是否是NaN，不能用==来判断，因为NaN不与任何值相等，只能用isNaN

eval()，解析运行方法，就是将括号内的js代码执行，返回产生了的值
alert(eval("1+1"));//2
alert(eval("new String('abc')"));

Math对象 
random()，生成0～1之间的随机数

数组对象
var arr1 = [1,2,3,4];
var arr2 = new Array(1,2,3,4);
var arr3 = new Array(4);4表示数组长度 

push    将一个值放入数组的0索引位置
pop   将0索引的变量移除并返回
reverse 将一个数组反转，会对数组本身顺序进行调整
sort排序，默认按照字符串比较的方式排序
var arr5 = [100,1,5,9,2]; arr5.sort()===>[1,100,2,5,9]

sort可以传入一个比较器（有两个参数的函数）
规则:a>b返回正数，a=b返回0，a<b返回负数
function abc(a,b){
 return a-b;
}

js中的array没什么原则，
1.数组中元素的类型可以任意类型
var arr6 = ["haha",3.14,true,null,undefined,new Object()];==>length=6
2.数组的长度是可以随时变化的,
arr6[10] = "heiehi"
此时arr6.length = 11;

Date对象
创建
var date1 = new Date();//1970.1.1 0:0:0
var date2 = new Date(1313123123)
date1.getFullYear();获取年份
date1.getMonth();注意0代表1月份
data1.toLocaleString()，以本地时间格式表示;1992年5月3日 1：1:1

正则对象RegExp()
创建:
var reg = new RegExp("e","gi");
参数1:正则表达式;
参数2:匹配模式  g:全局   i:忽略大小
var reg2 = /e/g;这样也可以创建

test方法:校验字符串是否能与正则表达式匹配;
alert(reg.test("hello"));//true,hello里面已经包含了e

String与正则结合的四个方法
var str = "hello world"
split切割:str.split(/o/g)==>hell, w,rld
replace:str.replace(/l/g,"a")==>heaao worad
match:str.match(/or/g)==>找到返回or，找不到返回null
search:str.search(/e/g)==>1,返回索引位置


BOM ：Browser Object Model，浏览器对象模型
将浏览器中的各个组件封装成对象，我们可以使用这些对象来操作浏览器的一些动作 
5个对象:
window     浏览器的窗口
location   浏览器的地址栏
history    浏览器的历史纪录
screen     屏幕信息
navigator  将浏览器信息封装对象

1。获得window对象，当使用浏览器加载网页时，由浏览器创建,直接使用
window中的方法
alert

confirm:确认框   
     var b = confirm("您确定要删除吗?");// 根据电击结果b为true/false  
     alert(b)
prompt：输入框

     var str = prompt("请输入一个整数","0");//第二个参数为默认值，类似placeholder，点击确定时，返回string,取消时，返回null
open:window.open("xxx.html")，返回值是新打开的window对象;//这里有四个参数，只用写一个参数就可以了，第二个参数为窗口名称，第三个为窗口特性,第四个参数为是否将新打开的创酷加入到浏览器历史纪录里
close:window.close();

setInterval  设置定时器
    第一个参数是字符串形势，可以写js代码/或者放函数对象(不带括号),第二个参数单位为ms,返回值为当前开启的定时器id
    var intervar1 = window.setInterval("alert('abc');",1000)
    window.setInterval(func1,1000)
    window.setInterval("func1()",1000)//效果同上
clearInterval 清除定时器
    window.clearInterval(interval1);
    
另一对定时器
setTimeOut:延迟定时器，参数2时间后执行参数1
     var intervar2 = window.setTimeOut("alert('abc');",1000)
clearTimeout；只有在第一次执行之前停止才有意义
     window.clearTimeout(interval2);
