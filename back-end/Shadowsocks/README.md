未越狱的iphone/ipad使用shadowsocks全局代理5406
原因：ios系统不支持socks代理，appstore下载的shadowsocks只能浏览网页，不支持后台运行

首先shadowsocks可以在PC上正常代理，设置步骤如下：0018
1.在编辑服务器窗口设置代理端口9189（可为任意不常用端口）
2.右键点击运行图标，选中允许来自局域网的连接
3.编辑pac文件，由于iphone/ipad不支持socks代理，我们这里要自己编辑pac文件。新建proxy.pac文件，写入以下代码：function FindProxyForURL(url, host) { return "SOCKS 192.168.0.102:9189"; }
192.168.xxx.xxx就是你电脑的ip,9189是你刚才配置shadowsocks客户端的那个代理端口。将proxy.pac放在你的网站目录中（www.url.com/proxy.pac）
4.手机端的代理：设置 -> 无线局域网-> 点击你连接的无线，在最下边的http代理，选择自动，输入你刚才放置pac文件的地址（http://www.url.com/proxy.pac）
5.完成
1279

** Server Side

Usage

ssserver -p 443 -k password -m aes-256-cfb
To run in the background:

sudo ssserver -p 443 -k password -m aes-256-cfb --user nobody -d start
To stop:

sudo ssserver -d stop
To check the log:

sudo less /var/log/shadowsocks.log
Check all the options via -h. You can also use a Configuration file instead.

** Client Side

PAC里配置需要代理的网址，一般情况下，点击"从GFWList更新本地PAC"即可自动配置。仍然缺少的网址可以手动添加到PAC文件中。

**** Linux下安装

```bash
sudo add-apt-repository ppa:hzwhuang/ss-qt5
sudo apt-get update
sudo apt-get install shadowsocks-qt5
```