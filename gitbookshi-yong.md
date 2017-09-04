1. 到官网[https://www.gitbook.com/editor下载gitbook图形客户端](https://www.gitbook.com/editor下载gitbook图形客户端)

2. 默认安装路径：C:\Users\Administrator\GitBook\Library\Import\spider

3. 安装使用gitbook命令

**首先安装node.js**，到官网[http://nodejs.cn/，下载Windows](http://nodejs.cn/，下载Windows) 系统 \(.msi\)64位

**配置node.js镜像**，可以使用命令：

```
npm config set registry http://registry.npm.taobao.org
```

或者直接修改配置文件：C:\Users\Administrator

```
在用户主目录下编辑 .npmrc 文件，添加一行 registry=http://registry.npm.taobao.org 保存
```

**全局安装gitbook**

```
执行 npm install gitbook-cli -g 命令，进行安装，执行 gitbook -v 查看安装的版本信息4.
```

1. gitbook命令使用

网站发布：先cd到C:\Users\Administrator\GitBook\Library\Import\spider，按住shift，右键弹出cmd

```
输入命令：gitbook serve，通过http://localhost:4000可以在浏览器访问
```

![](/assets/import.png)

其他命令

[http://blog.csdn.net/axi295309066/article/details/61420694](http://blog.csdn.net/axi295309066/article/details/61420694)

gitbook创建新项目，并与github关联

1. #### 登陆[https://www.gitbook.com，new](https://www.gitbook.com，new) organization，_需要注意填写title的时候，不能使用中文，否则会报 Path \`name\` is required.      _
2. ### 、关联 GitBook 和 GitHub 帐户 {#gb_8_1}

   关联设置也很简单，首先进入 GitBook 的“Account Settings（帐户设置）”页面，在“Profile（个人资料）”标签页找到“GitHub”选项卡，点击【Connect to GitHub】按钮会转向 GitHub 的“Authorize application”页面，点击【Authorize application】按钮即可完成关联。

3. ### 3、设置 GitBook 和 GitHuB 同步 {#gb_8_3}

   导出成功后，再回到 GitBook 项目设置页面的“GitHub”选项卡，在“GitHub Repository”中的输入框中填入 GitHub 的 Repository 名，如“GitHub用户名/myfirstbook”，点击【Save】按钮保存。

   保存后当前页面会出现一个名为“Integration”的选项卡，点击里面的【Add webhook】按钮，允许 GitBook 接收 Github 的内容更新。这样就把 GitBook 上的项目和 GitHub 相对应的项目关联上了。

   此后即可用 GitHub 管理电子书项目，在 GitBook 上对电子书内容修改也会自动同步到 GitHub 中。

#### ![](/assets/import2.png)

#### ![](/assets/import4.png)![](/assets/import3.png)

1. 在github上创建一个**repository**

例如：注册的github帐号名为dengsiwen，创建的repository名称为spider，那么你的仓库名为spider在github上的地址为：

HTTPS ：[https://github.com/dengsiwen/spider.git](https://github.com/dengsiwen/spider.git)

SSH ： [git](http://lib.csdn.net/base/git)@github.com:dengsiwen/spider.git

Subversion：[https://github.com/dengsiwen/spider](https://github.com/dengsiwen/spider)

```
本地创建一个文件，CD到该文件下，执行如下命令
F:\dsw\gitbook>git init
F:\dsw\gitbook>git clone https://github.com/dengsiwen/spider.git
拷贝原来项目spider目录下的所有文件到该目录spider
cd spider(如果是上层目录，可能会报：no changes added to commit)
$ git add *
git commit -m 'Initial commit project'
git remote add origin https://github.com/dengsiwen/spider.git
git push origin master
```

error: failed to push some refs to 解决办法

```
可以通过如下命令进行代码合并【注：pull=fetch+merge]
git pull --rebase origin master
```

fatal: Authentication failed for解决办法

```
ssh-keygen -t rsa      //一路回车下来
注：Windows下使用git bash操作命令行。
测试是否连接上github服务器
ssh -T git@github.com
这时一般会输出：
.........
Permission denied (publickey).
解决办法：将上面生成的public key(id_rsa.pub文件)拷贝到github服务器的SSH Keys中，具体操作，
登录后，点击右上角的Account settings——> SSH Keys。
（如果没有配置用户名和邮箱，那么需要执行以下命令：
git config --global user.name "XXX"
git config --global user.email "XXX@XXX.com" ）
```



