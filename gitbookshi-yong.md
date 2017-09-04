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

1. #### 登陆[https://www.gitbook.com，new](https://www.gitbook.com，new) organization，_需要注意填写title的时候，不能使用中文，否则会报 Path \`name\` is required._![](/assets/import2.png)
2. 在github上创建一个新项目
3. 


