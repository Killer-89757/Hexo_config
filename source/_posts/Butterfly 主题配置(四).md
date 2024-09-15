---
title: Butterfly 主题配置(四)  
categories:
  - Flask
tags:
  - 日志
cover: >-
  https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F03%2Fcd-11d078.jpg
abbrlink: 10709
date: 2024-03-19 13:27:55
---
# Butterfly 主题配置(四) 

### 侧边栏设置 (aside)

#### 侧边排版

可自行决定哪个项目需要显示，可决定位置，也可以设置不显示侧边栏。

修改 `主題配置文件`

```shell
aside:
  enable: true
  hide: false
  button: true
  mobile: true # display on mobile
  position: right # left or right
  display:
    archive: true
    tag: true
    category: true
  card_author:
    enable: true
    description:
    button:
      enable: true
      icon: fab fa-github
      text: Follow Me
      link: https://github.com/xxxxxx
  card_announcement:
    enable: true
    content: This is my Blog
  card_recent_post:
    enable: true
    limit: 5 # if set 0 will show all
    sort: date # date or updated
    sort_order: # Don't modify the setting unless you know how it works
  card_categories:
    enable: true
    limit: 8 # if set 0 will show all
    expand: none # none/true/false
    sort_order: # Don't modify the setting unless you know how it works
  card_tags:
    enable: true
    limit: 40 # if set 0 will show all
    color: false
    orderby: random # Order of tags, random/name/length
    order: 1 # Sort of order. 1, asc for ascending; -1, desc for descending
    sort_order: # Don't modify the setting unless you know how it works
  card_archives:
    enable: true
    type: monthly # yearly or monthly
    format: MMMM YYYY # eg: YYYY年MM月
    order: -1 # Sort of order. 1, asc for ascending; -1, desc for descending
    limit: 8 # if set 0 will show all
    sort_order: # Don't modify the setting unless you know how it works
  card_webinfo:
    enable: true
    post_count: true
    last_push_date: true
    sort_order: # Don't modify the setting unless you know how it works
  card_post_series:
    enable: true
    orderBy: 'date' # Order by title or date
    order: -1 # Sort of order. 1, asc for ascending; -1, desc for descending
```

> - position: left
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-aside-left-5d49a6.png)
>
> - position: right
>
> ![img](https://jsd.012700.xyz/gh/jerryc127/CDN/img/hexo-theme-butterfly-doc-aside-right.png)
>
> - card_tags color: false
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2F20200426182730-29fdae.png)
>
> - card_tags color: true
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2F20200426183025-2b2d67.png)
>
> - aside button
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-aside-button-e019ec.gif)

#### 访问人数 busuanzi (UV 和 PV)

访问 busuanzi 的官方网站查看更多的介紹。

修改 `主題配置文件`

```shell
busuanzi:
  site_uv: true
  site_pv: true
  page_pv: true
```

> 如果需要修改 busuanzi 的 CDN 链接，可通过 主题配置文件 的 CDN 中的 option 进行修改

```shell
CDN:
  option:
  	busuanzi: xxxxxxxxx
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-busuanzi-site-pv-d62aa8.png)

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-pv-a38dd0.png)

#### 运行时间

网页已运行时间

修改 `主題配置文件`

```shell
runtimeshow:
  enable: true
  publish_date: 6/7/2018 00:00:00  
  ##网页开通时间
  #格式: 月/日/年 时间
  #也可以寫成 年/月/日 时间
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-runtime-7b6ba8.png)

### 最新评论

在侧边栏显示最新评论板块

修改 `主題配置文件`

```shell
# Aside widget - Newest Comments
newest_comments:
  enable: true
  sort_order: # Don't modify the setting unless you know how it works
  limit: 6
  storage: 10 # unit: mins, save data to localStorage
  avatar: true
```

部分配置解释：

| 配置    | 解释                    |
| ------- | ----------------------- |
| limit   | 显示的数量              |
| storage | 设置缓存时间，单位 分钟 |
| avatar  | 是否显示头像            |

> - Demo
>
> ![image-20200830223037320](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-newest-comments-b570ce.png)

### 右下角按鈕 (Bottom right button)

#### 简繁转换

简体繁体互换

右下角会有简繁转换按钮。

修改 主题配置文件

```shell
translate:
  enable: true
  # 默认按钮显示文字(网站是简体，应设置为'default: 繁')
  default: 简
  #网站默认语言，1: 繁体中文, 2: 简体中文
  defaultEncoding: 1
  #延迟时间,若不在前, 要设定延迟翻译时间, 如100表示100ms,默认为0
  translateDelay: 0
  #当文字是简体时，按钮显示的文字
  msgToTraditionalChinese: "繁"
  #当文字是繁体时，按钮显示的文字
  msgToSimplifiedChinese: "简"
```

> - 简体
>
> ![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-simp-8a9222.png)
>
> - 繁体
>
> ![img](https://jsd.012700.xyz/gh/jerryc127/CDN/img/hexo-theme-butterfly-doc-tranditional.png)

#### 阅读模式

阅读模式下会去掉除文章外的内容，避免干扰阅读。

只会出现在文章页面，右下角会有阅读模式按钮。

修改 `主题配置文件`

```shell
readmode: true
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-read-mode-e02e63.png)

#### 夜间模式

右下角会有夜间模式按钮

修改 `主题配置文件`

```shell
# dark mode
darkmode:
  enable: true
  # dark mode和 light mode切换按钮
  button: true
  autoChangeMode: false
  # Set the light mode time. The value is between 0 and 24. If not set, the default value is 6 and 18
  start: # 8
  end: # 22
```

| 参数           | 解释                                                         |
| -------------- | ------------------------------------------------------------ |
| button         | 是否在右下角显示日夜模式切换按钮                             |
| autoChangeMode | 自动切换的模式<br/>autoChangeMode: 1 跟随系统而变化，不支持的浏览器/系统将按照时间 start 到 end 之间切换为 light mode<br/>autoChangeMode: 2 只按照时间 start 到 end 之间切换为 light mode ,其余时间为 dark mode<br/>autoChangeMode: false 取消自动切换 |
| start          | light mode 的开始时间                                        |
| end            | light mode 的结束时间                                        |

![image-20201230201029381](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-doc-dark-mode-1-ade1ea.png)

#### 滚动状态百分比

主题配置文件中

```shell
# show scroll percent in scroll-to-top button
rightside_scroll_percent: true
```

![img](https://cdn.jsdelivr.net/gh/jerryc127/CDN@m2/img/hexo-butterfly-docs-scroll-percent-right-btn.gif)

#### 按钮排序

```shell
# Don't modify the following settings unless you know how they work (非必要请不要修改 )
# Choose: readmode,translate,darkmode,hideAside,toc,chat,comment
# Don't repeat 不要重复
rightside_item_order:
  enable: false
  hide: # readmode,translate,darkmode,hideAside
  show: # toc,chat,comment
```

### 标签外挂（Tag Plugins）

> 标签外挂是Hexo独有的功能，并不是标准的Markdown格式。
>
> 以下的写法，只适用于Butterfly主题，用在其它主题上不会有效果，甚至可能会报错。使用前请留意

#### Gallery相册图库

一个图库集合。

写法

```shell
<div class="gallery-group-main">
{% galleryGroup name description link img-url %}
{% galleryGroup name description link img-url %}
{% galleryGroup name description link img-url %}
</div>
```

- name：图库名字
- description：图库描述
- link：连接到对应相册的地址
- img-url：图库封面的地址

例如：

```shell
<div class="gallery-group-main">
{% galleryGroup '壁纸' '收藏的一些壁纸' '/Gallery/wallpaper' https://i.loli.net/2019/11/10/T7Mu8Aod3egmC4Q.png %}
{% galleryGroup '漫威' '关于漫威的图片' '/Gallery/marvel' https://i.loli.net/2019/12/25/8t97aVlp4hgyBGu.jpg %}
{% galleryGroup 'OH MY GIRL' '关于OH MY GIRL的图片' '/Gallery/ohmygirl' https://i.loli.net/2019/12/25/hOqbQ3BIwa6KWpo.jpg %}
</div>
```

#### Gallery相册

区别于旧版的Gallery相册,新的 Gallery 相册会自动根据图片长度进行排版，书写也更加方便，与 markdown 格式一样。可根据需要插入到相应的 md。

写法:

```shell
{% gallery [lazyload],[rowHeight],[limit] %}
markdown 图片格式
{% endgallery %}
```

| 参数      | 解释                                                         |
| --------- | ------------------------------------------------------------ |
| lazyload  | 【可选】点击按钮加载更多图片，填写 true/false。默认为 false。 |
| rowHeight | 【可选】图片显示的高度，如果需要一行显示更多的图片，可设置更小的数字。默认为 220。 |
| limit     | 【可选】每次加载多少张照片。默认为 10。                      |

示例

```shell
{% gallery %}
markdown 图片格式
{% endgallery %}

{% gallery true,220,10 %}
markdown 图片格式
{% endgallery %}

{% gallery true,,10 %}
markdown 图片格式
{% endgallery %}
```

例如:

```shell
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

![image-20240914175242924](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fimage-20240914175242924-44788d.png)

#### tag-hide

> 请注意，tag-hide内的标签外挂content内都不建议有h1 - h6 等标题。因为Toc会把隐藏内容标题也显示出来，而且当滚动屏幕时，如果隐藏内容没有显示出来，会导致Toc的滚动出现异常。

如果你想把一些文字、内容隐藏起来，并提供按钮让用户点击显示。可以使用这个标签外挂。

{% tabs test1 %}
<!-- tab -->
inline 在文本里面添加按钮隐藏内容，只限文字

( content不能包含英文逗号，可用&sbquo;)

```shell
{% hideInline content,display,bg,color %}
```

- content: 文本内容
- display: 按钮显示的文字(可选)
- bg: 按钮的背景颜色(可选)
- color: 按钮文字的颜色(可选)

> Demo

```shell
哪个英文字母最酷？ {% hideInline 因为西装裤(C装酷),查看答案,#FF7242,#fff %}

门里站着一个人? {% hideInline 闪 %}
```

哪个英文字母最酷？ {% hideInline 因为西装裤(C装酷),查看答案,#FF7242,#fff %}

门里站着一个人? {% hideInline 闪 %}

<!-- endtab -->

<!-- tab -->
block独立的block隐藏内容，可以隐藏很多内容，包括图片，代码块等等

( display 不能包含英文逗号，可用&sbquo;)

```shell
{% hideBlock display,bg,color %}
content
{% endhideBlock %}
```

- content: 文本内容
- display: 按钮显示的文字(可选)
- bg: 按钮的背景颜色(可选)
- color: 按钮文字的颜色(可选)

> Demo

```shell
查看答案
{% hideBlock 查看答案 %}
傻子，怎么可能有答案
{% endhideBlock %}
```

查看答案
{% hideBlock 查看答案 %}
傻子，怎么可能有答案
{% endhideBlock %}

<!-- endtab -->

<!-- tab -->
如果你需要展示的内容太多，可以把它隐藏在收缩框里，需要时再把它展开。

( display 不能包含英文逗号，可用&sbquo;)

```shell
{% hideToggle display,bg,color %}
content
{% endhideToggle %}
```

> Demo

```shell
{% hideToggle Butterfly安装方法 %}
在你的博客根目录里

git clone -b master https://github.com/jerryc127/hexo-theme-butterfly.git themes/Butterfly

如果想要安装比较新的dev分支，可以

git clone -b dev https://github.com/jerryc127/hexo-theme-butterfly.git themes/Butterfly

{% endhideToggle %}
```

{% hideToggle Butterfly安装方法 %}
在你的博客根目录里

git clone -b master https://github.com/jerryc127/hexo-theme-butterfly.git themes/Butterfly

如果想要安装比较新的dev分支，可以

git clone -b dev https://github.com/jerryc127/hexo-theme-butterfly.git themes/Butterfly

{% endhideToggle %}

<!-- endtab -->
{% endtabs %}

#### mermaid

使用mermaid标签可以绘制Flowchart（流程图）、Sequence diagram（时序图 ）、Class Diagram（类别图）、State Diagram（状态图）、Gantt（甘特图）和Pie Chart（圆形图），具体可以查看mermaid文档

修改 `主题配置文件`

```shell
# mermaid
# see https://github.com/mermaid-js/mermaid
mermaid:
  enable: true
  # built-in themes: default/forest/dark/neutral
  theme:
    light: default
    dark: dark
```

写法：

```shell
{% mermaid %}
内容
{% endmermaid %}
```

例如：

```shell
{% mermaid %}
pie
    title Key elements in Product X
    "Calcium" : 42.96
    "Potassium" : 50.05
    "Magnesium" : 10.01
    "Iron" :  5
{% endmermaid %}
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-mermaid-a66953.png)

#### Tabs

移植于next主题

使用方法

```shell
{% tabs Unique name, [index] %}
<!-- tab [Tab caption] [@icon] -->
Any content (support inline tags too).
<!-- endtab -->
{% endtabs %}

Unique name   : Unique name of tabs block tag without comma.
                Will be used in #id's as prefix for each tab with their index numbers.
                If there are whitespaces in name, for generate #id all whitespaces will replaced by dashes.
                Only for current url of post/page must be unique!
[index]       : Index number of active tab.
                If not specified, first tab (1) will be selected.
                If index is -1, no tab will be selected. It's will be something like spoiler.
                Optional parameter.
[Tab caption] : Caption of current tab.
                If not caption specified, unique name with tab index suffix will be used as caption of tab.
                If not caption specified, but specified icon, caption will empty.
                Optional parameter.
[@icon]       : FontAwesome icon name (full-name, look like 'fas fa-font')
                Can be specified with or without space; e.g. 'Tab caption @icon' similar to 'Tab caption@icon'.
                Optional parameter.
```

> Demo 1 - 预设选择第一个【默认】

```shell
{% tabs test1 %}
<!-- tab -->
**This is Tab 1.**
<!-- endtab -->

<!-- tab -->
**This is Tab 2.**
<!-- endtab -->

<!-- tab -->
**This is Tab 3.**
<!-- endtab -->
{% endtabs %}
```

![image-20240914180405372](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fimage-20240914180405372-283e81.png)

> Demo 2 - 预设选择tabs

```shell
{% tabs test2, 3 %}
<!-- tab -->
**This is Tab 1.**
<!-- endtab -->

<!-- tab -->
**This is Tab 2.**
<!-- endtab -->

<!-- tab -->
**This is Tab 3.**
<!-- endtab -->
{% endtabs %}
```

![image-20240914180443211](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fimage-20240914180443211-2ec74f.png)

> Demo 3 - 没有预设值

```shell
{% tabs test3, -1 %}
<!-- tab -->
**This is Tab 1.**
<!-- endtab -->

<!-- tab -->
**This is Tab 2.**
<!-- endtab -->

<!-- tab -->
**This is Tab 3.**
<!-- endtab -->
{% endtabs %}
```

![image-20240914180532374](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fimage-20240914180532374-f36c37.png)

> Demo 4 - 自定义Tab名 + 只有icon + icon和Tab名

```shell
{% tabs test4 %}
<!-- tab 第一个Tab -->
**tab名字为第一个Tab**
<!-- endtab -->

<!-- tab @fab fa-apple-pay -->
**只有图标 没有Tab名字**
<!-- endtab -->

<!-- tab 炸弹@fas fa-bomb -->
**名字+icon**
<!-- endtab -->
{% endtabs %}
```

![image-20240914180602768](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fimage-20240914180602768-0781df.png)

#### Button

使用方法：

```shell
{% btn [url],[text],[icon],[color] [style] [layout] [position] [size] %}

[url]         : 链接
[text]        : 按钮文字
[icon]        : [可选] 图标
[color]       : [可选] 按钮背景顔色(默认style时）
                      按钮字体和边框顔色(outline时)
                      default/blue/pink/red/purple/orange/green
[style]       : [可选] 按钮样式 默认实心
                      outline/留空
[layout]      : [可选] 按钮佈局 默认为line
                      block/留空
[position]    : [可选] 按钮位置 前提是设置了layout为block 默认为左边
                      center/right/留空
[size]        : [可选] 按钮大小
                      larger/留空
```

> Demo

```shell
This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly %}
This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right %}
This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly,,outline %}
This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline %}
This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,larger %}
```

![image-20240914181510104](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fimage-20240914181510104-8860db.png)

```shell
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,block %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,block center larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,block right outline larger %}
```

![image-20240914181704341](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fimage-20240914181704341-345cdf.png)

```shell
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,blue larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,pink larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,red larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,purple larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,orange larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,green larger %}
```

![image-20240914181744330](C:\Users\waws\AppData\Roaming\Typora\typora-user-images\image-20240914181744330.png)

```shell
<div class="btn-center">
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline blue larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline pink larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline red larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline purple larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline orange larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline green larger %}
</div>
```

![image-20240914181936040](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fimage-20240914181936040-3a1462.png)

#### inlineImg

主题中的图片都是默认以块级元素显示，如果你想以内联元素显示，可以使用这个标签外挂。

```shell
{% inlineImg [src] [height] %}

[src]      :    图片链接
[height]   ：   图片高度限制【可选】
```

> Demo

```shell
你看我长得漂亮不

![](https://i.loli.net/2021/03/19/2P6ivUGsdaEXSFI.png)

我觉得很漂亮 {% inlineImg https://i.loli.net/2021/03/19/5M4jUB3ynq7ePgw.png 150px %}
```

![image-20210319001204045](https://jsd.012700.xyz/gh/jerryc127/CDN@m2/img/hexo-theme-butterfly-docs-inlineimg.png)

#### label

高亮所需的文字

```shell
{% label text color %}
```

| 参数  | 解释                                                         |
| ----- | ------------------------------------------------------------ |
| text  | 文字                                                         |
| color | 【可选】背景颜色，默认为 default</br>default/blue/pink/red/purple/orange/green |

> Demo

```shell
臣亮言：{% label 先帝 %}创业未半，而{% label 中道崩殂 blue %}。今天下三分，{% label 益州疲敝 pink %}，此诚{% label 危急存亡之秋 red %}也！然侍衞之臣，不懈于内；{% label 忠志之士 purple %}，忘身于外者，盖追先帝之殊遇，欲报之于陛下也。诚宜开张圣听，以光先帝遗德，恢弘志士之气；不宜妄自菲薄，引喻失义，以塞忠谏之路也。
宫中、府中，俱为一体；陟罚臧否，不宜异同。若有{% label 作奸 orange %}、{% label 犯科 green %}，及为忠善者，宜付有司，论其刑赏，以昭陛下平明之治；不宜偏私，使内外异法也。
```

![image-20240914182244017](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fimage-20240914182244017-7e66df.png)

#### timeline

```shell
{% timeline title,color %}
<!-- timeline title -->
xxxxx
<!-- endtimeline -->
<!-- timeline title -->
xxxxx
<!-- endtimeline -->
{% endtimeline %}
```

| 参数  | 解释                                                         |
| ----- | ------------------------------------------------------------ |
| title | 标题/时间线                                                  |
| color | timeline 颜色 default(留空) / blue / pink / red / purple / orange / green |

> Demo

```shell
{% timeline 2022 %}
<!-- timeline 01-02 -->
这是测试页面
<!-- endtimeline -->
{% endtimeline %}
```

![image-20240914182421758](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fimage-20240914182421758-1cd8d8.png)

```shell
{% timeline 2022,blue %}
<!-- timeline 01-02 -->
这是测试页面
<!-- endtimeline -->
{% endtimeline %}
```

![image-20240914182441904](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fimage-20240914182441904-ff557c.png)

```shell
{% timeline 2022,pink %}
<!-- timeline 01-02 -->
这是测试页面
<!-- endtimeline -->
{% endtimeline %}
```

![image-20240914182500984](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fimage-20240914182500984-7def5c.png)

```shell
{% timeline 2022,red %}
<!-- timeline 01-02 -->
这是测试页面
<!-- endtimeline -->
{% endtimeline %}
```

![image-20240914182523436](C:\Users\waws\AppData\Roaming\Typora\typora-user-images\image-20240914182523436.png)

```shell
{% timeline 2022,purple %}
<!-- timeline 01-02 -->
这是测试页面
<!-- endtimeline -->
{% endtimeline %}
```

![image-20240914182544763](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fimage-20240914182544763-3b9825.png)

```shell
{% timeline 2022,orange %}
<!-- timeline 01-02 -->
这是测试页面
<!-- endtimeline -->
{% endtimeline %}
```

![image-20240914182646077](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fimage-20240914182646077-a3b0c1.png)

```shell
{% timeline 2022,green %}
<!-- timeline 01-02 -->
这是测试页面
<!-- endtimeline -->
{% endtimeline %}
```

![image-20240914182658290](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fimage-20240914182658290-b65e80.png)

#### flink

可在任何界面插入类似友情链接列表效果

内容格式与友情链接界面一样，支持 yml 格式

```shell
{% flink %}
xxxxxx
{% endflink %}
```

> Demo

```shell
{% flink %}
- class_name: 友情链接
  class_desc: 那些人，那些事
  link_list:
    - name: JerryC
      link: https://jerryc.me/
      avatar: https://jerryc.me/img/avatar.png
      descr: 今日事,今日毕
    - name: Hexo
      link: https://hexo.io/zh-tw/
      avatar: https://d33wubrfki0l68.cloudfront.net/6657ba50e702d84afb32fe846bed54fba1a77add/827ae/logo.svg
      descr: 快速、简单且强大的网志框架

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
{% endflink %}
```

![img](https://cdn.jsdelivr.net/gh/Killer-89757/PicBed/images/2024%2F09%2Fhexo-theme-butterfly-docs-flink-demo-11b079.png)

#### series 系列文章

在页面上显示系列文章

修改 `主题配置文件`

```shell
series:
   enable: true
   orderBy: 'title' # Order by title or date
   order: 1 # Sort of order. 1, asc for ascending; -1, desc for descending
   number: true
```

写法：

```shell
{% series %}
{% series [series name] %}
```

在文章的 front-matter 上添加参数 series，并给与一个标识

使用此标签外挂，会把相同标识的文章以列表的形式展示

如果不写 series 标识，则默认为你使用此标签外挂所在的文章的 series 标识

> Demo

```shell
{% series markdown %}
```

![img](https://oss.012700.xyz/butterfly/2023/10/butterfly-series.png)