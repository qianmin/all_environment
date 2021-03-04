1.PCL的安装

在 Ubuntu 1604，PCL库已经存在于公共软件源中，直接安装即可。

sudo apt-get install libpcl-dev



由此即可安装编译好的点云库（PCL-1.7），附带安装了VTK-6.2.0等依赖库。

安装后的编译过程可能会出现库文件vtkproj4.so丢失的问题。为解决该问题可以直接软链接解决。代码如下：

sudo ln -s /usr/lib/libvtkproj4.so.5.10 /usr/lib/libvtkproj4.so


至此，PCL的安装就完成了。
2.PCL的可视化工具——pcl-viewer的安装

pcl-viewer是常用得pcl可视化工具。若不需要此工具请忽略此节。可以直接按照以下代码安装：

sudo apt-get install  pcl-tools


若无法定位软件包，可以改变一下软件源。本人用阿里源的时候出现无法定位软件包的问题，更换清华源后解决。

3.PCL的简单测试
。。。。
