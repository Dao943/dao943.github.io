---
title: Hexo 文章写作与发布
top: false
img: 'https://s3.bmp.ovh/imgs/2022/05/21/be5039a5f4f969cb.jpg'
tags: Hexo 文章
categories: Hexo
abbrlink: 2914401165
date: 2022-05-21 22:56:58
password:
keywords:
---
# 前言  

- [Typora](https://typoraio.cn/)
- [Visual Studio Code ](https://code.visualstudio.com/)

- [Markdown 基本语法 ](https://markdown.com.cn/basic-syntax/)

- [Markdown 扩展语法](https://markdown.com.cn/extended-syntax/)

## 第一部分 文章编辑器安装	

### 文章编辑器介绍	

- Typora	

  方便简捷，视觉效果好，编写文章轻松，官方的需要收费但可以另寻出路	

  ![](https://s3.bmp.ovh/imgs/2022/05/21/5ff746df512274ee.png)

- Visual Studio Code

  体积小，视觉效果简便，编写文章一般，微软官方免费	
  
  ![](https://s3.bmp.ovh/imgs/2022/05/21/ef35f4f6c0d0c103.png)

### 下载文章编辑器	

- [Typora （推荐）](https://typoraio.cn/)
- [Visual Studio Code](https://code.visualstudio.com/Download)

## 第二部分 创建文章	

1.Git命令创建	

```text
hexo n "文章名称"
```

2.手动创建

在博客目录\source\_posts文件夹里，右键新建md后缀的文件，例如：文章名称.md

## 第三部分 文章基本语法	

- [Markdown 基本语法](https://markdown.com.cn/basic-syntax/)
- [Markdown 扩展语法](https://markdown.com.cn/extended-syntax/)

## 第四部分 文章 Front-matter

了解Front-matter ，就是文章最上方分隔的区域，以下是定义参数	

| **配置选项**  |         **默认值**         |                           **描述**                           |
| :-----------: | :------------------------: | :----------------------------------------------------------: |
|     title     |    Markdown 的文件标题     |                 文章标题，强烈建议填写此选项                 |
|     date      |    文件创建时的日期时间    |       发布时间，强烈建议填写此选项，且最好保证全局唯一       |
|    author     | 根 _config.yml 中的 author |                           文章作者                           |
|      img      |  featureImages 中的某个值  |                   文章特征图，推荐使用图床                   |
|      top      |            true            | 推荐文章（文章是否置顶），如果 top 值为 true，则会作为首页推荐文章 |
|     cover     |           false            |            表示该文章是否需要加入到首页轮播封面中            |
|   coverImg    |             无             | 表示该文章在首页轮播封面需要显示的图片路径，如果没有，则默认使用文章的特色图片 |
|   password    |             无             | 文章阅读密码，如果要对文章设置阅读验证密码的话，就可以设置 password 的值，该值必须是用 SHA256 加密后的密码，防止被他人识破。前提是在主题的 config.yml 中激活了 verifyPassword 选项 |
|      toc      |            true            | 是否开启 TOC，可以针对某篇文章单独关闭 TOC 的功能。前提是在主题的 config.yml 中激活了 toc 选项 |
|    mathjax    |           false            | 是否开启数学公式支持 ，本文章是否开启 mathjax，且需要在主题的 _config.yml 文件中也需要开启才行 |
|    summary    |             无             | 文章摘要，自定义的文章摘要内容，如果这个属性有值，文章卡片摘要就显示这段文字，否则程序会自动截取文章的部分内容作为摘要 |
|  categories   |             无             | 文章分类，本主题的分类表示宏观上大的分类，只建议一篇文章一个分类 |
|     tags      |             无             |                文章标签，一篇文章可以多个标签                |
| reprintPolicy |           cc_by            | 文章转载规则， 可以是 cc_by, cc_by_nd, cc_by_sa, cc_by_nc, cc_by_nc_nd, cc_by_nc_sa, cc0, noreprint 或 pay 中的一个 |

### 1.清除本地缓存	

```复制
hexo clean
```

### 2.生成静态html文件	

```复制
hexo g
```

### 3.部署到 GitHub	

```复制
hexo d
```

```复制
hexo s #可以在本地查看预览效果 浏览器打开 http://localhost:4000/
```



## 第五部分 结束语	

- 以上就是Hexo写文章与发布文章
