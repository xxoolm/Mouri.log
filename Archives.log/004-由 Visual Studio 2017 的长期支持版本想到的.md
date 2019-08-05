# 由 Visual Studio 2017 的长期支持版本想到的

更新于 2018 年 9 月 2 日

[TOC]

## 发现和体验
- 前几天，我得知微软发布了 Visual Studio 2017 版本 15.8.2 更新，于是我习惯性的
  看了下其更新日志。其中在修复的问题列表中有一条“Git network operations not 
  working: Cannot spawn git-askpass.exe.”引起了我的注意，毕竟我经常因为这个问
  题而困扰。在阅读这个问题在 Visual Studio 社区的讨论贴的时候，发现有位微软员工
  说“Thank you for your feedback! We have fixed this issue and it's available 
  in VS 15.8.2 and 15.0.18. Thank you for helping us build a better Visual 
  Studio!”我对此表示惊讶，因为现在 Visual Studio 2017 版本已经出到 15.8.2，最
  早的 15.0 不是上古版本吗，为什么还有更新？带着疑惑我看了下 Visual Studio 2017
  版本 15.0.x 的更新日志，发现虽然一直在更新，但仅仅是修复各种 Bug 而已。于是我
  认为这应该就是 Visual Studio 2017 提供的长期支持版本。
- 这个版本并不提供公开的下载链接，只有你登陆了你的微软账户且开启了每个人都能免
  费开启的 Visual Studio Dev Essentials 订阅后才能下载。
- 安装的时候，一股令人怀念的感觉扑面而来。由于没有带任何 Visual Studio 2017 版
  本 15.1 及之后版本才有的新功能和新 SDK 支持，于是相对最新版本的 Visual Studio
  2017 的体积小了不少，安装我所需要的组件后只要 15GiB。于是我也顺理成章的安装了。
  安装后发现其自带的 MSVC 编译器是 Visual Studio 最开始的版本。由于之前告诉了鸭
  子 Visual Studio 2017 长期支持版本的存在，于是鸭子希望我能看下长期版本的 MSVC
  编译器版本以能够让 VC-LTL 适配。但我把版本号告诉鸭子后，鸭子表示 VC-LTL 已经
  支持了这个版本，于是并不需要任何额外的操作。
- 貌似由于是长期支持版本，也许是从新版本代码同步能够修复的内容的缘故，部分 UI 
  描述没有被本地化。

## 感想
- 由于现在 Visual Studio 2017 和 Office 365 一样采用滚动更新，于是我觉得当微软
  所说的下一代 Visual Studio 即 Visual Studio 2019 发布的时候，对于我这种早已经
  用上滚动更新的用户，应该并不会觉得下一代 Visual Studio 有太大的惊喜，就像 
  Office 365 从 Office 2013 升级到 2016 再升级到现在的最新的滚动更新版本那样。
  但是对于那些用着长期支持版本的用户而言，升级到下一代产品我觉得应该还是会惊讶
  一下的。
- 我个人觉得 Visual Studio 2017 长期支持版本由于功能够用而且体积相对小巧，应该
  适合在虚拟机里面安装使用。