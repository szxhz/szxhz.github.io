# https://szxhz.ikunh.top

**我使用了GitHub pages 和 hexo fluid 主题来进行网站布局和优化**
转载于：***https://blog.csdn.net/yaorongke/article/details/119089190***
步骤如下：
> 1,准备工作：
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
>  2,创建仓库：
>
>   - 新建仓库：其他默认，但仓库名得是 **用户名.github.io**
    ![新仓库](https://img-blog.csdnimg.cn/5b7236589dc8430d8b96c512e0989b23.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3lhb3JvbmdrZQ==,size_16,color_FFFFFF,t_70 "新仓库")
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
>  3,安装hexo：
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
      ![本地启动](https://img-blog.csdnimg.cn/656bf025f6934a35abc104b16e4dd2fc.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3lhb3JvbmdrZQ==,size_16,color_FFFFFF,t_70 "本地启动")
>
>   - 但到最后一定要**Ctrl+c**关闭。