---
title: LearnCpp 教程转换
date: 2023-12-12 20:18:53
permalink: /pages/992655/
categories:
  - 技术
  - 实用仓库
tags:
  - 
author: 
  name: yellowandgreen
  link: https://github.com/yellowandgreen
---
# LearnCpp 教程转换为PDF

本代码用来将[learnCpp](https://www.learncpp.com/) 转换为PDF书籍，便于离线阅读。

## 方法

1. 首先，使用**pyautogui**打开浏览器，然后打印所有的页面。

这里有两个前提条件：

1. 将浏览器放在Dock栏的第一个
2. 使用CSS来过滤多余的内容，以下是我采用的CSS代码：

```
#wpdcom{        display:none;    }
/ .prevnext-inline{        display:none;    } /
/* #masthead{        display:none;    }
.wpsolution{        display:block !important;    }
.solution_link_show{        display:none;    } */ 
```

1.  收集网址和章节名 
2.  使用浏览器来打印这些课程并组织打印的文件。 
3.  检查是否有遗漏和错误的文件。 
4.  使用**fitz**来组合成单个PDF文件。 

## 使用

1.  直接下载或者克隆本项目 git clone https://github.com/YellowAndGreen/LearnCpp-PDFconverter.git 

1.  使用webpage2pdf.py来下载课程。 

>  或许有一些参数需要根据实际情况调整（比如time.sleep(2)）。

1. 使用delete_lesson.py检查是否有遗漏和错误的课程，并重新打印。
2. 使用combine_pdf.py来合并PDF文件

## 为什么

**为什么不适用浏览器驱动（基于Selenium）来自动化这个过程？**

使用浏览器驱动很难修改格式，而且浏览器驱动打开的页面不包含任何驱动，也就是说很难去控制CSS。