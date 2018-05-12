Hexo-Theme-Freemind.386
===

![screenshot](http://7xofqj.com1.z0.glb.clouddn.com/free386screenshot.png)

Freemind.386 aims at fully taking advantages of Bootstrap.

* [Demo](http://blackshow.me)
* [Readme in Chinese](http://www.blackshow.me/2015/11/25/hexo-theme-freemind-386-readme-cn/)

## Requirements ##

* Hexo >= 3.0
* [hexo-tag-bootstrap](https://github.com/wzpan/hexo-tag-bootstrap) >= 0.0.8 (optional)
## Features ##

* **Bootstrap** - get the power of Twitter Bootstrap with minimal hassle;
* **Tag plugins** - luxuriant Bootstrap tag plugins, provided by [hexo-tag-bootstrap](https://github.com/wzpan/hexo-tag-bootstrap), including:
  - textcolor - a paragraph of text with specified color;
  - button - a button with target links, text and specified color;
  - label - a label with text and specified color;
  - badge - a badge with text;
  - alert - alert messages with text and specified color; 
* **Local Search Engine** - a build-in local search engine, with the help of [hexo-generator-search](https://github.com/paichyperiondev/hexo-generator-search).

## Install ##

1) install theme:

``` sh
$ git clone git@github.com:blackshow/hexo-theme-freemind.386.git
```

2) install [hexo-tag-bootstrap](https://github.com/wzpan/hexo-tag-bootstrap) (*optional*):

``` sh
$ npm install hexo-tag-bootstrap --save
```

3) install [hexo-generator-search](https://github.com/paichyperiondev/hexo-generator-search) (*optional*):

``` sh
$ npm install hexo-generator-search --save
```

4) Create pages

Freemind.386 offers you the customized Categories, Tags and About pages. But you need to manually create these page at your 'source' folder.

For example, to create a `Categories` page, you may create a `index.html` file at `source/categories/` folder with the following contents:

```
title: Categories
layout: categories
---
```

Tags and About pages are created in a similar way, except that the layouts are `tags` and `page` respectively.

Alternatively you can create About page using the following command:

``` sh
$ hexo new page about
```

Note that only About page can be created in that way.

## Enable ##

Modify `theme` setting in your `_config.yml` to `freemind.386`.

## Update ##

``` sh
$ cd themes/freemind.386
$ git pull
```

## Configuration ##

```
slogan: Yet another bootstrap theme.

menu:
  - title: Archives
    url: archives
    intro: All the articles.
    icon: fa fa-archive
  - title: Categories
    url: categories
    intro: All the categories.
    icon: fa fa-folder
  - title: Tags
    url: tags
    intro: All the tags.
    icon: fa fa-tags
  - title: About
    url: about
    intro: About me.
    icon: fa fa-user

links:
  - title: My Github
    url: http://www.github.com/blackshow
    intro: My Github account.
    icon: fa fa-github
  - title: My LinkedIn
    url: http://www.linkedin.com/in/blackshow
    intro: My Linkin account.
    icon: fa fa-linkedin

widgets:
- search
- category
- tagcloud
- recent_posts
- links

rss: atom.xml
favicon: favicon.png
fancybox: true
duoshuo_shortname:

# analytics
google_analytics:
  enable: false
  siteid:
baidu_tongji:
  enable: false
  siteid:

# Search
swiftype_key: 
```

* **slogan** - slogan display at the index page
* **menu** - Navigation menu
* **links** - reference links at the links widget
* **widgets** - Widgets displaying in sidebar
* **rss** - RSS link
* **fancybox** - Enable [Fancybox](http://fancyapps.com/fancybox/)
* **duoshuo_shortname** - DuoShuo ID, if you prefer to use duoshuo instead of Disqus
* **analytics** - Analytics ID. Supports both Google Analytics and Baidu Tongji.
* **swiftype_key** - Swifttype key to enable local searching. Leave it blank or comment this line if you want to use build-in local search engine.

If you prefer to use disqus, the setting of disqus should be placed at your **root** `_config.yml`:

```
# Disqus
disqus_shortname:
```

## Front-Matter ##

There are some new front-matter settings in Freemind.386 that you can use to decorate your articles.

* **description** - a short description about the articles that will be display at the top of the post
* **feature** - sets a feature image that will be show at the index page
* **toc** - renders a table of contents

For example:

```
title: Tag Plugins
date: 2014-03-16 10:17:16
tags: plugins
categories: Docs
description: Introduce tag plugins in freemind.
feature: images/tag-plugins/plugins.jpg
toc: true
---
```

## Init Hexo
1. 创建博客项目目录
```
mkdir blog
```

2. 初始化 hexo
```
cd blog

# 安装 hexo
npm install hexo-cli g
npm install hexo -g

# 初始化 hexo
hexo init

# 安装 hexo 的扩展插件
npm install

# 安装其它插件
npm install hexo-server --save
npm install hexo-admin --save
npm install hexo-generator-archive --save
npm install hexo-generator-feed --save
npm install hexo-generator-search --save
npm install hexo-generator-tag --save
npm install hexo-deployer-git --save
npm install hexo-generator-sitemap --save
```

3. 测试运行
```
# 生成静态文件
hexo g
# 开启 hexo 服务器
hexo s
```

## Theme Install
1. clone 该主题到本地
```
git clone git@github.com:windcode/hexo-theme-freemind.386.git
```

2. copy 项目到 hexo 博客项目的 theme 目录下

3. 修改 hexo 博客项目的 _config.yml 文件中默认的 theme
```
# Extensions
## Plugins: https://hexo.io/plugins/
## Themes: https://hexo.io/themes/
theme: hexo-theme-freemind.386
```

## How deploy
1. 修改 hexo 项目根目录下的 _config.yml 文件

2. 修改 Deployment 这一项，配置你的 github.io 仓库地址
```
# Deployment
## Docs: https://hexo.io/docs/deployment.html

deploy:
- type: git
  repo: https://github.com/username/username.github.io
```

## Publish post
1. 安装 hexo-admin
```
npm install hexo-admin --save
```

2. 在博客目录中启动 hexo 服务
```
hexo s
```

3. 访问 ```localhost:4000/admin```，添加新文章

4. 自动部署到 github
```
hexo g
hexo d
```

## License ##

This theme is provided under [MIT License](http://opensource.org/licenses/MIT).


## Credits ##

* The theme is built based on [Freemind](http://wzpan.github.io/hexo-theme-freemind/) and [BOOTSTRA.386](http://kristopolous.github.io/BOOTSTRA.386/);
* The beautiful icons are from [Font Awesome](http://fortawesome.github.io/Font-Awesome/icons/).

## Reference
* hexo的安装和主题的替换  
https://blog.csdn.net/y_z_w123/article/details/78801096

* hexo 自动部署到 github  
https://hexo.io/zh-cn/docs/deployment.html

* Hexo如何在线可视化写博客？ - lazyboy的回答 - 知乎  
https://www.zhihu.com/question/27384681/answer/139234890

* github怎么绑定自己的域名？ - 知乎  
https://www.zhihu.com/question/31377141
