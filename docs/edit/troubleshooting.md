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
