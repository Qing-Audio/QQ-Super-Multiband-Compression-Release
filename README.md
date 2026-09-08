# QQ Super Multiband Compression

**Qing Audio · 0.2.8 Stable**

QQ Super Compression 的多段扩展版。把声音分成最多五个频段，分别用 Ratio 与 Mix 控制压缩量，再用 MAKEUP、MATCH 和 Band Output 整理音量，在同一个窗口里观察处理前后的频谱和动态变化。

The multiband extension of QQ Super Compression. Split audio into up to five bands, shape compression with Ratio and Mix, balance levels with MAKEUP, MATCH and Band Output, and compare input/output spectra and dynamics in one window.

压缩核心没有传统 Attack/Release 的启动与释放动作，也不是把这两个时间参数藏在内部。Lookahead 用于预读处理。分频、增益变化和并行混合仍会改变声音；可通过频谱、动态显示和旁通对比判断效果。

The compression core does not use conventional attack/release envelope behavior or hide those timing controls internally. Lookahead provides advance processing. Filtering, gain changes and parallel mixing still change the signal; use the spectra, dynamic display and bypass to judge the result.

## 下载 / Downloads

[打开 0.2.8 Release / Open the 0.2.8 release](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/tag/v0.2.8)

| 下载 / Download | 适用 / For |
|---|---|
| [Windows 10/11 64-bit](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.2.8/QQ-Super-Multiband-Compression-0.2.8-Windows-x64-VST3.zip) | VST3 |
| [Apple Silicon · 原生 / native](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.2.8/QQ-Super-Multiband-Compression-0.2.8-macOS-Apple-Silicon-VST3.zip) | VST3 |
| [Intel / Rosetta](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.2.8/QQ-Super-Multiband-Compression-0.2.8-macOS-Intel-x86_64-VST3.zip) | VST3 |
| [Apple Silicon + Intel](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.2.8/QQ-Super-Multiband-Compression-0.2.8-macOS-Universal-2-AU.zip) | AU |
| [中文安装说明](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.2.8/QQ-Super-Multiband-Compression-0.2.8-Installation-zh-CN.txt) | TXT |
| [English installation guide](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.2.8/QQ-Super-Multiband-Compression-0.2.8-Installation-en.txt) | TXT |
| [中文用户手册（含 0.2.8 补充）](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.2.8/QQ-Super-Multiband-Compression-0.2.8-User-Manual-zh-CN.pdf) | PDF |
| [English manual with 0.2.8 addendum](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.2.8/QQ-Super-Multiband-Compression-0.2.8-User-Manual-en.pdf) | PDF |

macOS 需要 11.0 或更新版本。VST3 按宿主架构只选一个包；Apple Silicon 上使用 Rosetta 的 Intel 宿主请选择 Intel 包。Logic 用户可直接安装 Universal 2 AU。AU 与 VST3 可按需要分别安装。

macOS 11.0 or later is required. Choose one VST3 package matching your host architecture; Intel hosts under Rosetta use the Intel package. Logic users can install the Universal 2 AU. Install only the formats your host needs.

## 0.2.8 有什么变化 / What's new

- 更宽的 1200×800 默认窗口，两块图表仍可等分、放大和折叠。 / A wider 1200×800 default window with split, expanded and collapsed views.
- 顶部 A/B 比较整套设置，Bypass 对比整个插件处理前后，Sidechain 从顶部统一设置。 / Whole-setup A/B, whole-plug-in bypass and shared top-row sidechain controls.
- 每段仍有独立的 ON/OFF、Solo 和压缩/音量控制。 / Independent band ON/OFF, Solo, dynamics and level controls are retained.
- Light、Dark、Classic 三种风格，以及处理前后频谱、NET 净增益和动态历史显示。 / Three themes, input/output spectra, NET gain curves and dynamic history.

## 安装与开始使用 / Install and get started

1. 完全退出宿主，解压下载包，保留完整的 `.vst3` 或 `.component` bundle。升级时先把旧副本移出扫描目录，再装新版本。 / Quit your host, extract the archive and keep the complete bundle. Move old copies out of scan folders before upgrading.
2. Windows VST3 放到 `C:\Program Files\Common Files\VST3`；macOS VST3 放到 `~/Library/Audio/Plug-Ins/VST3`，AU 放到 `~/Library/Audio/Plug-Ins/Components`。 / Copy to the matching Windows or macOS folder, then reopen and rescan in your host.
3. 在空白频谱双击或点击 ADD BAND，拖动分界选择频段。Ratio 默认 1:1，配合 Mix 调压缩量，再调整 MAKEUP 或使用 MATCH。 / Add a band, drag its boundaries, then adjust Ratio and Mix before balancing MAKEUP or using MATCH.
4. 升级前另存工程。详见上方双语安装说明；20 页手册的第 19-20 页是 0.2.8 补充，原正文与截图保持原版。当前系统支持以安装说明为准。 / Save a session copy before upgrading. The 20-page manuals retain the original body and add 0.2.8 guidance on pages 19-20. Use the installation guides for current platform support.

## 使用注意 / Before use

- macOS 包为 ad-hoc 签名，未经过 Apple Developer ID 公证。遇到隔离提示时，请按安装说明针对可信的插件文件处理。 / macOS builds are ad-hoc signed, not Developer ID notarized. Follow the guide if a trusted download is blocked by quarantine.
- 普通与线性相位目前保留相同的分频延迟，再加选定的 Lookahead；请启用宿主延迟补偿。 / Both phase modes currently reserve the same crossover delay plus Lookahead. Enable host delay compensation.
- 旧工程显示 SC: MIXED 时，原各段侧链设置先保留；明确修改全局侧链后才统一。 / SC: MIXED preserves different legacy band-sidechain settings until you edit a global sidechain control.
- 本版本经过自动音频与加载检查；不同宿主的焦点、缩放和长期运行仍可能有差异。 / Automated audio/loading checks do not guarantee identical behavior in every host or long session.

## 版本变化 / Version history

首次公开下载同时保留此前版本的功能变化记录。较早条目不表示这些版本均有独立下载包。

This first public download includes the preceding feature history. Earlier entries do not imply separate downloadable releases.

### 0.2.8

界面改为更宽的 3:2 布局；顶部 A/B、Bypass、Sidechain 统一控制整个插件。旧工程保留原有侧链设置，必要时显示 SC: MIXED。本次发布增加 macOS 两类 VST3 和 Universal 2 AU，并在手册末尾补充新操作。

A wider 3:2 interface and whole-plug-in A/B, Bypass and Sidechain. Older sessions retain their sidechain settings and show SC: MIXED when needed. This release adds Apple Silicon/Intel VST3 and Universal 2 AU, with new controls explained at the end of the manuals.

### 0.2.7

同步新版 Light 和 Dark 外观，保留 Classic；记住最后选择的主题。

Updates the Light and Dark appearances, keeps Classic, and remembers the last theme.

### 0.2.6

加入 Light 浅色风格及与 Classic 的切换，保持多段操作方式。

Introduces the Light theme and switching with Classic while retaining the multiband workflow.

### 0.2.5

分频斜率首次默认改为 24 dB/oct；记住最后手动选择，新实例沿用，工程优先恢复自己的设置。

Makes 24 dB/oct the first-use slope and remembers manual choices for new instances; saved sessions restore their own settings.

### 0.2.4

两种相位均可选择 6/12/24/48 dB/oct。精简重复选段及 Input Gain 控件，保留 Band Output；移除 ST/MS/LR 选择，统一立体声联动。动态显示加入 Solo，并避免两块视图同时隐藏。

Adds 6/12/24/48 dB/oct slopes to both phase modes, simplifies duplicate selection/Input Gain controls, and retains Band Output. Processing becomes stereo-linked without an ST/MS/LR selector. Adds display Solo and prevents both panels from being hidden.

### 0.2.3

视图按钮改为图形图标；各段 ON/S/VIEW 移进频谱。彩色 NET 曲线加入 MAKEUP、Mix 和 Band Output 的影响，补偿超过减弱时曲线向上。

Uses graphic view buttons and moves band ON/S/VIEW controls into the spectrum. Coloured NET curves include MAKEUP, Mix and Band Output, rising above zero when compensation exceeds reduction.

### 0.2.2

修复关闭某段后该频段丢声的问题。新增处理前后频谱对比、图中分界编辑与纵向 Band Output 拖动；上下显示可等分或单独展开，减少重复电平表。

Fixes missing audio when a band is switched off. Adds input/output spectrum comparison, graph-based crossover editing and vertical Band Output dragging. Supports equal split or expanded views and removes duplicate meters.

### 0.2.1

修复全频已占满时 Add Band 无反应的问题，新增 Remove Band，并调整频谱与工具栏布局。

Fixes Add Band when the full spectrum is occupied, adds Remove Band, and rearranges the spectrum and toolbar.

### 0.2.0

恢复 QQ Super Compression 的完整动态历史显示和 Ratio/Mix/MAKEUP/MATCH 操作；频段可创建、关闭与重开，加入总输出、尺寸记忆及撤销重做。Lookahead 提供 10/26/40/80/100 ms。

Restores the original dynamic history and Ratio/Mix/MAKEUP/MATCH workflow. Adds editable band creation/on-off control, master output, remembered size and undo/redo. Lookahead offers 10/26/40/80/100 ms.

### 0.1.1

中间界面方案，未作为可下载版本交付；后续回到保留原版完整动态显示的方向。

An intermediate interface revision that was not delivered as a downloadable version; later work returned to preserving the original full dynamic display.

### 0.1.0

首个多段版本：最多五段，可调分界，普通/线性相位，每段 Ratio、Threshold、Wet Gain、Mix、响度匹配和输出增益，以及总输出和 Solo。

The first multiband version: up to five bands, adjustable crossovers, Normal/Linear Phase modes, per-band Ratio, Threshold, Wet Gain, Mix, loudness matching and output gain, plus master output and Solo.

## 关于源码 / About the source

本产品闭源，源码仓库保持私有。本仓库仅提供下载与使用说明。GitHub 自动列出的 “Source code” ZIP/TAR 仅打包本公开页面文件，不是插件安装包，也不包含压缩器源码。

This product is closed source and its source repository remains private. This repository provides downloads and user information only. GitHub's automatic “Source code” archives contain this public repository's page files, not the plug-in installer or compressor source.

Copyright © 2026 Qing Audio. All rights reserved.
