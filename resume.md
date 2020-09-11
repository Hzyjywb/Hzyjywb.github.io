---
layout: page
title: 学习笔记
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

### 抽象能力的高低 是 评判一个程序猿能力的重要标准（非严谨的表达：唯一标准）
> - PHP是一个语言，与计算机交流的语言，语法
> - 想在电脑中使用php语法与计算机交流 一定得需要一个翻译工具——php解析器——apache的“php”模块
> - 我们使用的是nginx 并且使用的是php-fpm作为php的解析器   docker

### Laravel框架（最重要 使用度最广）
> - 什么是框架
>    - 框架 跟 程序的种类 没有关系
>    - 一个程序（系统）的目录结构（表面的）
>    - 框架 是 一堆常用的模块（包/组件）组成的具有特定目录结构的一个空项目（大的组件）
>    -php模块（组件/包）：一些特殊（特定）的功能用php代码实现（model类/文件上传类/Excel解析/图片 识别/支付/。。。。）我们要想实现类似的功能 就需要下载这一块的代码（安装某组件）—— composer工具
>    - 组件 都具有高度 抽象性（将 多个事物的共同点抽离出来）
> - composer工具（https://www.phpcomposer.com/）——php的包管理工具
>    -这是一个帮助我们下载组件/包/模块 的一个工具
>    -这些组件都放在https://packagist.org这个网站当中
> - 安装 composer create-project --prefer-dist laravel/laravel manSys "5.5.*"