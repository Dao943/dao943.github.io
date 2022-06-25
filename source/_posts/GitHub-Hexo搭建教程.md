---
title: GitHub+Hexo 搭建教程
top: false
img: 'https://s3.bmp.ovh/imgs/2022/05/21/5affe48047373b22.jpg'
tags: GitHub+Hexo
categories: Hexo
abbrlink: 1759927173
date: 2022-05-21 14:50:04
password:
keywords:
---
# 前言  
- [Hexo 简介](https://hexo.io/zh-cn/docs/)    
- [GitHub 简介](https://baike.baidu.com/item/github/10145341)     
- [Visual Studio Code 简介](https://code.visualstudio.com/docs)    

## 第一部分 安装必要工具

### 1.安装 Git   
- [安装教程](https://blog.csdn.net/weixin_50094173/article/details/124846799)
- 下载地址  
[Git 官网](https://git-scm.com/)    
[国内镜像](https://registry.npmmirror.com/binary.html?path=git-for-windows/)    

### 2.安装 Node.js   
- [安装教程](https://blog.csdn.net/chanyeolchichi/article/details/121348541)    
- 下载地址  
[Node.js 官网](http://nodejs.cn/)  

### 3.安装淘宝镜像   
以管理员运行CMD     
1.安装淘宝镜像   
```复制
npm install -g cnpm --registry=https://registry.npm.taobao.org
```
2.安装模块  
```复制 
cnpm install [name]
```

### 4.安装Visual Studio Code  
- 下载地址  
[Visual Studio Code 官网](https://code.visualstudio.com/Download)

## 第二部分 安装 Hexo

### 4.安装 Hexo  
创建一个存放博客文件夹（不要中文和特殊符号），然后cd到这个文件夹下（或者在这个文件夹下直接右键git bash打开）。  
1.安装 Hexo    
```复制
npm install -g hexo-cli
```
2.初始化 Hexo   
```复制
hexo init myblog
```
3.最后安装  
```复制
cd myblog
npm install
```
4.打开博客文件夹，会有以下文件  
- node_modules: 依赖包  
- public：存放生成的页面  
- scaffolds：生成文章的一些模板  
- source：用来存放你的文章  
- themes：主题  
- _config.yml: 博客的配置文件   

5.本地运行博客  
1.输入以下命令  
```复制
hexo g
hexo server
```
2.浏览器输入以下网址查看本地生成的博客  
```复制
localhost:4000
```
如下图：    

![](https://s3.bmp.ovh/imgs/2022/05/21/1fe7821357497f56.png)   

## 第三部分 配置 GitHub  

### 1.注册 GitHub账户    
注册教程请百度  

### 2.创建 GitHub仓库    
1.创建一个和你用户名相同的仓库，后面加.github.io，只有这样，将来要部署到GitHub page的时候，才会被识别，也就是xxxx.github.io，其中xxx就是你注册GitHub的用户名 

![](https://s3.bmp.ovh/imgs/2022/05/21/242f9d24caae82e3.png)   

2.博客文件夹右键运行 Git bash        
```复制
git config --global user.name "你GitHub用户名"
git config --global user.email "你GitHub邮箱"
````
3.运行以下命令检查用户名和邮箱是否正确  
```复制
git config user.name
git config user.email
```
4.创建SSH,一路回车  
```复制
ssh-keygen -t rsa -C "youremail"
```
完成后密钥生成在C:用户/你的电脑用户名/.ssh的文件夹里.   

5.ssh，简单来讲，就是一个秘钥，其中，id_rsa是你这台电脑的私人秘钥，不能给别人看的，id_rsa.pub是公共秘钥，可以随便给别人看。把这个公钥放在GitHub上，这样当你链接GitHub自己的账户时，它就会根据公钥匹配你的私钥，当能够相互匹配时，才能够顺利的通过git上传你的文件到GitHub上。

![](https://s3.bmp.ovh/imgs/2022/05/21/4386ae20f329e3bb.png)

6.而后在GitHub的setting中，找到SSH keys的设置选项，点击New SSH key
把你的id_rsa.pub里面的信息复制进去。    

![](https://s3.bmp.ovh/imgs/2022/05/21/e95cd73216b7e967.png)    

![](https://s3.bmp.ovh/imgs/2022/05/21/0487364fbb29f8a3.png)    

7.返回Git bash中，查看是否成功  
```复制
ssh -T git@github.com
```

## 第四部分 部署到 GitHub   
1.配置站点文件_config.yml   
```复制
deploy:
  type: git
  repo: https://github.com/你的账户名称/你的账户名称.github.io.git
  branch: master
```
2.安装deploy-git    
```复制
npm install hexo-deployer-git --save
```
3.最后推送到GitHub  
```复制
hexo clean
hexo generate
hexo deploy
```
命令最后显示下面英文就说明推送成功，几分钟后浏览器访问 http://你的用户名.github.io 就可以看见自己做的博客了    
```复制
INFO Deploy done：git
```
## 第五部分 搭建结束语 
到这里所有搭建就完成了，其他更换主题、优化博客、写文章、发布文章，等等教程都在作者博客Hexo分类里，欢迎前来学习！