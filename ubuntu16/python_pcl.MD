# 1 源码安装
```
1：先装pcl
sudo apt-get update -y
sudo apt-get install libpcl-dev -y

2开始下载源码pcl
git clone https://github.com/strawlab/python-pcl.git
cd pcl=python

3进入conda环境
注意：别瞎鸡巴装xxpcl，都不对，pip list 看看，然后都卸载

python setup.py build_ext -i
python setup.py install
（等一等）
```
# 2 conda一句话（没试过，官网教材）
```
conda config --add channels conda-forge # add conda-forge channels 
conda install -c sirokujira python-pcl # pcl installation 
conda install -c jithinpr2 gtk3 # Gtk+ Gui dependency 
conda install -y ipython # install ipython 
conda install -y jupyter # install jupyter
```
