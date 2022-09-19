# -notes

1. http & https

    1.1 http & https

       协议名称：HyperText Transfer Protocol 超文本传输协议
       s：多了一个SSL安全保障

    1.2 URL：请求目标的组成

       import requests

       response = requests.get('http://www.xbiquge.la/10/10489/')

         #
         http：//      请求协议（http or https）
         www           服务器名字（world wide web）， mail
         xbiquge.la    域名
         /             root（资源在哪里，目录）route-路径
         10/10489/     位置

    1.3 Request - 请求

       1.3.1 headers 可以看到
       
         general里面有：
         1）request URL
         2）request method
         3）status code：200 - success
         4）remote address：14.215.177.。。。

         请求体：请求行、请求头部、空行、请求数据（结构如下）

         请求行：GET https：//。。。。
         请求头：
         请求空行：
         请求数据：
       

       1.3.2 Method

         GET：从server获取数据，不对server的resources产生影响   //访问网页
         POST: 向server发送数据、修改，会修改server资源         //发动态
         
       1.3.3 request headers （请求头）
       
         常见的：
         1）accept：什么类型的数据：文字、图片等
         2）accept- charset：接收的字符集？
         3）accept- encoding： 一般指压缩方法：gzip/ deflate/br
         4）accept- language：CN中文，等
         5）authorization：授权
         6）content- length：正文长度
         7）origin：起始资源位置，root？
         8）connection：处理这次请求后，是否断开链接还是保持链接
         9）cookie：发给web的cookie内容，用来判断是否登陆
         10）host：client- end指定的web域名/IP地址和端口号
         11）if- modified- since：？
         12）pragma：“no cache”，刷新cache后再返回
         13）referer：告诉服务器从哪个页面链接。防盗链接
         14）from：
         15）user- agent：浏览器本身身份：操作系统 Windows哪个版本
         16）upgrade- insecure- requests： 自动从http升级到https。可以看到如果现有哥

   
   
   
   

    
