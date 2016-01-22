---
title: Hexo搭建Github静态博客
date: 2016-01-17 18:57:52
tags: [hexo]
categories: 程序猿的自我修养
---

之前一直想有个好的环境能够写自己的博客,先是在csdn上面写了几篇文章，后来又跑到简书上面写了几篇，但是都感觉这些网站博客的排版不是很好看，索性自己按照网上的教程折腾了现在大家看到的这个博客。

好了，废话不多说，直接上干货。

<!--more-->


# 准备
---------------
第一次搭建博客的时候,可能大家像小编一样不知道从哪里开始，但是有一天，小编看到了一位大神博客最下面的一行字

由** *Hexo 强力驱动***  主题 -** *NexT.Muse***


当时就百度了一下 hexo 以及 next 到底是什么，具体的名词解释小编就不在这里浪费大家的时间了，大家可以谷歌的到，网上有很多的教程。至此，小编就花了大约一天的时间将自己的博客搭建完成了。

# Hexo 安装

--------------------------
关于hexo以及主题的教程网上已经有很多了，而且写的都很详细，小编就是按照他们的教程来安装的。在这里，小编主要提供一些好的大神写的教程以及自己安装过程中遇到的坑。

**参考资料**:

* [hexo系列教程：（二）搭建hexo博客](http://zipperary.com/2013/05/28/hexo-guide-2/) by zippera（推荐）
* [hexo系列教程：（三）搭建hexo博客](http://zipperary.com/2013/05/29/hexo-guide-3/) by zippera（推荐）
*  [hexo官网](https://hexo.io/zh-cn/docs/index.html)

## hexo安装遇到的坑

按照上面的教程一步一步来做的话，没有什么大的问题，但是还是会遇到一些坑。比如:

 **问题 **: 我们在编辑完站点的配置文件后,输入 `hexo depeloy`,显示`ERROR Deployer not found : github`

   **解决办法**: 在站点配置文件_config.yml里面将`deploy`的`type`改成`git`，然后运行下`npm install hexo-deployer-git --save`
再`hexo g`,在`hexo d`即可解决

  
 ** 问题** : 编辑完站点配置文件_config.yml后，在终端中运行指令,会出现`FATAL YAMLException: can not read a block mapping entry; a multiline key may not be an implicit key at line 12, column 1`:
 
 **解决办法**:检查_config.yml内容，`特别注意:后面需要有一个空格`,以后在写博客的时候，博客开头的，时间，日期冒号后面都得需要一个空格。
 
# 主题next的配置
***
安装完hexo后，我们就有了自己的博客，是不是很简单呢？但是hexo默认的主题 `landscape`不是很好看，所以，我们需要给他换一个新的主题。`next` 在github上面star的数量是最多的，主题简洁清新，很受欢迎。详细的教程在 [next主题安装配置](http://theme-next.iissnan.com/)

按照上面的教程就能够做出像我类似的博客了。也不是很复杂，主要是耐心。

# 多台电脑写blog
***
我们知道，hexo相当于是和GitHub绑定的，我们在本地写好blog，然后输入hexo 的几个命令，就能将本地的blog部署到github上面去，但是如果是在另外一台电脑上，写博客的话，应该怎么办呢？


