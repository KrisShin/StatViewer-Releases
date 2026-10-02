# StatViewer

> 轻量、实时、专注的 Windows 硬件与性能监控工具。普通版完全离线；Pro 版仅在激活、授权校验、版本检查、公告拉取及用户主动使用可选邮箱账号时联网，无广告、无遥测。<br>
> A lightweight, real-time and focused hardware & performance monitor for Windows. Standard is fully offline; Pro connects only for activation, authorization checks, version checks, announcements and optional email-account actions — no ads, no telemetry.

StatViewer 通过桌面悬浮窗实时展示 CPU、GPU、内存、磁盘、网络、电池与 FPS 等关键数据，
帮助用户直接了解计算机当前的运行状态。

StatViewer provides real-time CPU, GPU, memory, disk, network, battery and FPS metrics
in a desktop overlay, helping users understand the current state of their system.

**StatViewer 不做系统管家，不做自动优化建议，只专注于实时数据监控。**  
**StatViewer is not a system manager or optimizer. It focuses on real-time monitoring.**

---

## Editions / 版本

StatViewer is available in two editions.

StatViewer 提供两个版本：

| Edition / 版本 | Distribution / 发布渠道 | Description / 说明 |
|---|---|---|
| **StatViewer Standard** | Microsoft Store | 免费基础版 / Free edition with essential monitoring features |
| **StatViewer Pro** | Official Website & GitHub Releases | 完整功能版 / Full-featured edition |

This repository provides the **official public releases of StatViewer Pro**.

本仓库提供 **StatViewer Pro 的官方公开发行版本**。

For complete product information, visit the official website:

完整产品信息请访问官方网站：

**[StatViewer Official Website](https://statviewer.toputils.top/)**

---

## Features / 功能特性

### Real-Time Monitoring / 实时监控

| Feature / 功能 | Description / 说明 |
|---|---|
| CPU | Usage and frequency; temperature and power (Pro) / 使用率与频率；温度与功耗（Pro） |
| GPU | Usage, VRAM and frequency; temperature, power and model (Pro) / 使用率、显存与频率；温度、功耗与型号（Pro） |
| iGPU | Usage, shared-memory VRAM, frequency and power (Pro), with temperature derived from CPU temperature when no sensor exists / 核显使用率、共享内存显存、频率与功耗（Pro）；无独立温度传感器时按 CPU 温度推算 |
| Memory | Usage, capacity, speed and modules / 内存占用、容量、速度及内存模块 |
| Disk | Capacity, read/write speed, temperature and hardware information; SMART health & details when readable (Pro; NVMe requires Microsoft standard storage driver) / 容量、读写速度、温度及硬件信息；可读取时提供 SMART 健康度与属性详情（Pro；NVMe 需 Microsoft 标准存储驱动） |
| Network | Real-time traffic per adapter, with IPv4/IPv6 details in the Hardware Information page / 按网卡显示实时速率；硬件信息页提供 IPv4/IPv6 明细 |
| Battery | Status, capacity and health information / 电池状态、容量及健康信息 |
| System Power | Estimated total system power consumption (Pro) / 整机功耗估算（Pro） |
| FPS | Foreground-application FPS, 1% Low and sparkline (Pro; requires administrator; ETW host starts only while FPS and at least one FPS detail are enabled) / 前台应用 FPS、1% Low 与迷你曲线（Pro；需管理员；仅 FPS 与至少一个 FPS 子项启用期间启动 ETW Host） |
| Account | Optional email account (recommended, not required), email verification, security-notification toggle, device remark and recovery / 可选邮箱账号（推荐绑定，但不强制）、邮箱验证、安全通知开关、设备备注与原邮箱恢复 |
| Device Migration | Guided authorization migration after major hardware replacement; replacing a disk does not require migration / 更换主要硬件后可按提示迁移授权；更换硬盘不需要迁移 |
| Update Notice | Optional update check and reminder in the About page / 关于页提供检查更新与版本提醒 |

### Desktop Overlay / 桌面悬浮窗

- Real-time performance data at a glance  
  一眼查看整机实时性能状态

- Card and capsule layouts  
  卡片与胶囊两种布局

- Multiple theme presets  
  多套主题预设

- Glow, transparency and scaling  
  辉光、透明度与缩放
- Freely draggable overlay with edge/corner snapping; position remembered per display
  悬浮窗可自由拖拽(边缘 / 四角吸附),按显示器记忆位置

- Designed for desktop and gaming scenarios  
  适用于日常桌面与游戏场景

### Hardware Information / 硬件信息

StatViewer also provides a dedicated hardware information centre for viewing
the system, CPU, memory, GPU, disk, network and other major hardware components.

StatViewer 提供独立的硬件信息中心，用于查看系统、CPU、内存、显卡、磁盘、网络等主要硬件组件。

### System Tools & Logs / 系统工具与日志

- Windows Disk Cleanup for the system drive, optionally pinned to the tray menu / 一键调起系统盘 Windows 磁盘清理，可固定到托盘菜单
- Save the existing Serilog log files from the About page (up to 3 files) / 关于页保存现有 Serilog 日志文件（最多 3 个）

---

## Standard vs Pro / 普通版与 Pro 版

The Standard edition provides essential real-time monitoring through the Microsoft Store.
StatViewer Pro unlocks advanced monitoring and customization features.

普通版通过 Microsoft Store 提供基础实时监控功能；StatViewer Pro 提供完整的高级监控与自定义功能。

| Feature / 功能 | Standard | Pro |
|---|:---:|:---:|
| CPU usage & frequency / CPU 使用率与频率 | ✓ | ✓ |
| CPU temperature & power / CPU 温度与功耗 | — | ✓ |
| GPU usage, VRAM & frequency / GPU 使用率、显存与频率 | ✓ | ✓ |
| GPU temperature, power & model / GPU 温度、功耗与型号 | — | ✓ |
| iGPU usage, shared-memory VRAM & frequency / 核显使用率、共享内存显存与频率 | — | ✓ |
| iGPU temperature, power & model / 核显温度、功耗与型号 | — | ✓ |
| Memory monitoring / 内存监控 | ✓ | ✓ |
| Disk monitoring / 磁盘监控 | ✓ | ✓ |
| Network monitoring & IPv4/IPv6 details / 网络监控与 IPv4/IPv6 明细 | ✓ | ✓ |
| Battery monitoring / 电池监控 | ✓ | ✓ |
| System power estimate / 整机功耗估算 | — | ✓ |
| FPS, 1% Low & sparkline / FPS、1% Low 与曲线 | — | ✓ |
| Optional email account (recommended, not required) / 可选邮箱账号（推荐绑定，不强制） | — | ✓ |
| Device authorization migration / 设备授权迁移 | — | ✓ |
| Update notice / 更新提醒 | — | ✓ |
| Card layout / 卡片布局 | ✓ | ✓ |
| Capsule layout / 胶囊布局 | — | ✓ |
| Default theme / 默认主题 | ✓ | ✓ |
| Theme switching / 主题切换 | — | ✓ |
| Glow, opacity & scaling / 辉光、透明度与缩放 | ✓ | ✓ |
| Hardware information centre / 硬件信息中心 | ✓ | ✓ |
| SMART health & details (Pro; NVMe requires Microsoft standard storage driver) / SMART 健康度与详情（Pro；NVMe 需 Microsoft 标准存储驱动） | — | ✓ |
| Drag overlay & per-display position / 悬浮窗拖拽与按屏位置记忆 | ✓ | ✓ |
| Tools: Windows Disk Cleanup & tray pin / 工具：Windows 磁盘清理与托盘固定 | ✓ | ✓ |
| Save recent logs / 保存最近日志 | ✓ | ✓ |
| Announcement bar / 公告条 | — | ✓ |

> Features may change as StatViewer evolves.  
> 功能可能会随着 StatViewer 的后续版本持续更新。

---

## Design Philosophy / 产品理念

### Real-Time / 实时

StatViewer focuses on the information that matters **right now**.

StatViewer 专注于用户**当前这一刻**真正需要了解的数据。

It is designed to answer questions such as:

它主要用于回答：

- What is my CPU doing right now?
- 当前 CPU 正在以什么状态运行？
- How much power is the GPU using?
- 当前 GPU 正在消耗多少功耗？
- What frequency is the hardware running at?
- 当前硬件运行在什么频率？
- What is the current temperature?
- 当前温度是多少？
- What FPS is the application producing?
- 当前应用的 FPS 是多少？

### Lightweight / 轻量

StatViewer is designed to stay out of the way.

It does not aim to become a general-purpose system management suite.
It provides the monitoring data without unnecessary background features.

StatViewer 不希望成为一个臃肿的系统管理软件。

它只提供硬件与性能监控所需要的数据，不加入与核心用途无关的系统管理功能。

### Focused / 专注

StatViewer does not automatically optimize your computer or tell you how to configure it.

It provides the underlying real-time data and leaves analysis and decision-making to the user.

StatViewer 不负责自动优化，也不会告诉用户应该如何调整系统。

它负责提供真实、及时的数据，分析和决策交给用户自己完成。

---

## Privacy / 隐私

### Standard Edition / 普通版

StatViewer Standard is fully offline.

All monitoring data is collected and processed locally on the user's computer.
The Standard edition makes no network requests and does not collect telemetry,
usage analytics or hardware monitoring data.

**普通版完全离线运行。**

所有监控数据均在本机采集与处理。普通版不进行网络通信，
不收集遥测数据、使用分析数据或硬件监控数据。

- No telemetry / 无遥测
- No analytics / 无使用分析
- No advertising / 无广告
- No account required / 无需账号
- No hardware data upload / 不上传硬件监控数据

### Pro Edition / Pro 版

StatViewer Pro does not collect telemetry or hardware monitoring data.

Network communication is limited to license activation, authorization checks,
version checks, announcement retrieval and optional account actions initiated
by the user.

**Pro 版不收集遥测数据，也不会上传硬件监控数据。**

Pro 版仅在许可证激活、授权校验、版本检查、公告拉取及用户主动使用的可选
邮箱账号操作中进行网络通信。

During Pro activation and authorization checks, StatViewer uses purpose-specific
salted HMAC-SHA256 hashes of CPU, motherboard and boot-drive hardware serials.
It no longer uses an Install ID or device_id. Plaintext hardware identifiers are
neither displayed nor uploaded. The optional email account is recommended but
not required; if used, only the email, verification state and account credential
required for account ownership, support lookup and security notices are collected.

Pro 版激活与授权校验使用 CPU、主板和启动盘硬件序列号的用途专属加盐 HMAC-SHA256 哈希，不再使用 Install ID 或 device_id，不展示或上传明文硬件标识。可选邮箱账号推荐绑定，但不强制；仅在用户主动使用时采集账号归属、客服定位和安全通知所需的邮箱、验证状态与账号凭据。

For complete privacy details, please refer to the official privacy policy.

完整隐私说明请参阅官方网站上的隐私政策。

**[Privacy Policy / 隐私政策](https://statviewer.toputils.top/privacy)**

---

## Permissions / 权限说明

- **Administrator privilege (optional, Pro only)**: FPS monitoring uses ETW and requires administrator privilege. Pro launches the dedicated `StatViewer.FpsHost.exe` only while FPS and at least one FPS detail are enabled; the host exits when FPS or all FPS details are disabled. Pro may also install the PawnIO kernel driver with UAC confirmation to read CPU/GPU temperature and power.
- **管理员权限（可选，仅 Pro 版）**：FPS 监控使用 ETW，需要管理员权限。Pro 仅在 FPS 与至少一个 FPS 子项启用期间启动专用 `StatViewer.FpsHost.exe`，FPS 或全部 FPS 子项关闭后 Host 退出；Pro 也可在 UAC 确认后安装 PawnIO 内核驱动以读取 CPU/GPU 温度与功耗。
- **Standard**: never requests elevation, never shows UAC and installs no drivers.
- **普通版**：不请求提权、不弹出 UAC，也不安装任何驱动。

---

## Download / 下载

### StatViewer Pro

**Latest Release / 最新版本：`v1.4.0`**

| Edition / 版本 | Format / 格式 | Architecture / 架构 | GitHub | Gitee |
|---|---|---|---|---|
| Installer / 安装版 | MSI | x64 | [Download](https://github.com/KrisShin/StatViewer-Releases/releases/latest/download/StatViewer-Pro-installer-v1.4.0-x64.msi) | [Download](https://gitee.com/KrisShin/stat-viewer-releases/releases/download/v1.4.0/StatViewer-Pro-installer-v1.4.0-x64.msi) |
| Installer / 安装版 | MSI | x86 | [Download](https://github.com/KrisShin/StatViewer-Releases/releases/latest/download/StatViewer-Pro-installer-v1.4.0-x86.msi) | [Download](https://gitee.com/KrisShin/stat-viewer-releases/releases/download/v1.4.0/StatViewer-Pro-installer-v1.4.0-x86.msi) |
| Portable / 便携版 | ZIP | x64 | [Download](https://github.com/KrisShin/StatViewer-Releases/releases/latest/download/StatViewer-Pro-portable-v1.4.0-x64.zip) | [Download](https://gitee.com/KrisShin/stat-viewer-releases/releases/download/v1.4.0/StatViewer-Pro-portable-v1.4.0-x64.zip) |
| Portable / 便携版 | ZIP | x86 | [Download](https://github.com/KrisShin/StatViewer-Releases/releases/latest/download/StatViewer-Pro-portable-v1.4.0-x86.zip) | [Download](https://gitee.com/KrisShin/stat-viewer-releases/releases/download/v1.4.0/StatViewer-Pro-portable-v1.4.0-x86.zip) |

> This repository provides the official public releases of **StatViewer Pro**.
>
> 本仓库提供 **StatViewer Pro 的官方公开发行版本**。

### Standard Edition / 普通版

StatViewer Standard is distributed through the Microsoft Store.

StatViewer 普通版通过 Microsoft Store 发布，并支持商店自动更新。

**[Get StatViewer Standard from Microsoft Store / 从 Microsoft Store 获取普通版](https://apps.microsoft.com/detail/9PPJKKZMJ9NF)**

---

## System Requirements / 系统要求

- Windows 10 version 1809 or later, or Windows 11 / Windows 10 1809 或更高版本，或 Windows 11
- .NET Framework 4.8 (bundled with Windows 10/11; no runtime installation required) / .NET Framework 4.8（Windows 10/11 自带，无需安装运行时）
- x64 / x86 (x64 recommended) / x64 / x86（推荐 x64）

---

## Installation / 安装

### Pro Installer / Pro 安装版

Download the MSI package and run the installer.

下载 MSI 安装包并运行安装程序。

The installer provides Start Menu and Desktop shortcuts.

安装程序会创建开始菜单与桌面快捷方式。

### Pro Portable / Pro 便携版

Download the ZIP package, extract it to any directory, and run StatViewer.

下载 ZIP 压缩包，解压到任意目录后即可运行 StatViewer。

No installation is required.

无需安装。

### Standard / 普通版

Get StatViewer Standard from the Microsoft Store.

普通版请通过 Microsoft Store 获取。

---

## Release History / 版本历史

Complete release history and changelogs are available here:

完整版本历史与更新日志：

**[GitHub Releases](https://github.com/KrisShin/StatViewer-Releases/releases)**

**[Gitee Releases](https://gitee.com/KrisShin/stat-viewer-releases/releases)**

---

## Official Links / 官方链接

- **Official Website / 官方网站:** [StatViewer](https://statviewer.toputils.top/)
- **Microsoft Store / Microsoft Store:** [StatViewer Standard](https://apps.microsoft.com/detail/9PPJKKZMJ9NF)
- **GitHub Releases / GitHub 发行仓库:** [StatViewer-Releases](https://github.com/KrisShin/StatViewer-Releases)
- **Gitee Releases / Gitee 发行仓库:** [StatViewer Releases](https://gitee.com/KrisShin/stat-viewer-releases)

---

## About / 关于

StatViewer is an independent Windows application developed by two developers: [Kris Lyu](https://github.com/KrisShin) and [Elyven](https://github.com/liuyashoot).

StatViewer 是一款独立开发的 Windows 应用程序,由 [Kris Lyu](https://github.com/KrisShin) 与 [Elyven](https://github.com/liuyashoot) 两人共同开发。

**StatViewer Standard and StatViewer Pro are two editions of the same product,
distributed through different channels with different feature sets.**

**StatViewer 普通版与 Pro 版属于同一产品的两个版本，
通过不同渠道发行，并提供不同的功能范围。**

---

## License / 许可

StatViewer Standard is free.

StatViewer Pro is a paid edition with online license activation and validation.

StatViewer 普通版免费。

StatViewer Pro 为付费版本，通过在线许可证激活与授权校验提供授权服务。

Third-party component licenses and notices are included with the corresponding release.

第三方组件的许可证及相关声明包含在对应发行版本中。

**[Third-Party Notices / 第三方声明 (GitHub)](https://github.com/KrisShin/StatViewer-Releases/blob/main/THIRD-PARTY-NOTICES.md)**  ·  **[Third-Party Notices / 第三方声明 (Gitee)](https://gitee.com/KrisShin/stat-viewer-releases/blob/main/THIRD-PARTY-NOTICES.md)**
