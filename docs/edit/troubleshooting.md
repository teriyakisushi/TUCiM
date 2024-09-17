可能会出现的问题

## pip下载包过慢

使用如下命令将pip设置为**清华大学镜像源**

```shell
python -m pip install --upgrade pip
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
```

完成后重新使用pip安装依赖包

## git clone过慢

方法1：使用梯子

方法2：使用[Watt Toolkit](https://steampp.net/) 对Github加速

## 本地的梯子在WSL中无法使用

在 **Clash for Windows** 中 开启 "Allow LAN"，再开启 "TUN Mode" 即可。

> 若你的Clash版本比较低，那么需要你在开启 `Allow LAN` 后在WSL中编辑httpProxy变量，如下：

```shell
vim ~/.bashrc # 若使用zsh则为 ~/.zshrc
# ip为你PC的本地ipv4地址
# 7890为Clash的默认端口
export http_proxy=http://ip:7890 
export https_proxy=http://ip:7890
source ~/.bashrc
```

### 验证
    
```shell
curl -I google.hk
```
