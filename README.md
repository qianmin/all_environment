# all_environment
所有乱七八糟的配置！！！！

装驱动
# 司马conda
```
conda config --set remote_max_retries 1000000000000000
conda config --set remote_connect_timeot_secs 100
conda config --set remote_read_timeot_secs 100
```
```
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --set show_channel_urls yes
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/

conda install pytorch torchvision cudatoolkit=10.2
```
自动进入base取消
conda config --set auto_activate_base false

alias torch18='conda activate torch18'


司马pip
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple

python -m pip install --upgrade pip  --timeout 6000


# 华子
## python %APPDATA% pip.ini
```
[global]
index-url = http://cmc-cd-mirror.rnd.huawei.com/pypi/simple/
trusted-host = cmc-cd-mirror.rnd.huawei.com
```
