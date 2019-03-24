---
layout: post
title:  "构建远程AI实验环境"
date:   2019-03-03 22:02:02
categories: Machine Learning
---

## 申请一个Azure Machine Learning专用主机
* 使用iPad日常学习的配置，推荐使用Terminus App远程连接服务器
* 使用iPad远程学习的相关配置参考上一篇博客；

## Python和VIM配置
* 把ESC重新映射，因为ipad键盘的ESC没有
* 配置Python的VIM环境，使用pydoc3查看具体某个函数的文档

## 配置matplotlib和nginx
matplotlib实际支持Agg渲染，不需要桌面环境，可以保存图片，具体方法如下：
* 配置`~/.config/matplotlib/matplotlibrc`,
```
backend: Agg
```
Nginx配置为`autoindex on`可浏览文件夹，预览matplotlib产生的图片

## 使用Jupter notebook
安装Jupter notebook，Jupyter notebook可以远程访问和打开，只需要运行在指定端口上就可以了
设置中开到了8080端口，需要token或者密码登录；
