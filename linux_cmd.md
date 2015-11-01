df -h 显示挂载的所有文件系统的用量
rm -rf 删除目录和文件及子目录和子文件(小心操作)
mount /dev/cdrom /mnt 挂载光驱到/mnt

关机
shutdown -h 10 十分钟后关机
shutdown -h 23:30 下一个23：30关机
shutdown -h now 立即关机
reboot 重启

查看当前系统版本
cat /etc/redhat-release
所有指令均在CentOS Linux release 7.1.1503中测试

centos7 远程桌面

** 安装jekyll

sudo apt-get install ruby
修改ruby源
gem sources --add https://ruby.taobao.org/ --remove https://rubygems.org/
gem sources -l
在ubuntu15.10下安装还需要安装下两步
sudo apt-get install ruby-dev
sudo apt-get install zlib1g-dev
然后就可以安装了
sudo gem install github-pages
sudo gem install jekyll