# QQ Super Multiband Compression

**Qing Audio · 1.4.11 Stable**

## 1. 产品介绍 / About the plug-in

**QQ Super Multiband Compression（QQ 超级分段压缩）是一款面向人声、乐器、总线与母带的多段动态处理插件。** 低频太松、中频缺少细节、高频峰值太突出，往往需要不同的处理。它让你在最多五个频段内分别压低强音、抬升选定电平区间，或使用 Dual 双压同时管理两者，再用 Mix 保留需要的原始动态。

它来自 **QQ Super Compression（QQ 超级压缩）的动态核心**。超级压缩的 Compressor 模式处理全频信号；超级分段压缩先分频，再由各段独立检测、计算增益并合成输出。因此，控制低频起伏时，可以单独调整低频段的处理，而不必把整段声音一起压低。每段的算法、阈值、Ratio、Makeup、Mix 和输出都可以独立设置。

**Classic 与 Super 提供不同的动态曲线。** Classic 在有效区间内按固定 dB 比例进行下压；Super 使用 QQ 原创非线性曲线，实际压缩比例随电平变化。同样的 Ratio 在两种算法下会产生不同的动态变化。Dual 的 UP 与 DOWN 还可以分别选择算法与力度。两种算法的动态核心都直接根据检测电平计算增益，使用 **Lookahead 与 Window** 调整检测时序和参考范围；不采用传统 Attack / Release 压缩包络。

**QQ Super Multiband Compression is a multiband dynamics plug-in for vocals, instruments, buses and mastering.** Loose lows, recessed midrange detail and sharp high-frequency peaks often need different treatment. Up to five bands let you reduce louder signals, lift a selected level region or combine both with Dual compression, then blend back the original dynamics with Mix.

It is built on the **dynamics core of QQ Super Compression**. Super Compression's Compressor mode processes the full-band signal; the multiband version splits it by frequency, detects levels and calculates gain independently for each band, then recombines the output. You can control low-end movement within the low band without applying the same reduction to the entire signal. Each band has independent algorithm, threshold, ratio, makeup, mix and output settings.

**Classic and Super offer different gain curves.** Classic uses a fixed dB ratio for downward compression within the active region. Super uses the original QQ nonlinear curve, with an effective compression ratio that varies with level. The same Ratio setting therefore gives different dynamics. Dual allows separate algorithms and strengths for UP and DOWN. Both derive gain directly from detected levels, using **Lookahead and Window** to set detection timing and reference span rather than a conventional Attack / Release compressor envelope.

![QQ 超级分段压缩 1.4.11：五段动态处理与 Dual 双压 / Five-band dynamics and Dual compression](https://raw.githubusercontent.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/ee866b0c979b7bf8c9c3634d13a12378df7962e4/images/v1.4.11/overview-dark.png)

### 主要功能与特点 / Key features

- **每段都能单独处理。** Classic / Super、Single / Dual、内部或外部侧链、EQ、L/R Link 与 M/S Link，按频段选择。 / **Independent control per band:** Classic / Super, Single / Dual, internal or external sidechain, EQ and stereo/mid-side linking.
- **先匹配音量，再判断声音。** MATCH 将当前段累计的 Dry / Wet 音量差写入 Makeup；结合 Mix 与 A/B 比较需要的动态变化。 / **Compare at matched levels:** MATCH writes the current band's accumulated Dry / Wet difference into Makeup; use Mix and A/B to judge the dynamics.
- **把处理过程看清楚。** Display 同时呈现输入、输出、上压、下压与阈值，支持框选、缩放、平移、右键恢复全视图和 FREEZE。外部侧链模式可同时显示主信号与侧链频谱。 / **See the processing:** Display brings together input, output, boost, reduction and thresholds, with selection zoom, panning, full-view reset and FREEZE. External sidechain mode can show both spectra.
- **按工程需要调整。** 逐段 TRANSPARENT 与 Window，全局 Lookahead、1x / 4x / 8x / 16x 过采样，以及 ECO / FULL；提供深色与浅色界面。 / **Fit your session:** per-band TRANSPARENT and Window, global lookahead, 1x / 4x / 8x / 16x oversampling, ECO / FULL and dark or light themes.

<details>
<summary><strong>更多界面预览 / More interface views</strong></summary>

### 逐段动态控制 / Per-band dynamics

![1.4.11 浅色界面与逐段动态处理 / Light theme and per-band processing](https://raw.githubusercontent.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/ee866b0c979b7bf8c9c3634d13a12378df7962e4/images/v1.4.11/bands-light.png)

### 放大的动态显示 / Expanded Dynamic Display

![1.4.11 放大的动态显示 / Expanded Dynamic Display](https://raw.githubusercontent.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/ee866b0c979b7bf8c9c3634d13a12378df7962e4/images/v1.4.11/display-expanded.png)

### 外部侧链 EQ / External sidechain EQ

![1.4.11 外部侧链 EQ / External sidechain EQ](https://raw.githubusercontent.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/ee866b0c979b7bf8c9c3634d13a12378df7962e4/images/v1.4.11/sidechain-external.png)

截图均来自 1.4.11，参数用于展示功能。 / All screenshots show 1.4.11; settings are illustrative.

</details>


## 2. 许可与源码 / License and source

**Qing Audio 专有软件 / Proprietary software**  
Copyright © 2026 Qing Audio. All rights reserved. **保留所有权利。**

本产品保持闭源，源码仓库保持私有。此公开仓库提供已发布的插件成品、使用说明书、安装说明及界面截图。第一方软件、文档与素材属于专有内容；相关使用、复制、修改、再分发、再许可或销售授权，须由版权所有者另行授予。

The product remains closed source, and its source repository remains private. This public repository provides released plug-in binaries, manuals, installation guides and interface screenshots. First-party software, documentation and assets are proprietary; permission to use, copy, modify, redistribute, sublicense or sell this material must be obtained separately from the copyright holder.

第三方组件继续适用其各自许可证。本说明不替代第三方条款，也不追溯撤销历史副本已获得的权利。 / Third-party components retain their own licenses. This notice does not replace those terms or revoke rights previously granted for historical copies.


<a id="downloads"></a>

## 3. 最新版下载与说明书 / Latest downloads & manuals

**当前版本 / Current version：1.4.11 Stable** · **[最新版发布页 / Latest release](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/latest)**

发布日期 / Released：2026-10-27

插件、使用说明书和安装说明均为 **1.4.11**，在下表直接下载。 / All plug-ins, manuals and installation guides below are for **1.4.11**.

| 平台或资料 / Platform or document | 格式 / Format | 直接下载 / Direct download |
|---|---|---|
| Windows 10/11 · 64 位 / 64-bit | VST3 · ZIP | [下载 Windows 插件 / Windows plug-in](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.11/QQ-Super-Multiband-Compression-1.4.11-Windows-x64-VST3.zip) |
| Mac · Apple Silicon 原生宿主 / Native host | VST3 · ZIP | [下载 Apple Silicon 插件 / Apple Silicon plug-in](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.11/QQ-Super-Multiband-Compression-1.4.11-macOS-Apple-Silicon-VST3.zip) |
| Mac · Intel / Rosetta 宿主 / Host | VST3 · ZIP | [下载 Intel 插件 / Intel plug-in](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.11/QQ-Super-Multiband-Compression-1.4.11-macOS-Intel-VST3.zip) |
| Mac · Logic Pro 等 AU 宿主 / AU hosts | Universal 2 AU · ZIP | [下载通用 AU 插件 / Universal AU plug-in](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.11/QQ-Super-Multiband-Compression-1.4.11-macOS-Universal-2-AU.zip) |
| **中文使用说明书** | PDF · 41 页 | [**下载中文说明书**](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.11/QQ-Super-Multiband-Compression-1.4.11-Chinese-User-Manual.pdf) |
| **English User Manual** | PDF · 41 pages | [**Download English manual**](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.11/QQ-Super-Multiband-Compression-1.4.11-English-User-Manual.pdf) |
| 中文安装说明 | TXT | [下载中文安装说明](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.11/QQ-Super-Multiband-Compression-1.4.11-Chinese-Installation-Guide.txt) |
| English Installation Guide | TXT | [Download English installation guide](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.11/QQ-Super-Multiband-Compression-1.4.11-English-Installation-Guide.txt) |

macOS 11+：VST3 按宿主架构选择一个；Logic Pro 使用 AU。升级前退出宿主，完整安装步骤见同表中的安装说明。 / macOS 11+: choose one VST3 matching your host architecture, or AU for Logic Pro. Quit the host before upgrading; use the installation guides in the same table.

GitHub 自动生成的 `Source code (zip)` / `Source code (tar.gz)` 是本公开下载仓库的页面快照，**不是插件安装包**。 / GitHub's automatic Source code archives are snapshots of this download repository, **not installable plug-ins**.

### 安装与兼容性 / Installation and compatibility

Windows 10/11 64 位；macOS 11.0+。Apple Silicon VST3 为 arm64，Intel VST3 为 x86_64（适用于 Intel Mac 或 Rosetta 宿主）；按宿主架构只选一个 VST3 包。Universal 2 AU 同时包含 arm64 和 x86_64，适用于 Logic Pro 等 AU 宿主。
Windows 10/11 64-bit; macOS 11.0+. Apple Silicon VST3 is arm64; Intel VST3 is x86_64 for Intel Macs or Rosetta hosts. Choose one VST3 package matching the host architecture. Universal 2 AU includes both architectures for Logic Pro and other AU hosts.

升级前保存工程并退出宿主，移出旧版同名完整 bundle，再复制新版。Windows VST3 安装到 `C:\Program Files\Common Files\VST3`；Mac 使用 `~/Library/Audio/Plug-Ins/VST3` 或 `~/Library/Audio/Plug-Ins/Components`。重新扫描后确认界面显示 1.4.11；同一格式只保留一份。
Save sessions and quit hosts before moving the old bundle out and copying the complete new one into the matching folder above. Rescan and confirm version 1.4.11. Keep one installed copy per format and retain a session copy for rollback.

Mac 成品为 ad-hoc 签名，未经 Apple Developer ID 公证；单个 bundle 的隔离处理见双语安装说明。GitHub 自动生成的 Source code ZIP/TAR 只是此公开下载仓库的文档快照，不能作为插件安装。
Mac builds are ad-hoc signed, not Apple Developer ID notarized; the bilingual guides explain quarantine handling for the individual bundle. GitHub's automatic Source code ZIP/TAR contains this public download repository's documentation and is not an installable plug-in.

<details>
<summary>本版验证与限制 / Verification and limitations</summary>

Windows 复用已验收的 1.4.11 成品。Apple Silicon VST3 在自建 Mac 的原生 arm64 环境验证；Intel VST3 在自建 Apple Silicon Mac 上通过 Rosetta 执行 x86_64 测试程序，验证：阈值端点与默认值、Dual 动态及状态、Display/FREEZE/缩放、Display 高电平、实际 VST3 加载与中文悬停字形。三类 Mac 成品检查版本、架构、bundle 和签名；Universal 2 AU 在 Apple Silicon 上通过 auval。
The accepted Windows 1.4.11 binary is reused. Apple Silicon VST3 is tested natively on a self-hosted arm64 Mac; Intel VST3 is tested with an x86_64 test host through Rosetta on a self-hosted Apple Silicon Mac for threshold endpoints/defaults, Dual dynamics and state, Display/FREEZE/zoom, Display headroom, actual VST3 loading and Chinese tooltip glyphs. All Mac bundles are checked for version, architecture, structure and signature; Universal 2 AU passes auval on Apple Silicon.

Intel AU 未单独运行 auval；自动化验证不等同于对所有 DAW 和长期工程的实测。中英文手册均为对应本版本的 41 页 PDF，已检查字体、页面、书签和链接。
AU auval is not run separately on Intel. Automated checks do not represent testing every DAW or long-running session. Both matching manuals contain 41 pages, with fonts, pages, bookmarks and links checked.

</details>

## 4. 逐版本更新记录 / Version history

以下按新到旧列出各版本的真实变化；历史条目保留当时的功能、名称与状态。 / Changes are listed newest first. Historical entries retain the features, names and status applicable to those versions.

### 1.4.11

- Threshold、UP THR、DOWN THR 均可调至 -inf；Single / UP 默认保持 −90 dB，DOWN 默认保持 0 dB。保留有限阈值与旧工程数值。
- Threshold, UP THR and DOWN THR now reach -inf. Single / UP defaults remain -90 dB and DOWN remains 0 dB. Finite thresholds and saved session values are preserved.
- Display 中文悬停明确提示右键恢复全视图。中英文 41 页手册同步更新阈值、Display 平移、全视图恢复及 ECO/FREEZE 重开窗口说明。
- The Chinese Display hint explicitly identifies right-click full-view reset. Matching 41-page Chinese and English manuals cover thresholds, panning, reset and ECO/FREEZE editor reopening.

### 1.4.10

- Shift + 上下滚轮可在 -inf（静音底线）至 +24 dB 之间平移 Display，缩放比例保持不变；同步保存视图及中文悬停说明。
- Shift + vertical wheel pans Display between -inf (the silence floor) and +24 dB without changing its zoom span, with saved views and Chinese hints updated.

### 1.4.9

- 修复 Range OFF 时超过 0 dB 的检测、动态处理与 Display，使高电平仍按所选算法处理。
- Corrects detection, dynamics and Display above 0 dB with Range OFF, retaining the selected compression behavior at high levels.

### 1.4.8

- ECO 关闭界面再打开时，无论 FREEZE 是否点亮，Display 都清除旧图并从新采集数据开始显示；保留缩放与 FREEZE 选择。
- Reopening the editor in ECO clears old Display curves and starts with newly captured data whether FREEZE is on or off, while retaining zoom and the FREEZE choice.
- 界面持续打开时，FREEZE 仍保留停播曲线；FULL、声音处理与 MATCH 完整播放要求保持。中文 FREEZE 悬停同步更新。
- With the editor continuously open, FREEZE still retains stopped curves. FULL, audio processing and MATCH's complete-playback requirement are preserved. Chinese FREEZE help is updated.

上次完整同步/公开版本为 1.4.6，本次区间为 1.4.7、1.4.8；遗漏版本：无。 / Previous complete sync/public version: 1.4.6. Versions covered: 1.4.7 and 1.4.8; none omitted.

### 1.4.7

- 修复 QQ Host 等宿主保留并隐藏插件原生窗口时，ECO 未正确停止分析的问题；重开后拒绝旧表计及过期重算数据。五个频段统一处理，声音不变。
- Fixes ECO analysis remaining active when hosts such as QQ Host retain a hidden native editor. Reopening rejects stale meter and replay data across all five bands without changing audio.

### 1.4.6

- 精简 Display 中文悬停说明，直接说明框选、缩放与平移操作。中英文手册各 41 页，使用本版截图，将 FREEZE、TRANSPARENT、Lookahead / Window 和侧链 EQ 开关纳入原有章节。
- Concise Chinese Display help explains selection, zoom and pan. Both 41-page manuals use current screenshots and integrate FREEZE, TRANSPARENT, Lookahead / Window and the sidechain EQ switch into the existing chapters.

### 1.4.5

- 每段侧链 EQ 新增独立 ON/OFF，关闭滤波时保留侧链来源、Gain、Listen 与全部频点；旧工程默认 ON。补充中文图表悬停说明：左键添加、右键移除、滚轮调整 Q / Slope，以及两侧高通/低通和中间 Bell。
- Each band gains an independent sidechain EQ ON/OFF switch. Bypassing EQ preserves source, Gain, Listen and every node; older sessions default to ON. Chinese graph help covers adding/removing nodes, wheel Q / Slope, edge high-pass/low-pass filters and centre Bell filters.

### 1.4.4

- 改进 Display 边缘附近的框选操作；超出曲线的选择按边缘裁切，保留阈值拖动与 FREEZE 的操作优先级。
- Improves Display selection near graph edges, clamps selections to the graph, and preserves threshold-drag and FREEZE control priority.

### 1.4.3

- Shift + 上下滚轮改为上下移动 Display，保持缩放比例；普通滚轮和 Ctrl + 滚轮缩放继续保留。
- Shift + vertical wheel pans Display levels without changing scale. Ordinary wheel and Ctrl + wheel retain their zoom functions.

### 1.4.2

- Display 顶部支持以 0 dB 为上边界进行电平缩放，并支持 Ctrl + 滚轮横向时间缩放；停播时按鼠标位置观察细节。
- The Display header supports level zoom anchored to the 0 dB upper boundary and Ctrl + wheel time zoom, with pointer-centred detail inspection while stopped.

### 1.4.1

- 修正 Display 历史位置导致的显示滞后，播放时右侧跟随最新音频。新增 FREEZE：停播保留曲线，首次默认打开并记住最近手动选择；工程保留自己的状态。
- Corrects Display lag caused by history offsets, keeping the right edge on current audio during playback. FREEZE retains stopped curves, starts on and remembers the last manual choice; projects retain their own state.
- Lookahead 更新为 0 / 25.3 / 50.6 / 76 / 100 ms，兼容旧档位。真正改变 Lookahead 时重置各段 Window；重复选择同一档及恢复工程/A-B 不重置。SAFE 更名为 TRANSPARENT，并修正零 Window 边界。
- Lookahead becomes 0 / 25.3 / 50.6 / 76 / 100 ms with migration from older choices. Actual Lookahead changes reset per-band Window; selecting the same value or restoring a project/A-B does not. SAFE is renamed TRANSPARENT, with corrected zero-Window handling.

### 1.4.0

- 每段增加同时生效的 L/R Link 和 M/S Link，默认各 100%，支持工程、A/B、自动化与撤销。底部布局收紧，算法按钮缩短为 Classic / Super，OS 移至 FULL/ECO 左侧。
- Adds simultaneous per-band L/R Link and M/S Link, both defaulting to 100%, with project, A/B, automation and undo support. The compact footer uses shorter Classic / Super buttons; OS moves left of FULL/ECO.
- 新增 Display 框选和视图记忆，放大阈值标签。Super Single / Dual UP 默认 -90 dB，有限阈值最低 -90 dB；旧 -inf 或更低值恢复为 -90 dB，Range OFF 保留。
- Adds Display box selection and view memory, with larger threshold labels. Super Single / Dual UP default to -90 dB, with a -90 dB minimum for finite thresholds; older -inf/lower values migrate to -90 dB. Range OFF remains.

最近公开版本为 1.3.3；本次覆盖实际版本 1.4.0、1.4.1、1.4.2、1.4.3、1.4.4、1.4.5、1.4.6，遗漏版本为无。 / The previous public version was 1.3.3. This release covers every actual intermediate version, 1.4.0 through 1.4.6, with none omitted.

### 1.3.3 更新 / Changes in 1.3.3

- **外部侧链 Display 修复：**External key 显示选定侧链经本段 EQ 与 Gain 后的信号电平，与 Window / SAFE 的检测结果分开；历史预览正确使用各段的独立来源和滤波设置，调整 Window 或 EQ 时持续更新。 / **External-sidechain Display:** External key shows the selected sidechain level after per-band EQ and Gain, separately from the Window / SAFE detector result. History previews respect each band's source and filters and update while Window or EQ is adjusted.
- **主音频与侧链同时可见：**普通频谱在外部模式下显示 IN / OUT / EXT，SC EQ 页显示 MAIN / EXT / EQ OUT。 / **Simultaneous spectra:** external mode shows IN / OUT / EXT in the main view and MAIN / EXT / EQ OUT in SC EQ.
- **上方范围改为单击切换：**右上角 ±dB 按钮循环 ±6 / 12 / 24 / 48 dB，无需下拉菜单。下方逐段 Display 的 -30 / -60 / -90 dB 操作保留。 / **One-click upper gain range:** the +/- dB button cycles +/-6 / 12 / 24 / 48 dB without a menu. The lower per-band -30 / -60 / -90 dB Display control is retained.
- **中文悬停说明补齐：**按钮、旋钮、数值框与相关标题均提供中文帮助，包括 Makeup、Mix、Band Output、Master Out 和 Lookahead。Windows 与 Mac 使用支持中文的字体与统一换行。 / **Complete Chinese hover help:** buttons, knobs, value fields and relevant titles include help for Makeup, Mix, Band Output, Master Out and Lookahead. Windows and Mac use Chinese-capable fonts with consistent wrapping. Hover help is in Chinese; the full English manual is included.
- **双语说明书：**中文、英文各 40 页，使用 1.3.3 界面截图；频谱、侧链与悬停操作整合进对应章节。保留已整理的 MATCH、范围/阈值、Lookahead/Window 和独立 SAFE 章节顺序。 / **Bilingual manuals:** 40 pages each with 1.3.3 screenshots. Spectrum, sidechain and hover-help instructions are integrated into their chapters, preserving the MATCH, Display/threshold, Lookahead/Window and separate SAFE sequence.

从最近公开版 1.3.2 到本版，实际新增版本仅 1.3.3；历史版本记录保留在 README。 / Version 1.3.3 is the only new version since public 1.3.2; previous version records remain in the README.

### 1.3.2 - Display 范围与阈值 / Display range and thresholds

- **单击切换显示范围：**每个 Band 的 Display 右上角按钮依次循环 −30 → −60 → −90 → −30 dB，无下拉菜单。曲线、阈值线与右侧推子共用刻度；三档网格分别为 5 / 10 / 15 dB。 / **Single-click display range:** each band's upper-right Display button cycles −30 → −60 → −90 → −30 dB, without a menu. Curves, threshold lines and faders share the scale, with 5 / 10 / 15 dB grid divisions.
- **保留声音参数：**切换范围不改变阈值、Ratio、音量、Window、MATCH 或延迟。低于可见下限的阈值停靠底部并保留真实读数；向上拖动才进入当前范围。双击仍可输入完整参数范围，Alt 重置保持原有规则。 / **Preserved sound settings:** changing the view leaves thresholds, Ratio, gain, Window, MATCH and latency unchanged. Thresholds below the visible floor dock at the bottom while retaining their actual values. Drag upward to enter the visible range. Double-click still accepts the full parameter range and Alt-reset retains its original behavior.
- **逐段记忆：**显示范围随工程保存，重新打开窗口恢复；不参与声音 A/B，不新增音频自动化参数。旧工程及新实例默认 −90 dB。 / **Per-band recall:** ranges are saved with sessions and restored when the editor reopens. They stay outside sound A/B and add no audio automation parameter. Older states and new instances default to −90 dB.
- **重新组织的双语手册：**中文与英文各 40 页。上压、下压与补偿按实际操作顺序说明；MATCH 紧接增益补偿，Display 范围与阈值相邻，Window 与 Lookahead 合并讲解，SAFE 单独成章。 / **Reorganized bilingual manuals:** 40 pages each. Upward/downward compression and compensation follow the working sequence; MATCH follows gain, Display range sits with thresholds, Window is explained with Lookahead, and SAFE has its own chapter.

本次公开包从 1.3.0 直接升级至 1.3.2，同时包含以下 1.3.1 改动。 / This public package upgrades directly from 1.3.0 to 1.3.2 and includes the following 1.3.1 changes.

### 1.3.1 - 自 1.3.0 的更新 / Changes since 1.3.0

- **WINDOW 恢复为毫秒控制：**Normal 与 SAFE 均直接显示每段 WINDOW，取消界面的 DISTORT 百分比；切换 SAFE 保留窗口长度。范围为 0 至当前 Lookahead。 / **WINDOW in milliseconds:** Normal and SAFE both display per-band WINDOW directly, replacing the DISTORT percentage. Switching SAFE preserves its length, from 0 to the current Lookahead.
- **Lookahead 与窗口分工：**Lookahead 为全局预读预留时间，WINDOW 决定每段实际参考的前后时长；窗口逐采样移动，增益逐采样更新。只改 WINDOW 不改变总延迟。手动改 Lookahead 会恢复五段完整窗口；工程、A/B 与撤销恢复保存值。0 ms Lookahead 禁用 WINDOW 与 SAFE 控件，并保留 SAFE 选择。 / **Lookahead and window roles:** global Lookahead reserves read-ahead time; WINDOW sets each band's actual span on either side. Detection and gain update every sample. WINDOW alone does not change total latency. Manual Lookahead edits reset all five windows to full; sessions, A/B and undo restore saved values. At 0 ms Lookahead, WINDOW and SAFE controls are disabled while the SAFE choice is retained.
- **累计 MATCH：**每段从本轮播放开始累计，点击将补偿值写入 MAKEUP。重复点击不清空历史、不叠加上次补偿。普通参数修改、循环与跳转保留统计；停播保留有效结果，重新播放开始新一轮。ECO 分析缺失、Band 关闭、旁路或分频范围变化后，需恢复分析并重新播放。 / **Cumulative MATCH:** each band accumulates from the current playback start and writes compensation into MAKEUP. Repeated clicks neither clear history nor stack adjustments. Parameter edits, loops and seeks retain statistics; stopping keeps a valid result and restarting begins a new pass. After missing ECO analysis, band-off/bypass gaps or crossover changes, restore analysis and start a fresh pass.
- **兼容与手册：**保持已有工程、自动化与逐段窗口长度；保留全局 1x/4x/8x/16x OS、Display 时序、侧链、独立 Dual 算法及 ECO/FULL 静音优化。相关操作已整合进本次中英文 40 页手册。 / **Compatibility and manuals:** preserves existing sessions, automation and per-band window lengths, global 1x/4x/8x/16x OS, Display timing, sidechain, independent Dual algorithms and ECO/FULL silence handling. These operations are integrated into the current 40-page Chinese and English manuals.

### 1.3.0 — 自 1.2.7 的更新 / Changes since 1.2.7

- **逐段 SAFE 与检测窗口：**每段 SAFE 位于 Lookahead 上方，Window / Distort 位于下方。SAFE 使用过去与未来窗口峰值中的较大值；关闭时使用较小值。窗口可逐段调整，Distort 是窗口比例控制，不是实测失真率。 / **Per-band SAFE and detection window:** SAFE sits above Lookahead, with Window / Distort below. SAFE uses the larger past/future window peak; off uses the smaller. Each band has its own window. Distort controls window length, not measured distortion.
- **Lookahead 与迁移：**改为 0 / 26 / 40 / 80 / 100 ms，移除独立 10 ms 档。旧 10 ms 恢复为 26 ms；保留旧自动化入口，新自动化使用不带 Legacy 的 Lookahead。手动改 Lookahead 会重置各段完整窗口，工程、A/B 与撤销恢复保存值。 / **Lookahead and migration:** choices are 0 / 26 / 40 / 80 / 100 ms. Old 10 ms restores as 26 ms. Legacy automation remains; use plain Lookahead for new automation. Manual Lookahead edits reset all windows to full; sessions, A/B and undo restore saved values.
- **统一过采样：**顶部 SC EQ 左侧增加 OS，全局 1x / 4x / 8x / 16x 可用于所有 Lookahead。支持工程、A/B 和新实例偏好；没有 OS 的旧工程保持 1x。 / **Unified oversampling:** global OS to the left of SC EQ provides 1x / 4x / 8x / 16x at every Lookahead, with session, A/B and startup preference support. Old sessions without OS keep 1x.
- **Display 时序：**Lookahead、SAFE、Window、OS 和 A/B 改动会重算历史，保留采集时的音频对齐信息；过期后台结果不会覆盖新设置。 / **Display timing:** these edits recalculate history while preserving captured audio alignment; outdated background results cannot overwrite newer settings.
- **兼容与说明书：**沿用插件身份、原参数顺序、逐段侧链、独立 Dual UP/DOWN 算法与 ECO/FULL 静音优化。中英文完整手册各 39 页。 / **Compatibility and documentation:** retains plug-in identity, original parameter ordering, per-band sidechain, independent Dual UP/DOWN algorithms and ECO/FULL silence handling. Matching Chinese and English manuals have 39 pages each.

### 1.2.7

FULL 增加带增益与尾音保护的极低残留休眠；修正 macOS AU Ratio 参数别名标记，中英文手册更新至各 35 页。 / FULL adds gain- and tail-guarded very-low-residual sleep. macOS AU Ratio alias metadata was corrected, and both language manuals were updated to 35 pages.

---

### 1.2.6

ECO 明确停播时立即静音暂停；FULL 保留实时输入与尾音安全休眠，同时减少检测器冗余计算。 / ECO immediately mutes and suspends on a known Stop; FULL retains live input and tail-safe sleep, while redundant detector calculations were reduced.

### 1.2.5

新实例记住上次手动 ECO/FULL 选择；Linear Phase 在完整输入历史归零后跳过无效 FFT，重复相同参数通知不再干扰休眠。 / New instances remember the last manual ECO/FULL choice. Linear Phase skips FFT work after its full input history reaches zero, and redundant unchanged parameter notifications no longer interrupt idle waiting.

### 1.2.4

加入逐实例 ECO/FULL、Dual UP/DOWN 各自独立的 Classic/Super、分析优化和全零输入的尾音安全休眠。 / Added per-instance ECO/FULL, independent Classic/Super for Dual UP/DOWN, leaner analysis and tail-safe sleep for exact-zero input.

### 1.2.3

修正拖动旋钮、Master Output 或 Band Output 时切换 Shift 会让数值回跳的问题。 / Fixed value jumps when toggling Shift during knob, Master Output or Band Output dragging.

### 1.2.2

Makeup 与各段 Wet Gain 收窄至 ±30 dB，MATCH 同步使用这一范围。 / Makeup and each band's Wet Gain were limited to ±30 dB, with the same bound for MATCH.

### 1.2.1

新菜单提供 This Band、Internal Full、External；旧 Band 1–5 路由继续按 Legacy 恢复，并更新双语手册。此前用户确认的 Stable 为 1.2.1。 / New menus offer This Band, Internal Full and External, while saved Band 1–5 routes restore as Legacy. Updated bilingual manuals. The previously user-confirmed Stable was 1.2.1.

### 1.2.0

逐段新增侧链来源、检测 EQ、增益与 Listen，Single Ratio 扩展至 1:200–200:1；这是本机 Windows 升级，未单独公开 macOS 包。 / Added per-band sidechain sources, detector EQ, gain and Listen, and expanded Single Ratio to 1:200–200:1. This was a local Windows upgrade without a separate public macOS package.

### 1.1.0

- **逐段算法 / Per-band algorithms:** 下方 Ratio 左上角的 ALGO 只控制当前 Band。Classic 按固定 dB Ratio 工作，最低阈值 -90 dB；Super 保留原曲线及 -inf。各段记住最后手动选择，工程与 A/B 恢复各自模式。The ALGO button affects only the selected band. Classic uses a fixed dB ratio and a -90 dB floor; Super retains the original curve and -inf. Manual choices are remembered separately, while sessions and A/B retain their saved modes.
- **Ratio:** Single 1:32–32:1，Dual UP 1:32–1:1、DOWN 1:1–32:1，默认全部 1:1。Single spans 1:32–32:1, Dual UP 1:32–unity and DOWN unity–32:1; all default to unity.
- **A/B:** 可以直接比较不同算法及整套动态设置。相同分频、侧链检测和时序配置下，完整动态结果约 20 ms 交叉淡变；直接切算法约 10 ms。Compare algorithms and complete setups. Compatible configurations crossfade complete dynamics results over approximately 20 ms; direct algorithm changes use approximately 10 ms.
- **Lookahead:** 默认 26 ms，过去与未来窗口共同对齐当前声音，减少大声到来前的提前衰减；可选 10/26/40/80/100 ms。First-use default 26 ms. Past/future windows align detection to the current audio, reducing early attenuation before loud events. Choices: 10/26/40/80/100 ms.
- **MATCH / MAKEUP:** Makeup 扩展为 ±120 dB，移除固定绝对低电平检测门限，支持深度压缩后的有效音频匹配。Makeup extends to ±120 dB and MATCH removes the fixed absolute low-level gate. Valid very quiet signals remain usable; silence cannot provide a match.
- **Display:** 只重建可见 Band 曲线；隐藏 Band 保留历史。收起动态显示不停止音频；频谱复用窗口并在无新音频时跳过 FFT。Only visible-band curves are rebuilt while hidden bands retain history. Collapsing the display does not stop audio; spectrum work reuses its window and skips FFT without new audio.
- **手册 / Manuals:** 上压门槛、Range、Dual 开关与相对 LINK、算法曲线、输出低于阈值的解释、总延迟和旧工程迁移均有说明。Covers the upward gate, Range, Dual switches, relative LINK, algorithm curves, output below threshold, total latency and session migration.

### 1.0.0 — 本地对比版本 / Local comparison version

引入有限阈值的固定 dB Ratio 算法，并曾将 Ratio 扩展到 1:1000–1000:1。本次 1.1.0 根据使用目标恢复 1:32–32:1，并让每段可选择 Classic 或 Super。1.0.0 没有作为独立公开 Release 发布。

Introduced fixed-dB processing for finite thresholds and temporarily extended Ratio to 1:1000–1000:1. Version 1.1.0 returns to 1:32–32:1 and adds per-band Classic / Super selection. Version 1.0.0 was not published as a separate public release.

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

## 5. 历史版本下载 / Previous release downloads

[历史版本生成物与对应说明书 / Older plug-ins and their manuals](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases)
