# LCM.log

[LCM](https://github.com/lcm-proj/lcm) 是一个开源的轻量级且跨平台的进程通信库。
在自己所在的实验室里，曾经使用该项目实现 C++ 应用与 Python3 脚本的跨进程通信。
本文记录一些与这个有关的笔记。

- [安装](#安装)
  - [本文环境说明](#本文环境说明)
  - [安装依赖](#安装依赖)
  - [编译安装](#编译安装)
  - [在 Python3 注册 LCM 模块](#在-Python3-注册-LCM-模块)

## 安装

### 本文环境说明
- 系统：Xubuntu 16.04

### 安装依赖
> sudo apt-get install build-essential libglib2.0-dev python3-dev cmake

### 编译安装
```
mkdir build
cd build
cmake -DPYTHON_EXECUTABLE=/usr/bin/python3 ..
make
sudo make install
```

### 在 Python3 注册 LCM 模块
```
PYTHON_VERSION=$(/usr/bin/python3 -c "import sys; print(\"%s.%s\" % sys.version_info[:2])")
PYTHON_USER_SITE=$(/usr/bin/python3 -m site --user-site)
mkdir -p $PYTHON_USER_SITE
echo "$LCM_LIBRARY_DIR/python$PYTHON_VERSION/site-packages" > $PYTHON_USER_SITE/lcm.pth
```
