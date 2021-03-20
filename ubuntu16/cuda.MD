 ```
 sudo apt-get remove --purge nvidia*
 #若安装失败也是这样卸载以及
 ./NVIDIA-Linux-x86_64-390.48.run --uninstall #确保卸载干净。
 
 
 #其实很多你的环境已经安装了，所以一般并没有多少时间。
 sudo apt-get update 
 sudo apt-get install dkms build-essential linux-headers-generic
 sudo apt-get install gcc-multilib xorg-dev
 sudo apt-get install freeglut3-dev libx11-dev libxmu-dev install libxi-dev  libgl1-mesa-glx libglu1-mesa libglu1-mesa-dev
 
 
  sudo vi /etc/modprobe.d/blacklist-nouveau.conf 
 #在文件 blacklist-nouveau.conf 中加入如下内容：
  blacklist nouveau
  blacklist lbm-nouveau
  options nouveau modeset=0
  alias nouveau off
  alias lbm-nouveau off
  #保存   :wq
  
  
  #禁用nouveau 内核模块
echo options nouveau modeset=0 | sudo tee -a /etc/modprobe.d/nouveau-kms.conf
sudo update-initramfs -u
reboot #重启
lsmod |grep nouveau #无显示则成功 当然驱动没了你的桌面分辨率会比较大。

sudo service lightdm stop
cd 下载目录
chmod a+x NVIDIA-Linux-x86_64-384.90.run #添加权限
sudo ./NVIDIA-Linux-x86_64-384.90.run --dkms 台式机
sudo ./NVIDIA-Linux-x86_64-384.90.run --dkms --no-opengl-files 笔记本电脑


nvidia-smi #若列出GPU的信息列表，表示驱动安装成功
sudo service lightdm start #没自动跳的话 crtl+alt+f7
nvidia-settings #若弹出设置对话框，亦表示驱动安装成功
```
