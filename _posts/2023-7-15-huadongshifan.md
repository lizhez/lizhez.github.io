---
layout: post
read_time: true
show_date: true
title: 华东师范大学数据科学与工程学院暑期夏令营实践项目总结与反思
date: 2023-07-15
img: posts/20230715/back.webp
tags: [ 学习笔记]
author: 李哲
description: 夏令营项目--个人博客，总结反思
toc: yes # leave empty or erase for no TOC
---

在所给的四个项目中，经过仔细的考虑，选择完成【个人博客搭建】这个项目。其原因有一下三点：

- 首先，在比较了【关联时间序列】和【个人博客】的项目后，由于我未上手搭建过机器学习的模型，因此在14天的时间里是一个巨大的挑战。而本科期间，多项课程设计是有关网站系统的开发，选择【个人博客搭建】更加容易上手。
- 其次，在我看来【个人博客】是一个很好的展示自己个人能力、兴趣爱好的媒介。而GitHub Pages提供的这种静态网页，可以在没有个人域名和服务器的情况下向外提供个人网站链接，是一个很好的工具。
- 最后，我一直有过搭建个人博客来记录日常和学习的想法，但平时课程紧张，并没有来得及实现，而这次实践给了我一个合适的机会。

目前为止，整个博客构建的较为仓促，后期会对其进行补充和美化，并一直记录。下面我将从5个方面介绍此项目：


### 博客主题的选取

- Jekyll框架
    - Jekyll ，是由 Ruby 编写的、快速、简洁且高效的静态网站生成引擎， 使用一个模板目录作为网站布局的基础框架，并且支持 Markdown、Textile 等标记语言的解析，同时可以直接在 GitHub Pages 上使用 Jekyll来进行个人博客的搭建。
    - 本次项目，选择 Jekyll 正是由于其简易而强大的布局，可以快速上手开始项目搭建。同时 Jekyll Themes 提供了大量的页面模板，可以进行美化。
- 模板选择
    - 选择 Jekyll theme: Adam Blog 2.0 为模板进行网页的开发。它提供了主页、所有文章、标签、关于我、文章详情5种页面的设计模板，界面简单整洁。
- 参考链接
    - [源主题地址：Jekyll theme: Adam Blog 2.0](https://github.com/the-mvm/the-mvm.github.io)
    - [学习教程：B站-基于 GitHub Pages 和 Jekyll 搭建个人博客的简单心得](https://www.bilibili.com/video/BV14x411t7ZU/?spm_id_from=333.1007.top_right_bar_window_history.content.click&vd_source=d676acebe888563dfe01749d7eb1144f)


### 博客页面布局

- PC端
  - 主界面: 上方是页头，包括导航条按钮（默认关闭），博客标题，搜索按钮（可以点击以关键字搜索文章）。下方是文章列表和所有标签。最下方是页脚，包括关键的导航。
    ![主界面](./assets/img/posts/20230715/main.png)
    ![search](./assets/img/posts/20230715/search.png)
  - 导航: 通过点击页头左方三个横线的标志，可以展开导航栏。导航栏上方灯泡标志，控制页面的明亮或黑暗主题。
    ![导航](./assets/img/posts/20230715/nav.png) ![导航-暗](./assets/img/posts/20230715/nav-dark.png)
  - 所有文章：展示所有文章列表，竖向排列。
    ![所有文章](./assets/img/posts/20230715/all.png)
  - 标签：根据文章标签展示文章。
    ![标签](./assets/img/posts/20230715/tag.png)
  - 关于我：个人简单介绍。
    ![me](./assets/img/posts/20230715/me.png)
  - 文章详情：文章详情页。中间的正文，左侧的标签，而部分页面会显示导航，以及分享的链接按钮，最下方包括其他文章，作者信息，评论。
    ![detail](./assets/img/posts/20230715/detail.png)
    ![nags](./assets/img/posts/20230715/nags.png)
    ![other](./assets/img/posts/20230715/other.png)
    ![com](./assets/img/posts/20230715/com.png)
- 移动端
    ![phone](./assets/img/posts/20230715/phone.jpg)


### 博客功能实现

- 分页
  - 通过 Jekyll 中的分页插件实现主界面中文章的分页功能，这里设置六篇文章为一页。使用 ”jekyll install paginator“ 进行下载。
  - 根据当前页面是否由前一个或后一个进行自动的变化。
  - ![pages](./assets/img/posts/20230715/pages.png)
- 搜索
  - 这里可以通过关键字，对文章标题和文章内容进行检索。
- 标签
  - 除了对文章根据标题进行展示外，同时通过在文章页面的开头使用 "tags: \[ 学习笔记]" 为每个文章添加标签。此时可以根据标签对文章进行搜索。这里举例以证据学习查询，可以看到
  - ![e1](./assets/img/posts/20230715/e1.png)
  - ![e2](./assets/img/posts/20230715/e2.png)
- 评论
  - 使用 GitHub APPs 中的 utterances 实现评论功能
  - ```javascript
  # Comments
  comments: utteranc  #[disqus, utteranc]
  comments_opts:
  comments_curtain: yes # leave empty to show the disqus embed directly
  repo: lizhez/lizhez.github.io # The GitHub repo URL.  https://utteranc.es/
  issue_term: title # The GitHub issue label
  theme: github-light # The GitHub comment's there. e.g. github-dark
  ```

### 博客制作过程中遇到的问题

1. 参考资料相对较少

    相较于大型 web开发 框架（如 SpringBoot）网上存在大量资源和教程不同，Jekyll由于其轻量、简单的特点，从环境配置安装到使用，网络上系统化的学习资料很少。因此主要是根据实战视频，来了解 Jekyll 框架的结构和功能，并通过实际上手，来观察具体操作会影响到页面上什么内容的改变。
2. LaTeX公式书写的复杂度

    之前在记录学习笔记时，为了简单快速，很多都是直接截屏处理。而此尝试使用 LaTeX公式 的书写，来美化文章页面。由于时间问题，只在其中一个页面 [理解狄利克雷](https://lizhez.github.io/Dirichlet.html) 使用。


### 总结

经过此次实践过程，新学习了一项新的技术，同时完成了个人博客的搭建。这不仅仅是一项实践任务，同时也是一项可以实际使用的功能，向外提供了交流和学习的途径。

当前博客还有很多不足，计划在后续增加分类、播放等其他功能，继续完善。