## 1. 更换镜像源
```
$:sudo pacman-mirrors -i -c China -m rank
$:sudo pacman -Syy
```
我选用的是阿里云的源  
修改/etc/pacman.conf，在最后一行添加  
```
[archlinuxcn]
SigLevel = Optional TrustedOnly
Server = https://mirrors.aliyun.com/archlinuxcn/$arch
```
然后命令行运行：
```
sudo pacman -S archlinuxcn-keyring
sudo pacman -Syy
```

## 2.常用软件安装
1.yay
```
sudo pacman -S yay
```

2.搜狗输入法(第三步的时候报找不到，也没有安装上)

```
sudo pacman -S fcitx-im #全部安装
sudo pacman -S fcitx-configtool
sudo pacman -S fcitx-sogoupinyin
```
添加输入法配置文件，在~/.xprofile中添加如下内容
```
export GTK_IM_MODULE=fcitx
export QT_IM_MODULE=fcitx
export XMODIFIERS="@im=fcitx"
 ```

3.vim
```
sudo pacman -S vim
```

4.VLC视频播放器
```
yay pacman -S vlc

```

5.网易云
```
sudo pacman -S  netease-cloud-music
```

安装的时候提示包损坏，更新下密钥签名（试了没有用，还是报同样的错误）
```
sudo pacman-key --refresh-keys  //从密钥服务器中更新制定的或所有的密钥
sudo pacman -Sy archlinux-keyring //重新安装下archlinux-keyring
```

6.docker
```
docker
```

7.音乐播放器Clementine
```
yay -S clementine
```

8.安装Axel
```
yay -S axel  
```
使用axel下载东西
```
axel -a [下载地址]
```
