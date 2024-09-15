---
title: Butterfly 安裝(一)
categories:
  - Flask
tags:
  - web
  - 计算机
cover: >-
  https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F03%2F000_0-8c7898.jpeg
abbrlink: 23928
---
# Butterfly 安裝(一)

在你的 Hexo 根目录里

```
git clone https://github.com/jerryc127/hexo-theme-butterfly.git 
```

升級方法：在主題目录下，運行 `git pull`

## 應用主題

修改 Hexo 根目录下的 `_config.yml`，把主題改为 `butterfly`

```
theme: hexo-theme-butterfly
```

## 安裝插件

如果你沒有 pug 以及 stylus 的渲染器，请下载安裝：

> 一个错误：
>
> **Hexo启动页面显示extends includes/layout.pug block content include includes/recent-posts.pug include**
>
> Hexo更改主题后启动服务器，界面显如下字符:
>
> extends includes/layout.pug block content include includes/recent-posts.pug include includes/partial
>
> 解决方案:
>
> ```shell
> npm install --save hexo-renderer-jade hexo-generator-feed hexo-generator-sitemap hexo-browsersync hexo-generator-archive
> 
> 清除缓存
> hexo clean
> 
> 生成静态文件即可
> hexo g
> ```
>
> ![在这里插入图片描述](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fe3e1e2cc85571c4de776648c3873ea20-5b26e1.png)

```
npm install hexo-renderer-pug hexo-renderer-stylus --save
```

在 hexo 的根目錄創建一個文件 `_config.butterfly.yml`，並把**主題**目錄的 `_config.yml` **內容**复制到 `_config.butterfly.yml` 去。( **注意: 复制的是主題的 `_config.yml` ，而不是 hexo 的 `_config.yml`**)

> **注意：** 不要把主題目錄的 `_config.yml` 刪掉

> **注意：** 以後只需要在 `_config.butterfly.yml` 進行配置就行。
> 如果使用了 `_config.butterfly.yml`， 配置主題的 `_config.yml` 將不會有效果。

Hexo会自动合并主題中的 `_config.yml` 和 `_config.butterfly.yml` 里的配置，如果存在同名配置，会使用 `_config.butterfly.yml` 的配置，其优先度较高。

