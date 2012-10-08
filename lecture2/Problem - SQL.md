# 第一题：SQL
大家都有在[toyhouse](http://toyhouse.cc/)写博客，记录自己学习数据库的心得、收获的习惯。所以，[toyhouse](http://toyhouse.cc/)上的博客量也在不断增长。

王小二是[toyhouse](http://toyhouse.cc/)的DBA(Database Administrator)。有一天上司找到小二，很认真地问了一个问题：

>小二啊，我来考考你，我现在有两张表，第一张是我们网站的每月的博客量，第二张是从开始到当前的累计博客量，你看怎么写SQL语句从第一张表得到第二张表呢？

王小二平时不好好学习，基础没打好，现在非常纠结有木有！！！不过，作为王小二好朋友的你正好在学习数据库，赶紧开动脑筋，帮帮小二吧，不然，他可要丢掉工作啦！

表1
<table>
<tr>
<td>Month</td>
<td>Quantity</td>
</tr>
<tr>
<td>2012.06.01</td>
<td>100</td>
</tr>
<tr>
<td>2012.07.01</td>
<td>200</td>
</tr>
<tr>
<td>2012.08.01</td>
<td>230</td>
</tr>
<tr>
<td>2012.09.01</td>
<td>340</td>
</tr>
<tr>
<td>2012.10.01</td>
<td>120</td>
</tr>
</table>

表2
<table>
<tr>
<td>Month</td>
<td>Quantity</td>
</tr>
<tr>
<td>2012.06.01</td>
<td>100</td>
</tr>
<tr>
<td>2012.07.01</td>
<td>300</td>
</tr>
<tr>
<td>2012.08.01</td>
<td>530</td>
</tr>
<tr>
<td>2012.09.01</td>
<td>870</td>
</tr>
<tr>
<td>2012.10.01</td>
<td>990</td>
</tr>
</table>

#*Notes:*

1. 请使用mysql作为数据库测试平台；
2. 请自己建立表格；
3. 鼓励围绕这道题进行发散。