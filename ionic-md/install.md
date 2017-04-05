# 安装

##### 命令行安装
首先您需要安装 Node.js，我们在接下来的安装中需要使用到其 NPM 工具，更多 NPM 介绍可以查看我们的NPM 使用介绍。
然后通过命令行工具安装最新版本的 cordova 和 ionic 。通过参考Android 和 iOS 官方文档来安装。

##### Window 和 Linux 上打开命令行工具执行以下命令：
	$ npm install -g cordova ionic
##### Mac 系统上使用以下命令：
	sudo npm install -g cordova ionic
提示: IOS需要在Mac Os X. 和Xcode环境下面安装使用。

如果你已经安装了以上环境，可以执行以下命令来更新版本:

	npm update -g cordova ionic
	或
	sudo npm update -g cordova ionic

##### 创建应用
使用ionic官方提供的现成的应用程序模板，或一个空白的项目创建一个ionic应用：

	$ ionic start myApp tabs

##### 运行我们刚才创建的ionic项目
使用 ionic tool 创建，测试，运行你的apps(或者通过Cordova直接创建)。
创建Android应用

	$ cd myApp
	$ ionic platform add android
	$ ionic build android
	$ ionic emulate android