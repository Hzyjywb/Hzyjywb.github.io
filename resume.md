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

> - 软件入口：.exe
> - 如果你的环境中有apache 那么 他会自带有一个外挂（apache的一个模块）这个外挂的名字叫php，所以他叫php模块，这就是 php翻译工具
> - 在终端中 “用一个软件打开一个文件”的命令是“软件名 文件路径” ==== “软件的入口文件地址 要执行的文件地址”
> - 环境变量PATH的作用是：为了帮助人类去寻找 软件入口文件
> - 只需要你把常用的命令（软件入口文件的坐在地址）添加到PATH中，这样就只需要 使用软件入口文件的文件名，他会自动根据你输入的这个文件名 在PATH对应的这些路径当中去寻找相应的入口文件
> - URL的本质 就是 远程路径
> - php -r "", 用php去解析双引号中的php代码
> - laravel安装的那条命令
>     - 用composer安装组件的常规命令 composer require 组件名 
>     - 用composer安装框架（大组件） composer create-project 组件名 --prefer-dist manSys "5.5.*" 
> - composer的安装过程
>     - php -r "": 用php去解析 双引号中的内容（双引号中的内容是php代码）
>     - copy函数：复制一个文件到另外一个新的文件中
>     - unlink函数：删除一个文件
>     - 不要忘记 最后的文档中的“全局安装”
> - laravel项目的安装过程
>     - 配置中国镜像（阿里云）——下载快 少bug `composer config -g repo.packagist composer https://mirrors.aliyun.com/composer/` 
> - 跟“配置”composer有关的 第一参数（子命令）是“config”
> - -g 表示全局 因为我们的composer 是全局安装的 所以 要加这个参数
> - 配置内容是 repo.packagist （下载链接）
> - 需要配置的composer对应的新链接
>     - 查看composer的配置项 composer config -l -g
> - -l 列表查看
>     - 下载laravel composer create-project laravel/laravel  "5.5.*"
> - composer最主要的目的下载PHP组件 与下载有关的操作有一下三个子命令
>     - require 下载普通组件
>     - create-project 下载想laravel这样的大组件（包含了很多普通组件框架）
>     - install 
>     - laravel/laravel 这是组件名
>     - --prefer-dist blog 自定义项目名为blog
>     - 5.5.* 代表组件的版本号
>     - php artisan key:generate 生成KEY
> - 第一个错误： 换源（国外源会慢很多）
>     - `composer config -g repo.packagist composer https://mirrors.aliyun.com/composer/` 换源
>     - composer config -l -g 查看composer 所有的配置项 其中有一个 源地址
>     - git 远程代码版本管理工具
>     - composer clearcache 清除缓存
>     - 通过查看composer所有的配置项中找到缓存的文件路径 进行手动删除
>     - 我可以确定这肯定是composer的错误 因为 我记忆中在没有换源之前他就报了这个错误 所以他跟源没有关系
>     - composer的配置项都是在 composer的安装目录中的composer.json文件中 我将这个文件删除
>     - 删除composer 重新安装 为了追求最干净的进行操作 所以不吧嗒作为全局命令 也就是局部安装 php composer.phar（就是 composer.phar这个文件的地址）  ==== 全局下的 composer