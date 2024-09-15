---
title: Butterfly 主题配置(三) 
categories:
  - Flask
tags:
  - 日志
cover: >-
  https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F03%2Fcd-11d078.jpg
abbrlink: 10709
date: 2024-03-19 13:27:55
---
# Butterfly 主题配置(三) 

## 语言

修改站点配置文件 `_config.yml`

默认語言是 en

主题支持三种語言

- default(en)
- zh-CN (简体中文)
- zh-TW (繁体中文)

## 网站资料

修改网站各种资料，例如标题、副标题和邮箱等个人资料，请修改博客根目录的_config.yml

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2F20191120000444-185238.png)

### 导航栏设置 (Navigation bar settings)

#### 参数设置

主题配置文件中

```shell
nav:
  logo: #image
  display_title: true
  fixed: false # fixed navigation bar
```

| 参数          | 解释                                    |
| ------------- | --------------------------------------- |
| logo          | 网站的 logo，支持图片，直接填入图片链接 |
| display_title | 是否显示网站标题，填写 true 或者 false  |
| fixed         | 是否固定狀态栏，填写 true 或者 false    |

#### 菜单/目录

修改`主题配置文件`

```shell
Home: / || fas fa-home
Archives: /archives/ || fas fa-archive
Tags: /tags/ || fas fa-tags
Categories: /categories/ || fas fa-folder-open
List||fas fa-list:
  Music: /music/ || fas fa-music
  Movie: /movies/ || fas fa-video
Link: /link/ || fas fa-link
About: /about/ || fas fa-heart
```

必须是 `/xxx/`，后面`||`分开，然后写图标名。

如果不希望显示图标，图标名可不写。

默认子目录是展开的，如果你想要隐藏，在子目录里添加 hide 。

```shell
List||fas fa-list||hide:
  Music: /music/ || fas fa-music
  Movie: /movies/ || fas fa-video
```

注意： 导航的文字可自行更改

例如：

```shell
menu:
  首页: / || fas fa-home
  时间轴: /archives/ || fas fa-archive
  标签: /tags/ || fas fa-tags
  分类: /categories/ || fas fa-folder-open
  清单||fa fa-heartbeat:
    音乐: /music/ || fas fa-music
    照片: /Gallery/ || fas fa-images
    电影: /movies/ || fas fa-video
  友链: /link/ || fas fa-link
  关于: /about/ || fas fa-heart
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-menu-c914db.png)

### 代码 (Code Blocks)

> 代码块中的所有功能只适用于 Hexo 自帶的代码渲染
>
> 如果使用第三方的渲染器，不一定会有效

- Butterfly 支持6种代码高亮樣式：
  - `darker`
  - `pale night`
  - `light`
  - `ocean`
  - `mac`
  - `mac light`

修改 主题配置文件

```shell
highlight_theme: light
```

> - darker
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-code-darker-188e05.png)
>
> - pale night
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-code-pale-night-6b75a2.png)
>
> - light
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-code-light-44a831.png)
>
> - ocean
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-highlight-ocean-da54f0.png)
>
> - mac
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-highlight-mac-f62cb8.png)
>
> - mac light
>
> ![image-20200731175026827](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-mac-light-5fcfad.png)

#### 代码复制

主题支持代码复制功能

修改 `主题配置文件`

```shell
highlight_copy: true
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-code-copy-8562b8.png)

#### 代码框展开/开关

在默认情况下，代码框自动展开，可设置是否所有代码框都开关狀态，点击 `>` 可展开代码

- true 全部代码框不展开，需点击 `>` 打开
- false 代码框展开，有 `>` 点击按钮
- none 不显示 `>` 按钮

修改 `主题配置文件`

```shell
highlight_shrink: true #代码框不展开，需点击 '>' 打开
```

> 你也可以在post/page页对应的markdown文件 `front-matter` 添加`highlight_shrink` 来读立配置。
>
> 当主题配置文件中的 `highlight_shrink` 设为true时，可在`front-matter`添加`highlight_shrink: false`来单读配置文章展开代码框。
>
> 当主题配置文件中的 `highlight_shrink` 设为false时，可在`front-matter`添加`highlight_shrink: true`来单读配置文章收缩代码框。
>

> - highlight_shrink: true
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-highlight-shrink-true-f36dab.png)
>
> - highlight_shrink: false
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-highlight-shrink-false-7abb2d.png)
>
> - highlight_shrink: none
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-highlight-shirk-none-f66b39.png)

#### 代码换行

在默认情况下，Hexo 在编译的时候不会实现代码自动换行。如果你不希望在代码块的区域里有橫向滚动条的话，那么你可以考虑开启这个功能。

修改 `主题配置文件`

```shell
code_word_wrap: true
```

如果你是使用 highlight 渲染，需要找到你站点的 Hexo 配置文件_config.yml，将line_number改成false:

```shell
highlight:
  enable: true
  line_number: false # <- 改这里
  auto_detect: false
  tab_replace:
```

如果你是使用 prismjs 渲染，需要找到你站点的 Hexo 配置文件_config.yml，将line_number改成false:

```shell
prismjs:
  enable: false
  preprocess: true
  line_number: false # <- 改这里
  tab_replace: ''
```

设置code_word_wrap之前:

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-code-word-wrap-before-f5e26c.png)

设置code_word_wrap之后:

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-code-word-wrap-after-a0569a.png)

#### 代码高度限制

3.7.0 及以上支持

可配置代码高度限制，超出的部分会隐藏，并显示展开按钮。

```shell
highlight_height_limit: false # unit: px
```

注意：

1. 单位是 px，直接添加数字，如 200
2. 实际限制高度为 `highlight_height_limit` + 30 px ，多增加 30px 限制，目的是避免代码高度只超出`highlight_height_limit` 一点时，出现展开按钮，展开沒內容。

3. 不适用于隐藏后的代码块（ css 设置 display: none）


![hexo-theme-butterfly-docs-highlight-heigh-limit](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-highlight-heigh-limit-6de8bd.gif)

### 社交图标 (Social Settings)

Butterfly支持 font-awesome v6 图标.

书写格式 图标名：url || 描述性文字 || color

```shell
social:
  fab fa-github: https://github.com/xxxxx || Github || "#hdhfbb"
  fas fa-envelope: mailto:xxxxxx@gmail.com || Email || "#000000"
```

图标名可在这尋找

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-fontawesome-ec4d4b.png)

PC:

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-social-icon-pc-6228d1.png)

Mobile:

![1560603353743](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-socila-icon-mobile-aea91a.png)

### 头像

修改 `主题配置文件`

```shell
avatar:
  img: /img/avatar.png
  effect: true # 头像会一直转圈
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-avatar-acd739.png)

### 顶部图

> - 如果不要显示顶部图，可直接配置 disable_top_img: true
>
> 顶部图的获取顺序，如果都沒有配置，则不显示顶部图。
>
> - 页面顶部图的获取顺序：
>   - 各自配置的 top_img > 配置文件的 default_top_img
>
> - 文章页顶部图的获取顺序：
>   - 各自配置的 top_img > cover > 配置文件的 default_top_img

配置中的值：

| 配置             | 解释                                                         |
| ---------------- | ------------------------------------------------------------ |
| index_img        | 主页的 top_img                                               |
| default_top_img  | 默认的 top_img，当页面的 top_img 沒有配置时，会显示 default_top_img |
| archive_img      | 归档页面的 top_img                                           |
| tag_img          | tag 子页面 的 默认 top_img                                   |
| tag_per_img      | tag 子页面的 top_img，可配置每个 tag 的 top_img              |
| category_img     | category 子页面 的 默认 top_img                              |
| category_per_img | category 子页面的 top_img，可配置每个 category 的 top_img    |


其它页面 （tags/categories/自建页面）和 文章页 的 `top_img` ，请到对应的 md 页面设置`front-matter`中的`top_img`

以上所有的 top_img 可配置以下值

> 3.2.0 以下版本的配置只支持
>
> - 留空，true 和 false - 显示默认的顔色
> - img链接 - 显示所配置的图片

| 配置的值                                                     | 效果                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| 留空                                                         | 显示默认的 top_img（如有），否则显示默认的顔色<br/>（文章页top_img留空的话，会显示 cover 的值） |
| img链接                                                      | 图片的链接，显示所配置的图片                                 |
| 顔色(<br/>HEX值 - #0000FF<br/>RGB值 - rgb(0,0,255)<br/>顔色单詞 - orange<br/>渐变色 - linear-gradient( 135deg, #E2B0FF 10%, #9F44D3 100%)<br/>） | 对应的顔色                                                   |
| transparent                                                  | 透明                                                         |
| false                                                        | 不显示 top_img                                               |

tag_per_img 和 category_per_img 是 3.2.0 新增的內容，可对 tag 和 category 进行单读的配置

并不推荐为每个 tag 和每个 category 都配置不同的顶部图，因为配置太多会拖慢生成速度

```shell
tag_per_img:
  aplayer: https://xxxxxx.png
  android: ddddddd.png
  
category_per_img：
  随想: hdhdh.png
  推荐: ddjdjdjd.png
```

> - top_img: false
>
> ![image-20200924224536013](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Ftheme-butterfly-docs-page-top-img-false-e13478.png)
>
> ![image-20201027210949089](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Ftheme-butterfly-docs-post-top-img-false-new-a6f180.png)
>
> - top_img: orange
>
> ![image-20200924225024153](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Ftheme-butterfly-docs-top-img-orange-e39308.png)
>
> - top_img: 'linear-gradient(20deg, #0062be, #925696, #cc426e, #fb0347)'
>
> ![image-20200924225300934](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Ftheme-butterfly-docs-top-img-color-ad7883.png)

### 文章封面

文章的 markdown 文檔上,在 `Front-matter` 添加 `cover` ,并填上要显示的图片地址。

如果不配置 `cover`,可以设置显示默认的 `cover`。

如果不想在首页显示 `cover`, 可以设置为 `false`。

> 文章封面的获取顺序 Front-matter 的 cover > 配置文件的 default_cover > false

修改 `主题配置文件`

```shell
cover:
  # 是否显示文章封面
  index_enable: true
  aside_enable: true
  archives_enable: true
  # 封面显示的位置
  # 三个值可配置 left , right , both
  position: both
  # 当沒有设置cover时，默认的封面显示
  default_cover: 
```

| 参数            | 解释                                                         |
| --------------- | ------------------------------------------------------------ |
| index_enable    | 主页是否显示文章封面图                                       |
| aside_enable    | 侧栏是否显示文章封面图                                       |
| archives_enable | 归档页面是否显示文章封面图                                   |
| position        | 主页卡片文章封面的显示位置<br/>left：全部显示在左边<br/>right：全部显示在右边<br/>both：封面位置以左右左右轮流显示 |
| default_cover   | 默认的 cover, 可配置图片链接/顔色/渐变色等                   |

当配置多张图片时,会随机选择一张作为cover.此时写法应为

```shell
default_cover:
  - https://jsd.012700.xyz/gh/jerryc127/CDN@latest/cover/default_bg.png
  - https://jsd.012700.xyz/gh/jerryc127/CDN@latest/cover/default_bg2.png
  - https://jsd.012700.xyz/gh/jerryc127/CDN@latest/cover/default_bg3.png
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-post-cover-ad06b7.png)

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-post-cover-show-9a8c78.png)

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-cover-false-b80add.png)

> - left
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-cover-left-cd0c48.png)
>
> - right
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-cover-right-7914d8.png)
>
> - both
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-cover-both-dee8ea.png)

### 页面 meta 显示

这个选项是用来显示文章的相关信息的。

修改 `主题配置文件`

```shell
post_meta:
  page:
    date_type: both # created or updated or both 主页文章日期是创建日或者更新日或都显示
    date_format: relative # date/relative 显示日期还是相对日期
    categories: true # true or false 主页是否显示分类
    tags: true # true or false 主页是否显示标签
    label: true # true or false 显示描述性文字
  post:
    date_type: both # created or updated or both 文章页日期是创建日或者更新日或都显示
    date_format: relative # date/relative 显示日期还是相对日期
    categories: true # true or false 文章页是否显示分类
    tags: true # true or false 文章页是否显示标签
    label: true # true or false 显示描述性文字
```

> - 主页
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-page-meta-78975c.png)
>
> - 文章页
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-post-info-522d36.png)
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-post-tag-cea65e.png)
>
> date_format 是 3.2.0 新增的內容，配置时间显示明确时间还是相对时间
>
> 相对时间
>
> ![image-20200928201701560](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Ftheme-butterfly-docs-relative-time-9fccb5.png)
>
> 明确时间
>
> ![image-20200928201911032](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Ftheme-butterfly-docs-full-date-3061d1.png)

### 主页文章节选(自动节选和文章页description)

因为主题UI的关係，`主页文章节选`只支持`自动节选`和`文章页description`。

在`butterfly`里，有四种可供选择

- description： 只显示description
- both： 优先选择description，如果沒有配置description，则显示自动节选的內容
- auto_excerpt：只显示自动节选
- false： 不显示文章內容

修改 `主题配置文件`

```shell
index_post_content:
  method: 3
  length: 500 # if you set method to 2 or 3, the length need to config
```

description在front-matter里添加

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-post-description-7555d3.png)

### 页面锚点

开启页面锚点后，当你在进行滚动时，页面链接会根据标题ID进行替换
(注意: 每替换一次，会留下一个历史记录。所以如果一篇文章有很多锚点的话，网页的历史记录会很多。)

修改 `主题配置文件`

```shell
# anchor
anchor:
  # when you scroll, the URL will update according to header id.
  auto_update: false
  # Click the headline to scroll and update the anchor
  click_to_scroll: false
```

### 图片描述

可开启图片Figcaption描述文字显示

优先显示图片的 title 属性，然后是 alt 属性

修改 `主题配置文件`

```shell
photofigcaption: true
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-photo-figcaption-512f4f.png)

### 复制相关配置

可配置网站是否可以复制、复制的內容是否添加版权信息

```shell
# copy settings
# copyright: Add the copyright information after copied content (复制的內容后面加上版权信息)
copy:
  enable: true
  copyright:
    enable: true
    limit_count: 50
```

| 配置        | 解释                                                         |
| ----------- | ------------------------------------------------------------ |
| enable      | 是否开启网站复制权限                                         |
| copyright   | 复制的內容后面加上版权信息                                   |
| enable      | 是否开启复制版权信息添加                                     |
| limit_count | 字数限制，当复制文字大于这个字数限制时，将在复制的內容后面加上版权信息 |

添加版权信息后

```shell
Lorem ipsum dolor sit amet, test link consectetur adipiscing elit. Strong text pellentesque ligula commodo viverra vehicula. Italic text at ullamcorper enim. Morbi a euismod nibh. Underline text non elit nisl. Deleted text tristique, sem id condimentum tempus, metus lectus venenatis mauris, sit amet semper lorem felis a eros. Fusce egestas nibh at sagittis auctor. Sed ultricies ac arcu quis molestie. Donec dapibus nunc in nibh egestas, vitae volutpat sem iaculis. Curabitur sem tellus, elementum nec quam id, fermentum laoreet mi. Ut mollis ullamcorper turpis, vitae facilisis velit ultricies sit amet. Etiam laoreet dui odio, id tempus justo tincidunt id. Phasellus scelerisque nunc sed nunc ultricies accumsan.


作者: Jerry
連结: http://localhost:4000/posts/bd3c650b/#Paragraph
来源: Butterfly
著作权归作者所有。商业转载请联络作者获得授权，非商业转载请註明出处。
```

### 文章页相关配置

#### 文章版权

为你的博客文章展示文章版权和许可协议。

修改 `主题配置文件`

```shell
post_copyright:
  enable: true
  decode: false
  author_href:
  license: CC BY-NC-SA 4.0
  license_url: https://creativecommons.org/licenses/by-nc-sa/4.0/
```

由于Hexo 4.1开始，默认对网址进行解码，以至于如果是中文网址，会被解码，可设置decode: true来显示中文网址。

如果有文章（例如：转载文章）不需要显示版权，可以在文章Front-matter单读设置

```shell
copyright: false
```

從3.0.0开始，支持对单读文章设置版权信息，可以在文章Front-matter单读设置

```shell
copyright_author: xxxx
copyright_author_href: https://xxxxxx.com
copyright_url: https://xxxxxx.com
copyright_info: 此文章版权归xxxxx所有，如有转载，请註明来自原作者
```

版权显示截图

![image-20210130161913121](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-post-copyright-abbdc6.png)

#### 文章打赏

在你每篇文章的结尾，可以添加打赏按钮。相关二维码可以自行配置。

对于沒有提供二维码的，可配置一张软件的icon图片，然后在link上添加相应的打赏链接。用户点击图片就会跳转到链接去。

link可以不写，会默认为图片的链接。

修改 `主题配置文件`

```shell
reward:
  enable: true
  text:
  QR_code:
    - img: /img/wechat.jpg
      link:
      text: 微信
    - img: /img/alipay.jpg
      link:
      text: 支付宝
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-post-donate-71f274.png)

#### TOC

在文章页，会有一个目录，用于显示TOC。

修改 `主题配置文件`

```shell
toc:
  post: true
  page: true
  number: true
  expand: false
  style_simple: false # for post
  scroll_percent: true
```

| 属性           | 解释                                          |
| -------------- | --------------------------------------------- |
| post           | 文章页是否显示 TOC                            |
| page           | 普通页面是否显示 TOC                          |
| number         | 是否显示章节数                                |
| expand         | 是否展开 TOC                                  |
| style_simple   | 简洁模式（侧边栏只显示 TOC, 只对文章页有效 ） |
| scroll_percent | 是否显示滚动进度百分比                        |

> - Toc PC
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-toc-pc-new-447897.png)
>
> - Toc Mobile
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-toc-mobile-new-4f8ba1.png)
>
> - style_simple: true
>
> ![image-20201209232104167](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-toc-style-simple-80f749.png)

##### 为特定的文章配置

在你的文章md文件的头部，加入`toc_number` 和`toc`，并配置`true`或者`false`即可。

主题会优先判断文章Markdown的Front-matter是否有配置，如有，则以Front-matter的配置为准。否则，以主题配置文件中的配置为准

#### 相关文章

> 当文章封面设置为 false 时，或者沒有获取到封面配置，相关文章背景将会显示主题色。

相关文章推荐的原理是根据文章tags的比重来推荐

修改 `主题配置文件`

```shell
related_post:
  enable: true
  limit: 6 # 显示推荐文章数目
  date_type: created # or created or updated 文章日期显示创建日或者更新日
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-releatedpost-c82808.png)

#### 文章过期提醒

可设置是否显示文章过期提醒，以更新时间为基准。

```shell
# Displays outdated notice for a post (文章过期提醒)
noticeOutdate:
  enable: true
  style: flat # style: simple/flat
  limit_day: 365 # When will it be shown
  position: top # position: top/bottom
  message_prev: It has been
  message_next: days since the last update, the content of the article may be outdated.
```

- limit_day： 距離更新时间多少天才显示文章过期提醒

- message_prev ： 天数之前的文字

- message_next：天数之后的文字

> - style: flat
>
> ![image-20200731175909296](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butteffly-docs-outdate-flat-bd4c60.png)
>
> - style: simple
>
> ![image-20200731180037968](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-outdated-simple-a77271.png)

#### 文章编辑按钮

在文章标题旁边显示一个编辑按钮，点击会跳转到对应的链接去。

```shell
# Post edit
# Easily browse and edit blog source code online.
post_edit:
  enable: false
  # url: https://github.com/user-name/repo-name/edit/branch-name/subdirectory-name/
  # For example: https://github.com/jerryc127/butterfly.js.org/edit/main/source/
  url:
```

![image-20210130160108360](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-post-edit-f5d09f.png)

![image-20210130160208436](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-post-edit-2-9cc69f.png)

#### 文章分页按钮

当文章封面设置为 false 时，或者沒有获取到封面配置，分页背景将会显示主题色。

可设置分页的逻辑，也可以开关分页显示

```shell
# post_pagination (分页)
# value: 1 || 2 || false
# 1: The 'next post' will link to old post
# 2: The 'next post' will link to new post
# false: disable pagination
post_pagination: false
```

| 参数                   | 解释                 |
| ---------------------- | -------------------- |
| post_pagination: false | 开关分页按钮         |
| post_pagination: 1     | 下一篇显示的是舊文章 |
| post_pagination: 2     | 下一篇显示的是新文章 |

![image-20210130161545100](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-post-pagination-6f36b2.png)

#### Footer 设置

##### 博客年份

since是一个来展示你站点起始时间的选项。它位于页面的最底部。

修改 `主题配置文件`

```shell
footer:
  owner:
    enable: true
    since: 2018
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-since-58e187.png)

##### 页腳自定义文本

custom_text是一个給你用来在页腳自定义文本的选项。通常你可以在这里写声明文本等。支持 HTML。

修改 `主题配置文件`

```shell
custom_text: Hi, welcome to my <a href="https://butterfly.js.org/">blog</a>!
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-footer-text-ffb948.png)

对于部分人需要写 ICP 的，也可以写在 custom_text 里

```shell
custom_text: <a href="icp链接"><img class="icp-icon" src="icp图片"><span>備案號：xxxxxx</span></a>
```

