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

### 博客功能实现


### 博客制作过程中遇到的问题

### 总结

经过此次实践过程，