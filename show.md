# GitHub与Jupyterlab的小白上手过程展示
*5.20王莉莎*


## Juyterlab
### Juyterlab介绍
它是Jupyter notebook的升级版<br>
所以特点：<br>
1. 在浏览器中打开，与其他网页的交互性，联动性强，也就是说如果用chrome打开的话，chrome插件也是可以照常用在jupyterlab上的
2. 集成型工具，功能强大，由于有很多插件，可以管理各类型文件，比如你关闭了Lab的页面，重新访问Lab，甚至是从另一台设备访问Lab，你都可以得到一个完美复原的环境，包括你打开的页面，它们的位置，甚至运行情况都会得以保存。即相当于你有了云桌面
3. 脚本的编辑，运行，可视化一站式体验<br>


### Jupyterlab的使用
#### 安装
有两种途径进行安装：<br>
1. 通过pip 
2. 通过conda<br>
两者的区别：<br>
conda是一种集成形安装工具包的聚集地，pip只是python的工具包，所以建议使用conda，因为在后续jupyterlab添加插件以及下载其他工具更加便捷<br>
[Jupyterlab安装步骤链接](https://jupyter.org/install)<br>
[还可以更换打开jupyterlab的浏览器](https://cloud.tencent.com/developer/article/1740382)<br>
[也可以添加快捷方式](https://blog.csdn.net/mark__tuwen/article/details/106030691)<br>

#### 简单功能介绍
![截图3](https://s2.loli.net/2022/05/18/7YHRNTazV6UhJjb.png "Jupyterlab界面")

在help中可以找到Jupyterlab reference ：会有详细的介绍，以及应用指南。[Jupyterlab官网](https://jupyter.org/)
以及[补充介绍链接](https://zhuanlan.zhihu.com/p/87403131)<br>
也可输出各种类型的文件<br>
![截图1](https://s2.loli.net/2022/05/18/ogLtpe7xj9RJrTG.png "输出文件处截图")<br>
其中一个有意思的小功能的介绍：<br>
![截图2](https://s2.loli.net/2022/05/18/9sYLNAmza7yOwQh.png "一个小功能介绍")<br>
将其打开，可以拖入文档，光标点击代码处的时候会出现此代码的函数教学，有助于学习以及差错<br>
补充：
[Markdown语法官方教学](https://markdown.com.cn/)

notebook和console的区别：<br>
Notebook可以随时改代码，再重新运行，但是console只能拉下来代码之后更改再运行，目前我理解的是，console可以比较清楚看到代码修改对比

#### 拓展安装
1. GitHub插件
方便学习github，可以在Jupyterlab左边栏中填写账号名，即可获取此账号下的所有仓库文件，打开即可阅读<br>
缺点：文件只能读取，不能修改。解决方法：将github中的文件clone下来到本地，之后再在jupyterlab中打开就可以修改了<br>
[GitHub插件安装步骤](https://github.com/lisa348/jupyterlab-github/blob/master/README.md)<br>
2. Matplotlib插件
作图的，可以做到代码的可视化<br>
我目前的问题，还不能做到交互式变更
[找到的解决方法链接](https://zhuanlan.zhihu.com/p/371673879)<br>
[Matplotlib官网](https://matplotlib.org/)<br>
[Matplotlib补充介绍](https://blog.csdn.net/qq_34859482/article/details/80617391)<br>
3. 安装R语言<br>
[操作步骤](https://dzone.com/articles/using-r-on-jupyternbspnotebook)<br>
`install.packages('IRkernel')`<br>
`IRkernel::installspec(user = FALSE)`<br>
操作之后就可以在界面上看到R语言<br>
![截图7](https://s2.loli.net/2022/05/18/LIzhaJ8byfi7QKw.png "添加R之后的界面变化")
#### 可视化展示
直接在Jupyterlab上展示

## GitHub
### github介绍
>GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

这句我是引用的github docs中的一句介绍，关键词：1多人协作2版本控制<br>
这个有着众多现成脚本的开源平台，还是免费的，而且有许多官方教学课程以及指南，对于编程小白来说相对友好<br>
### GitHub的使用
1. 注册
2. 创建ssh key
原因：由于github是一个开源的网站，为了安全问题，每次pull、push都需要输入密码，所以为了简便，使用ssh密钥就不需要输密码了<br>
什么是ssh
>SSH 专为远程登录会话和其他网络服务提供安全性的协议。利用 SSH 协议可以有效防止远程管理过程中的信息泄露问题。
SSH是标准的网络协议，可用于大多数UNIX操作系统，能够实现字符界面的远程登录管理，具有更高的安全性。
说白了就是在远程的时候增加了安全性，实验室的服务器使用远程也需要先弄ssh<br>
3. GitHub上建仓
建仓之后就可以在里面编写代码，也可以fork他人的仓库到自己的账号下面<br>
可以在里面直接编写，然后提交<br>
在更改的时候可以创建分支，这里就可以看到更改的全过程，也可以对于更改写备注（评语）
![截图4](https://s2.loli.net/2022/05/18/HeGuf7DWsyaqIE9.png "GitHub创建分支")
4. 将GitHub上的文件下载到本地
在想要存放的地方新建文件夹，在当前文件夹点击右键，git bash here，输入`git init`
去你将要clone的github仓库，将URL网址copy下来，输入`git clone url`（url为刚刚copy下来的地址），就可以在新建的文件夹中看到想要的文件<br>
5. 将本地文件上传GitHub
这里有两种方法：<br>
[网上大牛的介绍，很详细](https://blog.csdn.net/u013553529/article/details/59144904)<br>
[GitHub对此的官方说明](https://docs.github.com/cn/repositories/working-with-files/managing-files/adding-a-file-to-a-repository)<br>
[简明解释](https://zhuanlan.zhihu.com/p/359552966)<br>

**对于GitHub中fork、clone、pull、push的逻辑理解：**<br>
![图片8](https://s2.loli.net/2022/05/18/URaPwixFEbfzq14.png)
![图片9](https://s2.loli.net/2022/05/18/x1H73eICAhrXPsE.png)

6.  Git的补充说明<br>
.git文件夹中的一堆文件都代表什么
[官方说明](https://git-scm.com/docs/gitrepository-layout)

## 两者的联动
1. jupyterlab-github插件
在红框中输入github账号即可进此账号，并显示账号所有仓库<br>
![截图5](https://s2.loli.net/2022/05/18/I9hUurNMG26VW5l.png "GitHub插件")<br>
可以在jupyterlab中打开，但是只能读取<br>
![截图6](https://s2.loli.net/2022/05/18/SVqZOQNwsjUM1zd.png "只能读取")
2. 将本地文件上传到github中<br>
上述已介绍

## 后续延展
1. 如何后续应用于生物信息分析
2. excel我使用的办公工具，如何利用jupyterlab
3. 与我常用的notion相结合，如何写代码创建自己的模板





