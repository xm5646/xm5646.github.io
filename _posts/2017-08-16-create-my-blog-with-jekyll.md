---
layout: post
title:  "github+Jekyll搭建静态博客"
date:   2017-08-16 22:14:54
categories: jekyll
tags: jekyll RubyGems mac
---

* content
{:toc}

一直以来都想搭建一个自己的博客，自己直接使用Python Django搭建的博客还没有成型，由于时间关系先采用简单的方式部署，将我在有道云笔记上的笔记慢慢的转移到这个上面来。




## 搭建过程

在jekyll的官网上 [http://jekyllrb.com/](http://jekyllrb.com/) 其实已经说得比较明白了，我在这里还是简单的说一下吧。我用的是mac系统。    
主要环节有：安装Ruby，安装RubyGems，安装jekyll，安装代码高亮插件，安装node.js

### 安装Ruby

```
直接使用  brew install ruby  
```

### 用RubyGems安装Jekyll

执行下面的语句安装   
```
sudo gem update —system
sudo gem install jekyll
```
至此jekyll就已经安装完毕了，后续就是个性化的自己设定了。

### 创建博客
``` 
执行jekyll new name创建新的工作区   
```

文件结构如下：   
```
.   
|--_config.yml>  
|--_drafts  
    |--articles1.textile 
    |--articles2.md
|--_includes
    |--footer.html
    |--header.html
|--_layouts
    |--default.html
    |--post.html
|--_posts
    |--2014-06-17-articles1.textile
    |--2014-06-17-articles1.md
|--_site
|--index.html
|--other files
```

- _config.yml：保存配置数据。
- _drafts：存放未发布的文章。
- _includes：存放页面片段，即页头（head.html）、页脚（footer.html）、导航（navigation.html）、评论（disquscomments.html）等，这些资源通过标签添加到index.html中，从而形成一个完整的页面。
- _layouts：存放模板文件。文章模板、关于页面模板、首页模板等。
- _posts：存放文章的文件。并且文章文件名称要符合YEAR-MONTH-DAY-title.MARKUP格式。
- _site：经过jekyll转换的页面。
- index.html：网站首页。
- other files：其他文件，存放css、js、image等。

开启服务器   
```
jekyll serve 
```

watch为了检测文件夹内的变化，即修改后不需要重新启动jekyll
```
访问 http://localhost:4000/   
```

## 参考文档
```
http://www.devtalking.com/articles/git-gitHub-markdown-jekyll/
http://www.jianshu.com/p/88c9e72978b4

http://cenalulu.github.io/jekyll/choose-a-template-for-your-blog/#toc1

https://mademistakes.com/work/jekyll-themes/

https://github.com/cenalulu/cenalulu.github.io/blob/master/index.html

https://github.com/sunxiaobiu/sunxiaobiu.github.io

http://sunxiaobiu.github.io/

https://gaohaoyang.github.io/

https://dailc.github.io/blog/archive.html
```
- 官方网站看这个

```
http://jekyllcn.com/docs/
```
- 我的博客参考
```
https://whydejavu.github.io/
```

## 问题记录及相关命令
### 命令
- 安装失败删除重新安装
```
gem uninstall jekyll & gem install jekyll
```