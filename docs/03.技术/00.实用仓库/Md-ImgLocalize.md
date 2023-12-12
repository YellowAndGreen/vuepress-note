---
title: Md-ImgLocalize
date: 2023-12-12 20:23:54
permalink: /pages/9ad3ba/
categories:
  - 技术
  - 实用仓库
tags:
  - 
author: 
  name: yellowandgreen
  link: https://github.com/yellowandgreen
---
# Md-ImgLocalize 2.0：让您的Markdown文件离线也能看图片

[Md-ImgLocalize](https://github.com/YellowAndGreen/Md-ImgLocalize/blob/main/README_ZH.md) 是一个开源的Python脚本，它可以扫描文件夹中的所有markdown文件，查找图片链接，并将markdown文件中的URL替换为本地文件名，并下载这些图片。这个工具的主要目的是为了解决一个问题：离线的markdown文件是存储和组织信息的可靠方式。当从网页复制文本时，文本会直接复制，但图片会作为链接复制。如果链接在未来过期，或者您处于离线状态，您就会丢失信息。因此，最好将每个添加为链接的图片下载到本地存储。

## 主要特点

- **支持多种标签**：它支持<img>和! [] ()标签，这意味着无论您的markdown文件中的图片是如何添加的，这个工具都可以找到并下载它们。
- **自定义行为**：提供更多选项来自定义行为，例如是否修改源markdown文件。这意味着您可以根据自己的需求来使用这个工具，使其更符合您的工作流程。
- **异步下载**：以异步模式下载图片，可以减少执行时间。这意味着即使您的markdown文件中有很多图片，这个工具也可以快速地下载它们。
- **循环遍历**：支持markdown文件的循环遍历。这意味着无论您的markdown文件有多少，或者它们在多少个不同的文件夹中，这个工具都可以找到并下载其中的图片。
- **保存图片和链接之间的字典关系**：能够使该程序自动检查并下载未下载的图片，也可重新运行该程序以只检查并下载未下载的图片。
- **转换所有的绝对路径文件到相对路径文件**：这个功能可以帮助您更好地管理您的文件系统。
- **支持多种图片格式**：搜索的图片扩展名包括png、jpg、jpeg、gif、bmp和svg，可以通过编辑正则表达式模式"png|jpg|jpeg|gif|bmp|svg"来添加更多。

## 如何使用

1. **安装Python**：首先，您需要在您的计算机上安装Python。
2. **克隆仓库**：然后，您需要克隆这个仓库。
3. **安装aiohttp**：接下来，您需要安装aiohttp。
4. **运行脚本**：最后，您可以运行python main.py --md_path=[md_path]。这里的md_path应该是您的markdown文件目录。
5. **保存日志文件**：您还可以使用--log来保存日志文件。
6. **直接修改源markdown文件**：使用--modify_source来直接修改源markdown文件，这个选项会在markdown文件目录下创建图片文件夹。
7. **指定协程数量**：使用--coroutine_num来指定协程数量，如果不需要使用协程，可设置为1。
8. **删除all_img_dict.json**：使用--del_dict来删除all_img_dict.json。
9. **转换所有的绝对路径到相对路径**：使用--relative来转换所有的绝对路径到相对路径，使用此选项则不会进行图片下载。

## 结论

总的来说，**Md-ImgLocalize** 是一个强大而灵活的工具，它可以帮助您更好地管理您的markdown文件。无论您是一个学生，一个研究人员，还是一个写作者，只要您使用markdown文件来存储和组织信息，这个工具都可以为您提供帮助。所以，如果您还没有试过这个工具，那么现在就是时候了。(该文章由bing生成)