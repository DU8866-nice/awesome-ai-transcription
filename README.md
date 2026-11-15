<!-- 本文件由 scripts/build_readme.py 生成，请勿直接修改。要改内容请编辑 data/tools.yaml 后重新生成。 -->

# Awesome AI Transcription · AI 语音转文字工具大全

[![Stars](https://img.shields.io/github/stars/DU8866-nice/awesome-ai-transcription?style=flat-square)](https://github.com/DU8866-nice/awesome-ai-transcription) [![Last commit](https://img.shields.io/github/last-commit/DU8866-nice/awesome-ai-transcription?style=flat-square)](https://github.com/DU8866-nice/awesome-ai-transcription/commits) [![License: CC0-1.0](https://img.shields.io/badge/license-CC0--1.0-lightgrey?style=flat-square)](LICENSE) [![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square)](CONTRIBUTING.md)

**简体中文** | [English](README.en.md)

> 实时字幕、同声传译、AI 会议纪要、语音输入和音视频转文字的开源工具精选。每个工具标明支持的系统、能否完全本地运行、要不要自备 API Key、是否中文友好，星标每周自动刷新。

上网课、开会、看外语直播、写东西，都离不开把声音变成文字。过去几个月，开源的语音转文字工具更新得很快：有的给任何正在播放的声音加实时双语字幕，有的不往会议里塞机器人就能写纪要，有的按住快捷键说话就能代替打字，很多还能完全在自己电脑上运行，录音不上传。

这份清单按用途整理这些工具，标明每个工具支持什么系统、能不能完全本地运行、要不要自备 API Key，以及是否中文友好。

收录 69 个项目 · 数据更新于 2026-11-16

## 目录

- [按用途找工具](#pick)
- [用之前先知道](#rules)
- [实时字幕与同声传译](#cat-live)（10）
- [AI 会议纪要](#cat-meetings)（10）
- [语音输入：说话代替打字](#cat-dictation)（18）
- [录音、音视频转文字和字幕生成](#cat-files)（8）
- [看外语视频、玩外语游戏](#cat-watch)（3）
- [手机和智能眼镜](#cat-mobile)（5）
- [模型与引擎（开发者）](#cat-engines)（15）
- [常见问题](#faq)
- [让 AI 助手帮你挑](#finder)
- [相关合集](#related)
- [参与贡献](#contributing)

<a id="pick"></a>
## 按用途找工具

| 你想做什么 | Windows | Mac | 手机 |
|---|---|---|---|
| 网课、直播、外语视频加实时双语字幕 | [LiveCaptions-Translator](https://github.com/SakiRinn/LiveCaptions-Translator)、[知了](https://github.com/wquguru/cicada)、[声稿](https://github.com/niyongsheng/AudioScript) | [知了](https://github.com/wquguru/cicada)、[声稿](https://github.com/niyongsheng/AudioScript)、[v2s](https://github.com/franklioxygen/v2s) | [同传字幕](https://github.com/KorenKrita/simul-subtitle)、[Mimi](https://github.com/yuxino/Mimi)（Android） |
| 开会自动出纪要 | [Meetily](https://github.com/Zackriya-Solutions/meetily)、[听过](https://github.com/tancheng33/tingo)（中文会议） | [Meetily](https://github.com/Zackriya-Solutions/meetily)、[Muesli](https://github.com/Muesli-HQ/muesli)、[Yogurt](https://github.com/FrigadeHQ/yogurt) | [Nomily](https://github.com/Nomily-Ai/nomily-app)（导入录音） |
| 说话代替打字 | [CapsWriter-Offline](https://github.com/HaujetZhao/CapsWriter-Offline)（中文）、[Handy](https://github.com/cjpais/Handy) | [Handy](https://github.com/cjpais/Handy)、[Type4Me](https://github.com/joewongjc/type4me)（中文）、[VoiceInk](https://github.com/Beingpax/VoiceInk) | [说点啥](https://github.com/BryceWG/BiBi-Keyboard)（Android） |
| 录音、视频转文字或出字幕 | [Buzz](https://github.com/chidiwilliams/buzz)、[妙幕](https://github.com/buxuku/SmartSub) | [Buzz](https://github.com/chidiwilliams/buzz)、[Vibe](https://github.com/thewh1teagle/vibe)、[妙幕](https://github.com/buxuku/SmartSub) | [Notely Voice](https://github.com/Notely-Voice/NotelyVoice) |
| 访谈、研究录音，要区分说话人 | [aTrain](https://github.com/aTrainTranscription/aTrain) | [aTrain](https://github.com/aTrainTranscription/aTrain) | — |

<a id="rules"></a>
## 用之前先知道

> [!IMPORTANT]
> - **本地还是云端。** 标 🔒 的可以完全在你的设备上运行，录音不上传；标 🔑 的需要你自己的 API Key，音频或文字会发给你选的服务商，可能产生费用。
> - **录音先打招呼。** 很多国家和地区要求录音前征得参与者同意，公司和学校也可能有自己的规定。开会、上课录音转写之前，先告诉大家。
> - **电脑配置。** 本地模型可能比较吃内存和显卡。一些 Mac 应用的本地模式只支持 Apple 芯片（如 MacParakeet，知了在 Apple 芯片上才全程本机识别，Buzz 新版也不再支持 Intel Mac）；Meetily 的 Windows 安装包需要支持 AVX2 的 CPU；没有独立显卡可以试只用 CPU 的 hayamimi 或较小的模型。
> - **中文场景。** 优先看标了 🀄 的工具，其中不少用阿里的 FunASR、SenseVoice 或 Qwen3-ASR 模型。Tingo 的作者提到，FunASR 处理中文标点、数字和人名比通用的英文方案好。

本清单不收录标榜“隐身”的面试、考试作弊助手，也不收录以偷录、侵犯隐私为卖点的工具。

**图例**：🔒 可完全本地运行（录音不上传）· 🔑 需要自备 API Key · 🀄 中文友好（有中文界面或文档，或专为中文场景做）· 🆕 近 60 天新建 · 💤 超过一年未更新 · 📦 已归档

> [!NOTE]
> 标记和支持的系统依据各项目 README 的说明，只在 README 写明时才标，没标不代表不支持。收录指核对过仓库说明，不等于逐个实测过识别效果。

<a id="cat-live"></a>
## 实时字幕与同声传译

直接听电脑或手机正在播放的声音，给网课、会议、直播和外语视频加上实时字幕或双语翻译，不用往会议里加机器人。

- **[LiveCaptions-Translator](https://github.com/SakiRinn/LiveCaptions-Translator)** · ★ 4.1k<br>Windows 自带“实时字幕”加翻译接口：系统识别准、占用低，再接上大模型翻译，不需要 Copilot+ PC。<br><sub>Windows · 更新于 2026-08 · Apache-2.0</sub><br><sub>💡 需要 Windows 11</sub>
- **[cicada](https://github.com/wquguru/cicada)** · ★ 2.3k · 🀄 🆕<br>知了：任何会议和直播的实时双语字幕、同声传译和结构化纪要，支持腾讯会议、飞书、钉钉、Zoom、B 站直播等；按住说话键，对方能直接听到你的译文语音。<br><sub>macOS / Windows / Linux / Android · 更新于 2026-11 · Apache-2.0</sub><br><sub>💡 Apple 芯片的 Mac 上全部本机识别，其他平台看 README 说明</sub>
- **[LiveCaptions](https://github.com/abb128/LiveCaptions)** · ★ 1.8k · 🔒 💤<br>Linux 桌面的实时字幕，桌面声音和麦克风都能识别，音频不发往任何地方。<br><sub>Linux · 更新于 2025-02 · GPL-3.0</sub><br><sub>💡 目前只支持英语</sub>
- **[LiveTranslate](https://github.com/TheDeathDragon/LiveTranslate)** · ★ 914 · 🔑<br>Windows 实时音频翻译：抓取系统声音和麦克风，本地识别后交给大模型翻译，透明浮窗显示。<br><sub>Windows · 更新于 2026-08 · MIT</sub>
- **[Mimi](https://github.com/yuxino/Mimi)** · ★ 888 · 🔑<br>给正在播放的视频、直播和网课加实时翻译字幕，可以只听指定应用的声音，字幕可导出为笔记；默认不保存录音。<br><sub>macOS / Windows / Linux / Android · 更新于 2026-11 · MIT</sub><br><sub>💡 Apple 芯片 Mac（macOS 26 以上）可用苹果本地识别，其他情况需要自备服务商 API Key</sub>
- **[auto-caption](https://github.com/HiMeditator/auto-caption)** · ★ 610 · 🔒 🀄<br>跨平台实时字幕显示软件，可用 Vosk、SenseVoice 等本地模型，也能接 Ollama 或在线接口做翻译。<br><sub>Windows / macOS / Linux · 更新于 2026-10 · MIT</sub>
- **[v2s](https://github.com/franklioxygen/v2s)** · ★ 513 · 🔒<br>macOS 菜单栏双语字幕条：可只抓某个应用的声音，用苹果系统自带的本地识别和翻译，还能生成摘要。<br><sub>macOS · 更新于 2026-10</sub>
- **[hayamimi](https://github.com/oboroge0/hayamimi)** · ★ 464 · 🔒<br>只用 CPU 的多语言实时转写：实时字幕、网页面板、说话人标注和即时翻译，不需要显卡和云端接口。<br><sub>更新于 2026-09</sub>
- **[AudioScript](https://github.com/niyongsheng/AudioScript)** · ★ 376 · 🔒 🀄 🆕<br>声稿：监听系统声音，把外语播客、视频和会议实时转成“原文 + 译文”双语悬浮字幕，识别和翻译都在本机完成，作者称是讯飞同传的免费平替。<br><sub>macOS / Windows / Linux · 更新于 2026-11 · MIT</sub>
- **[simul-subtitle](https://github.com/KorenKrita/simul-subtitle)** · ★ 119 · 🔑 🆕<br>日语、英语视频和直播的同传悬浮字幕，浮在任何播放器上方；语音识别在本地离线完成，翻译用你自己的大模型接口。<br><sub>Android / macOS / Windows · 更新于 2026-10 · MIT</sub>

<a id="cat-meetings"></a>
## AI 会议纪要

Granola、Otter、飞书妙记的开源替代：录下会议声音，转成文字、分清说话人，再整理成纪要和待办。

- **[meetily](https://github.com/Zackriya-Solutions/meetily)** · ★ 32.7k · 🔒<br>注重隐私的 AI 会议助手：在本机用 Whisper 或 Parakeet 转写，纪要可用本地 Ollama，也可接 Claude、Groq 等。<br><sub>Windows / macOS / Linux · 更新于 2026-11 · MIT</sub><br><sub>💡 Linux 用一行命令安装；Windows 安装包需要支持 AVX2 的 CPU</sub>
- **[anarlog](https://github.com/fastrepl/anarlog)** · ★ 9.9k<br>本地优先的开源会议记事本，Granola 的开源替代，社区版保持 MIT 开源。<br><sub>macOS / Windows / Linux · 更新于 2026-11 · MIT</sub>
- **[yogurt](https://github.com/FrigadeHQ/yogurt)** · ★ 1.6k · 🆕<br>Granola 的免费开源替代：不往会议里加机器人，实时转写、自动写纪要，笔记留在你的电脑上。<br><sub>macOS / Windows / Linux · 更新于 2026-11 · MIT</sub>
- **[muesli](https://github.com/Muesli-HQ/muesli)** · ★ 1.6k · 🔒<br>macOS 原生的听写和会议转写应用，默认本机识别，不加会议机器人，可把纪要交给 ChatGPT 或 Codex 继续处理。<br><sub>macOS · 更新于 2026-11 · MIT</sub>
- **[minutes](https://github.com/silverstein/minutes)** · ★ 1.6k<br>本机录音转写会议、通话和语音备忘，存成你自己的 Markdown 文件，再让 Claude Code、Codex 等通过 MCP 检索。<br><sub>macOS / Linux · 更新于 2026-11 · MIT</sub>
- **[macparakeet](https://github.com/moona3k/macparakeet)** · ★ 788 · 🔒<br>Apple 芯片 Mac 上的本地语音应用：全局听写、音视频文件转写和会议录音三合一。<br><sub>macOS · 更新于 2026-11</sub>
- **[VoiceFlow](https://github.com/infiniV/VoiceFlow)** · ★ 437 · 🔒<br>Windows 和 Linux 的本地 Whisper 听写，新版加入会议模式：同时录麦克风和系统声音，本地转写后用你自己的大模型写纪要。<br><sub>Windows / Linux · 更新于 2026-06 · MIT</sub>
- **[DayBee](https://github.com/nexmoe/DayBee)** · ★ 430 · 🔒<br>托盘常驻的长时间录音应用，自动分段存档，可用苹果系统识别或 SenseVoice、Qwen3-ASR 等本地模型实时转写。<br><sub>macOS · 更新于 2026-10</sub>
- **[phorminx](https://github.com/impossibleG/phorminx)** · ★ 126<br>Windows 上的本地听写、会议和研究笔记工具，可搜索文字稿，不用付费 AI 服务也能做格式整理。<br><sub>Windows · 更新于 2026-10 · MIT</sub>
- **[tingo](https://github.com/tancheng33/tingo)** · ★ 45 · 🔒 🀄 🆕<br>听过：为中文会议做的本地纪要工具，录腾讯会议、飞书、Zoom 和麦克风，本地用 FunASR 转写并区分说话人，纪要里每条结论都能点回原话。<br><sub>Windows / macOS / Linux · 更新于 2026-11 · MIT</sub><br><sub>💡 纪要可用 DeepSeek、通义千问等接口，也可用本地 Ollama 全程断网</sub>

<a id="cat-dictation"></a>
## 语音输入：说话代替打字

按住快捷键说话，松开文字就出现在光标处，很多还能用大模型顺手润色。Wispr Flow、Superwhisper 的开源替代。

- **[Handy](https://github.com/cjpais/Handy)** · ★ 38.9k · 🔒<br>免费开源、完全离线的语音输入：按快捷键说话，文字出现在任何输入框，不往云端发送任何信息。<br><sub>Windows / macOS / Linux · 更新于 2026-11 · MIT</sub>
- **[openwhispr](https://github.com/OpenWhispr/openwhispr)** · ★ 11.6k · 🔒<br>Wispr Flow 和 Granola 的开源替代：语音输入、会议转写和笔记，可用本地 Parakeet、Whisper，也可接自己的云端接口。<br><sub>macOS / Windows / Linux · 更新于 2026-11 · MIT</sub>
- **[VoiceInk](https://github.com/Beingpax/VoiceInk)** · ★ 7.1k<br>macOS 上几乎即时的语音转文字应用，注重隐私和效率。<br><sub>macOS · 更新于 2026-11</sub><br><sub>💡 源码开源可自行编译；官网编译版收费，提供免费试用</sub>
- **[CapsWriter-Offline](https://github.com/HaujetZhao/CapsWriter-Offline)** · ★ 7.1k · 🔒 🀄<br>按住 CapsLock 说话、松开上屏的 Windows 离线语音输入，中文数字自动转换、热词和正则替换，还能把音视频文件转成字幕。<br><sub>Windows · 更新于 2026-09 · MIT</sub>
- **[OpenSuperWhisper](https://github.com/Starmel/OpenSuperWhisper)** · ★ 3.2k · 🔒<br>macOS 实时录音转写，可选 Whisper 或 Parakeet 引擎，支持自定义快捷键。<br><sub>macOS · 更新于 2026-11 · MIT</sub>
- **[remote-mic-app](https://github.com/HD838A/remote-mic-app)** · ★ 2.9k · 🀄<br>无线麦 SayAll：把小米蓝牙遥控器 2 / 2 Pro 变成 Mac 的语音输入设备，拿着遥控器就能说话打字、控制 Mac。<br><sub>macOS · 更新于 2026-11 · GPL-3.0</sub>
- **[ququ](https://github.com/yan5xu/ququ)** · ★ 2.3k · 🀄 💤<br>蛐蛐：为中文用户做的 Wispr Flow 开源替代，本地用 FunASR 识别，再用可配置的大模型整理文字。<br><sub>更新于 2025-10</sub>
- **[typewhisper-mac](https://github.com/TypeWhisper/typewhisper-mac)** · ★ 1.9k<br>macOS 语音转文字加 AI 文本处理：本机模型或 Groq、OpenAI 等云端接口，结果可套用可复用的工作流。<br><sub>macOS · 更新于 2026-11 · GPL-3.0</sub>
- **[voxtype](https://github.com/peteonrails/voxtype)** · ★ 1.8k · 🔒<br>Wayland 下按住热键说话的听写工具，普通 CPU 上也能跑出 9–11 倍实时速度，默认本地运行。<br><sub>Linux · 更新于 2026-11 · MIT</sub>
- **[amical](https://github.com/amicalhq/amical)** · ★ 1.6k<br>本地优先的 AI 听写应用，用开源模型识别，可接 Ollama 润色。<br><sub>macOS / Windows · 更新于 2026-11 · MIT</sub>
- **[type4me](https://github.com/joewongjc/type4me)** · ★ 1.6k · 🀄<br>免费开源的 macOS 语音输入法，边说边出字，还能一键润色、翻译或向 AI 提问；识别引擎和大模型由你选，历史存在本机。<br><sub>macOS / iOS · 更新于 2026-11 · MIT</sub><br><sub>💡 推荐的云端版需要自备语音识别和大模型 API Key</sub>
- **[hyprwhspr](https://github.com/goodroot/hyprwhspr)** · ★ 1.3k<br>Linux 原生全局听写，支持 Parakeet、Whisper、Qwen3-ASR 等多种引擎，主流发行版都能装。<br><sub>Linux · 更新于 2026-11 · MIT</sub>
- **[voquill](https://github.com/voquill/voquill)** · ★ 1.0k<br>跨平台 AI 语音打字：在任何桌面应用里听写，AI 清理文字稿，个人词库同步。<br><sub>Windows / macOS / Linux · 更新于 2026-11</sub>
- **[vocalinux](https://github.com/VocaHQ/vocalinux)** · ★ 1.0k · 🔒<br>Linux 上 100% 离线的语音听写，在任何地方说话打字，基于 whisper.cpp 等引擎。<br><sub>Linux · 更新于 2026-11 · AGPL-3.0</sub>
- **[opentypeless](https://github.com/tover0314-w/opentypeless)** · ★ 684<br>Wispr Flow、Superwhisper 的开源替代：语音输入、改写和语音问答，支持自带 API Key 或本地 Ollama。<br><sub>macOS / Windows / Linux · 更新于 2026-11 · MIT</sub>
- **[betterwispr](https://github.com/opennookorg/betterwispr)** · ★ 539 · 🔒 🆕<br>macOS 免费开源听写：按住 ⌥ 空格说话，本机用 Whisper、Parakeet 或苹果语音识别，选了云端接口才会上传。<br><sub>macOS · 更新于 2026-11 · Apache-2.0</sub>
- **[SayIt](https://github.com/crosswk/SayIt)** · ★ 490 · 🀄<br>随口说、出色写：按快捷键说话，AI 把口语整理成书面文字，直接输入到光标位置。<br><sub>Windows / macOS · 更新于 2026-11 · AGPL-3.0</sub>
- **[SpeakoFlow](https://github.com/AbhishekBarali/SpeakoFlow)** · ★ 402 · 🔒<br>免费开源的语音输入和 AI 助手，默认本地运行，说话打字、提问回答，还能整理会议纪要。<br><sub>Windows / macOS / Linux · 更新于 2026-10 · MIT</sub>

<a id="cat-files"></a>
## 录音、音视频转文字和字幕生成

把课程录音、采访、播客和视频文件转成文字稿或字幕，很多还能翻译字幕、整理笔记。

- **[buzz](https://github.com/chidiwilliams/buzz)** · ★ 22.8k · 🔒<br>在自己电脑上离线转写和翻译音频，基于 OpenAI Whisper，有图形界面，最老牌的选择之一。<br><sub>Windows / macOS / Linux · 更新于 2026-11 · MIT</sub><br><sub>💡 Intel Mac 最后支持的版本是 1.4.5</sub>
- **[vibe](https://github.com/thewh1teagle/vibe)** · ★ 8.1k · 🔒<br>在本机转写音频和视频，界面简洁，支持多种导出格式。<br><sub>Windows / macOS / Linux · 更新于 2026-11 · MIT</sub>
- **[FunClip](https://github.com/modelscope/FunClip)** · ★ 6.6k · 🔒 🀄<br>阿里通义实验室的开源视频剪辑工具：用 FunASR 识别出文字稿，选中文字就能剪出对应片段并生成字幕，本地运行。<br><sub>更新于 2026-11 · MIT</sub>
- **[SmartSub](https://github.com/buxuku/SmartSub)** · ★ 6.0k · 🔒 🀄<br>妙幕：视频转字幕、字幕翻译、AI 配音和字幕烧录的一站式桌面工具，用 Whisper、FunASR 等本地模型离线识别，可批量处理。<br><sub>Windows / macOS / Linux · 更新于 2026-11 · MIT</sub>
- **[AudioNotes](https://github.com/harry0703/AudioNotes)** · ★ 2.6k · 🔒 🀄<br>本地把会议、访谈、课程和语音备忘转成文字，整理成 Markdown 笔记，还能针对内容提问；用 FunASR 和 Ollama，默认不发给第三方。<br><sub>更新于 2026-08 · MIT</sub>
- **[aTrain](https://github.com/aTrainTranscription/aTrain)** · ★ 1.2k · 🔒<br>格拉茨大学研究者开发的离线转写工具，适合访谈和研究录音，自动区分说话人，不上传任何数据。<br><sub>Windows / macOS / Linux · 更新于 2026-11 · AGPL-3.0</sub>
- **[WhisperSubTranslate](https://github.com/Blue-B/WhisperSubTranslate)** · ★ 845 · 🔒<br>把视频变成多语言字幕：本地用 whisper.cpp 生成字幕，再用下载的离线翻译模型或在线引擎翻译。<br><sub>更新于 2026-10</sub>
- **[MioSub](https://github.com/corvo007/MioSub)** · ★ 842 · 🀄<br>能读懂上下文的 AI 字幕编辑器：贴链接后自动完成下载、转录、翻译和压制，省去逐句校对机翻。<br><sub>更新于 2026-10 · AGPL-3.0</sub>

<a id="cat-watch"></a>
## 看外语视频、玩外语游戏

- **[Translumo](https://github.com/ramjke/Translumo)** · ★ 5.9k<br>实时屏幕翻译，适合游戏、视频里的硬字幕和其他画面文字。<br><sub>更新于 2026-09 · Apache-2.0</sub>
- **[LLPlayer](https://github.com/umlx5h/LLPlayer)** · ★ 4.7k<br>为学语言设计的播放器：双语字幕、AI 生成字幕、实时翻译和查词。<br><sub>Windows · 更新于 2026-11 · GPL-3.0</sub>
- **[overlay-translator](https://github.com/ciddwd/overlay-translator)** · ★ 1.3k<br>免 root 的安卓屏幕实时翻译，适合游戏、视觉小说和漫画，支持端侧和云端识别、离线大模型，译文直接盖在画面上。<br><sub>Android · 更新于 2026-10 · Apache-2.0</sub>

<a id="cat-mobile"></a>
## 手机和智能眼镜

- **[MentraOS](https://github.com/Mentra-Community/MentraOS)** · ★ 2.4k<br>开源智能眼镜系统，眼镜上能看实时字幕、和 AI 对话；需要它支持的眼镜型号。<br><sub>更新于 2026-11 · Apache-2.0</sub>
- **[CyIME](https://github.com/Cyletix/CyIME)** · ★ 1.3k · 🀄 🆕<br>基于 Rime 的安卓中文输入法，支持离线语音输入和字幕模式，还有九键、双拼、五笔和手写。<br><sub>Android · 更新于 2026-11 · GPL-3.0</sub>
- **[nomily-app](https://github.com/Nomily-Ai/nomily-app)** · ★ 1.0k · 🔑<br>录音伴侣：从 Apple Watch、iPhone 或录音设备导入音频，用你自己的服务商转写、区分说话人和写摘要，也支持本地识别端点。<br><sub>iOS / Android · 更新于 2026-11</sub>
- **[BiBi-Keyboard](https://github.com/BryceWG/BiBi-Keyboard)** · ★ 875 · 🀄<br>说点啥：安卓上的 AI 语音输入法键盘，结合语音识别和大模型，让语音输入更自然。<br><sub>Android · 更新于 2026-11 · Apache-2.0</sub>
- **[NotelyVoice](https://github.com/Notely-Voice/NotelyVoice)** · ★ 824 · 🔒<br>完全私密的 AI 语音转写和笔记应用，手机上用 Whisper 离线识别 100 多种语言，适合记课堂、会议和问诊。<br><sub>Android / iOS · 更新于 2026-11 · GPL-3.0</sub>

<a id="cat-engines"></a>
## 模型与引擎（开发者）

上面这些应用背后的识别模型和库，适合想自己搭服务或二次开发的人。

- **[whisper](https://github.com/openai/whisper)** · ★ 112.8k<br>OpenAI 的通用语音识别模型，大多数工具都基于它或它的衍生版本。<br><sub>更新于 2026-08 · MIT</sub>
- **[whisper.cpp](https://github.com/ggml-org/whisper.cpp)** · ★ 55.2k<br>Whisper 的 C/C++ 实现，CPU 和各种设备上都能高效运行。<br><sub>更新于 2026-11 · MIT</sub>
- **[faster-whisper](https://github.com/SYSTRAN/faster-whisper)** · ★ 26.8k<br>基于 CTranslate2 的 Whisper 加速实现。<br><sub>更新于 2026-11 · MIT</sub>
- **[whisperX](https://github.com/m-bain/whisperX)** · ★ 25.3k<br>Whisper 加词级时间戳和说话人分离。<br><sub>更新于 2026-11 · BSD-2-Clause</sub>
- **[FunASR](https://github.com/modelscope/FunASR)** · ★ 21.0k · 🀄<br>阿里达摩院的语音识别工具包，含流式识别、断句、标点和说话人分离，中文效果好。<br><sub>更新于 2026-11 · MIT</sub>
- **[sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx)** · ★ 16.0k<br>离线语音识别、合成、说话人分离等，支持手机、嵌入式和各种语言绑定。<br><sub>更新于 2026-11 · Apache-2.0</sub>
- **[WhisperLiveKit](https://github.com/QuentinFuxa/WhisperLiveKit)** · ★ 11.3k<br>本地实时语音转文字服务：流式识别、说话人分离和翻译，可搭成自己的实时字幕后端。<br><sub>更新于 2026-11 · Apache-2.0</sub>
- **[pyannote-audio](https://github.com/pyannote/pyannote-audio)** · ★ 10.8k<br>说话人分离的主流开源工具包。<br><sub>更新于 2026-11 · MIT</sub>
- **[SenseVoice](https://github.com/QwenAudio/SenseVoice)** · ★ 9.8k · 🀄<br>SenseVoice Small 模型：普通话、粤语、英语、日语、韩语识别，附语种和情绪识别。<br><sub>更新于 2026-09 · MIT</sub>
- **[whisper-diarization](https://github.com/MahmoudAshraf97/whisper-diarization)** · ★ 5.7k<br>基于 Whisper 的转写加说话人分离脚本。<br><sub>更新于 2026-08 · BSD-2-Clause</sub>
- **[WhisperLive](https://github.com/collabora/WhisperLive)** · ★ 4.4k<br>接近实时的 Whisper 服务端实现。<br><sub>更新于 2026-11 · MIT</sub>
- **[Qwen3-ASR](https://github.com/QwenLM/Qwen3-ASR)** · ★ 3.9k · 🀄<br>通义千问团队的开源语音识别模型系列。<br><sub>更新于 2026-06 · Apache-2.0</sub>
- **[FluidAudio](https://github.com/FluidInference/FluidAudio)** · ★ 3.3k<br>苹果设备上的 CoreML 语音模型：识别、合成和语音检测，适合做 Mac / iOS 应用。<br><sub>更新于 2026-11 · Apache-2.0</sub>
- **[MOSS-Transcribe-Diarize](https://github.com/OpenMOSS/MOSS-Transcribe-Diarize)** · ★ 2.3k<br>0.9B 的长音频转写模型，支持 50 多种语言，带说话人分离和时间戳。<br><sub>更新于 2026-10 · Apache-2.0</sub>
- **[Fun-ASR](https://github.com/QwenAudio/Fun-ASR)** · ★ 1.6k · 🀄<br>Fun-ASR 语音识别模型，原生支持 Hugging Face Transformers。<br><sub>更新于 2026-11 · Apache-2.0</sub>

<a id="faq"></a>
## 常见问题

**哪个识别最准？**
取决于语言、口音和录音质量，这份清单没有做统一测评。中文可以先试 FunASR、SenseVoice 系的工具，英文场景最常见的是基于 Whisper 和 Parakeet 的工具。

**能识别腾讯会议、Zoom 里对方的声音吗？**
大部分实时字幕和会议纪要工具直接录电脑的系统声音，不用往会议里加机器人，对方说话也能识别，知了、Yogurt、Tingo 的 README 都写明了这一点。手机系统一般不允许录其他应用的通话声音，知了建议开外放用“面对面”模式。

**要花钱吗？**
这里都是开源项目，本地运行不花钱；用云端接口要按服务商的价格付费。VoiceInk 的官网编译版收费，源码可以自己编译。

**星标数多久更新一次？**
每周一由 GitHub Actions 自动刷新并重新排序，链接每周检查一次。

<a id="finder"></a>
## 让 AI 助手帮你挑

这份清单也是一个 skill。把仓库里的 [`skills/transcription-finder`](skills/transcription-finder) 文件夹装进你的 AI 助手（或运行 `npx skills add DU8866-nice/awesome-ai-transcription`），然后问它：

> 我在澳洲读研，用 Windows 笔记本，想给英文网课加中文实时字幕，最好不花钱，用哪个？

它会按你的系统、用途、预算和隐私要求，从清单里挑两三个并说明理由，同时提醒录音要先征得同意。

<a id="related"></a>
## 相关合集

| 项目 | 说明 | ⭐ | 最近更新 |
|---|---|---:|---|
| [awesome-diarization](https://github.com/wq2012/awesome-diarization) | 说话人分离的论文、库和数据集合集。 | 1.9k | 2026-10 |

<a id="contributing"></a>
## 参与贡献

欢迎推荐项目或纠错：[提交 Issue](https://github.com/DU8866-nice/awesome-ai-transcription/issues/new/choose)，或者修改 [`data/tools.yaml`](data/tools.yaml) 后提 PR，详见[贡献指南](CONTRIBUTING.md)。README 由脚本生成，请不要直接改它。

## Star 趋势

[![Star History Chart](https://api.star-history.com/svg?repos=DU8866-nice/awesome-ai-transcription&type=Date)](https://star-history.com/#DU8866-nice/awesome-ai-transcription&Date)
