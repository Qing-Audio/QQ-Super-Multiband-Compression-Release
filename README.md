# QQ Super Multiband Compression 1.4.11 Stable

Qing Audio · 2026-10-27

**[下载 1.4.11 / Download 1.4.11](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/tag/v1.4.11)** · [最新版本 / Latest release](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/latest)

五频段动态处理：逐段 Classic / Super、独立上压与下压、侧链及 EQ、L/R Link 与 M/S Link、Lookahead / Window、TRANSPARENT 和过采样。本产品闭源，本仓库仅提供公开文档和编译成品，源码保持私有。
Five-band dynamics with per-band Classic / Super, independent upward/downward processing, sidechain and EQ, L/R and M/S links, Lookahead / Window, TRANSPARENT and oversampling. This product is closed source; this repository provides public documentation and compiled downloads. Source remains private.

## 下载与手册 / Downloads and manuals

- [Windows 64 位 VST3 / Windows x64 VST3](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.11/QQ-Super-Multiband-Compression-1.4.11-Windows-x64-VST3.zip)
- [Apple Silicon 原生 VST3 / Native Apple Silicon VST3](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.11/QQ-Super-Multiband-Compression-1.4.11-macOS-Apple-Silicon-VST3.zip)
- [Intel 或 Rosetta 宿主 VST3 / Intel or Rosetta host VST3](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.11/QQ-Super-Multiband-Compression-1.4.11-macOS-Intel-VST3.zip)
- [通用 AU / Universal 2 AU](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.11/QQ-Super-Multiband-Compression-1.4.11-macOS-Universal-2-AU.zip)
- [安装说明（中文）](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.11/QQ-Super-Multiband-Compression-1.4.11-Chinese-Installation-Guide.txt)
- [Installation Guide (English)](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.11/QQ-Super-Multiband-Compression-1.4.11-English-Installation-Guide.txt)
- [用户手册 中文版（41 页）](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.11/QQ-Super-Multiband-Compression-1.4.11-Chinese-User-Manual.pdf)
- [User Manual English (41 pages)](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.11/QQ-Super-Multiband-Compression-1.4.11-English-User-Manual.pdf)

共 8 个文件：4 个平台 ZIP、2 份安装说明、2 份本版手册。中文资料使用中文显示标签；本地包直接使用中文文件名。
Eight files: four platform ZIPs, two installation guides and two matching manuals. Chinese documents use Chinese display labels; the local package retains Chinese filenames.

## 安装与平台选择 / Installation and platform selection

Windows 10/11 64 位；macOS 11.0+。Apple Silicon VST3 为 arm64，Intel VST3 为 x86_64（适用于 Intel Mac 或 Rosetta 宿主）；按宿主架构只选一个 VST3 包。Universal 2 AU 同时包含 arm64 和 x86_64，适用于 Logic Pro 等 AU 宿主。
Windows 10/11 64-bit; macOS 11.0+. Apple Silicon VST3 is arm64; Intel VST3 is x86_64 for Intel Macs or Rosetta hosts. Choose one VST3 package matching the host architecture. Universal 2 AU includes both architectures for Logic Pro and other AU hosts.

升级前保存工程并退出宿主，移出旧版同名完整 bundle，再复制新版。Windows VST3 安装到 `C:\Program Files\Common Files\VST3`；Mac 使用 `~/Library/Audio/Plug-Ins/VST3` 或 `~/Library/Audio/Plug-Ins/Components`。重新扫描后确认界面显示 1.4.11；同一格式只保留一份。
Save sessions and quit hosts before moving the old bundle out and copying the complete new one into the matching folder above. Rescan and confirm version 1.4.11. Keep one installed copy per format and retain a session copy for rollback.

Mac 成品为 ad-hoc 签名，未经 Apple Developer ID 公证；单个 bundle 的隔离处理见双语安装说明。GitHub 自动生成的 Source code ZIP/TAR 只是此公开下载仓库的文档快照，不能作为插件安装。
Mac builds are ad-hoc signed, not Apple Developer ID notarized; the bilingual guides explain quarantine handling for the individual bundle. GitHub's automatic Source code ZIP/TAR contains this public download repository's documentation and is not an installable plug-in.


## 逐版本更新 / Changes by version

### 1.4.9

- 修复 Range OFF 时超过 0 dB 的检测、动态处理与 Display，使高电平仍按所选算法处理。
- Corrects detection, dynamics and Display above 0 dB with Range OFF, retaining the selected compression behavior at high levels.

### 1.4.10

- Shift + 上下滚轮可在 -inf（静音底线）至 +24 dB 之间平移 Display，缩放比例保持不变；同步保存视图及中文悬停说明。
- Shift + vertical wheel pans Display between -inf (the silence floor) and +24 dB without changing its zoom span, with saved views and Chinese hints updated.

### 1.4.11

- Threshold、UP THR、DOWN THR 均可调至 -inf；Single / UP 默认保持 −90 dB，DOWN 默认保持 0 dB。保留有限阈值与旧工程数值。
- Threshold, UP THR and DOWN THR now reach -inf. Single / UP defaults remain -90 dB and DOWN remains 0 dB. Finite thresholds and saved session values are preserved.
- Display 中文悬停明确提示右键恢复全视图。中英文 41 页手册同步更新阈值、Display 平移、全视图恢复及 ECO/FREEZE 重开窗口说明。
- The Chinese Display hint explicitly identifies right-click full-view reset. Matching 41-page Chinese and English manuals cover thresholds, panning, reset and ECO/FREEZE editor reopening.


## 验证与限制 / Verification and limits

Windows 复用已验收的 1.4.11 成品。Apple Silicon VST3 在自建 Mac 的原生 arm64 环境验证；Intel VST3 在自建 Apple Silicon Mac 上通过 Rosetta 执行 x86_64 测试程序，验证：阈值端点与默认值、Dual 动态及状态、Display/FREEZE/缩放、Display 高电平、实际 VST3 加载与中文悬停字形。三类 Mac 成品检查版本、架构、bundle 和签名；Universal 2 AU 在 Apple Silicon 上通过 auval。
The accepted Windows 1.4.11 binary is reused. Apple Silicon VST3 is tested natively on a self-hosted arm64 Mac; Intel VST3 is tested with an x86_64 test host through Rosetta on a self-hosted Apple Silicon Mac for threshold endpoints/defaults, Dual dynamics and state, Display/FREEZE/zoom, Display headroom, actual VST3 loading and Chinese tooltip glyphs. All Mac bundles are checked for version, architecture, structure and signature; Universal 2 AU passes auval on Apple Silicon.

Intel AU 未单独运行 auval；自动化验证不等同于对所有 DAW 和长期工程的实测。中英文手册均为对应本版本的 41 页 PDF，已检查字体、页面、书签和链接。
AU auval is not run separately on Intel. Automated checks do not represent testing every DAW or long-running session. Both matching manuals contain 41 pages, with fonts, pages, bookmarks and links checked.


## 历史公开记录 / Previous public records

以下保留历史版本原文；当前下载使用上方 1.4.11 链接。
Historical records follow unchanged. Use the 1.4.11 links above for current downloads.

---

# QQ Super Multiband Compression 1.4.8 Stable

Qing Audio · 2026-10-18

五频段动态处理，支持逐段 Classic / Super、独立上压与下压、外部侧链及 EQ、L/R Link 与 M/S Link、Lookahead / Window、TRANSPARENT 和过采样。
Five-band dynamics with per-band Classic / Super, independent upward/downward processing, external sidechain and EQ, L/R and M/S links, Lookahead / Window, TRANSPARENT and oversampling.

**[下载 1.4.8 / Download 1.4.8](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/tag/v1.4.8)** · [最新版本 / Latest release](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/latest)

本产品闭源，本仓库只提供公开说明和编译成品，源码保持私有。
This product is closed source. This repository contains public documentation and compiled downloads; source remains private.

## 下载选择 / Choose a download

- [Windows 64 位 VST3 / Windows x64 VST3](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.8/QQ-Super-Multiband-Compression-1.4.8-Windows-x64-VST3.zip) — `QQ-Super-Multiband-Compression-1.4.8-Windows-x64-VST3.zip`
- [Apple Silicon 原生 VST3 / Native Apple Silicon VST3](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.8/QQ-Super-Multiband-Compression-1.4.8-macOS-Apple-Silicon-VST3.zip) — `QQ-Super-Multiband-Compression-1.4.8-macOS-Apple-Silicon-VST3.zip`
- [Intel 或 Rosetta 宿主 VST3 / Intel or Rosetta host VST3](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.8/QQ-Super-Multiband-Compression-1.4.8-macOS-Intel-VST3.zip) — `QQ-Super-Multiband-Compression-1.4.8-macOS-Intel-VST3.zip`
- [通用 AU / Universal 2 AU](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.8/QQ-Super-Multiband-Compression-1.4.8-macOS-Universal-2-AU.zip) — `QQ-Super-Multiband-Compression-1.4.8-macOS-Universal-2-AU.zip`
- [安装说明（中文）](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.8/QQ-Super-Multiband-Compression-1.4.8-Chinese-Installation-Guide.txt) — `QQ-Super-Multiband-Compression-1.4.8-Chinese-Installation-Guide.txt`
- [Installation Guide (English)](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.8/QQ-Super-Multiband-Compression-1.4.8-English-Installation-Guide.txt) — `QQ-Super-Multiband-Compression-1.4.8-English-Installation-Guide.txt`

Windows 10/11 64 位；macOS 11.0+。macOS VST3 按宿主运行架构选择一个；Universal 2 AU 同时包含 arm64 和 x86_64。GitHub 的 Source code ZIP/TAR 仅是本下载页面仓库快照，不能安装为插件。
Windows 10/11 64-bit; macOS 11.0+. Choose one macOS VST3 matching the host architecture; Universal 2 AU contains arm64 and x86_64. GitHub's Source code ZIP/TAR is a snapshot of this download-page repository, not an installable plug-in.

## 安装与升级 / Installation and upgrade

保存工程并退出宿主，将旧版完整 bundle 移出扫描路径后，再复制新 bundle。Windows VST3 使用 `C:\Program Files\Common Files\VST3`；macOS 使用 `~/Library/Audio/Plug-Ins/VST3` 或 `~/Library/Audio/Plug-Ins/Components`。重新打开宿主并重新扫描，确认界面版本 1.4.8。同一格式只保留一份。
Save sessions and quit hosts. Move the old complete bundle out of scan paths, then copy the new bundle to the matching directory above. Reopen and rescan, confirm version 1.4.8, and keep one copy of each format.

Mac 成品为 ad-hoc 签名，未经过 Apple Developer ID 公证；必要的单个 bundle 解除隔离步骤见安装说明。
Mac builds are ad-hoc signed, not Apple Developer ID notarized. See the installation guides for quarantine handling for the individual trusted bundle.

## 手册 / Manuals

本次不修订或重命名手册。[1.4.6 中英文手册](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/tag/v1.4.6)仍可用于一般功能参考；它们不包含下述 ECO 重开修复，请以本次更新说明为准。
The [1.4.6 manuals](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/tag/v1.4.6) remain unchanged and available for general reference. They do not document the ECO reopening fix below; these release notes take precedence.

## 1.4.7 → 1.4.8 更新 / Changes since 1.4.6

### 1.4.7

- 修复 QQ Host 等宿主保留并隐藏插件原生窗口时，ECO 未正确停止分析的问题；重开后拒绝旧表计及过期重算数据。五个频段统一处理，声音不变。
- Fixes ECO analysis remaining active when hosts such as QQ Host retain a hidden native editor. Reopening rejects stale meter and replay data across all five bands without changing audio.

### 1.4.8

- ECO 关闭界面再打开时，无论 FREEZE 是否点亮，Display 都清除旧图并从新采集数据开始显示；保留缩放与 FREEZE 选择。
- Reopening the editor in ECO clears old Display curves and starts with newly captured data whether FREEZE is on or off, while retaining zoom and the FREEZE choice.
- 界面持续打开时，FREEZE 仍保留停播曲线；FULL、声音处理与 MATCH 完整播放要求保持。中文 FREEZE 悬停同步更新。
- With the editor continuously open, FREEZE still retains stopped curves. FULL, audio processing and MATCH's complete-playback requirement are preserved. Chinese FREEZE help is updated.

上次完整同步/公开版本为 1.4.6，本次区间为 1.4.7、1.4.8；遗漏版本：无。 / Previous complete sync/public version: 1.4.6. Versions covered: 1.4.7 and 1.4.8; none omitted.


## 验证与已知限制 / Verification and limits

Windows 已完成原生保留窗口/重建窗口回归、五频段音频一致性、Display/Freeze/缩放、中文悬停及真实 VST3 加载验证。macOS 的 Apple Silicon VST3 在原生 arm64 环境、Intel VST3 在原生 Intel Mac 上执行插件加载与回归；Universal 2 AU 在 Apple Silicon 上通过 auval，并检查两种架构及签名。Windows 的原生隐藏窗口专项用例不代表已在 Mac QQ Host 中执行同样验证；Intel AU 未单独运行 auval。
Windows verification covers retained/recreated native editors, five-band audio equality, Display/Freeze/zoom, Chinese hints and actual VST3 loading. Apple Silicon VST3 runs on native arm64 and Intel VST3 runs on an Intel Mac for loading and regressions. Universal 2 AU passes auval on Apple Silicon with both architectures and signatures checked. The Windows native-hidden-window fixture is not a claim of equivalent Mac QQ Host testing; AU auval is not run separately on Intel.

## 历史公开记录 / Previous public records

以下原文保留对应历史版本；当前下载使用上方 1.4.8 链接。
The following records retain their historical versions. Use the 1.4.8 links above for current downloads.

---

# QQ Super Multiband Compression 1.4.6

**Qing Audio · Stable 1.4.6 · 2026-10-16**

最多五段独立动态处理，每段提供 Classic / Super、上压 / 下压 / Dual、L/R Link 与 M/S Link、TRANSPARENT、Window 和侧链 EQ；全局 Lookahead、过采样及 ECO / FULL 统一控制时序与性能。

Up to five independent bands with Classic / Super, upward / downward / Dual compression, L/R Link and M/S Link, TRANSPARENT, Window and sidechain EQ. Global Lookahead, oversampling and ECO / FULL control timing and performance.

本产品闭源。本仓库仅提供编译插件和用户文档，源码保持私有。 / This product is closed source. This repository provides compiled plug-ins and user documentation; source remains private.

## 下载 / Downloads

[**1.4.6 正式下载 / Release 1.4.6**](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/tag/v1.4.6)

| 文件 / File | 下载 / Download |
|---|---|
| Windows x64 · VST3 | [Windows x64 · VST3](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.6/QQ-Super-Multiband-Compression-1.4.6-Windows-x64-VST3.zip) |
| Apple Silicon / arm64 · VST3 | [Apple Silicon / arm64 · VST3](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.6/QQ-Super-Multiband-Compression-1.4.6-macOS-Apple-Silicon-VST3.zip) |
| Intel / x86_64 · VST3 | [Intel / x86_64 · VST3](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.6/QQ-Super-Multiband-Compression-1.4.6-macOS-Intel-VST3.zip) |
| Universal 2 · AU | [Universal 2 · AU](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.6/QQ-Super-Multiband-Compression-1.4.6-macOS-Universal-2-AU.zip) |
| 安装说明（中文） | [安装说明（中文）](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.6/QQ-Super-Multiband-Compression-1.4.6-Chinese-Installation-Guide.txt) |
| Installation Guide (English) | [Installation Guide (English)](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.6/QQ-Super-Multiband-Compression-1.4.6-English-Installation-Guide.txt) |
| 用户手册 中文版 · 41 页 | [用户手册 中文版 · 41 页](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.6/QQ-Super-Multiband-Compression-1.4.6-Chinese-User-Manual.pdf) |
| User Manual English · 41 pages | [User Manual English · 41 pages](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.4.6/QQ-Super-Multiband-Compression-1.4.6-English-User-Manual.pdf) |

Windows 使用 Win 包；macOS VST3 按宿主实际架构二选一，Logic Pro 使用 Universal 2 AU。GitHub 使用兼容的附件文件名，中文资料在下载入口和附件标签中标为中文；桌面包中文资料直接使用中文文件名。GitHub 自动生成的 “Source code” 归档仅包含此下载仓库的文档，不包含插件源码或安装文件。

Use the Windows package on Windows. Select one macOS VST3 package for the host architecture, or Universal 2 AU for Logic Pro. GitHub asset filenames use compatible characters; Chinese documents have Chinese download labels. GitHub-generated “Source code” archives contain this download repository's documentation, not plug-in source or installers.

## 逐版本更新 / Version history since the previous public release

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

## 安装、兼容性与验证 / Installation, compatibility and validation

Windows 10/11 x64；macOS 11.0 或更新版本。先保存工程、保留旧完整 bundle 并退出宿主，再移出扫描路径内的旧同名插件、复制完整新 bundle、重新扫描。同一格式只保留一份。

Windows 10/11 x64 and macOS 11.0 or newer. Save the session, keep the old complete bundle and exit the host before replacing it. Remove duplicate bundles from scan paths, copy the complete new bundle and rescan.

- Windows VST3：`C:\Program Files\Common Files\VST3`
- macOS VST3：`~/Library/Audio/Plug-Ins/VST3` 或 / or `/Library/Audio/Plug-Ins/VST3`
- macOS AU：`~/Library/Audio/Plug-Ins/Components` 或 / or `/Library/Audio/Plug-Ins/Components`

macOS 成品为 ad-hoc 签名，未经 Developer ID 公证；首次加载可能需要按安装说明处理下载隔离。AU 与 VST3 为独立格式；Apple Silicon 与 Intel VST3 不要同时安装。

macOS bundles are ad-hoc signed and not Developer ID notarized. First load may require the quarantine steps in the installation guide. AU and VST3 are separate formats; do not install both VST3 architecture packages together.

保留插件身份及原参数 ID/顺序；新增声道 Link 与 EQ 开关参数追加在原参数之后。旧工程缺少 Link 时为 100%/100%，缺少 EQ 开关时为 ON，旧 SAFE 状态映射到 TRANSPARENT。升级前另存工程，核对 Lookahead、阈值、侧链与自动化后试听；回滚时退出宿主并恢复旧 bundle 与升级前工程。

Plug-in identity and existing parameter IDs/order are retained; Link and EQ-switch parameters are appended. Older sessions default missing Links to 100%/100% and missing EQ switches to ON; saved SAFE state maps to TRANSPARENT. Save a session copy and check Lookahead, thresholds, sidechain and automation after upgrading. To roll back, exit the host and restore the old bundle and pre-upgrade session.

Windows 复用已验证成品。Apple Silicon 与 Intel VST3 进行原生音频、状态、延迟、实际加载/界面、中文字体及 Display/EQ 检查；Universal 2 AU 在 Apple Silicon 上运行 auval，并核对双架构与签名。Intel AU 未单独运行 auval；这些检查不代替各宿主实际工程试听。

Windows reuses the accepted build. Apple Silicon and Intel VST3 undergo native audio/state/latency, actual loading/editor, Chinese font and Display/EQ checks. Universal 2 AU runs auval on Apple Silicon, with both architectures and signature verified. Intel AU has no separate auval runtime check; these checks do not replace auditioning real sessions in each host.

---

## 以往公开记录 / Earlier public records

# QQ Super Multiband Compression 1.3.3

**Qing Audio · Stable 1.3.3 · 2026-10-12**

最多五段独立动态处理，每段可选择 Classic / Super、上压 / 下压 / Dual、SAFE、Window 和侧链 EQ。全局 Lookahead、1x / 4x / 8x / 16x 过采样及 ECO / FULL 用于统一时序和性能设置。

Up to five independently controlled bands with Classic / Super algorithms, upward / downward / Dual compression, SAFE, Window and sidechain EQ. Global Lookahead, 1x / 4x / 8x / 16x oversampling and ECO / FULL control timing and performance.

本产品闭源，本仓库只提供编译成品与用户文档，源码保持私有。 / This is a closed-source product. This repository distributes compiled plug-ins and user documentation; source code remains private.

## 下载与附件清单 / Downloads and assets

[打开 1.3.3 下载页 / Open the release](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/tag/v1.3.3)

| 文件 / File | 格式 / Format |
|---|---|
| [Windows x64 VST3](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.3/QQ-Super-Multiband-Compression-1.3.3-Windows-x64-VST3.zip) | ZIP |
| [macOS Apple Silicon VST3](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.3/QQ-Super-Multiband-Compression-1.3.3-macOS-Apple-Silicon-VST3.zip) | ZIP |
| [macOS Intel VST3](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.3/QQ-Super-Multiband-Compression-1.3.3-macOS-Intel-VST3.zip) | ZIP |
| [macOS Universal 2 AU](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.3/QQ-Super-Multiband-Compression-1.3.3-macOS-Universal-2-AU.zip) | ZIP |
| [中文安装说明](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.3/QQ-Super-Multiband-Compression-1.3.3-Chinese-Installation-Guide.txt) | TXT |
| [English installation guide](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.3/QQ-Super-Multiband-Compression-1.3.3-English-Installation-Guide.txt) | TXT |
| [中文用户手册 · 40 页](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.3/QQ-Super-Multiband-Compression-1.3.3-Chinese-User-Manual.pdf) | PDF |
| [English user manual · 40 pages](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.3/QQ-Super-Multiband-Compression-1.3.3-English-User-Manual.pdf) | PDF |

共 8 个附件。GitHub 使用兼容下载文件名，中文资料保留中文显示标签；桌面交付包直接使用中文文件名。 / Eight assets. GitHub uses compatible download filenames with Chinese display labels; the desktop package uses Chinese filenames directly.

## 1.3.3 更新 / Changes in 1.3.3

- **外部侧链 Display 修复：**External key 显示选定侧链经本段 EQ 与 Gain 后的信号电平，与 Window / SAFE 的检测结果分开；历史预览正确使用各段的独立来源和滤波设置，调整 Window 或 EQ 时持续更新。 / **External-sidechain Display:** External key shows the selected sidechain level after per-band EQ and Gain, separately from the Window / SAFE detector result. History previews respect each band's source and filters and update while Window or EQ is adjusted.
- **主音频与侧链同时可见：**普通频谱在外部模式下显示 IN / OUT / EXT，SC EQ 页显示 MAIN / EXT / EQ OUT。 / **Simultaneous spectra:** external mode shows IN / OUT / EXT in the main view and MAIN / EXT / EQ OUT in SC EQ.
- **上方范围改为单击切换：**右上角 ±dB 按钮循环 ±6 / 12 / 24 / 48 dB，无需下拉菜单。下方逐段 Display 的 -30 / -60 / -90 dB 操作保留。 / **One-click upper gain range:** the +/- dB button cycles +/-6 / 12 / 24 / 48 dB without a menu. The lower per-band -30 / -60 / -90 dB Display control is retained.
- **中文悬停说明补齐：**按钮、旋钮、数值框与相关标题均提供中文帮助，包括 Makeup、Mix、Band Output、Master Out 和 Lookahead。Windows 与 Mac 使用支持中文的字体与统一换行。 / **Complete Chinese hover help:** buttons, knobs, value fields and relevant titles include help for Makeup, Mix, Band Output, Master Out and Lookahead. Windows and Mac use Chinese-capable fonts with consistent wrapping. Hover help is in Chinese; the full English manual is included.
- **双语说明书：**中文、英文各 40 页，使用 1.3.3 界面截图；频谱、侧链与悬停操作整合进对应章节。保留已整理的 MATCH、范围/阈值、Lookahead/Window 和独立 SAFE 章节顺序。 / **Bilingual manuals:** 40 pages each with 1.3.3 screenshots. Spectrum, sidechain and hover-help instructions are integrated into their chapters, preserving the MATCH, Display/threshold, Lookahead/Window and separate SAFE sequence.

从最近公开版 1.3.2 到本版，实际新增版本仅 1.3.3；历史版本记录保留在 README。 / Version 1.3.3 is the only new version since public 1.3.2; previous version records remain in the README.

## 兼容性与验证 / Compatibility and validation

本次调整显示和界面帮助，保留插件身份、宿主参数与延迟。Windows 1.3.2/1.3.3 的 16 组真实 VST3 对比逐采样差值为 0。Windows 与 Mac 均通过实际 VST3 加载及中文提示检查；两种 Mac VST3 通过动态、侧链、Lookahead/Window、MATCH、显示范围及外部 Display 回归。Universal 2 AU 通过 Apple Silicon 上的 auval，两个架构切片与签名已检查。

These changes address display and interface help, preserving plug-in identity, host parameters and latency. Sixteen actual Windows VST3 comparisons against 1.3.2 produced zero sample difference. Windows and Mac passed real VST3 loading and Chinese tooltip checks; both Mac VST3 architectures passed dynamics, sidechain, Lookahead/Window, MATCH, range and external Display regressions. Universal 2 AU passed auval on Apple Silicon; both architecture slices and signatures were checked.

## 安装与升级 / Installation and upgrade

- Windows 10/11 x64：关闭宿主，将整个 `.vst3` 文件夹复制到 `C:\Program Files\Common Files\VST3`，重新扫描并确认 1.3.3。 / Windows 10/11 x64: quit the host, copy the entire `.vst3` folder to `C:\Program Files\Common Files\VST3`, rescan and confirm 1.3.3.
- macOS 11+：按宿主架构只选择一种 VST3；原生 Apple Silicon 选 arm64，Intel/Rosetta 宿主选 Intel。放入 `~/Library/Audio/Plug-Ins/VST3`；AU 放入 `~/Library/Audio/Plug-Ins/Components`。 / macOS 11+: choose one VST3 architecture matching the host: arm64 for native Apple Silicon, Intel for Intel/Rosetta. Install VST3 in `~/Library/Audio/Plug-Ins/VST3`, AU in `~/Library/Audio/Plug-Ins/Components`.
- 保存工程副本与旧插件后再升级；扫描目录不要保留同格式重复副本。先选 Band、确认来源与阈值，再调 Ratio、Mix 和增益；MATCH 用于当前段响度比较。 / Save a session copy and previous bundle before upgrading. Keep one installed copy per format. Select a band, confirm source and thresholds, then adjust Ratio, Mix and gain; use MATCH for per-band level comparison.

## 已知限制 / Known limitations

Mac 采用 ad-hoc 签名，未经过 Developer ID 公证；首次加载与隔离处理见安装说明。Intel AU 切片已检查，但没有独立的 Intel AU 运行验证。自动验证不代表所有宿主与长期工程均已人工试听。Normal 分频的原有相位特性与声音处理未在本版改变。

Mac builds are ad-hoc signed, without Developer ID notarization; see the installation guide for first-load and quarantine steps. The Intel AU slice was inspected without a separate Intel AU runtime test. Automated checks do not imply long-session listening tests in every host. Existing Normal crossover phase behavior and audio processing are unchanged.


---

<details>
<summary>历史版本记录 / Earlier version history</summary>

以下内容描述其原版本。 / These records describe their original versions.

# QQ Super Multiband Compression 1.3.2

**Qing Audio · Stable 1.3.2 · 2026-10-11**

QQ Super Compression 的多段扩展版：最多五段，独立 Classic/Super、向上/向下/双压及侧链 EQ。1.3.2 增加逐段 Display 范围单击切换，并包含 1.3.1 的毫秒 Window 与累计 MATCH。

The multiband extension of QQ Super Compression: up to five bands with independent Classic/Super, upward/downward/Dual processing and sidechain EQ. Version 1.3.2 adds per-band Display range cycling and includes the millisecond Window and cumulative MATCH changes from 1.3.1.

## 下载 / Downloads

[打开 1.3.2 下载页 / Open the 1.3.2 release](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/tag/v1.3.2)

| 下载 / Download | 格式 / Format |
|---|---|
| [Windows 10/11 x64](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.2/QQ-Super-Multiband-Compression-1.3.2-Windows-x64-VST3.zip) | VST3 |
| [macOS Apple Silicon](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.2/QQ-Super-Multiband-Compression-1.3.2-macOS-Apple-Silicon-VST3.zip) | VST3 |
| [macOS Intel / Rosetta](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.2/QQ-Super-Multiband-Compression-1.3.2-macOS-Intel-VST3.zip) | VST3 |
| [macOS Universal 2](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.2/QQ-Super-Multiband-Compression-1.3.2-macOS-Universal-2-AU.zip) | AU |
| [中文安装说明](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.2/QQ-Super-Multiband-Compression-1.3.2-Chinese-Installation-Guide.txt) | TXT |
| [English installation guide](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.2/QQ-Super-Multiband-Compression-1.3.2-English-Installation-Guide.txt) | TXT |
| [中文用户手册 · 40 页](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.2/QQ-Super-Multiband-Compression-1.3.2-Chinese-User-Manual.pdf) | PDF |
| [English user manual · 40 pages](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.2/QQ-Super-Multiband-Compression-1.3.2-English-User-Manual.pdf) | PDF |

## 1.3.2 - Display 范围与阈值 / Display range and thresholds

- **单击切换显示范围：**每个 Band 的 Display 右上角按钮依次循环 −30 → −60 → −90 → −30 dB，无下拉菜单。曲线、阈值线与右侧推子共用刻度；三档网格分别为 5 / 10 / 15 dB。 / **Single-click display range:** each band's upper-right Display button cycles −30 → −60 → −90 → −30 dB, without a menu. Curves, threshold lines and faders share the scale, with 5 / 10 / 15 dB grid divisions.
- **保留声音参数：**切换范围不改变阈值、Ratio、音量、Window、MATCH 或延迟。低于可见下限的阈值停靠底部并保留真实读数；向上拖动才进入当前范围。双击仍可输入完整参数范围，Alt 重置保持原有规则。 / **Preserved sound settings:** changing the view leaves thresholds, Ratio, gain, Window, MATCH and latency unchanged. Thresholds below the visible floor dock at the bottom while retaining their actual values. Drag upward to enter the visible range. Double-click still accepts the full parameter range and Alt-reset retains its original behavior.
- **逐段记忆：**显示范围随工程保存，重新打开窗口恢复；不参与声音 A/B，不新增音频自动化参数。旧工程及新实例默认 −90 dB。 / **Per-band recall:** ranges are saved with sessions and restored when the editor reopens. They stay outside sound A/B and add no audio automation parameter. Older states and new instances default to −90 dB.
- **重新组织的双语手册：**中文与英文各 40 页。上压、下压与补偿按实际操作顺序说明；MATCH 紧接增益补偿，Display 范围与阈值相邻，Window 与 Lookahead 合并讲解，SAFE 单独成章。 / **Reorganized bilingual manuals:** 40 pages each. Upward/downward compression and compensation follow the working sequence; MATCH follows gain, Display range sits with thresholds, Window is explained with Lookahead, and SAFE has its own chapter.

本次公开包从 1.3.0 直接升级至 1.3.2，同时包含以下 1.3.1 改动。 / This public package upgrades directly from 1.3.0 to 1.3.2 and includes the following 1.3.1 changes.

## 1.3.1 - 自 1.3.0 的更新 / Changes since 1.3.0

- **WINDOW 恢复为毫秒控制：**Normal 与 SAFE 均直接显示每段 WINDOW，取消界面的 DISTORT 百分比；切换 SAFE 保留窗口长度。范围为 0 至当前 Lookahead。 / **WINDOW in milliseconds:** Normal and SAFE both display per-band WINDOW directly, replacing the DISTORT percentage. Switching SAFE preserves its length, from 0 to the current Lookahead.
- **Lookahead 与窗口分工：**Lookahead 为全局预读预留时间，WINDOW 决定每段实际参考的前后时长；窗口逐采样移动，增益逐采样更新。只改 WINDOW 不改变总延迟。手动改 Lookahead 会恢复五段完整窗口；工程、A/B 与撤销恢复保存值。0 ms Lookahead 禁用 WINDOW 与 SAFE 控件，并保留 SAFE 选择。 / **Lookahead and window roles:** global Lookahead reserves read-ahead time; WINDOW sets each band's actual span on either side. Detection and gain update every sample. WINDOW alone does not change total latency. Manual Lookahead edits reset all five windows to full; sessions, A/B and undo restore saved values. At 0 ms Lookahead, WINDOW and SAFE controls are disabled while the SAFE choice is retained.
- **累计 MATCH：**每段从本轮播放开始累计，点击将补偿值写入 MAKEUP。重复点击不清空历史、不叠加上次补偿。普通参数修改、循环与跳转保留统计；停播保留有效结果，重新播放开始新一轮。ECO 分析缺失、Band 关闭、旁路或分频范围变化后，需恢复分析并重新播放。 / **Cumulative MATCH:** each band accumulates from the current playback start and writes compensation into MAKEUP. Repeated clicks neither clear history nor stack adjustments. Parameter edits, loops and seeks retain statistics; stopping keeps a valid result and restarting begins a new pass. After missing ECO analysis, band-off/bypass gaps or crossover changes, restore analysis and start a fresh pass.
- **兼容与手册：**保持已有工程、自动化与逐段窗口长度；保留全局 1x/4x/8x/16x OS、Display 时序、侧链、独立 Dual 算法及 ECO/FULL 静音优化。相关操作已整合进本次中英文 40 页手册。 / **Compatibility and manuals:** preserves existing sessions, automation and per-band window lengths, global 1x/4x/8x/16x OS, Display timing, sidechain, independent Dual algorithms and ECO/FULL silence handling. These operations are integrated into the current 40-page Chinese and English manuals.

## 安装与使用 / Installation and use

升级前保存工程副本并完全退出音频宿主，替换整个插件 bundle。Windows 使用 x64 VST3；macOS 按宿主架构选择 Apple Silicon 或 Intel VST3，Logic 等 AU 宿主使用 Universal 2 AU。macOS 需 11.0 或更新版本，同一种格式不要重复安装。

Save a session copy and fully quit audio hosts before replacing the complete bundle. Use x64 VST3 on Windows. On macOS 11 or later, choose Apple Silicon or Intel VST3 for the host architecture, or Universal 2 AU for Logic and other AU hosts. Avoid duplicate installations of the same format.

短窗口尤其低于 10 ms 时，可比较较高 OS 对混叠的改善。总延迟包含分频、Lookahead 和 OS 滤波器，0 ms Lookahead 不等于整机零延迟。FULL 支持停播监听；ECO 在明确停播时静音，播放中关闭 ECO 窗口会使本轮 MATCH 统计不完整。

For short windows, especially below 10 ms, compare higher OS for alias reduction. Total latency includes crossover, Lookahead and OS filters, so 0 ms Lookahead is not zero plug-in latency. FULL supports stopped monitoring; ECO mutes on a known Stop. Closing the ECO editor during playback makes that MATCH pass incomplete.

## 验证与已知事项 / Validation and known considerations

Windows 沿用已验收的 1.3.2 单击切换版构建及既有验证；新增显示范围专项与真实 VST3 加载均通过。两种 macOS VST3 均验证原生加载、动态、侧链、SAFE/Window/OS/Display 、WINDOW/累计 MATCH 及 1.3.2 显示范围；Apple Silicon 另验证 FULL 静音。Universal 2 AU 在 Apple Silicon 通过 auval，并核对两种架构切片与 ad-hoc 签名。未单独执行 Intel AU auval，未做 Apple Developer ID 公证；自动检查不等同于所有 DAW 的长期试听。

The accepted Windows 1.3.2 click-cycle build and its existing checks are reused, including display-range regression and actual VST3 loading. Both macOS VST3 builds validate native loading, dynamics, sidechain, SAFE/Window/OS/Display, WINDOW/cumulative MATCH, and 1.3.2 Display range; Apple Silicon additionally validates FULL idle handling. Universal 2 AU passes auval on Apple Silicon, with both architecture slices and ad-hoc signatures checked. Separate Intel AU auval and Apple Developer ID notarization were not performed. Automated checks do not replace long-session listening in every DAW.

## 许可与源码 / License and source

产品保持闭源。此公开仓库只提供编译成品和用户文档。GitHub 自动生成的 Source code ZIP/TAR 仅包含本公开页面仓库，不含压缩器源码，也不是插件安装包。中文文档在页面上使用中文标签和下载链接；本地包使用中文文件名。

This product remains proprietary. This public repository provides compiled binaries and user documentation. GitHub's automatic Source code archives contain only this public page repository, not compressor source or plug-in installers. Chinese documents have Chinese display labels and download links; the local package uses Chinese filenames.

Copyright © 2026 Qing Audio. All rights reserved.

---

<details>
<summary>历史版本记录 / Earlier version history</summary>

以下内容描述其原版本。 / The following records describe their original versions.

# QQ Super Multiband Compression 1.3.0

**Qing Audio · Stable 1.3.0 · 2026-10-09**

QQ Super Compression 的多段扩展版：最多五段，独立 Classic / Super、向下 / 向上 / 双压、侧链检测 EQ。本版加入逐段 SAFE 与 Window / Distort、全局 OS，并更新 Lookahead 与 Display 时序。

The multiband extension of QQ Super Compression: up to five bands with independent Classic / Super, downward / upward / Dual processing and sidechain detector EQ. This release adds per-band SAFE and Window / Distort, global OS, and revised Lookahead and Display timing.

## 下载 / Downloads

[打开 1.3.0 下载页 / Open the 1.3.0 release](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/tag/v1.3.0)

| 下载 / Download | 格式 / Format |
|---|---|
| [Windows 10/11 x64](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.0/QQ-Super-Multiband-Compression-1.3.0-Windows-x64-VST3.zip) | VST3 |
| [macOS Apple Silicon](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.0/QQ-Super-Multiband-Compression-1.3.0-macOS-Apple-Silicon-VST3.zip) | VST3 |
| [macOS Intel / Rosetta](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.0/QQ-Super-Multiband-Compression-1.3.0-macOS-Intel-VST3.zip) | VST3 |
| [macOS Universal 2](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.0/QQ-Super-Multiband-Compression-1.3.0-macOS-Universal-2-AU.zip) | AU |
| [中文安装说明](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.0/QQ-Super-Multiband-Compression-1.3.0-Chinese-Installation-Guide.txt) | TXT |
| [English installation guide](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.0/QQ-Super-Multiband-Compression-1.3.0-English-Installation-Guide.txt) | TXT |
| [中文用户手册 · 39 页](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.0/QQ-Super-Multiband-Compression-1.3.0-Chinese-User-Manual.pdf) | PDF |
| [English user manual · 39 pages](https://github.com/Qing-Audio/QQ-Super-Multiband-Compression-Release/releases/download/v1.3.0/QQ-Super-Multiband-Compression-1.3.0-English-User-Manual.pdf) | PDF |

## 1.3.0 — 自 1.2.7 的更新 / Changes since 1.2.7

- **逐段 SAFE 与检测窗口：**每段 SAFE 位于 Lookahead 上方，Window / Distort 位于下方。SAFE 使用过去与未来窗口峰值中的较大值；关闭时使用较小值。窗口可逐段调整，Distort 是窗口比例控制，不是实测失真率。 / **Per-band SAFE and detection window:** SAFE sits above Lookahead, with Window / Distort below. SAFE uses the larger past/future window peak; off uses the smaller. Each band has its own window. Distort controls window length, not measured distortion.
- **Lookahead 与迁移：**改为 0 / 26 / 40 / 80 / 100 ms，移除独立 10 ms 档。旧 10 ms 恢复为 26 ms；保留旧自动化入口，新自动化使用不带 Legacy 的 Lookahead。手动改 Lookahead 会重置各段完整窗口，工程、A/B 与撤销恢复保存值。 / **Lookahead and migration:** choices are 0 / 26 / 40 / 80 / 100 ms. Old 10 ms restores as 26 ms. Legacy automation remains; use plain Lookahead for new automation. Manual Lookahead edits reset all windows to full; sessions, A/B and undo restore saved values.
- **统一过采样：**顶部 SC EQ 左侧增加 OS，全局 1x / 4x / 8x / 16x 可用于所有 Lookahead。支持工程、A/B 和新实例偏好；没有 OS 的旧工程保持 1x。 / **Unified oversampling:** global OS to the left of SC EQ provides 1x / 4x / 8x / 16x at every Lookahead, with session, A/B and startup preference support. Old sessions without OS keep 1x.
- **Display 时序：**Lookahead、SAFE、Window、OS 和 A/B 改动会重算历史，保留采集时的音频对齐信息；过期后台结果不会覆盖新设置。 / **Display timing:** these edits recalculate history while preserving captured audio alignment; outdated background results cannot overwrite newer settings.
- **兼容与说明书：**沿用插件身份、原参数顺序、逐段侧链、独立 Dual UP/DOWN 算法与 ECO/FULL 静音优化。中英文完整手册各 39 页。 / **Compatibility and documentation:** retains plug-in identity, original parameter ordering, per-band sidechain, independent Dual UP/DOWN algorithms and ECO/FULL silence handling. Matching Chinese and English manuals have 39 pages each.

## 安装与使用 / Installation and use

升级前保存工程副本并完全退出宿主，替换完整插件 bundle，再重新扫描。Windows VST3：`C:\Program Files\Common Files\VST3`；macOS VST3：`~/Library/Audio/Plug-Ins/VST3`；AU：`~/Library/Audio/Plug-Ins/Components`。macOS 需 11.0 或更新版本，按宿主实际架构只选一个 VST3，Rosetta 下的 Intel 宿主选 Intel 包。详细安装和安全处理见上方中文安装说明。

Save a session copy and fully quit the host before replacing the complete bundle and rescanning. Windows VST3: `C:\Program Files\Common Files\VST3`; macOS VST3: `~/Library/Audio/Plug-Ins/VST3`; AU: `~/Library/Audio/Plug-Ins/Components`. macOS 11 or later is required. Choose one VST3 matching the host architecture; Intel hosts under Rosetta need the Intel build. See the installation guide for detailed steps and security handling.

选择频段后设置 Ratio、Threshold、Mix 和窗口。停播需实时监听时选 FULL；ECO 在明确停播时静音并暂停 DSP。SAFE 是检测模式，不会消除 Normal 分频的相位偏移。总延迟包含分频、Lookahead 和 OS 滤波器，0 ms Lookahead 也有插件延迟；升级旧 10 ms 工程后请检查关键片段和宿主补偿。

Select a band and set Ratio, Threshold, Mix and its window. Use FULL for live stopped-input monitoring; ECO mutes and suspends on a known Stop. SAFE is a detector mode and does not remove Normal crossover phase rotation. Total latency includes crossover, Lookahead and OS filters: 0 ms Lookahead still has plug-in latency. Check key passages and host compensation after upgrading an old 10 ms session.

## 验证与已知事项 / Validation and known considerations

Windows 成品沿用已接受的构建与验证。两种 macOS VST3 均通过原生加载、动态、侧链及 1.3.0 SAFE / Window / OS / Display 回归；Apple Silicon 另通过 FULL 静音回归。Universal 2 AU 在 Apple Silicon 通过 auval，两种架构切片及 ad-hoc 签名已核对。未单独执行 Intel AU 的 auval，未做 Apple Developer ID 公证。自动检查不等于所有 DAW 的长期工程试听。

The accepted Windows build and verification are reused. Both macOS VST3 architectures passed native loading, dynamics, sidechain and 1.3.0 SAFE / Window / OS / Display regression; Apple Silicon also passed FULL idle regression. Universal 2 AU passed auval on Apple Silicon, with both architecture slices and ad-hoc signatures checked. Separate Intel AU auval and Apple Developer ID notarization were not performed. Automated checks do not replace long-session listening in every DAW.

## 许可与源码 / License and source

本产品保持闭源，公开仓库只提供成品与用户文档。GitHub 自动列出的 Source code ZIP/TAR 是本公开页面仓库的文件，不是插件安装包，也不含压缩器源码。中文资料以中文标签和链接标明；GitHub 下载文件使用兼容文件名。

This product remains proprietary. The public repository provides compiled downloads and user documentation. GitHub's automatic Source code archives contain this public page repository, not plug-in installers or compressor source. Chinese documents have Chinese display labels and download links; GitHub downloads use portable filenames.

Copyright © 2026 Qing Audio. All rights reserved.

---

<details>
<summary>历史版本记录 / Earlier version history</summary>

以下内容按其版本日期保留，其中参数范围、手册页数与截图代表对应历史版本。 / The following records describe their dated historical versions.

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

</details>

</details>

</details>
