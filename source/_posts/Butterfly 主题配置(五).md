---
title: Butterfly 主题配置(五) 
categories:
  - Flask
tags:
  - 日志
cover: >-
  https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F03%2Fcd-11d078.jpg
abbrlink: 10709
date: 2024-03-19 13:27:55

---

# Butterfly 主题配置(五) 

### 搜索

{% tabs test1 %}
<!-- tab algoliasearch -->

> 记得运行 hexo clean 

> 如果你使用 hexo-algoliasearch，请记得配置 fields 参数的 title, permalink 和 content

1. 你需要安装 hexo-algolia或 hexo-algoliasearch. 根据它们的説明文档去做相应的配置。

2. 修改 `主题配置文件`

```shell
algolia_search:
  enable: true
  hits:
    per_page: 6
```

<!-- endtab -->

<!-- tab 本地搜索 -->

> 记得运行 hexo clean

1. 你需要安装 hexo-generator-searchdb 或者 hexo-generator-search，根据它的文档去做相应配置

2. 修改 `主题配置文件`

```shell
# Local search
local_search:
  enable: false
  # Preload the search data when the page loads.
  preload: false
  # Show top n results per article, show all results by setting to -1
  top_n_per_article: 1
  # Unescape html strings to the readable one.
  unescape: false
  CDN:
```

| 参数              | 解释                                                         |
| ----------------- | ------------------------------------------------------------ |
| enable            | 是否开启本地搜索                                             |
| preload           | 预加载，开启后，进入网页后会自动加载搜索文件。关闭时，只有点击搜索按钮后，才会加载搜索文件 |
| top_n_per_article | 匹配的文章结果，默认显示最开始的 1段结果                     |
| unescape          | 将 html 字符串解码为可读字符串                               |
| CDN               | 搜索文件的 CDN 地址（默认使用的本地链接）                    |

<!-- endtab -->

<!-- tab DocSearch -->

DocSearch 是另一款由 algolia 提供的搜索服务，具体申请和使用请查看 DocSearch 文档

```shell
docsearch:
  enable: false
  appId:
  apiKey:
  indexName:
  option:
```

| 参数      | 解释                                               |
| --------- | -------------------------------------------------- |
| enable    | 【必须】是否开启 docsearch                         |
| appId     | 【必须】你的 Algolia 应用 ID                       |
| apiKey    | 【必须】你的 Algolia 搜索 API key                  |
| indexName | 【必须】你的 Algolia index name                    |
| option    | 【可选】其余的 docsearch 配置<br/>具体配置可查这里 |

![DocSearch](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-docsearch-dcd8ae.png)

<!-- endtab -->
{% endtabs %}

### 分享

> 只能选择一个分享服务商

{% tabs test1 %}
<!-- tab sharejs -->

如果你不知道 sharejs，看看它的説明。

修改 `主题配置文件`

```shell
sharejs:
  enable: true
  sites: facebook,twitter,wechat,weibo,qq  #想要显示的内容
```

<!-- endtab -->

<!-- tab addtoany -->

可以到addtoany查看使用説明

```shell
addtoany:
  enable: true
  item: facebook,twitter,wechat,sina_weibo,facebook_messenger,email,copy_link
```

<!-- endtab -->
{% endtabs %}

### 分析统计

{% tabs test1 %}
<!-- tab 百度统计 -->

1. 登录百度统计的官方网站
2. 找到你百度统计的统计代码

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-baidu-tongji-1dcdce.jpeg)

3. 修改 主题配置文件

```shell
baidu_analytics: 你的代码
```

<!-- endtab -->

<!-- tab 谷歌分析 -->

1. 登录百度统计的官方网站
2. 找到你百度统计的统计代码

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-google-analytics-eb178c.jpeg)

```shell
google_analytics: 你的代码 # 通常以`UA-`打头
```

<!-- endtab -->

<!-- tab Cloudflare -->

1. 登录 Cloudflare 分析的官方网站
2. 找到 JavaScript 程式码片段
3. 找到你的 token

![image-20201230195158742](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-cloudflare-analytics-id-a71900.png)

4. 修改 主题配置文件

```shell
# Cloudflare Analytics
# https://www.cloudflare.com/zh-tw/web-analytics/
cloudflare_analytics:
```

<!-- endtab -->

{% endtabs %}

### 网站验证

如果需要搜索引擎收录网站，可能需要登录对应搜索引擎的管理平台进行提交。
各自的验证码可从各自管理平台拿到

修改 `主题配置文件`

```shell
site_verification:
  # - name: google-site-verification
  #   content: xxxxxx
  # - name: baidu-site-verification
  #   content: xxxxxxx
```

### 美化/特效

#### 自定义主题色

可以修改大部分UI颜色

修改 主题配置文件，比如：

> 颜色值必须被双引号包裹，就像"#000"而不是#000。否则将会在构建的时候报错！

```shell
theme_color:
  enable: true
  main: "#49B1F5"
  paginator: "#00c4b6"
  button_hover: "#FF7242"
  text_selection: "#00c4b6"
  link_color: "#99a9bf"
  meta_color: "#858585"
  hr_color: "#A4D8FA"
  code_foreground: "#F47466"
  code_background: "rgba(27, 31, 35, .05)"
  toc_color: "#00c4b6"
  blockquote_padding_color: "#49b1f5"
  blockquote_background_color: "#49b1f5"
  scrollbar_color: "#49b1f5"
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-color_1-db763c.png)

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-color_2-ce6242.png)

#### 主页top_img显示大小

默认的显示为全屏。site-info的区域会居中显示

```shell
# 主页设置
# 默认top_img全屏，site_info在中间
# 使用默认, 都无需填写（建议默认）
index_site_info_top: # 主页标题距离顶部距离  例如 300px/300em/300rem/10%
index_top_img_height:  #主页top_img高度 例如 300px/300em/300rem  不能使用百分比
```

注意：index_top_img_height的值不能使用百分比。
2个都不填的话，会使用默认值

```shell
index_top_img_height: 400px
```

效果

![img](https://jsd.012700.xyz/gh/jerryc127/CDN/img/hexo-theme-butterfly-doc-index-top-img-setting.png)

#### 文字左右对齊

可设置文字向两侧对齊，对最后一行无效

```shell
# Stretches the lines so that each line has equal width（文字向两侧对齊，对最后一行无效）
text_align_justify: true
```

> text_align_justify: false

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Ftext-align-justify-false-12739c.png)

> text_align_justify: true

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Ftext-align-justify-true-62cfe4.png)

#### 网站背景

默认显示白色，可设置图片或者颜色

修改 `主题配置文件`

```shell
# 图片格式 url(http://xxxxxx.com/xxx.jpg)
# 颜色（HEX值/RGB值/顔色单词/渐变色)
# 留空 不显示背景
background:
```

留意: 如果你的网站根目录不是'/',使用本地图片时，需加上你的根目录。
例如：网站是 https://yoursite.com/blog,引用一张img/xx.png图片，则设置background为 `url(/blog/img/xx.png)

> background:'#49B202'

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-set-body-background-color-8b4fe8.png)

> background: url(https://i.loli.net/2019/09/09/5oDRkWVKctx2b6A.png)

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-set-body-background-img-c7f555.png)

#### footer 背景

修改 `主题配置文件`

```shell
# footer是否显示图片背景(与top_img一致)
footer_bg: true
```

| 配置的值                                                     | 效果                         |
| ------------------------------------------------------------ | ---------------------------- |
| 留空/false                                                   | 显示默认的顔色               |
| img链接                                                      | 图片的链接，显示所配置的图片 |
| 顔色(<br/>HEX值 - #0000FF<br/>RGB值 - rgb(0,0,255)<br/>顔色单词 - orange<br/>渐变色 - linear-gradient( 135deg, #E2B0FF 10%, #9F44D3 100%)<br/>） | 对应的顔色                   |
| true                                                         | 显示跟 top_img 一样          |

> true

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-footer-img-533c3b.png)

#### 背景特效

{% tabs test1 %}
<!-- tab 静止彩带 -->

好看的綵带背景，可设置每次刷新更换彩带，或者每次点击更换彩带
修改 `主题配置文件`

```shell
canvas_ribbon:
  enable: false
  size: 150
  alpha: 0.6
  zIndex: -1
  click_to_change: false  #设置是否每次点击都更换綵带
  mobile: false # false 手机端不显示 true 手机端显示
```

相关配置可查看canvas_ribbon

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-canvas-ribbon-637c1f.png)

<!-- endtab -->

<!-- tab 动态彩带 -->

好看的綵带背景，会飘动
修改 `主题配置文件`

```shell
canvas_fluttering_ribbon:
  enable: true
  mobile: false # false 手机端不显示 true 手机端显示
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-canvas-ribbon-piao-bd105a.gif)****

<!-- endtab -->

<!-- tab canvas-nest -->
修改 `主题配置文件`

```shell
canvas_nest:
  enable: true
  color: '0,0,255' #color of lines, default: '0,0,0'; RGB values: (R,G,B).(note: use ',' to separate.)
  opacity: 0.7 # the opacity of line (0~1), default: 0.5.
  zIndex: -1 # z-index property of the background, default: -1.
  count: 99 # the number of lines, default: 99.
  mobile: false # false 手机端不显示 true 手机端显示
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-canvas_nest-40b815.gif)

<!-- endtab -->

{% endtabs %}

#### 自定义字体和字体大小

##### 全局字体

可自行设置字体的font-family
如不需要配置，请留空

修改 `主题配置文件`

```shell
# Global font settings
# Don't modify the following settings unless you know how they work (非必要不要修改)
font:
  global-font-size:
  code-font-size:
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Helvetica Neue", Lato, Roboto, "PingFang SC", "Microsoft JhengHei", "Microsoft YaHei", sans-serif
  code-font-family: consolas, Menlo, "PingFang SC", "Microsoft JhengHei", "Microsoft YaHei", sans-serif
```

##### Blog 标题字体

可自行设置字体的font-family
如不需要配置，请留空。
如不需要使用网络字体，只需要把font_link留空就行

修改 `主题配置文件`

```shell
# Font settings for the site title and site subtitle
# 左上角网站名字 主页居中网站名字
blog_title_font:
  font_link: https://fonts.googleapis.com/css?family=Titillium+Web&display=swap
  font-family: Titillium Web, 'PingFang SC', 'Hiragino Sans GB', 'Microsoft JhengHei', 'Microsoft YaHei', sans-serif
```

##### 网站副标题

可设置主页中显示的网站副标题或者喜欢的座右铭。

修改 `主题配置文件`

```shell
# 主页subtitle
subtitle:
  enable: false
  # Typewriter Effect (打字效果)
  effect: true
  startDelay: 300 # time before typing starts in milliseconds
  typeSpeed: 150 # type speed in milliseconds
  backSpeed: 50 # backspacing speed in milliseconds
  # loop (循环打字)
  loop: true
  # source 调用第三方服务
  # source: false 关闭调用
  # source: 1  调用一言网的一句话（简体） https://hitokoto.cn/
  # source: 2  调用一句网（简体） http://yijuzhan.com/
  # source: 3  调用今日诗词（简体） https://www.jinrishici.com/
  # subtitle 会先显示 source , 再显示 sub 的内容
  source: false
  # 如果关闭打字效果，subtitle 只会显示 sub 的第一行文字
  sub:
    - 今日事&#44;今日毕
    - Never put off till tomorrow what you can do today
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-index-subtitle-a2197a.gif)

##### 页面加载动画 preloader

当进入网页时，因为加载速度的问题，可能会导致 top_img 图片出现断层显示，或者网页加载不全而出现等待时间，开启preloader后，会显示加载动画，等页面加载完，加载动画会消失。

主题支持 pace.js 的加载动画，具体可查看 pace.js

配置 `butterly.yml`

```shell
# 加载动画 Loading Animation
preloader:
  enable: false
  # source
  # 1. fullpage-loading
  # 2. pace (progress bar)
  source: 1
  # pace theme (see https://codebyzach.github.io/pace/)
  pace_css_url:
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-preloader-f63c0f.gif)

### 字数统计

要为Butterfly配上字数统计特性, 你需要如下几个步骤:

1. 打开 hexo 工作目录

2. `npm install hexo-wordcount --save` or `yarn add hexo-wordcount`

3. 修改 `主题配置文件`:

```shell
wordcount:
  enable: true
  post_wordcount: true
  min2read: true
  total_wordcount: true
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-word-count-80891b.png)

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-wordcount-totalcount-690ba1.png)

### 图片大图查看模式

{% tabs test1 %}
<!-- tab 注意 -->

如果你并不想为某张图片添加大图查看模式，你可以使用 html 格式引用图片，併为图片添加 no-lightbox class 名。

<!-- endtab -->

<!-- tab 静止彩带 -->

修改 `主题配置文件`

```shell
# fancybox http://fancyapps.com/fancybox/3/
fancybox: true
```

![fancybox.gif](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Ffancybox-9aa32f.gif)

<!-- endtab -->

<!-- tab medium_zoom -->

修改 `主题配置文件`

```shell
medium_zoom: true
```

![medium_zoom.gif](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fmedium_zoom-773609.gif)

<!-- endtab -->

{% endtabs %}



### Instantpage

当鼠标悬停到链接上超过 65 毫秒时，Instantpage 会对该链接进行预加载，可以提升访问速度。

修改`配置文件`

```shell
# https://instant.page/
# prefetch (预加载)
instantpage: true
```

