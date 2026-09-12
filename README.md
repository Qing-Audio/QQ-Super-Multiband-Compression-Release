# QQ Super Multiband Compression 0.3.2

**Qing Audio · Stable · 2026-09-12**

QQ Super Compression的多段扩展版：最多五段，每段可选择下压、上压或双压，通过Ratio与Mix控制动态，并在频谱和Dynamic Display中比较处理前后。

The multiband extension of QQ Super Compression: up to five bands, each with downward, upward or Dual processing. Shape dynamics with Ratio and Mix and compare the result in the spectrum and Dynamic Display.

压缩核心没有传统Attack/Release的启动与释放动作，也不是把时间参数藏在内部。Lookahead用于提前观察信号；分频和动态处理仍会影响波形。

The compression core has no conventional attack/release envelope behavior or hidden attack/release timing controls. Lookahead observes the signal ahead; crossovers and dynamic processing still affect the waveform.

## 新增上压与Range / Upward processing and Range

Single Ratio向左为上压，例如1:8；向右为下压，例如8:1。上压处理Threshold以上的内容。Range设定检测电平上界，达到或超过后停止动态处理；它不是“最多压多少dB”。MAKEUP和输出增益仍可改变最终音量。

Turn Single Ratio left for upward processing, such as 1:8, or right for downward processing, such as 8:1. Upward processing acts above Threshold. Range is the upper detector-level boundary: dynamic processing stops at or above it. It is not a maximum reduction amount. MAKEUP and output gains can still change the final level.

![Single upward / 单压向上处理](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.3.2/Single-Upward-0.3.2.png)

## 双压如何使用 / Using Dual

- 低于或等于UP阈值：不抬升、不压低。 / At or below UP: no upward or downward action.
- 高于UP、低于DOWN：按UP Ratio抬升。 / Above UP and below DOWN: lift according to UP Ratio.
- 高于DOWN：停止抬升，改按DOWN Ratio下压；在DOWN边界动态增益回到0 dB。 / Above DOWN: stop lifting and reduce according to DOWN Ratio; at DOWN itself, dynamic gain returns to 0 dB.

Dual没有Range，两个分支各有ON/OFF，并提供反向联动的LINK。先关闭LINK、观察Display设好上下阈值，再分别调整两个Ratio；需要联动时再开启LINK。开关保留交叉淡变。

Dual has no Range. Each branch has ON/OFF, and LINK couples the two Ratios inversely. Start with LINK off, use the Display to place both thresholds, then adjust each Ratio. Enable LINK when coupled adjustment is useful. Switching is crossfaded.

同一频段、输入与检测设置下，Single的Threshold=-inf、Range OFF、Mix100%时，8:1下压与1:8上压经输出音量匹配，理论上有相同的相对动态。Dual默认UP=-inf、DOWN=0 dB，从默认LINK状态联动时也可能与对应Single等效。双压的意义在于有意识地分配处理区间和力度，不是只切换模式。详见两份手册第7–11页。

For the same band, input and detection settings, Single at Threshold=-inf, Range OFF and Mix100% gives theoretically identical relative dynamics for 8:1 downward and 1:8 upward after output level matching. Default Dual thresholds (UP=-inf, DOWN=0 dB) with LINK used from its default state can also match the corresponding Single result. Use Dual to deliberately choose operating regions and strengths, not just to change the mode label. See manual pages 7–11.

![Dual display / 双压动态显示](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.3.2/Dual-Display-0.3.2.png)

截图是0.3.2的实际界面示例，数值不是通用预设。 / Screenshots show actual 0.3.2 interface examples, not universal presets.

## 下载 / Downloads

[打开0.3.2 Release / Open release](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/tag/v0.3.2)

- [Windows x64 VST3](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.3.2/QQ-Super-Multiband-Compression-0.3.2-Windows-x64-VST3.zip)
- [macOS Apple Silicon VST3](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.3.2/QQ-Super-Multiband-Compression-0.3.2-macOS-Apple-Silicon-VST3.zip)
- [macOS Intel / Rosetta VST3](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.3.2/QQ-Super-Multiband-Compression-0.3.2-macOS-Intel-x86_64-VST3.zip)
- [macOS Universal 2 AU](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.3.2/QQ-Super-Multiband-Compression-0.3.2-macOS-Universal-2-AU.zip)
- [中文安装说明](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.3.2/QQ-Super-Multiband-Compression-0.3.2-Installation-zh-CN.txt)
- [English installation guide](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.3.2/QQ-Super-Multiband-Compression-0.3.2-Installation-en.txt)
- [中文手册 · 22页](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.3.2/QQ-Super-Multiband-Compression-0.3.2-User-Manual-zh-CN.pdf)
- [English manual · 22 pages](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.3.2/QQ-Super-Multiband-Compression-0.3.2-User-Manual-en.pdf)
- [Single upward screenshot](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.3.2/Single-Upward-0.3.2.png)
- [Dual display screenshot](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v0.3.2/Dual-Display-0.3.2.png)

## 安装、兼容性与升级 / Installation, compatibility and upgrading

Windows 10/11 64-bit：安装完整QQ Super Multiband Compression.vst3到`C:\Program Files\Common Files\VST3`。macOS 11.0以上：按宿主架构只选一个VST3包，安装到`~/Library/Audio/Plug-Ins/VST3`；AU安装到`~/Library/Audio/Plug-Ins/Components`。Universal 2 AU包含Apple Silicon和Intel。Rosetta下的Intel宿主选Intel VST3。各ZIP内保留使用许可和第三方说明。

Windows 10/11 64-bit: copy the complete QQ Super Multiband Compression.vst3 bundle to `C:\Program Files\Common Files\VST3`. On macOS 11.0+, choose one VST3 package matching the host architecture and install in `~/Library/Audio/Plug-Ins/VST3`; AU goes in `~/Library/Audio/Plug-Ins/Components`. Universal 2 AU includes Apple Silicon and Intel. Intel hosts under Rosetta use Intel VST3. Each ZIP includes license and third-party notices.

完全关闭宿主后再升级，移出旧副本，避免用户和系统目录重复安装。重新打开并扫描插件；升级前另存工程，检查原有自动化和声音。详细步骤、Logic重扫及安全处理见双语安装说明。

Quit the host before upgrading, move old copies out of scan folders and avoid duplicate user/system installations. Reopen and rescan. Save a session copy and check existing automation and sound. The bilingual guides include detailed steps, Logic rescanning and security handling.

## 使用注意 / Known limitations

- 两种相位都可能出现分频振铃；陡Slope和明显段间增益差可能使其更突出。0.3.2不包含已撤回的LOW RING实验，也不宣称消除振铃。 / Crossover ringing can occur in both phase modes, especially with steep slopes and large band-gain differences. The withdrawn LOW RING experiment is absent; this release does not claim to eliminate ringing.
- Normal与Linear Phase保留相同分频延迟，加上Lookahead；启用宿主延迟补偿。 / Normal and Linear Phase reserve the same crossover delay plus Lookahead; enable host delay compensation.
- macOS成品为ad-hoc签名，未经过Apple Developer ID公证；仅对可信下载按安装指南处理隔离。 / Mac builds are ad-hoc signed, not Developer ID notarized. Follow the guide for quarantine handling only for trusted downloads.
- 自动检查不代表所有宿主、缩放或长期会话完全一致。 / Automated checks do not guarantee identical behavior in every host, scale or long session.

本产品闭源，源码仓库保持私有。此仓库仅提供公开成品、手册和截图。 / This is a proprietary product. Source remains private; this repository provides compiled products, manuals and screenshots only.

## 从0.2.8以来的变化 / Changes since 0.2.8

### 0.3.2 — Stable

记住最后手动选择的Normal/Linear Phase与Slope，新实例沿用，工程优先恢复自己的参数。沿用移除LOW RING后的原动态逻辑。中英文说明书均更新为22页，完整说明上压、Range、双压、LINK及等音量比较。

Remembers manual Normal/Linear Phase and Slope choices for new instances while saved projects retain their own parameters. Keeps the original dynamics after LOW RING removal. Both manuals are now 22 pages, covering upward processing, Range, Dual, LINK and level-matched comparison.

### 0.3.1 — 实验版，已撤回 / Withdrawn experiment

曾测试LOW RING以减少振铃，但其对频段重叠和音量的影响不符合原动态目标，已取消，不作为本次功能提供。

Tested LOW RING to reduce ringing. Its effects on band overlap and level did not meet the original dynamic goals. The experiment was withdrawn and is not included here.

### 0.3.0 — 上压与双压 / Upward and Dual

每段加入双向Single Ratio、Range、Dual两阈值和两个Ratio、分支开关与LINK；显示同时呈现Boost/Cut。保留每段Match、Mix、输出和开关交叉淡变。

Adds bidirectional Single Ratio, Range, Dual thresholds and Ratios, branch switches and LINK per band. Displays show Boost and Cut. Retains per-band Match, Mix, output controls and switching fades.

### 0.2.9 — 显示修复 / Display fix

修复宽屏界面高频段OUT/NET与Hz标签位置错误；压缩和分频行为不变。

Fixes misplaced high-frequency OUT/NET and Hz labels in wide layouts, without changing compression or crossovers.


## 既有公开版本记录 / Earlier version history

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
