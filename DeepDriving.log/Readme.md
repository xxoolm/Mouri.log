# DeepDriving.log

[DeepDriving](http://deepdriving.cs.princeton.edu/)
是普林斯顿大学提供的基于卷积神经网络的用来实现自动驾驶的解决方案。
也是我在自己所在大学的实验室摸索过的项目之一，
为了帮助未来的自己更快的想起这些经历，于是我在这里写点笔记。

- [安装](#安装)
  - [安装一个 Linux 发行版](#安装一个-Linux-发行版)
  - [下载 DeepDriving 源代码](#下载-DeepDriving-源代码)
  - [升级当前系统](#升级当前系统)
  - [安装 DeepDriving 自带的魔改版 TORCS](#安装-DeepDriving-自带的魔改版-TORCS)
  - [安装 DeepDriving 自带的魔改版 Caffe](#安装-DeepDriving-自带的魔改版-Caffe)
- [测试](#测试)

## 安装

### 安装一个 Linux 发行版
选择一个你用起来舒服的 Linux 发行版即可，我用的是`Xubuntu 16.04`。

### 下载 DeepDriving 源代码
请到 http://deepdriving.cs.princeton.edu/ 下载 DeepDrivingCode_v2.zip。然后使用
你用起来舒服的解压缩工具解压到你想解压的目录。我把压缩包解压在`~/workspace`下。

### 升级当前系统
在安装 DeepDriving 前，我们需要升级一下自己正在使用的 Linux 发行版。如果你和我
用的一样的环境，那么你可以像我一样输入下面的命令，按照提示操作即可。
> sudo apt-get update

> sudo apt-get upgrade

如果你刚刚安装好你的环境，也许还需要安装 gcc 编译器。如果你和我用的一样的环境，
那么你可以像我一样输入下面的命令，按照提示操作即可。
> sudo apt-get install build-essential

### 安装 DeepDriving 自带的魔改版 TORCS
由于 DeepDriving 使用其自带的魔改版 TORCS 进行效果的演示，
所以我们需要安装下这家伙。

首先我们得为其安装依赖。如果你和我用的一样的环境，
那么你可以像我一样输入下面的命令，按照提示操作即可。
> sudo apt-get install libplib-dev libopenal-dev libalut-dev libvorbis-dev libxxf86vm-dev libxmu-dev libxi-dev libxrender-dev libxrandr-dev libz-dev libpng-dev

然后切换到`DeepDriving/torcs-1.3.6`目录，实际做法依你解压的目录而定。
我的例子如下：
> cd ~/workspace/DeepDriving/torcs-1.3.6

接着我们就可以开始安装了。
> ./configure

> make

> sudo make install

> sudo make datainstall

再接着我们需要使用 root 用户权限将`DeepDriving/modified_tracks`
目录的全部内容复制到`/usr/local/share/games/torcs/tracks/road`下即可。

最后我们在终端输入`torcs`看其是否能正常运行即可。

## 安装 DeepDriving 自带的魔改版 Caffe
由于 DeepDriving 使用其自带的魔改版 Caffe 进行训练和重载用于自动驾驶的神经网络，
当然，我们必须要安装这家伙。关于 Caffe 的配置教程很多，
但由于我在虚拟机下运行 DeepDriving，这个用途应该是比较少见的。
且其自带的 Caffe 又比较老，于是要多费一些功夫去配置。
如果你也碰到和我一样的情况，那么就请接着阅读本段，
否则你需要选择性阅读本段且需要额外查阅资料。

首先我们得为其安装依赖。如果你和我用的一样的环境，
那么你可以像我一样输入下面的命令，按照提示操作即可。
> sudo apt-get install --no-install-recommends libboost-all-dev

> sudo apt-get install libprotobuf-dev libleveldb-dev libsnappy-dev libopencv-dev libhdf5-serial-dev protobuf-compiler libgflags-dev libgoogle-glog-dev liblmdb-dev libatlas-base-dev python3-dev

然后切换到`DeepDriving/Caffe_driving`目录，实际做法依你解压的目录而定。
我的例子如下：
> cd ~/workspace/DeepDriving/Caffe_driving

下载 [Modifiled_Caffe_driving.zip](Modifiled_Caffe_driving.zip)，
并解压到`DeepDriving/Caffe_driving`中，
以使 DeepDriving 自带的魔改版 Caffe 支持仅 CPU 模式。

最后我们就可以开始安装了。
> make

## 测试
0. 请确保按照你已经成功安装好 DeepDriving。
1. 首先运行`torcs`，然后再运行`DeepDriving/Caffe_driving/torcs/torcs_test.sh`。
2. 在游戏中，接连点击`Quick Race`和`Configure Race`，
   选择一个带有`chenyi-`前缀的修改版赛道。（
   如果你没有修改`DeepDriving/Caffe_driving/torcs/torcs_test.sh`，
   也就是三条道示例的话，请选择`chenyi-E-Track 6`。）
3. 接着按照下面的顺序设置游戏中的驾驶员排序。
   ```
   1 chenyi_AI12
   2 chenyi_AI11
   ...
   12 chenyi_AI1
   13 chenyi
   ```
4. 进入游戏，按`1`到`6`、`9`、`M`键以移除游戏中的控件，
   按`F2`键切换到驾驶员第一视角。神经卷积网络程序默认是暂停的，
   请切换到`visualization`窗口，接着按下`P`让其开始执行。
   让游戏画面中的车子先跑一段时间，
   然后按下`C`键激活控制器让车子跑起来。
   （`top-down view`窗口背景如果是红色的话，则控制器是被禁用的。）
   提示：你也许需要按`Page Up`和`Page Down`键切换到我们的车子即`chenyi`的视角。
5. 最后由于其他的车子都以不同速度匀速行驶且我们的车子速度则是最快的，
   于是你将会看到我们的车子就像秋名山老司机那样把他们一个一个超过去。
