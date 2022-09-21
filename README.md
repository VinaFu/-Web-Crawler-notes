#  Web Crawler-notes

用F12去看内容

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
         3）status code：200 - success；307redirect
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
         user-agent
         host
         referer 多一些
         
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
         16）upgrade- insecure- requests： 自动从http升级到https。可以看到如果现有
         
       1.3.5
          
          用：
          response.request.method
          response.request.url
          response.request.headers 来查看请求中的信息
          会自带一些默认的设置在里面，比如：accept- encoding、connection
          
    1.4 Response - 响应

       set-cookie：修改了
       add-cookie：
       1.4.1
       
       1.4.2 常见方法和属性
           response.text
           response.content
           response.json（）
           response.headers
           response.encoding
           response.apparent—encoding 
           response.cookies     获取响应体的cookies
           response.url
           response.status——code  获取状态码
            状态码   100-200:    server成功收到了请求
                    200-299:    请求成功
                    300-399:    重定向（URL位置变了，比如上面的307）；301永久重定向；302临时重定向-未登陆界面
                    400-499:    客户端发送的请求地址有误（URL没有数据）；403权限不够
                    500-599:    服务器问题（宕机）
        1.4.3 json
           在request.url里面看json
           
           格式：外层{} [] 包裹，嵌套数据         
               {字段一:值1，字段二：{嵌套字段1：嵌套字段值}} -- string
               和dictionary很像，但dictionary -- dict

               response.json（）方法会在底层把string转换为dict形式。前提：json是规范的。有小括号啥的都不行，从大括号开始才是对的
             
   
   
   

    
