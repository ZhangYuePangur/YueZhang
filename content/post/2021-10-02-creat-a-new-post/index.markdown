---
title: 个人网站管理
author: ''
date: '2021-10-02'
slug: []
categories: []
tags: []
subtitle: ''
description: 'This is a short guide'
image: img/post-bg-coffee.jpeg
---

# 主页配置

这个部分配置的是你的首页，就是一打开你的网站就看见的那个页面。首先你需要找到这个文件并打开，就在你的YueZhang文件夹一打开就是。

`config.yaml`

#### 背景图

60行，就是你的桌面那个图。我猜你不想换。在img这个文件夹里放你想换的图片，然后在这里把图片名换掉就好了，注意后缀也写上。img文件夹在YueZhang/static里。 `header_image: img/Desk.jpg`

404后显示的背景hhhhhhh。 `image_404: img/404-bg.jpg`

搜索引擎检索你的网站的关键词。逗号分隔。 `keyword: ZhangYue, zhangyue, 张玥的网络日志, 张玥的博客, ZhangYue Blog, 博客`

70行标语，打了＃意思就是不让它起作用。 `slogan: 路在脚下，心向远方`

#### 头像

69行`sidebar_avatar: img/ZhangYue.jpg`。在img这个文件夹里放你想换的图片，然后在这里把图片名换掉就好了，注意后缀。img文件夹在YueZhang/static里。

个人描述68行，冒号后面想打啥打啥。

`sidebar_about_description: The most beautiful, brilliant, talented, gentle, cute girl.`

#### GIRLFRIEND

不许编辑

#### BOOKMARKS

第45行开始

      bookmark_link:
        - href: https://martinfowler.com
          title: Martin Fowler
        - href: http://www.servicemesher.com
          title: ServiceMesher
      bookmarks: yes

`bookmarks`写成no就不会显示书签，yes就显示。href是链接的网址，title是显示出来的名字。这个例子中显示的就是[Martin Fowler](https://martinfowler.com)和[ServiceMesher](http://www.servicemesher.com)。

#### MUSIC

建议你直接找我给你换。首先，打开这个文件。

`themes/hugo-theme-cleanwhite/layouts/partials/sidebar.html`

第264行的`src="//music.163.com/outchain/player?type=2&id=xxxxxxxx&auto=1&height=66"`

xxxxxxxx换成网易云音乐的id。

#### 社交媒体

71-82行

      social:
        email: zhang.yue.zy@outlook.com
        github: https://github.com/ZhangYuePangur
    #    linkedin: https://www.linkedin.com/in/yourlinkedinid
        rss: yes
    #    stackoverflow: https://stackoverflow.com/users/yourstackoverflowid
    #    wechat: your wechat qr code image
    #    weibo: 
    #    zhihu: 
    #    instagram: 
    #    twitter: 
    #    facebook: 

打了＃就是不起作用。想用哪个把前面的\#删掉，直接输入链接就可以了。微信是二维码位置，你可以放到img这个文件夹里，然后比如你的二维码是`QR.jpg`，这里就写`img/QR.jpg`。img文件夹在YueZhang/static里。

#### 赞赏支持

67行`reward: yes`，换成no就关了

# 文章创建、发布和管理

## 创建文章

首先，打开你的RStudio，找到`Addins > New Post`

![](images/newpost.png)

界面会变成：

![](images/postset.png)

title: 文章名

author: 作者

date: 时间

subdirectory: 你准备把这个文章放到首页最上面哪个栏目里就选哪个。

categories: 分类

tags: 标签，你可以写成 tags: \['tag1', 'tag2'\]，没有个数限制。

Archetype: 不管

Filename: 文件名，建议别改，自动生成的就挺好

slug: 不用管

format: 选`R markdown (Rmarkdown)`

然后你的RStudio中就会出现你刚才创建的文件：

![](images/Rmarkdown-01.png)

你也可以在这里修改title, author, tags等参数。

subtitle: 副标题

description: 在首页看见的文章summary

image: 文章页背景图，默认设置的是`img/post-bg-coffee.jpeg`，想换哪个就放在img文件夹里，并在这里把文件名改了。

如果不想要右侧的导航栏，就在image下面加一行`showtoc: no`

    ---
    title: 个人网站管理
    author: ''
    date: '2021-10-02'
    slug: []
    categories: []
    tags: []
    subtitle: ''
    description: 'This is a short guide'
    image: img/post-bg-coffee.jpeg
    showtoc: no
    ---

在最后一行的`---`下面写文章内容。

## 编辑内容

编辑文章有两种模式，第一种是在R markdown中直接编辑，另一种是打开visual markdown editor。我经常两种模式换着用，尤其是需要插入图片和参考文献（或者忘了代码怎么打）的时候切到visual模型，非常快乐。visual markdown editor就是类似于word的编辑模式。![](images/visualeditor.png)按一下A这个按钮就打开了visual模式，打开后再按一下就关掉了visual模式。

### 格式

![](images/Format.png)

选中内容，按Bold，或者在要加粗的内容两侧打\*\*。

Bold: 加粗 `**加粗**` **加粗**

Italic: 斜体 `*斜体*` *斜体*

高亮：这个符号在你键盘上的Tab键上面，\`高亮\`，`高亮`

Bulleted List:

-   分好几点

-   第二点

-   第三点balabala

直接打就是

    - 分好几点

    - 第二点

    - 第三点balabala

    Numbered List

1.  第一点
2.  第二点

它还可以缩减list的距离和加上check box

![](images/list.png)

1.  [x] 第一点
2.  [ ] 第二点

多级标题：

几个井号就是几级

    # 一级标题
    ## 二级标题 
    ### 三级标题

    也可以通过下图位置实现

![](images/Format2.png)

### 插入

![](images/insert.png)

#### 图片

在visual模型下，直接点上面的图片标志，然后就可以插入图片了，不需要在imges文件里。我这里插入了一个存储在YueZhang文件夹之外的图片。

![](images/insertpicture.png)

直接写就是`![](images/Rmarkdown-01.png)` 在你的对应文章的文件夹里，找到`images`，放进去，输入对应的名称就ok了。\[\]中填图片名称，()里图片位置，网络图片也可以，输出链接就可以了。

#### emoji

😋打开方式`Insert < Special Characters < Insert Emoji`

![](images/emoji.png)

（虽然可以用代码写，但是我觉得你不想看，只想直接用）


```r
`r emo::ji("smile")` 
```

它就会显示😄。完整的emoji列表：[emo](https://github.com/hadley/emo)。为了防止你翻不了墙，找了一篇CSDN的文章有这个列表[emo](https://blog.csdn.net/weixin_36330260/article/details/114361164)。

#### 引用quote

![](images/block.png)

> 谁知道这是谁说的呢，反正引用就vans了

`> 谁知道这是谁说的呢，反正引用就vans了`

#### 引用（内部链接），超链接

比如说我引用了前文中的`[GIRLFRIEND](#GIRLFRIEND)`部分，就会[GIRLFRIEND](#girlfriend)。方框里填什么都行。

网址也是类似的格式`[这里填要显示的字](https://zhangyue.netlify.app/)`括号里写链接。[这里填要显示的字](https://zhangyue.netlify.app/)

#### 表格

`Table`

其实也可以直接读取excel文件直接输出的，不过我感觉你应该不用这个网站来插入表格和代码。

### 插件

终于到了令人激动的插件环节了。

#### bilibili

`{{</* bilibili 视频ID */>}}`

`{{</* bilibili BV1uk4y127gq */>}}`

{{< bilibili BV1uk4y127gq >}}

#### mindmap

    {{%/* mind */%}}
    - Root
        - Level 1
            - Level 2
            - Level 2
                - Level 3
                - Level 3
                    - Level 4
                        - Level 5
                            - Level 6
        - Level 1
            - Level 2
            - Level 2
         - Level 1
            - Level 2
            - Level 2
         - Level 1
            - Level 2
            - Level 2
         - Level 1
            - Level 2
            - Level 2
    {{%/* /mind */%}}

{{% mind %}}

-   Root

    -   Level 1

        -   Level 2

        -   Level 2

            -   Level 3

            -   Level 3

                -   Level 4

                    -   Level 5

                        -   Level 6

    -   Level 1

        -   Level 2
        -   Level 2

    -   Level 1

        -   Level 2
        -   Level 2

    -   Level 1

        -   Level 2
        -   Level 2

    -   Level 1

        -   Level 2
        -   Level 2 {{% /mind %}}

#### 网易云音乐

`{{</* cloudmusic 1830664234 */>}}`

{{< cloudmusic 1830664234 >}}

#### 日程

`显示菜单 < 更多 < 链接到这个看板`

![](images/trello.png)

复制b后面那一串

`{{</* trello 1V9CSXyY */>}}`

{{< trello 1V9CSXyY >}}

### 使用小技巧

#### 大纲栏

![](images/outline.png)

点一下就可以蹦过去。

#### 多级标题折叠

![](images/title.png)

关掉visual模式，点小三角可以展开或收缩标题，非常非常非常写作友好。可以先打好各级标题，差不多文章框架就搭好了。但是有些部分暂时不想写，或者已经写完了，就可以折叠起来。专注展开的一小块写作就好了。也不用非要从开头开始写，想先写哪就先写哪。

#### 搜索与替换

![](images/replace.png)

### 预览文章

放大镜右边的毛线球Knit点一下。在右下角的Viewer窗口就可以看见文章，下面的红框的按钮把窗口弹出到浏览器。（但在未上传到github之前，都是只改变了本地的文件，没有联网。）

![](images/view.png)

## 发布文章

终于写完了，然后就打开你的github

1\.

![](images/github.png)

Commit to main

2\.

![](images/push.png)

push origin

就好了！然后这篇文章就被发布到网站上了。

## 管理文章

你的所有文章都保存在`content这个文件夹里。主页的文章都在`\`content/post`里，每个文件夹对应一篇文章。如果你想把文章移动到life或者note栏，把对应文件夹剪切到content/life`就可以了。想要删除文章就把对应文件夹删掉。

# 网站管理

## 预览

![](images/site.png)

\`Addins \< Serve Site\`

## 上传修改

同[发布文章](#发布文章)

## 版本控制

## 评论管理

[Leancloud](https://console.leancloud.cn/apps)

登录后进入Zhang Yue Blog

![](images/comment.png)

`数据存储 < 结构化数据 < Comment`

选中评论，可以删除，下载，分析等。

## 日程管理

\[trello\](<https://trello.com/>)

## 增加其他功能

请留言

# 结语

写给我可爱的小张🐇😘

小李于

02/10/2021
