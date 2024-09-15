---
title: Butterfly 主題页面(二) 
categories:
  - Flask
tags:
  - 日志
cover: >-
  https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F03%2Fcd-11d078.jpg
abbrlink: 10709
date: 2024-03-19 13:27:55
---

# Butterfly 主題页面(二) 

## Front-matter

**Front-matter 是 markdown 文件最上方以 `---` 分隔的区域，用于指定個別档案的变数。**

- Page Front-matter 用于`页面`配置
- Post Front-matter 用于`文章页`配置

>  如果标注`可选`的参数，可根据自己需要添加，不用全部都写在 markdown 里

### Page Front-matter

```
---
title:
date:
updated:
type:
comments:
description:
keywords:
top_img:
mathjax:
katex:
aside:
aplayer:
highlight_shrink:
random:
---
```

| 寫法             | 解释                                                         |
| ---------------- | ------------------------------------------------------------ |
| title            | 【必需】页面标题                                             |
| date             | 【必需】页面创建日期                                         |
| type             | 【必需】标签、分类和友情链接三个页面需要配置                 |
| updated          | 【可选】页面更新日期                                         |
| description      | 【可选】页面描述                                             |
| keywords         | 【可选】页面关键字                                           |
| comments         | 【可选】显示页面评论模块 (确认 true)                         |
| top_img          | 【可选】页面顶部图片                                         |
| mathjax          | 【可选】显示mathjax (当设置mathjax的per_page: false時，才需要配置，确认 false) |
| katex            | 【可选】显示katex (当设置katex的per_page: false時，才需要配置，确认 false) |
| aside            | 【可选】显示侧边栏 (确认 true)                               |
| aplayer          | 【可选】在需要的页面加载aplayer的js和css,请参考文章下面的`音樂` 配置 |
| highlight_shrink | 【可选】配置代码框是否展開 (true/false) (确认为设置中highlight_shrink的配置) |
| random           | 【可选】配置友情链接是否随机排序（确认为 false)              |

### Post Front-matter

```
---
title:
date:
updated:
tags:
categories:
keywords:
description:
top_img:
comments:
cover:
toc:
toc_number:
toc_style_simple:
copyright:
copyright_author:
copyright_author_href:
copyright_url:
copyright_info:
mathjax:
katex:
aplayer:
highlight_shrink:
aside:
abcjs:
---
```

| 寫法                  | 解释                                                         |
| --------------------- | ------------------------------------------------------------ |
| title                 | 【必需】文章标题                                             |
| date                  | 【必需】文章创建日期                                         |
| updated               | 【可选】文章更新日期                                         |
| tags                  | 【可选】文章标签                                             |
| categories            | 【可选】文章分类                                             |
| keywords              | 【可选】文章关键字                                           |
| description           | 【可选】文章描述                                             |
| top_img               | 【可选】文章顶部图片                                         |
| cover                 | 【可选】文章缩略图(如果沒有设置top_img,文章頁顶部將显示缩略图，可设为false/图片地址/留空) |
| comments              | 【可选】显示文章评论模块(确认 true)                          |
| toc                   | 【可选】显示文章TOC(确认为设置中toc的enable配置)             |
| toc_number            | 【可选】显示toc_number(确认为设置中toc的number配置)          |
| toc_style_simple      | 【可选】显示 toc 简洁模式                                    |
| copyright             | 【可选】显示文章版权模块(确认为设置中post_copyright的enable配置) |
| copyright_author      | 【可选】文章版权模块的`文章作者`                             |
| copyright_author_href | 【可选】文章版权模块的`文章作者`链接                         |
| copyright_url         | 【可选】文章版权模块的`文章連結`链接                         |
| copyright_info        | 【可选】文章版权模块的`版权聲明`文字                         |
| mathjax               | 【可选】显示mathjax(当设置 mathjax 的 per_page: false 時，才需要配置，确认 false ) |
| katex                 | 【可选】显示 katex (当设置 katex 的 per_page: false 時，才需要配置，确认 false ) |
| aplayer               | 【可选】在需要的页面加载 aplayer 的 js 和 css,请参考文章下面的`音樂` 配置 |
| highlight_shrink      | 【可选】配置代码框是否展開(true/false)(确认为设置中 highlight_shrink 的配置) |
| aside                 | 【可选】显示侧边栏 (确认 true)                               |
| abcjs                 | 【可选】加载 abcjs (当设置 abcjs 的 per_page: false 時，才需要配置，确认 false ) |

## 标签页

1. 前往你的 Hexo 博客的根目录

2. 輸入 `hexo new page tags`

3. 你会找到 `source/tags/index.md` 这个文件

4. 修改这个文件：

   **记得添加 `type: "tags"`**

```
---
title: 标签
date: 2018-01-05 00:00:00
type: "tags"
orderby: random
order: 1
---
```

| 参数    | 解释                                                         |
| ------- | ------------------------------------------------------------ |
| type    | 【必须】页面类型，必须为 `tags`                              |
| orderby | 【可选】排序方式 ：random/name/length                        |
| order   | 【可选】排序次序： 1, asc for ascending; -1, desc for descending |

## 分类页

1. 前往你的 Hexo 博客的根目录

2. 輸入 `hexo new page categories`

3. 你会找到 `source/categories/index.md` 这个文件

4. 修改这个文件：

   **记得添加 `type: "categories"`**

```
---
title: 分类
date: 2018-01-05 00:00:00
type: "categories"
---
```

## 友情链接

为你的博客创建一個友情链接！

### 创建友情链接页面

1. 前往你的 Hexo 博客的根目录

2. 輸入 `hexo new page link`

3. 你会找到 `source/link/index.md` 这个文件

4. 修改这个文件：

   记得添加 `type: "link"`

```
---
title: 友情链接
date: 2018-06-07 22:17:49
type: "link"
---
```

### 友情链接添加

在Hexo博客目录中的 `source/_data`（如果沒有 _data 文件夹，请自行创建），创建一個文件 `link.yml`

```
- class_name: 友情链接
  class_desc: 那些人，那些事
  link_list:
    - name: Hexo
      link: https://hexo.io/zh-tw/
      avatar: https://d33wubrfki0l68.cloudfront.net/6657ba50e702d84afb32fe846bed54fba1a77add/827ae/logo.svg
      descr: 快速、简单且強大的网络框架

- class_name: 网站
  class_desc: 值得推荐的网站
  link_list:
    - name: Youtube
      link: https://www.youtube.com/
      avatar: https://i.loli.net/2020/05/14/9ZkGg8v3azHJfM1.png
      descr: 视频网站
    - name: Weibo
      link: https://www.weibo.com/
      avatar: https://i.loli.net/2020/05/14/TLJBum386vcnI1P.png
      descr: 中国最大社交分享平台
    - name: Twitter
      link: https://twitter.com/
      avatar: https://i.loli.net/2020/05/14/5VyHPQqR6LWF39a.png
      descr: 社交分享平台
```

`class_name` 和 `class_desc` 支持 html 格式书写，如不需要，也可以留空。

### 友情链接随机排序

主題支持友情链接随机排序，只需要在顶部 `front-matter` 添加 `random: true`

### 友情链接界面设置

由 2.2.0 起，友情链接界面可以由用户自己自定义，只需要在友情链接的md檔设置就行，以普通的Markdown格式书写。

## 图库

图库页面只是普通的页面，你只需要 `hexo n page xxxxx` 创建你的页面就行

然後使用标签外掛 [galleryGroup](https://butterfly.js.org/posts/4aa8abbe/#Gallery相冊图库)，具体用法请查看对应的內容。

```
<div class="gallery-group-main">
{% galleryGroup '壁紙' '收藏的一些壁紙' '/Gallery/wallpaper' https://i.loli.net/2019/11/10/T7Mu8Aod3egmC4Q.png %}
{% galleryGroup '漫威' '关于漫威的图片' '/Gallery/marvel' https://i.loli.net/2019/12/25/8t97aVlp4hgyBGu.jpg %}
{% galleryGroup 'OH MY GIRL' '关于OH MY GIRL的图片' '/Gallery/ohmygirl' https://i.loli.net/2019/12/25/hOqbQ3BIwa6KWpo.jpg %}
</div>
```

### 子页面

子页面也是普通的页面，你只需要 `hexo n page xxxxx` 创建你的页面就行

然後使用标签外掛 [gallery](https://butterfly.js.org/posts/4aa8abbe/#Gallery相冊)，具体用法请查看对应的內容。

```
{% gallery %}
![](https://i.loli.net/2019/12/25/Fze9jchtnyJXMHN.jpg)
![](https://i.loli.net/2019/12/25/ryLVePaqkYm4TEK.jpg)
![](https://i.loli.net/2019/12/25/gEy5Zc1Ai6VuO4N.jpg)
![](https://i.loli.net/2019/12/25/d6QHbytlSYO4FBG.jpg)
![](https://i.loli.net/2019/12/25/6nepIJ1xTgufatZ.jpg)
![](https://i.loli.net/2019/12/25/E7Jvr4eIPwUNmzq.jpg)
![](https://i.loli.net/2019/12/25/mh19anwBSWIkGlH.jpg)
![](https://i.loli.net/2019/12/25/2tu9JC8ewpBFagv.jpg)
{% endgallery %}
```

> 如果你想要使用 `/photo/ohmygirl` 这样的链接显示你的图片內容
>
> 你可以把创建好的 `ohmygirl` 整個文件夹移到 `photo` 文件夹里去

## 404页面

主題內置了一個简单的 404 页面，可在设置中开启

本地预览時，訪問出錯的网站是不会跳到 404 页面的。

如需本地预览，请訪問 `http://localhost:4000/404.html`

```
# A simple 404 page
error_404:
  enable: true
  subtitle: "页面沒有找到"
  background: 
```