apache和tomcat
apache是一个web服务器，只能支持静态网页(html),但是可以通过插件支持php,还可以与tomcat联通使用。
tomcat是一个应用(java)服务器，他只是一个servlet容器，是apache的扩展，asp,php,cgi,jsp等动态网页需要Tomcat来处理。
两者都是一种容器，只不过发布的东西不同。
通俗点来说，是jsp网站的服务器之一，jsp使用脚本语言编写，需要服务器来解释运行，如果你的网页是纯html的，浏览器就可以直接解释查看效果，但是你的网页一般是.jsp .asp.php等的动态网页时浏览器自己就无法解释了，需要上面说到的服务器。tomcat便可以解释jsp等java编写的网站。

