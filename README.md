菜鸟教程git
[Git 各平台安装包下载地址为](http://git-scm.com/downloads)

Debian/Ubuntu

Debian/Ubuntu Git 安装命令为：

$ apt-get install libcurl4-gnutls-dev libexpat1-dev gettext \
  libz-dev libssl-dev

$ apt-get install git

$ git --version
git version 1.8.1.2

Centos/RedHat

如果你使用的系统是 Centos/RedHat 安装命令为：

$ yum install curl-devel expat-devel gettext-devel \
  openssl-devel zlib-devel

$ yum -y install git-core

$ git --version
git version 1.7.1

源码安装

我们也可以在官网下载源码包来安装
[最新源码包下载地址](https://git-scm.com/download)

安装指定系统的依赖包：

########## Centos/RedHat ##########
$ yum install curl-devel expat-devel gettext-devel \
  openssl-devel zlib-devel

########## Debian/Ubuntu ##########
$ apt-get install libcurl4-gnutls-dev libexpat1-dev gettext \
  libz-dev libssl-dev

解压安装下载的源码包：

$ tar -zxf git-1.7.2.2.tar.gz
$ cd git-1.7.2.2
$ make prefix=/usr/local all
$ sudo make prefix=/usr/local installv


Windows 平台上安装

在 Windows 平台上安装 Git 同样轻松，有个叫做 msysGit 的项目提供了安装包，可以到 GitHub 的页面上下载 exe 安装文件并运行：

[安装包下载地址](https://gitforwindows.org/)

Mac 平台上安装

在 Mac 平台上安装 Git 最容易的当属使用图形化的 Git 安装工具，
[下载地址为](http://sourceforge.net/projects/git-osx-installer/ )


[最新git源码下载地址1](https://github.com/git/git/releases)
[最新git源码下载地址2](https://www.kernel.org/pub/software/scm/git/ )

移除旧版本git

centos自带Git，7.x版本自带git 1.8.3.1（应该是，也可能不是）， 安装新版本之前需要使用yum remove git卸载（安装后卸载也可以）。

[root@Git ~]# git --version    ## 查看自带的版本
git version 1.8.3.1
[root@Git ~]# yum remove git   ## 移除原来的版本

安装所需软件包

[root@Git ~]# yum install curl-devel expat-devel gettext-devel openssl-devel zlib-devel 
[root@Git ~]# yum install gcc-c++ perl-ExtUtils-MakeMaker

下载&安装

[root@Git ~]# cd /usr/src
[root@Git ~]# wget https://www.kernel.org/pub/software/scm/git/git-2.7.3.tar.gz

解压

[root@Git ~]# tar xf git-2.7.3.tar.gz

配置编译安装

[root@Git ~]# cd git-2.7.3
[root@Git ~]# make configure
[root@Git ~]# ./configure --prefix=/usr/git ##配置目录
[root@Git ~]# make profix=/usr/git
[root@Git ~]# make install

加入环境变量

[root@Git ~]# echo "export PATH=$PATH:/usr/git/bin" >> /etc/profile
[root@Git ~]# source /etc/profile

检查版本

[root@Git git-2.7.3]# git --version 
git version 2.7.3




