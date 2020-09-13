---
layout: self
title: 留言区
subtitle: 欢迎评论
liziyue: 
---
<form method="post" action="sava_book.php">
  			<tr>
  				<td>姓名：</td>
  				<td><input type="text" name="name" size="25"></td>
  			</tr>
  			<tr>
  				<td>E-mail:</td>
  				<td><input type="text" name="email" size="25"></td>
  			</tr>
  			<tr>
  				<td>主题</td>
  				<td><input type="text" name="title" size="26"></td>
  			</tr>
  			<br>
  			<tr>
  				<td valign="top">留言:</td>
  				<td><textarea rows="7" cols="25" name="content"></textarea></td>
  			</tr>
  			<td colspan="3">
  			<table align="center" width="100%" cellspacing="0" cellpadding="0" bordercolordark="#ffccff">
  				<tr>
  					<td align="center"><input type="submit" value="提交留言"></td>
  					<td align="center"><a href="ViewMessageServlet"><font size="2">查看留言</font></a></td>
  					<td align="center"><input type="reset" value="重新填写"></td>
  				</tr>
  			</table>
  			<hr>
  			</td>
  		</form>

