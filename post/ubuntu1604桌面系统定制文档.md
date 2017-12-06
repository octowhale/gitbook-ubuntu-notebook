# ubuntu 1604 优化指南
## 安装 gnome 界面工具

sudo apt-get install gnome-tweak-tool

## fcitx 输入法黑框问题
>> http://forum.ubuntu.org.cn/viewtopic.php?t=473340

```bash
sudo killall fcitx-qimpanel
sudo dpkg -r fcitx-ui-qimpanel
```

everything-like in ubuntu
fsearch: http://www.omgubuntu.co.uk/2016/10/fsearch-fast-file-search-tool-linux
catfish: http://forum.ubuntu.org.cn/viewtopic.php?t=257536

# 安装主题
http://tieba.baidu.com/p/4718551318
http://piaolingspace.blogspot.com/2017/07/ubuntu-1604-gnome.html
http://blog.topspeedsnail.com/archives/4726
http://blog.topspeedsnail.com/archives/5124

arc-theme安装方法：

sudo add-apt-repository ppa:noobslab/themes
sudo apt-get update 
sudo apt-get install arc-theme 


安装gnome-tweak-tool用于切换主题：
sudo apt-get install gnome-tweak-tool
运行gnome-tweak-tool选择Arc-Dark为GTK+主题。


# 安装字体
http://www.mycode.net.cn/platform/741.html


# 挂在 smb
http://blog.csdn.net/maowenbin/article/details/5603679

sudo apt install smbclient

SMB_USER="uyinn@live.com"
SMB_PASS="SirTang(x)_2BankNo3"
SMB_AUTH="username=${SMB_USER},password=${SMB_PASS}"
PRIVILEGES="uid=1000,gid=1000"

sudo mount -t cifs //192.168.56.1/Documents $HOME/Documents -o ${SMB_AUTH},$}{PRIVILEGES},rw
