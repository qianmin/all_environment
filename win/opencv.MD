①官网下载win release

②环境变量D:\software\opencv\release451\opencv\build\x64\vc15\bin

③opencv_world451d.dll和opencv_world451.dll丢到system32

qt使用：
```
INCLUDEPATH+= D:\software\opencv\release451\opencv\build\include
LIBS += -LD:/software/opencv/release451/opencv/build/x64/vc15/lib/ -lopencv_world451d
```
