How-To-Install-Node.js-In-Windows-8.1
=====================================

  引言：最近想接触下angular.js，于是在图灵社区看到了免费的电子书《AngularJS入门教程》，下载下来看的时候发现，教程中有使用到node.js，虽然之前有稍微了解过，但是还是知之甚少，所以想深入地学习下。百度了下，虽然网上有些资料，但要不很旧，要不就是介绍的不清楚。这里我就简要的说明下，windows下如何安装和配置node.js。
  
	本机的环境是Windows 8.1 64位，不过node.js作为优秀的跨平台工具，兼容性应该是没有问题的，言归正传，正式介绍流程吧。
	
	1.首先便是去nodejs官网下载最新的windows msi格式安装包，首页或进入download页都可以。
	
	2.下载下来直接安装，安装完成后，在开始菜单Node.js下找到Node.js command prompt运行即可，这一操作是用来自动配置环境变量的，成功后会有命令窗口提示
	
	Your environment has been set up for using Node.js 0.10.24 (x64) and npm.
	
	3.在命令行中输入node -v检测下安装的版本，显示v0.10.24则表明安装成功了。
	
	4.测试下服务运行是否正常，编写如下代码，保存至helloworld.js。
	
	var http = require("http");
	
	http.createServer(function(request, response) {  
	
    		response.writeHead(200, {"Content-Type": "text/plain"});  
    		
    		response.write("Hello World");  
    		
    		response.end();
    		
	}).listen(8888);
	
	console.log("nodejs start listen 8888 port!");
	
	5.例如把该js放在我在安装目录下建立的myapp文件夹下，打开命令行，输入
	
	D:\Program Files\nodejs\myapp>node helloworld.js
	
	显示如下信息，则表明服务已开启：
	
	nodejs start listen 8888 port!
	
	6.打开浏览器，在地址栏中输入http://localhost:8888/，便会看到浏览器页面显示Hello World。
	
	OK，搞定！
	
