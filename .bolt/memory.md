# Project memory

## Product intent & audience

- MelodyFlow 播放器应用的 OTA（在线更新）版本清单仓库。
- 用途：应用在检查更新时读取 `version.json`，对比版本号后提示用户更新。
- 非传统网页应用，无界面、无数据库，仅为供应用读取的配置文件仓库。
- 受众：MelodyFlow 应用本身（自动化读取）；以及可能查看版本历史的用户。

## Brand personality & voice

- 极简、技术化；当前仅以最短说明表达用途，无营销语气。

## Visual design & UX direction

- 无 UI / 无前端交互；项目仅由静态文件组成，不涉及视觉设计。
- 用户可读内容仅限 `README.md` 一句话说明与 `version.json` 中的更新说明文本。

## Decisions, constraints & rationale

- 仅包含两个文件：
  - `version.json`：OTA 版本信息，当前版本 **1.0.10**，发布日期 **2026-11-12**。
  - `README.md`：一句话说明，表明这是 MelodyFlow 的公开 OTA 版本清单。
- `version.json` 记录内容：版本号、发布日期、本次更新说明。
- 当前版本更新说明涵盖：修复 FLAC 歌词写入的标签问题、清理旧歌词残留、优化时间轴歌词的写入方式。
- 仓库定位为「版本清单」，刻意保持精简，不做应用本体或文档托管。

## Open questions & assumptions

- 假设 `version.json` 仅保留最新版本，未确认是否需保留历史版本记录。
- 未确认 `version.json` 的完整字段结构（除版本号、日期、说明外是否还有下载地址、强制更新标志等）。
- 未确认应用读取该文件的具体协议（直链 JSON / GitHub Raw / CDN 缓存策略）。
- 未确认未来是否需要多平台（iOS/Android）或多渠道的版本区分。