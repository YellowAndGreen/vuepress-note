---
title: OmniAnki
date: 2023-12-12 20:22:11
permalink: /pages/5dda49/
categories:
  - 技术
  - 实用仓库
tags:
  - 
author: 
  name: yellowandgreen
  link: https://github.com/yellowandgreen
---
# OmniAnki

仓库：​github.com/YellowAndGreen/OmniAnki

![img](https://pic3.zhimg.com/80/v2-e1ff20c5e49f75fb646583e882a1c5f7_1440w.jpg)

## 起因 

Anki的模版功能比较简化并且当模版复杂时加载速度很慢，并且额外功能只能通过插件实现。虽然Anki提供了丰富的功能和插件系统，但对于开发者而已还需要额外了解PyQt和相关api，具有有一定的学习成本。且Anki的在线同步功能时好时坏，很难完全掌控自己的单词库，因此使用Django+Bootstrap实现了一个简易版的Anki，在其中也加入了自己对于单词记忆的想法。

在线Demo：用户名admin 密码1234yellowandgreen.xyz:7777

>  OmniAnki只是一个玩具项目，并没有经过验证的记忆曲线程序。

## 原则

首先是为了实行单词记忆的例句原则，OmniAnki的卡片正面只有英文单词和英文例句，只能通过例句回忆起对应释义。 *根据Anki的简化原则，每张卡片只对应一个释义，即只需要回忆起一个释义即可。*

## 功能

添加了一些基础的功能： 

1. 点按字典：类似于kindle的长按查看词典释义，添加了COCA排序 
2. 在线发音：使用有道在线语音        

![img](https://pic2.zhimg.com/80/v2-4a47cc8bd8e0e273dbdae723f7d1bba0_1440w.jpg)

3. 例句替换：支持使用字典中的例句作为随机例句

再就是Anki的同步网速时好时坏，让人担心记忆库丢失的问题，因此在OmniAnki中内置了定时的数据库备份功能，也支持手动导出。

## 端到端

最后是我想将其做成一个端到端的英语学习模式。现在很多单词软件都试图打通英文阅读和单词记忆的积累， 但大多只是简单的将英文生词添加进入单词表中，而忽略了更重要的信息——阅读文本中的例句。 对于个人而言，原文无论是故事还是论述，其内容结合例句能够有效的增强单词的记忆熟悉度， 例如好几年前的权力的游戏中的单词tart既可以表示甜果馅饼也可表示坤坤，虽然是一个不太常用的词， 但结合剧情中瑟曦和荆棘女王的互怼，时至今日仍然记忆犹新。 因此在OmniAnki中额外加入了一个简易的新闻获取与阅读模块，同时简化了查词和添加词汇的功能，可以一键添加原文例句和字典例句。

![img](https://pic2.zhimg.com/80/v2-59f37468ccd78170bdff65867cf53298_1440w.jpg)