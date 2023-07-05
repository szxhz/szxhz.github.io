# https://szxhz.github.io/

**我使用了GitHub pages 和 hexo fluid 主题来进行网站布局和优化**
转载于：***https://blog.csdn.net/yaorongke/article/details/119089190***
步骤如下：
> **1,准备工作** ：
>
>  - 安装 *nodejs* 和 *git*
>
>    - node.js 官网： ***https://nodejs.org/*** 去下载相对稳定版：
     ![nodejs首页](https://szxhz.github.io/szxhz.github.io-source/img/20230705002.png "node.js 网站首页")

>    
>    - git 官网：***https://git-scm.com/download/win*** 安装过程一直下一步就行
     ![git官网](https://szxhz.github.io/szxhz.github.io-source/img/20230705003.png "git")
    
>    - 一切的一切就是你必须要有一个GitHub账号！***https://github.com/login***
>
>  **2,创建仓库** ：
>
>   - 新建仓库：其他默认，但仓库名得是 **用户名.github.io**
    ![新仓库](https://szxhz.github.io/szxhz.github.io-source/img/20230705008.png "新仓库")
>
>   - 新建一个文件，文件名为index.html:

    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="UTF-8">
            <title>test</title>
        </head>
        <body>
            <h1>test的个人主页</h1>
            <h1>Hello ~</h1>
        </body>
    </html>

    恭喜你，你已经拥有了一个GitHub page。
>
>  **3,安装hexo** ：
>
>  - 你可以根据hexo官网来进行安装：https://hexo.io
>
>  - 你在电脑上新建一个存放博客的文件夹，在该文件夹打开git bash here。
>
>    - 分别输入以下命令:

        $ npm install -g hexo-cli

        $ hexo -v

        $ hexo init hexo-blog

        $ cd hexo-blog

        $ npm install
>
>   - 如果都没有报错就输入如下命令：
    
        $ hexo g
        
        $ hexo s
>
>   - 这个时候你就可以让电脑本地启动博客，使用浏览器打开：***http://localhost:4000/***
      ![本地启动](https://szxhz.github.io/szxhz.github.io-source/img/20230705009.png "本地启动")
>
>   - 但到最后一定要**Ctrl+c**关闭。
>
>  **4，更换主题** :
>
>  - 这个界面虽说不上丑，但真的不好看，不如换个主题吧！可以去官网选一个：***https://hexo.io/themes*** 这里我使用的是fluid。
>
>  - 打开这个链接：***https://github.com/fluid-dev/hexo-theme-fluid/releases*** 下载最新版的 ***Source code (zip)***
     ![d-f](https://szxhz.github.io/szxhz.github.io-source/img/20230705004.png "d-f")
>
>  - 下载完成后解压到 ***/themes*** ，将文件重命名为 ***fluid***
>
>  - 然后更改 ***/_config.yml*** , 
   ![更改](https://szxhz.github.io/szxhz.github.io-source/img/20230705010.png "更改")
    找到 **theme** ，更改为如下：

    theme: next
>
找到 **language** ，更改为如下：

    language: zh-CN  

>  - 创建「关于页」:
>
>    - 因为这个主题没有关于页，需要手动创建：

     $ hexo new page about

>
>    - 新建的页面就在 ***/source/about/index.md*** hexo的页面是用MarkDown语法的，具体操作手册可以看官方手册： ***https://markdown.com.cn/basic-syntax/*** 。

    ---

    title: about
    date: 2020-02-23 19:20:33
    layout: about

    ---

    这里写关于页的正文，支持 Markdown, HTML

>
>  **5，自定义主题** ：
>
>  - 首先在 ***/_config.yml*** 中修改：（建议自定义的我用了中文，能改的在文段最上面)

    # Hexo Configuration
    ## Docs: https://hexo.io/docs/configuration.html
    ## Source: https://github.com/hexojs/hexo/

    # Site
    title: 你想要的title
    subtitle: '另一个title'
    description: '另一个title'
    keywords:
    author: 文章作者名
    language: zh-CN  
    timezone: ''

    # URL
    ## Set your site url here. For example, if you use GitHub Page, set url as 'https://username.github.io/project'
    url: 你的网站链接
    permalink: :year/:month/:day/:title/
    permalink_defaults:
    pretty_urls:
        trailing_index: true # Set to false to remove trailing 'index.html' from permalinks
        trailing_html: true # Set to false to remove trailing '.html' from permalinks


>  - 接着在 ***/themes/fluid/_config,yml*** 中修改：
>
>  - 我们可以更改浏览器标签的图标。

    # 用于浏览器标签的图标
    # Icon for browser tab
    favicon: /img/图标名

    # 用于苹果设备的图标
    # Icon for Apple touch
    apple_touch_icon: /img/图标名

>
>  - 上面 ***/img*** 实际上就在 ***/themes/fluid/source/img*** 里面。
>
>  - 其实背景图片也能改：在 ***/themes/fluid/source/img*** 里面有一个 ***default.png*** 文件，将他删掉，把你想要的背景放到这个文件夹中，改名为 ***default.png*** 。
>
>  - 我们可以更改导航栏左侧标题：

    navbar:
        # 导航栏左侧的标题，为空则按 hexo config 中 `title` 显示
        # The title on the left side of the navigation bar. If empty, it is based on `title` in hexo config
        blog_title: "自定义标题"

>  - 主页标题也可以更改：

    index:
        # 首页 Banner 头图，可以是相对路径或绝对路径，以下相同
        # Path of Banner image, can be a relative path or an absolute path, the same on other pages
        banner_img: /img/default.png

        # 头图高度，屏幕百分比
        # Height ratio of banner image
        # Available: 0 - 100
        banner_img_height: 100

        # 头图黑色蒙版的不透明度，available: 0 - 1.0， 1 是完全不透明
        # Opacity of the banner mask, 1.0 is completely opaque
        # Available: 0 - 1.0
        banner_mask_alpha: 0.3

        # 首页副标题的独立设置
        # Independent config of home page subtitle
        slogan:
            enable: true

            # 为空则按 hexo config.subtitle 显示
            # If empty, text based on `subtitle` in hexo config
            text: "自定义标题"

>    
>  - 现在我们构建再启动：

    $ hexo g -d
    $ hexo s

>
>  - 可以看见成果：
    ![2](https://szxhz.github.io/szxhz.github.io-source/img/20230705005.png "2")
>
>  **6，创建文章** ：

    $ hexo new "文章名"

>
>  - 常见的文章在 ***/source/_posts/你的文章名.md*** ，没错，你的文章也要用MD语法。
>
>  **7,上传GitHub page** :
>
>  - 方式1：
>    - 获取 *hexo-deployer-git*

    $ npm install hexo-deployer-git --save

>
>    - 获取克隆链接：
    ![3](https://szxhz.github.io/szxhz.github.io-source/img/20230705006.png "3")
>
>    - 获取tokens： ***https://github.com/settings/tokens***
>
>    - 打开 ***/_config.yml*** 最后一行进行编辑：

    deploy:
        type: git
        repo: 克隆链接
        branch: main
        token: 你的token

>
>    - 然后构建：

    hexo g -d

>
>    - 接着会提示你按格式输入邮箱和用户名，用GitHub验证登录。验证完成后再次输入构建命令。
    ![4](https://raw.githubusercontent.com/szxhz/szxhz.github.io-source/main/img/20230705007.png "4")
>
>  - 方式2：
>
>    - 这个方法简单粗暴，直接将 ***/public*** 里面的所有文件上传即可。
    ![5](https://raw.githubusercontent.com/szxhz/szxhz.github.io-source/main/img/20230705011.png "5")
>
>    - 这个方法简单，但以后一但更新，就得重新上传。
>
>  - 我个人认为 **方式1** 更方便，且可以长期使用。

那么，这个博客就搭建完成了，放心食用。如果像上传服务器，可以参考之前提到的原文。