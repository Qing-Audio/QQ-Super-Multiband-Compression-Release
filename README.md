# QQ Super Multiband Compression 1.2.7

**Qing Audio · Stable 1.2.7 · 2026-10-02**

QQ Super Compression 的多段扩展版：最多五段，每段可独立选择 Classic/Super、侧链来源与检测 EQ，并使用向下、向上或双压。ECO 在宿主明确停播时立即静音和暂停处理；FULL 保留停播时的实时输入监听，并在极低残留与尾音满足安全条件后休眠。中英文 1.2.7 用户手册各 35 页。本项目闭源，公开仓库只提供安装包与用户文档。

The multiband extension of QQ Super Compression: up to five bands with independent Classic/Super, sidechain sources and detector EQ, plus downward, upward or Dual compression. ECO immediately mutes and suspends on a known host Stop. FULL retains live stopped-input monitoring and sleeps only after very low residuals and signal tails meet guarded conditions. The 1.2.7 Chinese and English manuals have 35 pages each. The product is proprietary; this public repository contains installation packages and user documents only.

## 下载 / Downloads

[打开 1.2.7 Release / Open the 1.2.7 release](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/tag/v1.2.7)

| 下载 / Download | 格式 / Format |
|---|---|
| [Windows 10/11 x64](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.2.7/QQ-Super-Multiband-Compression-1.2.7-Windows-x64-VST3.zip) | VST3 |
| [macOS Apple Silicon](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.2.7/QQ-Super-Multiband-Compression-1.2.7-macOS-Apple-Silicon-VST3.zip) | VST3 |
| [macOS Intel / Rosetta](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.2.7/QQ-Super-Multiband-Compression-1.2.7-macOS-Intel-VST3.zip) | VST3 |
| [macOS Universal 2](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.2.7/QQ-Super-Multiband-Compression-1.2.7-macOS-Universal-2-AU.zip) | AU |
| [中文安装说明](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.2.7/QQ-Super-Multiband-Compression-1.2.7-Chinese-Installation-Guide.txt) | TXT |
| [English installation guide](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.2.7/QQ-Super-Multiband-Compression-1.2.7-English-Installation-Guide.txt) | TXT |
| [中文用户手册 · 35 页](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.2.7/QQ-Super-Multiband-Compression-1.2.7-Chinese-User-Manual.pdf) | PDF |
| [English user manual · 35 pages](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.2.7/QQ-Super-Multiband-Compression-1.2.7-English-User-Manual.pdf) | PDF |

## 安装与使用 / Install and use

升级前保存工程副本并完全退出宿主，解压后替换完整插件 bundle，再重新扫描。Windows VST3 安装到 `C:\Program Files\Common Files\VST3`；macOS VST3 安装到 `~/Library/Audio/Plug-Ins/VST3`，AU 安装到 `~/Library/Audio/Plug-Ins/Components`。macOS 需要 11.0 或更新版本；按宿主架构只选一个 VST3。Apple Silicon 上以 Rosetta 运行的 Intel 宿主应选 Intel 包。详细步骤、安全提示和升级注意事项见对应语言的安装说明。

Save a session copy and fully quit the host before upgrading. Extract and replace the complete plug-in bundle, then rescan. Use `C:\Program Files\Common Files\VST3` on Windows, `~/Library/Audio/Plug-Ins/VST3` for macOS VST3, or `~/Library/Audio/Plug-Ins/Components` for AU. macOS 11 or later is required. Choose one VST3 matching the host architecture; an Intel host under Rosetta needs the Intel build. See your installation guide for detailed steps, security prompts and upgrade notes.

选择频段后设置 Ratio、Threshold 和 Mix；需要另一频段或外部信号触发压缩时，在 SC EQ 中选择检测来源并调整 EQ。ECO 适合停播后无需监听实时输入的情况；停播时仍需监听输入则选 FULL。项目保存当前实例模式，新实例沿用最后一次手动选择。Normal 分频具有频率相关相位响应，请开启宿主延迟补偿。

Select a band and adjust Ratio, Threshold and Mix. To trigger compression from another signal, choose the detector source and EQ under SC EQ. Use ECO when live input need not pass during Stop; use FULL for stopped live monitoring. Sessions save each instance's mode, while new instances use the last manual choice. Normal crossover has frequency-dependent phase response; enable host delay compensation.

## 兼容性与已知事项 / Compatibility and known considerations

Windows x64 VST3 与三类 macOS 成品已通过相应自动构建与验证；AU 在 Apple Silicon 上通过 `auval`，Intel AU 切片已核对但未在独立 Intel 机器运行 `auval`。Mac 为 ad-hoc 签名，未做 Developer ID 公证。FULL 在极端增益或已连接但未使用的侧链仍有噪声时会保守地继续处理。自动检查不等于所有 DAW 的长期工程试听。

Windows x64 VST3 and all three macOS packages passed their respective automated builds and checks. AU passed `auval` on Apple Silicon; its Intel slice was inspected but was not separately run through `auval` on an Intel machine. Mac packages are ad-hoc signed, not Developer ID notarized. FULL can conservatively continue processing with extreme gain or noise on a connected but unused sidechain. Automated checks are not a long-session test in every DAW.

## 从上次公开版起的版本记录 / Version history since the last public release

### 1.2.0

逐段新增侧链来源、检测 EQ、增益与 Listen，Single Ratio 扩展至 1:200–200:1；这是本机 Windows 升级，未单独公开 macOS 包。 / Added per-band sidechain sources, detector EQ, gain and Listen, and expanded Single Ratio to 1:200–200:1. This was a local Windows upgrade without a separate public macOS package.

### 1.2.1

新菜单提供 This Band、Internal Full、External；旧 Band 1–5 路由继续按 Legacy 恢复，并更新双语手册。此前用户确认的 Stable 为 1.2.1。 / New menus offer This Band, Internal Full and External, while saved Band 1–5 routes restore as Legacy. Updated bilingual manuals. The previously user-confirmed Stable was 1.2.1.

### 1.2.2

Makeup 与各段 Wet Gain 收窄至 ±30 dB，MATCH 同步使用这一范围。 / Makeup and each band's Wet Gain were limited to ±30 dB, with the same bound for MATCH.

### 1.2.3

修正拖动旋钮、Master Output 或 Band Output 时切换 Shift 会让数值回跳的问题。 / Fixed value jumps when toggling Shift during knob, Master Output or Band Output dragging.

### 1.2.4

加入逐实例 ECO/FULL、Dual UP/DOWN 各自独立的 Classic/Super、分析优化和全零输入的尾音安全休眠。 / Added per-instance ECO/FULL, independent Classic/Super for Dual UP/DOWN, leaner analysis and tail-safe sleep for exact-zero input.

### 1.2.5

新实例记住上次手动 ECO/FULL 选择；Linear Phase 在完整输入历史归零后跳过无效 FFT，重复相同参数通知不再干扰休眠。 / New instances remember the last manual ECO/FULL choice. Linear Phase skips FFT work after its full input history reaches zero, and redundant unchanged parameter notifications no longer interrupt idle waiting.

### 1.2.6

ECO 明确停播时立即静音暂停；FULL 保留实时输入与尾音安全休眠，同时减少检测器冗余计算。 / ECO immediately mutes and suspends on a known Stop; FULL retains live input and tail-safe sleep, while redundant detector calculations were reduced.

### 1.2.7

FULL 增加带增益与尾音保护的极低残留休眠；修正 macOS AU Ratio 参数别名标记，中英文手册更新至各 35 页。 / FULL adds gain- and tail-guarded very-low-residual sleep. macOS AU Ratio alias metadata was corrected, and both language manuals were updated to 35 pages.

---

## 以前的公开版本 / Earlier public release

# QQ Super Multiband Compression 1.1.0

**Qing Audio · Stable 1.1.0 · 2026-09-27**

QQ Super Compression 的多段扩展版：最多五段，每段独立选择 Classic / Super，以及向下、向上或双压，通过 Ratio、Mix 和增益控制塑造动态。保持原有 Light / Dark / Classic 主题。

The multiband extension of QQ Super Compression: up to five bands, each with independent Classic / Super algorithms and downward, upward or Dual processing. Shape dynamics with Ratio, Mix and gain controls in the familiar Light / Dark / Classic themes.


本版让每个频段独立选择 Classic / Super，同步新版对齐检测与 A/B 淡变，并减少多段 Display 的重复刷新。中英文手册均更新为 28 页，包含两种算法的静态曲线图和操作示例。

Each band can now choose Classic or Super independently. This release brings aligned detection, improved A/B transitions and reduced display work, with matching 28-page Chinese and English manuals and a static transfer-curve comparison.

## 主要变化 / Changes

- **逐段算法 / Per-band algorithms:** 下方 Ratio 左上角的 ALGO 只控制当前 Band。Classic 按固定 dB Ratio 工作，最低阈值 -90 dB；Super 保留原曲线及 -inf。各段记住最后手动选择，工程与 A/B 恢复各自模式。The ALGO button affects only the selected band. Classic uses a fixed dB ratio and a -90 dB floor; Super retains the original curve and -inf. Manual choices are remembered separately, while sessions and A/B retain their saved modes.
- **Ratio:** Single 1:32–32:1，Dual UP 1:32–1:1、DOWN 1:1–32:1，默认全部 1:1。Single spans 1:32–32:1, Dual UP 1:32–unity and DOWN unity–32:1; all default to unity.
- **A/B:** 可以直接比较不同算法及整套动态设置。相同分频、侧链检测和时序配置下，完整动态结果约 20 ms 交叉淡变；直接切算法约 10 ms。Compare algorithms and complete setups. Compatible configurations crossfade complete dynamics results over approximately 20 ms; direct algorithm changes use approximately 10 ms.
- **Lookahead:** 默认 26 ms，过去与未来窗口共同对齐当前声音，减少大声到来前的提前衰减；可选 10/26/40/80/100 ms。First-use default 26 ms. Past/future windows align detection to the current audio, reducing early attenuation before loud events. Choices: 10/26/40/80/100 ms.
- **MATCH / MAKEUP:** Makeup 扩展为 ±120 dB，移除固定绝对低电平检测门限，支持深度压缩后的有效音频匹配。Makeup extends to ±120 dB and MATCH removes the fixed absolute low-level gate. Valid very quiet signals remain usable; silence cannot provide a match.
- **Display:** 只重建可见 Band 曲线；隐藏 Band 保留历史。收起动态显示不停止音频；频谱复用窗口并在无新音频时跳过 FFT。Only visible-band curves are rebuilt while hidden bands retain history. Collapsing the display does not stop audio; spectrum work reuses its window and skips FFT without new audio.
- **手册 / Manuals:** 上压门槛、Range、Dual 开关与相对 LINK、算法曲线、输出低于阈值的解释、总延迟和旧工程迁移均有说明。Covers the upward gate, Range, Dual switches, relative LINK, algorithm curves, output below threshold, total latency and session migration.

## 使用与升级 / Use and upgrading

上压只提升 Threshold 以上的允许区间；门槛以下仍有原声音。Range 是检测电平上界，到达或超过后动态增益为 0 dB，有限边界内连续过渡；OFF 表示无有限上界。Dual 在 UP 与 DOWN 之间提升，超过 DOWN 后只向下压，各分支有独立开关。LINK 保留原有相对比例，不强行改成完全倒数。

Upward processing lifts only the allowed region above Threshold and does not mute quieter sound. Range is an upper detector-level boundary: dynamic gain is 0 dB at or above it, with a continuous transition inside a finite boundary. OFF removes the finite upper limit. Dual lifts between UP and DOWN, then uses only downward processing above DOWN. Each branch has its own switch; LINK preserves the relative ratio offset.

升级前保存工程副本。1.0.0 工程恢复 Classic，更早工程恢复 Super；旧全局算法扩展到每个 Band。超出范围的 Ratio 限制到 32:1 或 1:32；Classic 中旧 -inf 解释为 -90 dB。Ratio 归一化自动化映射随范围变化，请检查旧自动化与极端设置。

Save a session copy before upgrading. Version 1.0.0 sessions restore Classic; earlier sessions restore Super. Legacy global algorithm choices expand to all bands. Out-of-range ratios clamp to 32:1 or 1:32; Classic reads old -inf as -90 dB. The changed Ratio range affects normalized host automation, so recheck affected sessions.

分频、侧链或 Lookahead 不同的 A/B 仍需重配置。两种相位保留相同分频延迟，再加 Lookahead；48 kHz、26 ms 档总延迟约 79.33 ms。分频振铃和快速调幅残差仍可能出现，不宣称所有信号零失真。

A/B changes to crossovers, sidechain or Lookahead still require reconfiguration. Both phase modes retain the same crossover delay plus Lookahead: about 79.33 ms total at 48 kHz with 26 ms selected. Crossover ringing and rapid-modulation residuals remain possible; zero distortion for all signals is not claimed.

Windows 10/11 x64 VST3；macOS 11+ Apple Silicon VST3、Intel/Rosetta VST3、Universal 2 AU。Mac 为 ad-hoc 签名，未做 Developer ID 公证。按宿主架构只选一个 VST3。先完全关闭宿主再替换完整 bundle；详细步骤见双语安装指南。

Windows 10/11 x64 VST3; macOS 11+ Apple Silicon VST3, Intel/Rosetta VST3 and Universal 2 AU. Mac builds are ad-hoc signed, not Developer ID notarized. Choose one VST3 architecture matching the host. Quit the host before replacing a complete bundle; see the bilingual installation guides.

源码继续保持私有；公开仓库只提供成品、手册、截图和使用说明。Source remains private. The public repository contains compiled downloads, manuals, screenshots and user documentation only.

## 当前界面 / Current interface

下方 Ratio 区域左上角的 ALGO 只改变当前 Band。上压示例：

The ALGO control at the upper left of the lower Ratio area affects only the selected band. Single upward example:

![Single upward / 单压向上处理](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.1.0/Single-Upward-1.1.0.png)

Dual 为中间区间提供向上提升，并对 DOWN 以上的部分向下压缩；两个分支可分别关闭，LINK 相对联动两个 Ratio。

Dual lifts the middle level region and reduces levels above DOWN. Each branch can be disabled independently, and LINK adjusts the ratios relatively.

![Dual processing / 双压处理](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.1.0/Dual-Display-1.1.0.png)

截图来自当前插件界面，数值只用于展示，不是通用预设。 / Screenshots show the current editor; the values illustrate the controls and are not universal presets.

## 下载 / Downloads

[打开 1.1.0 Release / Open release](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/tag/v1.1.0)

- [Windows x64 VST3](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.1.0/QQ-Super-Multiband-Compression-1.1.0-Windows-x64-VST3.zip)
- [macOS Apple Silicon VST3](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.1.0/QQ-Super-Multiband-Compression-1.1.0-macOS-Apple-Silicon-VST3.zip)
- [macOS Intel / Rosetta VST3](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.1.0/QQ-Super-Multiband-Compression-1.1.0-macOS-Intel-x86_64-VST3.zip)
- [macOS Universal 2 AU](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.1.0/QQ-Super-Multiband-Compression-1.1.0-macOS-Universal-2-AU.zip)
- [中文安装说明](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.1.0/QQ-Super-Multiband-Compression-1.1.0-Installation-zh-CN.txt)
- [English installation guide](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.1.0/QQ-Super-Multiband-Compression-1.1.0-Installation-en.txt)
- [中文手册 · 28 页](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.1.0/QQ-Super-Multiband-Compression-1.1.0-User-Manual-zh-CN.pdf)
- [English manual · 28 pages](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.1.0/QQ-Super-Multiband-Compression-1.1.0-User-Manual-en.pdf)

## 安装 / Installation

Windows：把完整 `.vst3` bundle 放入 `C:\Program Files\Common Files\VST3`。Mac：VST3 放入 `~/Library/Audio/Plug-Ins/VST3`，AU 放入 `~/Library/Audio/Plug-Ins/Components`。完全关闭宿主后升级，避免重复副本。架构选择、Logic 重扫及安全提示见安装指南。

Windows: install the complete `.vst3` bundle in `C:\Program Files\Common Files\VST3`. Mac: VST3 goes in `~/Library/Audio/Plug-Ins/VST3`, AU in `~/Library/Audio/Plug-Ins/Components`. Quit the host before upgrading and avoid duplicate copies. See the guides for architecture selection, Logic rescanning and security handling.

## 验证范围 / Validation scope

Windows 成品通过本地 DSP、状态、A/B、逐段算法及实际 VST3 加载检查。Mac 两种 VST3 分别在原生架构验证，Universal 2 AU 在 Apple Silicon 上执行 auval，并核对 arm64/x86_64 两切片。未单独执行 Intel AU 运行验证。自动检查不等于所有宿主与长期工程的实际听感验收。

Windows passed local DSP, state, A/B, per-band algorithm and actual VST3 loading checks. Both Mac VST3s are tested on their native architectures. Universal 2 AU is checked with auval on Apple Silicon and both arm64/x86_64 slices are verified; separate Intel AU runtime validation is not claimed. Automated tests are not a listening assessment of every host or long session.

## 1.0.0 — 本地对比版本 / Local comparison version

引入有限阈值的固定 dB Ratio 算法，并曾将 Ratio 扩展到 1:1000–1000:1。本次 1.1.0 根据使用目标恢复 1:32–32:1，并让每段可选择 Classic 或 Super。1.0.0 没有作为独立公开 Release 发布。

Introduced fixed-dB processing for finite thresholds and temporarily extended Ratio to 1:1000–1000:1. Version 1.1.0 returns to 1:32–32:1 and adds per-band Classic / Super selection. Version 1.0.0 was not published as a separate public release.

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
