---
title: 基本决策方法整理
layout: post
categories: [主题研究, 决策, 决策方法]
---

# 个人简介
我是一个软件工程师
# 教育经历
# 工作经历
Hexo自定义原理
Hexo 系列的博客中的文章都是经Hexo的主题渲染的静态网页。所以Hexo博客大部分都呈现出一种高度的统一化与规范化。不过 Hexo 提供了跳过渲染功能，使得我们可以直接在博客中放入自定义网页。

比如在博客中放入图片、自定义404.html、自定义About页面、简历等

创建自定义网页
网页可以是自己编写的，也可以是别人现成的源码（下载喜欢的页面）。

网页编写完成后，在Hexo\source目录下创建一个文件夹（文件夹名称任意，比如我创建的是about这个文件夹，部署完成后，访问http://mrlsm.github.io/about即可看到效果，依此类推）

将 html 文件放置于此文件夹，并重命名为 index.html 。

跳过渲染
跳过渲染有下述两种方法：

在html文件中添加跳过渲染指令
用编辑器打开放入\Hexo\source\创建的文件夹中的 index.html 文件，在开头添加如下代码即可

---
layout: false
---

添加该指令后，执行 hexo g命令时便会跳过该 index.html文件，使得index.html不受当前 hexo 主题影响，完全是一个独立的网页，如果网页引用了 css 或 js，css 和 js 需使用外链或者将css js 文件放入index.html同目录下引用。

引用图片亦是如此

在_config.yml文件中设置skip_render
使用编辑器打开 Hexo 目录下的_config.yml文件，找到skip_render

skip_render一般有以下四种常用参数：

跳过source目录下的 test.html: skip_render: test.html

跳过source目录下 test 文件夹内所有文件：skip_render: test/*

跳过source目录下 test 文件夹内所有文件包括子文件夹以及子文件夹内的文件：skip_render: test/**

跳过多个路径：

skip_render:
 - test.html
 - test/*

添加完成后便不会渲染指定文件/文件夹。

完成
执行hexo g -d 发布，就可以在自己的网页上看到自定义页面了（可以制作一份自己的简历哦）。

©著作权归作者所有,转载或内容合作请联系作者
2人点赞
github
更多精彩内容，就在简书APP


作者：店_小二
链接：https://www.jianshu.com/p/524b073f9b37
来源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

Hexo自定义原理
Hexo 系列的博客中的文章都是经Hexo的主题渲染的静态网页。所以Hexo博客大部分都呈现出一种高度的统一化与规范化。不过 Hexo 提供了跳过渲染功能，使得我们可以直接在博客中放入自定义网页。

比如在博客中放入图片、自定义404.html、自定义About页面、简历等

创建自定义网页
网页可以是自己编写的，也可以是别人现成的源码（下载喜欢的页面）。

网页编写完成后，在Hexo\source目录下创建一个文件夹（文件夹名称任意，比如我创建的是about这个文件夹，部署完成后，访问http://mrlsm.github.io/about即可看到效果，依此类推）

将 html 文件放置于此文件夹，并重命名为 index.html 。

跳过渲染
跳过渲染有下述两种方法：

在html文件中添加跳过渲染指令
用编辑器打开放入\Hexo\source\创建的文件夹中的 index.html 文件，在开头添加如下代码即可

---
layout: false
---

添加该指令后，执行 hexo g命令时便会跳过该 index.html文件，使得index.html不受当前 hexo 主题影响，完全是一个独立的网页，如果网页引用了 css 或 js，css 和 js 需使用外链或者将css js 文件放入index.html同目录下引用。

引用图片亦是如此

在_config.yml文件中设置skip_render
使用编辑器打开 Hexo 目录下的_config.yml文件，找到skip_render

skip_render一般有以下四种常用参数：

跳过source目录下的 test.html: skip_render: test.html

跳过source目录下 test 文件夹内所有文件：skip_render: test/*

跳过source目录下 test 文件夹内所有文件包括子文件夹以及子文件夹内的文件：skip_render: test/**

跳过多个路径：

skip_render:
 - test.html
 - test/*

添加完成后便不会渲染指定文件/文件夹。

完成
执行hexo g -d 发布，就可以在自己的网页上看到自定义页面了（可以制作一份自己的简历哦）。

©著作权归作者所有,转载或内容合作请联系作者
2人点赞
github
更多精彩内容，就在简书APP


作者：店_小二
链接：https://www.jianshu.com/p/524b073f9b37
来源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
