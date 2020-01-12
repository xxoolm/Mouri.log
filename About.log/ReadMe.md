# Mouri's Resume

## 简介

- 姓名：卢起 / 男 / 19971205
- 笔名：Mouri_Naruto (MN, 毛利), Naruto Mouri (毛利鸣人), Kenji Mouri (毛利研二)
- 邮箱：Mouri_Naruto@Outlook.com
- 博客：https://mourinaruto.github.io
- GitHub：https://github.com/MouriNaruto
- 远景论坛 ID：Mouri_Naruto
- 吾爱破解 ID：Mouri_Naruto

## 教育

- 2016.09 至 2020.06 (预计) 本科 常熟理工学院 汽车工程学院 汽车服务工程
- 2018.03 至今 常熟理工学院车联网大数据实验室 (301实验室)

## 工作经历

### 初雨团队 (2014.07 至今)

- 概述
  - 实现卷影复制 (VSS) 的快照的获取与销毁，以协助鸭子完成 Dism++ 映像热备份功能
    的开发。
  - 在鸭子同意的情况下，以团队名义在远景论坛发布了 Dism++ 的第一版的帖子。
  - 向鸭子提出 Dism++ 多语言支持的建议，并做出了第一版英文语言包并推广至 My 
    Digital Life 论坛。
  - 开发了 Dism++ NCleaner.dll 清理增强组件，提供 Visual Studio 2017/2019 安装
    源、Package Cache 目录、系统还原点、Windows 事件日志和 Windows Installer 安
    装源缓存的清理功能。
  - 创建了 MINT 项目，整合了来自 ntdll.dll、samlib.dll 和 winsta.dll 的 Windows
    未文档化的用户模式 API 定义，且对 MSVC 工具链进行了优化。
  - 实现了 VC-LTL 项目的使用示例和配置批处理。
  - 现在从忙于 VC-LTL 开发的鸭子手里接手 Dism++，并进行 Dism++ 10.5 分支的开发。
- 体现的个人技能
  - 熟悉 C, C++
  - 熟悉 Win32 SDK, COM, ATL, WTL, STL
  - 熟悉 Visual Studio, IDA

### 常熟理工学院车联网大数据实验室 (301实验室) (2018.03 至今)

- 概述
  - 协助姚锋学长和吴龙飞学长完成物联网平台的开发，在其中添加了对 S7-1200 PLC 的
    支持，重构了展示界面并扩充了其 SDK。
  - 与赵健成合作进行了自动驾驶避障算法的研究。
  - 完成了自动驾驶控制代码的第一次重构，并协助姚锋学长实现了远程驾驶的支持。
  - 与实验室的其他人一同参加了第十六届“挑战杯”，并获取江苏省大学生课外学术科
    技作品竞赛二等奖。
  - 现为实验室车联网与人机交互组组长，并带领后辈进行相关方面的工作。
- 体现的个人技能
  - 熟悉 C, C++, C#, Python
  - 熟悉 ROS (Kinetic, Melodic), Qt, ASP.NET Core
  - 熟悉 CMake (catkin_make, colcon build)

## 技术足迹

### 开源项目

#### NSudo

- 简介
  - 一个强大的系统管理工具，一般用于 TrustedInstaller 令牌获取。
  - 项目地址：https://github.com/M2Team/NSudo
- 已实现特性
  - 以 TrustedInstaller 令牌运行应用
  - 以 System 令牌运行应用
  - 以 当前用户 令牌运行应用 (如果未禁用 UAC，则该模式权限为经过 UAC 提升前的权
    限) 
  - 以 当前进程 令牌运行应用 (该模式一般为经过 UAC 提升后的权限) 
  - 支持对 当前进程 令牌进行 LUA 降权 (等效于 Internet Explorer 的 iertutil.dll
    的内部实现) 
  - 支持简单的特权设置 (启用全部特权、禁用所有特权) 
  - 支持以指定的完整性 (Mandatory Level 或者 Integrity Level) 选项创建进程 (系
    统、高、中、低) 
  - 支持以指定的进程优先级创建进程 (低、低于正常、正常、高于正常、高、实时) 
  - 支持以指定的默认窗口模式创建进程 (显示窗口、隐藏窗口、最大化、最小化) 
  - 支持等创建的进程执行完毕后再退出 (仅命令行模式可用，一般在脚本中使用该特性) 
  - 支持以指定的当前目录创建进程
  - 支持以当前控制台窗口创建进程 (适用于运行基于控制台的应用) 
  - 支持快捷命令列表 (可以通过编辑 NSudo.json 自定义) 
  - 适配多种命令行风格 (看命令行帮助就知道了) 
  - 多语言支持 (简体中文、繁体中文、英语、法语、意大利语) 
  - 完整的高 DPI 支持 (和 Windows Shell 的 DPI 缩放实现一样完美) 
  - 完整的 UI 自动化支持 (能与 Windows 讲述人完美配合) 
  - 多处理器架构支持 (x86、x86-64、ARM、ARM64) 
  - 能在 Windows Vista RTM 及更新平台完美使用本工具
  - 高效能 (由于不需要创建额外的服务和进程，于是效率一般情况下优于同类项目) 
  - 精巧的体积控制 (感谢初雨团队的 VC-LTL) 
  - 以宽松的开源许可发行 (MIT 许可) 
- 引用本项目的部分第三方项目
  - MSMG ToolKit
  - Sledgehammer (原 WUMT Wrapper Script) 
  - "乱世"木马家族 (360 分析报告：http://www.360.cn/n/10477.html) 
- 体现的个人技能
  - 熟悉 C, C++, C#
  - 熟悉 Win32 SDK, COM, ATL, STL, .NET Core
  - 熟悉 Visual Studio, IDA

#### Nagisa

- 简介
  - 一个开源的基于 UWP 平台的文件传输工具
  - 项目地址：https://github.com/Project-Nagisa/Nagisa
- 已实现特性
  - 支持 HTTP, HTTPS, FTP, FTPS, WebSocket and WebSocket Secure 传输协议
  - 多语言支持：英语、西班牙语、简体中文
  - 支持后台下载
  - 支持断点续传
  - 支持单线程多任务下载
- 因本项目产生的开源贡献
  - 推进了 OpenSSL 官方分支对 UWP 平台的支持
    - https://github.com/openssl/openssl/blob/42b3f10b5e461496aab1f74d24103d6902ebfcd5/CHANGES#L350
  - 改善了 OpenSSL 微软分支的效能问题
    - https://github.com/microsoft/openssl/pull/61
- 体现的个人技能
  - 熟悉 C, C++
  - 熟悉 Win32 SDK, WRL, C++/CX, C++/WinRT
  - 熟悉 Visual Studio

### 开源贡献

- OpenSSL
  - https://github.com/openssl/openssl/pulls?q=is:pr+author:MouriNaruto+
  - https://github.com/microsoft/openssl/pulls?q=is:pr+author:MouriNaruto+
- winfile
  - https://github.com/microsoft/winfile/pulls?q=is:pr+author:MouriNaruto+
- CovScript
  - https://github.com/covscript/covscript/pulls?q=is:pr+author:MouriNaruto+
- FFmpegInteropX
  - https://github.com/ffmpeginteropx/FFmpegInteropX/tree/FFmpegUniversal
  - https://github.com/ffmpeginteropx/FFmpegInteropX/pulls?q=is:pr+author:MouriNaruto+

### 技术文章

- 实现每显示器高DPI识别(Per-Monitor DPI Aware)的注意事项
  - https://www.52pojie.cn/thread-512713-1-1.html
- 开启Win10的文件资源管理器的每显示器DPI缩放 (Per-Monitor DPI Aware) 支持
  - https://www.52pojie.cn/thread-506556-1-1.html
- 浅谈Windows 10 Build 9879的磁盘清理的System Compression
  - http://bbs.pcbeta.com/viewthread-1567726-1-1.html
- 浅谈Metro App的沙盒AppContainer
  - http://bbs.pcbeta.com/viewthread-1611980-1-1.html
- 自定义开始屏幕的大小
  - http://bbs.pcbeta.com/viewthread-1524688-1-1.html
- 反汇编Windows系统还原代码的成果
  - http://bbs.pcbeta.com/viewthread-1535789-1-1.html
- Windows系统还原新探 (Windows系统还原的较深入研究) 
  - http://bbs.pcbeta.com/viewthread-1507617-1-1.html
- 原生集成Windows 8/8.1 自带的Windows Defender病毒库的教程
  - http://bbs.pcbeta.com/viewthread-1519551-1-1.html
- 使用系统自带工具把磁盘从MBR转换成GPT的教程
  - http://bbs.pcbeta.com/viewthread-1488892-1-1.html
