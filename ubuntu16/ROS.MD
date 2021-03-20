ros update 一直timeout
```
更改 /usr/lib/python2.7/dist-packages/rosdep2/下的三个文件sources_list.py、gbpdistro_support.py、rep3.py
中的DOWNLOAD_TIMEOUT = 15.0值，改大一点就可以了。
操作如下
sudo vim /usr/lib/python2.7/dist-packages/rosdep2/gbpdistro_support.py
```
