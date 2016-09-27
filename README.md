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
