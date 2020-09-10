---
layout: page
title: Résumé
subtitle: An ordinary person
---

<span style="float: right; "><a href="{{ '/assets/resume.pdf' | prepend: site.baseurl }}"><strong>> Download as PDF</strong></a> </span>
<br>

### 搭建个人技术博客
> 使用GitHus Pages +Jekyll 快速部署个人博客

> - GitHub Pages
>     - 定义：给所有用户提供一个个人主页
>     - 如何访问： 个人域名：用户名.github.io
>     - 如何编写主页： 建立一个用个人域名为项目名的远程版本仓库，只需要向该远程版本仓库中的master分支提交代码即可 （该代码中必须有一个文件，叫index.html文件）
> - Jekyll
>     - 定义：可以将markdow语法自动编译成html语法的一个工具
>     - 安装：不需要我们自己安装，在github网站当中预安装的
>     - 使用：不需要人为的使用，当你请求个人域名的时候，gidhub服务器会读取仓库（一个人域名命名的那个远程版本仓库）中的master分支中的代码，如果该代码为markdow语法，会自动调用Jekyll将其编译为html代码并返回客户端

- 建立一个以个人域名为项目名的远程版本仓库
- 访问一个网址：主题网址：http://jekyllthemes.org/ 选择一个主题将其代码复制到我们仓库master分支
- 以上两步可以合为一步，在主题仓库中点击fork,点击setting设置仓库名，即可
-   将远程版本库中的代码克隆到本地
-   -    点击头像，点击code，复制链接
-   -    在文件打开终端执行克隆：  git clone -b master https://github.com/Hzyjywb/Hzyjywb.github.io.git myBlog
-   -    从远程版本库中克隆下来的代码会自动创建本地版本仓库

- 修改配置文件以及页面内容
- 书写博客 