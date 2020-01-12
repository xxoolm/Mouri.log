# Mouri's Resume

## 简介

- 姓名：卢起 / 男 / 19971205 / 本科 常熟理工学院 汽车服务工程
- 笔名：Mouri_Naruto (MN, 毛利), Naruto Mouri (毛利鸣人), Kenji Mouri (毛利研二)
- 手机：(+86) 182-6175-7560
- 邮箱：Mouri_Naruto@Outlook.com
- GitHub：https://github.com/MouriNaruto
- 博客：https://mourinaruto.github.io
- 论坛 ID：Mouri_Naruto (主要混迹于远景论坛和吾爱破解论坛)

## 技能

- 熟悉 C, C++, C#, Python
- 熟悉 Windows SDK (Win32, COM, ATL, WTL, WRL, C++/CX, C++/WinRT)
- 熟悉 .NET Framework (包括 WPF, Windows Forms)
- 熟悉 .NET Core (包括 ASP.NET Core), ROS (Kinetic, Melodic), Qt
- 熟悉 EDK II, Project Mu
- 熟悉 Visual Studio, IDA, CMake (包括 catkin_make, colcon build), Git, VSTS

## 开源项目

### NSudo (https://github.com/M2Team/NSudo)

- 一个强大的系统管理工具，一般用于 TrustedInstaller 令牌获取。
- 引用本项目的部分第三方项目
  - [MSMG ToolKit](https://forums.mydigitallife.net/threads/50572/)
  - [Sledgehammer (原 WUMT Wrapper Script)](https://forums.mydigitallife.net/threads/72203/)
  - "乱世"木马家族 ([360 分析报告](http://www.360.cn/n/10477.html))

### Nagisa (https://github.com/Project-Nagisa/Nagisa)

- 一个基于 UWP 平台的文件传输工具，还处于早期开发阶段。
- 因本项目产生的开源贡献
  - [推进了 OpenSSL 官方分支对 UWP 平台的支持](https://github.com/openssl/openssl/blob/42b3f10b5e461496aab1f74d24103d6902ebfcd5/CHANGES#L350)
  - [改善了 OpenSSL 微软分支的效能问题](https://github.com/microsoft/openssl/pull/61)

## 开源贡献

- 推进和改善了 OpenSSL [官方分支](https://github.com/openssl/openssl/pulls?q=is:pr+author:MouriNaruto+)和[微软分支](https://github.com/microsoft/openssl/pulls?q=is:pr+author:MouriNaruto+)对 UWP 平台的支持。 
- 添加了[微软开源的旧版文件管理器 winfile](https://github.com/microsoft/winfile/pulls?q=is:pr+author:MouriNaruto+) 的简体中文支持并共同确定了多语言支持目录结构。
- 改善了 [Covariant Script 编程语言](https://github.com/covscript/covscript/pulls?q=is:pr+author:MouriNaruto+)的 Windows 平台体验。
- 创建了 [FFmpegInteropX](https://github.com/ffmpeginteropx/FFmpegInteropX/pulls?q=is:pr+author:MouriNaruto+) 项目的 [FFmpeg 单动态链接库文件分支](https://github.com/ffmpeginteropx/FFmpegInteropX/tree/FFmpegUniversal)。
- 在进行使用 Windows GDI 进行部分加速的软件 3D 渲染器的开发，[争取合并入 imgui 项目主分支](https://github.com/ocornut/imgui/pull/2724)。

<div style="page-break-after: always; break-after: page;"></div>

## 工作经历

### 初雨团队 (2014.07 至今)

- 参与了 Dism++ 映像热备份功能的开发和多语言方面的适配工作。
- 开发了 Dism++ NCleaner.dll 清理增强组件，提供 Visual Studio 2017/2019 安装源、Package Cache 目录、系统还原点、Windows 事件日志和 Windows Installer 安装源缓存的清理功能。
- 创建了 MINT 项目，整合了来自 ntdll.dll、samlib.dll 和 winsta.dll 的 Windows 未文档化的用户模式 API 定义，且对 MSVC 工具链进行了优化。
- 实现了 VC-LTL 项目的使用示例和 Visual Studio 集成的部分工作。
- 现在进行 Dism++ 10.5 分支的开发。

### 常熟理工学院车联网大数据实验室 (301实验室) (2018.03 至今)

- 参与了实验室物联网平台的开发，在其中添加了对 S7-1200 PLC 的支持，重构了展示界面并扩充了其 SDK。
- 合作进行了自动驾驶避障算法的研究。
- 完成了自动驾驶控制代码的第一次重构，并实现了远程驾驶的控制端支持。
- 合作参加第十六届“挑战杯”，并获取江苏省大学生课外学术科技作品竞赛二等奖。
- 现为实验室车联网与人机交互组组长，并带领后辈进行相关方面的工作。 

## 技术文章

- [实现每显示器高DPI识别(Per-Monitor DPI Aware)的注意事项](https://www.52pojie.cn/thread-512713-1-1.html)
- [开启Win10的文件资源管理器的每显示器DPI缩放 (Per-Monitor DPI Aware) 支持](https://www.52pojie.cn/thread-506556-1-1.html)
- [浅谈Windows 10 Build 9879的磁盘清理的System Compression](http://bbs.pcbeta.com/viewthread-1567726-1-1.html)
- [浅谈Metro App的沙盒AppContainer](http://bbs.pcbeta.com/viewthread-1611980-1-1.html)
- [自定义开始屏幕的大小](http://bbs.pcbeta.com/viewthread-1524688-1-1.html)
- [反汇编Windows系统还原代码的成果](http://bbs.pcbeta.com/viewthread-1535789-1-1.html)
- [Windows系统还原新探 (Windows系统还原的较深入研究)](http://bbs.pcbeta.com/viewthread-1507617-1-1.html)
- [原生集成Windows 8/8.1 自带的Windows Defender病毒库的教程](http://bbs.pcbeta.com/viewthread-1519551-1-1.html)
- [使用系统自带工具把磁盘从MBR转换成GPT的教程](http://bbs.pcbeta.com/viewthread-1488892-1-1.html)
