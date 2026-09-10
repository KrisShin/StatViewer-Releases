# Third-Party Notices

StatViewer 为闭源商业软件。以下第三方组件随本软件分发，按其各自许可证条款使用。
分发本软件时须保留本文件及各组件版权声明。

## 组件清单

| 组件 | 版本 | 许可证 | 用途 |
|---|---|---|---|
| LibreHardwareMonitorLib | 0.9.6 | MPL-2.0 | 硬件传感器采集（CPU/GPU/主板/磁盘等） |
| DiskInfoToolkit | 1.1.2 | MPL-2.0 | 磁盘信息（LHM 依赖） |
| RAMSPDToolkit-NDD | 1.4.2 | MPL-2.0 | 内存 SPD 读取（LHM 依赖） |
| HidSharp | 2.6.4 | MPL-2.0 | HID 设备访问（LHM 依赖） |
| Microsoft.Diagnostics.Tracing.TraceEvent | 3.1.19 | MIT | FPS 帧率 ETW 采集 |
| CommunityToolkit.Mvvm | 8.4.2 | MIT | MVVM 工具 |
| Microsoft.Extensions.\* / System.Text.Json / System.Management / System.Memory | — | MIT | 依赖注入 / 日志 / JSON / WMI |
| PawnIO 内核驱动（独立安装器随包分发） | — | GPL-2.0-or-later + 特殊例外 | CPU 温度/功耗特权读取 |

许可证全文：
- MPL-2.0：https://www.mozilla.org/en-US/MPL/2.0/
- MIT：https://opensource.org/license/mit/
- GPL-2.0：https://www.gnu.org/licenses/old-licenses/gpl-2.0.html

## PawnIO

Copyright (C) 2026 namazso <admin@namazso.eu>

许可证：GNU GPL v2 或（由您选择）任意更新版本，含以下特殊例外：

> “作为特殊例外，PawnIO 的版权持有人允许您将 PawnIO 程序与按 GNU LGPL
> 发布的自由软件程序或库、以及与**仅通过设备 IO 控制接口与 PawnIO 通信的
> 独立模块**相结合。您可以按照 GNU GPL（针对 PawnIO）及其他相关代码的许可
> 条款复制和分发此类系统，前提是当 GNU GPL 要求分发源代码时，您同时提供
> 其他代码的源代码。”
>
> “此例外不适用于通过 Pawn 接口与 PawnIO 通信的程序。”

StatViewer 以**未修改的官方安装器**形式随包分发 PawnIO，不链接其源码/库，
不使用 Pawn 脚本接口，属于例外条款所述的独立模块，StatViewer 自身代码
不受 GPL 传染。

- 项目主页：https://pawnio.eu
- 源代码：https://github.com/namazso/PawnIO（按 GPL 要求，分发二进制时须提供源码获取途径）

## LibreHardwareMonitorLib

Copyright (c) LibreHardwareMonitor contributors

许可证：MPL-2.0
源代码：https://github.com/LibreHardwareMonitor/LibreHardwareMonitor

## DiskInfoToolkit / RAMSPDToolkit-NDD

Copyright (c) Blacktempel

许可证：MPL-2.0
源代码：https://github.com/Blacktempel/DiskInfoToolkit 、 https://github.com/Blacktempel/RAMSPDToolkit

## HidSharp

Copyright (c) HidSharp contributors

许可证：MPL-2.0
主页：https://software.seekye.com/hidsharp

## Microsoft.Diagnostics.Tracing.TraceEvent

Copyright (c) Microsoft Corporation

许可证：MIT
源代码：https://github.com/microsoft/perfview

## CommunityToolkit.Mvvm

Copyright (c) .NET Foundation and Contributors

许可证：MIT
源代码：https://github.com/CommunityToolkit/dotnet

## Microsoft.Extensions.\* 等 MIT 组件

Copyright (c) Microsoft Corporation

许可证：MIT
组件包括 Microsoft.Extensions.DependencyInjection / Logging / Options、
System.Text.Json、System.Management、System.Memory 等。