# Apache-Ambari-ZH

当前Ambari的汉化版本为2.7.4.0.0,汉化采用对该版本的ambari源码直接修改的方式进行,如有翻译不当之处,请批评指正


## 一、使用方法如下：

`message.js` 因为ambari的前端是一个纯前端的工程，所以如果你要是想使用的话需要重新编译这个包去使用，在`ambari-web`上`brunch build`即可，然后把生成`public`文件夹覆盖到`ambari-server`的`/usr/lib/ambari-server/web`目录即可。
或者下载`https://github.com/liuwenru/Apache-Ambari-ZH/releases/download/v0.1/public.tar.gz`直接使用


## 二、ambari-web 构建编译方法

查看`ambari-web`的工程目录可以知道，这是一个基于`nodsjs`的工程，构建工具使用`brunch`,有兴趣的同学可以详细学习一下`brunch`的使用，对于不是做前端的同学可以简单的使用如下命令进行安装，构建编译之前需要你的环境中有`nodejs V8`，建议使用[`NVM` 安装](https://github.com/nvm-sh/nvm), 构建环境建议使用`Fedora30+`操作系统

```bash

Shell> curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
Shell> nvm install v8.17.0
Shell> git clone https://github.com/liuwenru/Apache-Ambari-ZH.git
Shell> cd Apache-Ambari-ZH/ambari-web 
Shell> npm install 
Shell> npm install -g brunch@1.7
SHell> brunch build 

```

构建完成后，`publibc`目录就是可以直接使用的版本，拷贝到`/usr/lib/ambari-server/web`上重启`ambari-server`即可。



