# Third-Party Notices

StatViewer 是一款独立开发的 Windows 桌面应用。它随包分发或在构建时使用以下
第三方组件，各自遵循其许可证。

## PawnIO 驱动安装器

- 文件：`redist/PawnIO_setup.exe`，版本随安装包
- 版权：Copyright (C) namazso <admin@namazso.eu>
- 许可证：**GNU GPL v2 或（由您选择）任意更新版本，含独立程序例外条款**
- 项目主页：https://pawnio.eu
- 源代码：https://github.com/namazso/PawnIO

StatViewer 以**未修改的官方安装器**形式随包分发 PawnIO，不链接其源码或库，
不使用 Pawn 脚本接口，仅通过设备 I/O 控制接口与驱动通信——属于例外条款所述的
独立程序，本程序自身代码不受 GPL 传染。

## PawnIO 模块

- 文件：`pawnio-modules/AMDFamily17.bin`、`IntelMSR.bin`、`LpcIO.bin`
- 版权：Copyright (C) namazso 及 PawnIO.Modules 贡献者
- 许可证：**GNU LGPL v2.1**
- 来源：https://github.com/namazso/PawnIO.Modules

这些模块被编译进 `StatViewer.exe`，运行时装入 PawnIO 驱动。按 LGPL 的要求，
**其完整源代码随本仓库与每个发行版的安装包一并提供**，位于
`pawnio-modules/source/`；`pawnio-modules/COPYING` 为其许可证全文。

## Rust 依赖

| 组件 | 用途 | 许可证 |
|---|---|---|
| `windows` / `windows-numerics` | Win32、Direct2D、DirectComposition、DirectWrite、PawnIO 的接口绑定 | MIT OR Apache-2.0 |
| `serde` / `serde_json` | 设置文件的读写 | MIT OR Apache-2.0 |
| `zip` | 便携版在线更新包的原生 ZIP 读取 | MIT |
| `flate2` / `crc32fast` / `typed-path` | ZIP 的 Deflate 解压、校验与路径处理 | MIT OR Apache-2.0 |
| `zlib-rs` | Deflate 解压后端 | Zlib |
| `embed-resource`（构建期） | 把图标、清单与版本信息写进 exe | MIT |

完整的依赖树与其许可证可由 `cargo metadata` 或 `cargo deny` 复现。

## 字体

界面使用 **Microsoft YaHei UI**，为 Windows 自带的系统字体，**不随本软件分发**。

## Halo Battery（协议移植参考）

- 项目：Halo Battery 1.15.0
- 版权：Copyright (C) Halo Battery contributors
- 许可证：**MIT**
- 项目主页：https://github.com/HeyOkay/HaloBattery

`src/collect/peripherals/providers/` 下多个厂商协议实现（Corsair、HyperX、ASUS、
SteelSeries、Razer 等）移植自该项目的 `providers/*.py`：报文格式、字节偏移、
设备型号表与协议时序按其实现逐一对应，Rust 侧代码为独立编写。每个移植文件
头部保留出处与 MIT 许可声明；本项目不属于 Halo Battery 的衍生分发品，
上述署名出于对原作者的尊重。

## MyFinder Device Battery（协议事实参考）

- 项目：MyFinder Device Battery
- 版权：Copyright (C) wushuai0802
- 许可证：**AGPL-3.0-only**
- 项目主页：https://github.com/wushuai0802/myfinder-device-battery

`g3m`、`vgn_dragonfly3`、`vgn_keyboard`、`eweadn`、`cherry`、`atk_headset`
六个 provider **不包含该项目的任何代码**。仅采用其公开记录的协议事实（厂商与
产品 ID、目标 HID 集合、请求字节、回复偏移与校验条件），Rust 实现为本项目
按自身 `Hid`/`HidSystem` 抽象独立编写。该项目的 AGPL-3.0 许可证不延伸至
仅参考协议事实的独立实现；此处署名用于标明事实来源。

## 开源许可

本项目自身为闭源商业软件（普通版免费，Pro 版付费授权）。
