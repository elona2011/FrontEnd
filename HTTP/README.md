
请求报文：
请求方法+请求URI+协议版本+可选的首部字段+内容实体

响应报文：
协议版本+状态码+状态码原因短语+可选的响应首部字段+内容实体


HTTP 状态消息 http://www.w3school.com.cn/tags/html_ref_httpmessages.asp

HTTP是一种无状态协议，不建立持久的连接，服务端不保留连接的相关信息。
HTTP请求过程的7个步骤：
1.建立TCP连接
2.Web浏览器向Web服务器发送请求命令
3.Web浏览器发送请求头信息
4.Web服务器应答
5.Web服务器发送应答头信息
6.Web服务器向浏览器发送数据
7.Web服务器关闭TCP连接

###### HTTP状态码由3位数字构成：
* 1XX：信息类，表示收到Web浏览器请求，正在进一步处理中
* 2XX：成功，表示用户请求被正确接收、理解和处理
* 200 OK
* 204 No Content
* 206 Partial Content

###### 3XX：重定向，表示请求没成功，客户必须采取进一步的动作
* 301 Moved Permanently

永久性重定向，例如可以保存书签，对错误网址的重定向

* 302 Found

临时性重定向，例如不需要保存书签

* 303 See Other
* 304 Not Modified
* 307 Temporary Redirect

###### 4XX：客户端错误，表示客户端提交的请求有错误
* 400 Bad Request
* 401 Unauthorized
* 403 Forbidden
* 404 NOT Found，请求中引用的文档不存在

###### 5XX：服务器错误，表示服务器不能处理请求
* 500 Internal Server Error
* 503 Service Unavailable

###### 方便的命令行调试小工具

[https://github.com/jkbrzt/httpie](https://github.com/jkbrzt/httpie)

安装遇到的问题：
我的系统版本CentOS Linux release 7.1.1503，安装后http命令运行报错，后来发现可能是版本低，安装了开发版本就可以了

```bash
sudo pip install --upgrade https://github.com/jkbrzt/httpie/tarball/master
```

Windows安装

1.安装python2.7或以上版本

2.下载并安装pip，之后要手动添加C:\Python27\Scripts到环境变量

3.安装httpie

```bash
pip install --upgrade https://github.com/jkbrzt/httpie/tarball/master
```

###### HTTP术语

* hop-by-hop Header 逐级首部，只对下一级有效，通过代理或缓存不再转发

* end-to-end Header 端到端首部，必然发送到目的端，必须转发



## HTTP首部

###### 通用首部

-> Cache-Control: no-cache 缓存服务器需要对cache重新确认以响应

-> Cache-Control: no-store 真正不缓存，可能包含机密信息

-> Cache-Control: max-age 缓存的最大时间(秒)

-> Cache-Control: min-fresh 指定未来时间内仍有效的缓存(秒)

-> Cache-Control: max-stale 指定可接收的最大过期时间。未指定数值，则始终接收过期缓存

only-if-cached 在缓存的情况下响应

must-revalidate 

no-transform 阻止缓存被压缩等操作

###### 请求首部

-> Accept: text/plain; q=0.3, text/htm 逗号为分隔符，"; q=0.3"是对格式的权重补充，不补充则为1，最高

-> Host: 请求的主机名和端口号(必须,但可为空)

###### Cookie

<- Set-Cookie
