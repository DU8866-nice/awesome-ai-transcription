# Catalog

Generated from data/tools.yaml. Fields: repo | stars | last push | os | flags (offline = runs fully local, byok = needs own API key, cn = Chinese-friendly: Chinese UI or docs, or built for Chinese use) | description (zh / en)

## 实时字幕与同声传译 / Live captions and interpreting

- https://github.com/SakiRinn/LiveCaptions-Translator | stars=4075 | pushed=2026-08-17 | os=win | flags=-
  - Windows 自带“实时字幕”加翻译接口：系统识别准、占用低，再接上大模型翻译，不需要 Copilot+ PC。
  - Windows Live Captions plus a translation API: accurate, lightweight system captions with LLM translation, no Copilot+ PC required.
  - caveat: Requires Windows 11
- https://github.com/wquguru/cicada | stars=2301 | pushed=2026-11-14 | os=mac,win,linux,android | flags=cn
  - 知了：任何会议和直播的实时双语字幕、同声传译和结构化纪要，支持腾讯会议、飞书、钉钉、Zoom、B 站直播等；按住说话键，对方能直接听到你的译文语音。
  - Cicada: live bilingual captions, interpreting and structured notes for any meeting or stream, from Tencent Meeting and Feishu to Zoom and YouTube; hold a key and the other side hears your words translated.
  - caveat: Fully on-device on Apple Silicon Macs; see the README for other platforms
- https://github.com/abb128/LiveCaptions | stars=1812 | pushed=2025-02-27 | os=linux | flags=offline
  - Linux 桌面的实时字幕，桌面声音和麦克风都能识别，音频不发往任何地方。
  - Live captions for the Linux desktop from desktop or mic audio, which is never sent anywhere.
  - caveat: English only for now
- https://github.com/TheDeathDragon/LiveTranslate | stars=914 | pushed=2026-08-17 | os=win | flags=byok
  - Windows 实时音频翻译：抓取系统声音和麦克风，本地识别后交给大模型翻译，透明浮窗显示。
  - Real-time audio translation for Windows: captures system audio and the mic, recognizes speech locally and translates through an LLM API in a transparent overlay.
- https://github.com/yuxino/Mimi | stars=888 | pushed=2026-11-15 | os=mac,win,linux,android | flags=byok
  - 给正在播放的视频、直播和网课加实时翻译字幕，可以只听指定应用的声音，字幕可导出为笔记；默认不保存录音。
  - Adds live translated captions to whatever video, stream or class is playing; it can listen to a single app and export captions as notes, and saves nothing by default.
  - caveat: Apple Silicon Macs on macOS 26+ can use on-device Apple speech; otherwise you need your own provider key
- https://github.com/HiMeditator/auto-caption | stars=610 | pushed=2026-10-14 | os=win,mac,linux | flags=offline,cn
  - 跨平台实时字幕显示软件，可用 Vosk、SenseVoice 等本地模型，也能接 Ollama 或在线接口做翻译。
  - A cross-platform live caption overlay that runs local models such as Vosk and SenseVoice, with optional translation through Ollama or online APIs.
- https://github.com/franklioxygen/v2s | stars=513 | pushed=2026-10-11 | os=mac | flags=offline
  - macOS 菜单栏双语字幕条：可只抓某个应用的声音，用苹果系统自带的本地识别和翻译，还能生成摘要。
  - A macOS menu-bar bilingual caption bar that can capture a single app, using Apple's on-device speech and translation, with summaries.
- https://github.com/oboroge0/hayamimi | stars=464 | pushed=2026-09-17 | os=- | flags=offline
  - 只用 CPU 的多语言实时转写：实时字幕、网页面板、说话人标注和即时翻译，不需要显卡和云端接口。
  - Multilingual real-time transcription on CPU only: live subtitles, a browser dashboard, speaker labels and translation, with no GPU or cloud API.
- https://github.com/niyongsheng/AudioScript | stars=376 | pushed=2026-11-12 | os=mac,win,linux | flags=offline,cn
  - 声稿：监听系统声音，把外语播客、视频和会议实时转成“原文 + 译文”双语悬浮字幕，识别和翻译都在本机完成，作者称是讯飞同传的免费平替。
  - AudioScript turns system audio from podcasts, videos and meetings into floating bilingual captions, with recognition and translation done on your machine.
- https://github.com/KorenKrita/simul-subtitle | stars=119 | pushed=2026-10-21 | os=android,mac,win | flags=byok
  - 日语、英语视频和直播的同传悬浮字幕，浮在任何播放器上方；语音识别在本地离线完成，翻译用你自己的大模型接口。
  - Floating live-interpreting captions for Japanese and English videos and streams over any player; recognition runs offline on the device and translation uses your own LLM key.

## AI 会议纪要 / AI meeting notes

- https://github.com/Zackriya-Solutions/meetily | stars=32721 | pushed=2026-11-14 | os=win,mac,linux | flags=offline
  - 注重隐私的 AI 会议助手：在本机用 Whisper 或 Parakeet 转写，纪要可用本地 Ollama，也可接 Claude、Groq 等。
  - A privacy-first meeting assistant that transcribes on your machine with Whisper or Parakeet and summarizes with local Ollama or providers like Claude and Groq.
  - caveat: One-line install on Linux; the Windows installer needs an AVX2 CPU
- https://github.com/fastrepl/anarlog | stars=9898 | pushed=2026-11-15 | os=mac,win,linux | flags=-
  - 本地优先的开源会议记事本，Granola 的开源替代，社区版保持 MIT 开源。
  - A local-first open-source meeting notepad and Granola alternative; the community app stays MIT-licensed.
- https://github.com/FrigadeHQ/yogurt | stars=1635 | pushed=2026-11-15 | os=mac,win,linux | flags=-
  - Granola 的免费开源替代：不往会议里加机器人，实时转写、自动写纪要，笔记留在你的电脑上。
  - A free, open-source Granola alternative that records calls without a bot, transcribes live and writes summaries, with notes kept on your computer.
- https://github.com/Muesli-HQ/muesli | stars=1628 | pushed=2026-11-15 | os=mac | flags=offline
  - macOS 原生的听写和会议转写应用，默认本机识别，不加会议机器人，可把纪要交给 ChatGPT 或 Codex 继续处理。
  - A native macOS app for dictation and meeting transcription, on-device by default with no meeting bot, and a plugin for ChatGPT and Codex.
- https://github.com/silverstein/minutes | stars=1605 | pushed=2026-11-13 | os=mac,linux | flags=-
  - 本机录音转写会议、通话和语音备忘，存成你自己的 Markdown 文件，再让 Claude Code、Codex 等通过 MCP 检索。
  - Records and transcribes meetings, calls and voice memos on your device into Markdown you own, searchable from Claude Code, Codex or any MCP client.
- https://github.com/moona3k/macparakeet | stars=788 | pushed=2026-11-09 | os=mac | flags=offline
  - Apple 芯片 Mac 上的本地语音应用：全局听写、音视频文件转写和会议录音三合一。
  - A local-first voice app for Apple Silicon Macs that combines dictation, file transcription and meeting recording.
- https://github.com/infiniV/VoiceFlow | stars=437 | pushed=2026-06-21 | os=win,linux | flags=offline
  - Windows 和 Linux 的本地 Whisper 听写，新版加入会议模式：同时录麦克风和系统声音，本地转写后用你自己的大模型写纪要。
  - Local Whisper dictation for Windows and Linux, now with a meeting mode that records mic and system audio and summarizes with your own LLM.
- https://github.com/nexmoe/DayBee | stars=430 | pushed=2026-10-25 | os=mac | flags=offline
  - 托盘常驻的长时间录音应用，自动分段存档，可用苹果系统识别或 SenseVoice、Qwen3-ASR 等本地模型实时转写。
  - A tray recorder for long sessions that splits and archives audio and transcribes live with Apple speech or local models such as SenseVoice and Qwen3-ASR.
- https://github.com/impossibleG/phorminx | stars=126 | pushed=2026-10-29 | os=win | flags=-
  - Windows 上的本地听写、会议和研究笔记工具，可搜索文字稿，不用付费 AI 服务也能做格式整理。
  - Local-first dictation, meetings and research notes for Windows, with searchable transcripts and AI formatting without a paid AI service.
- https://github.com/tancheng33/tingo | stars=45 | pushed=2026-11-13 | os=win,mac,linux | flags=offline,cn
  - 听过：为中文会议做的本地纪要工具，录腾讯会议、飞书、Zoom 和麦克风，本地用 FunASR 转写并区分说话人，纪要里每条结论都能点回原话。
  - Tingo, a local meeting-notes tool built for Chinese: records Tencent Meeting, Feishu, Zoom and your mic, transcribes and labels speakers locally with FunASR, and links every conclusion back to the recording.
  - caveat: Summaries can use DeepSeek or Qwen APIs, or local Ollama fully offline

## 语音输入：说话代替打字 / Dictation: speak instead of typing

- https://github.com/cjpais/Handy | stars=38882 | pushed=2026-11-15 | os=win,mac,linux | flags=offline
  - 免费开源、完全离线的语音输入：按快捷键说话，文字出现在任何输入框，不往云端发送任何信息。
  - Free, open-source and fully offline: press a shortcut, speak, and your words appear in any text field without anything sent to the cloud.
- https://github.com/OpenWhispr/openwhispr | stars=11628 | pushed=2026-11-15 | os=mac,win,linux | flags=offline
  - Wispr Flow 和 Granola 的开源替代：语音输入、会议转写和笔记，可用本地 Parakeet、Whisper，也可接自己的云端接口。
  - An open-source alternative to Wispr Flow and Granola for dictation, meeting transcription and notes, with local Parakeet or Whisper or your own cloud keys.
- https://github.com/Beingpax/VoiceInk | stars=7133 | pushed=2026-11-11 | os=mac | flags=-
  - macOS 上几乎即时的语音转文字应用，注重隐私和效率。
  - A macOS voice-to-text app that transcribes almost instantly, built for privacy and speed.
  - caveat: Open source to build yourself; the official builds are paid with a free trial
- https://github.com/HaujetZhao/CapsWriter-Offline | stars=7118 | pushed=2026-09-14 | os=win | flags=offline,cn
  - 按住 CapsLock 说话、松开上屏的 Windows 离线语音输入，中文数字自动转换、热词和正则替换，还能把音视频文件转成字幕。
  - Hold Caps Lock to talk, release to type: offline voice input for Windows with Chinese number formatting, hotwords and rules, plus file-to-subtitle transcription.
- https://github.com/Starmel/OpenSuperWhisper | stars=3152 | pushed=2026-11-10 | os=mac | flags=offline
  - macOS 实时录音转写，可选 Whisper 或 Parakeet 引擎，支持自定义快捷键。
  - Real-time recording and transcription on macOS with Whisper or Parakeet and custom shortcuts.
- https://github.com/HD838A/remote-mic-app | stars=2930 | pushed=2026-11-15 | os=mac | flags=cn
  - 无线麦 SayAll：把小米蓝牙遥控器 2 / 2 Pro 变成 Mac 的语音输入设备，拿着遥控器就能说话打字、控制 Mac。
  - SayAll turns a Xiaomi Bluetooth remote into a voice input device for your Mac, so you can dictate and control the Mac from the remote.
- https://github.com/yan5xu/ququ | stars=2289 | pushed=2025-10-08 | os=- | flags=cn
  - 蛐蛐：为中文用户做的 Wispr Flow 开源替代，本地用 FunASR 识别，再用可配置的大模型整理文字。
  - QuQu, a Wispr Flow alternative for Chinese users that recognizes speech locally with FunASR and tidies text with a configurable LLM.
- https://github.com/TypeWhisper/typewhisper-mac | stars=1927 | pushed=2026-11-15 | os=mac | flags=-
  - macOS 语音转文字加 AI 文本处理：本机模型或 Groq、OpenAI 等云端接口，结果可套用可复用的工作流。
  - Speech-to-text and AI text processing for macOS with on-device models or cloud APIs like Groq and OpenAI, plus reusable workflows.
- https://github.com/peteonrails/voxtype | stars=1786 | pushed=2026-11-14 | os=linux | flags=offline
  - Wayland 下按住热键说话的听写工具，普通 CPU 上也能跑出 9–11 倍实时速度，默认本地运行。
  - Push-to-talk dictation for Wayland that runs 9–11× realtime on a plain CPU and stays local by default.
- https://github.com/amicalhq/amical | stars=1619 | pushed=2026-11-12 | os=mac,win | flags=-
  - 本地优先的 AI 听写应用，用开源模型识别，可接 Ollama 润色。
  - A local-first AI dictation app powered by open models, with optional Ollama cleanup.
- https://github.com/joewongjc/type4me | stars=1557 | pushed=2026-11-10 | os=mac,ios | flags=cn
  - 免费开源的 macOS 语音输入法，边说边出字，还能一键润色、翻译或向 AI 提问；识别引擎和大模型由你选，历史存在本机。
  - A free macOS voice input method that types as you speak and can polish, translate or ask AI in one step; you choose the engines, and history stays local.
  - caveat: The recommended cloud build needs your own speech and LLM keys
- https://github.com/goodroot/hyprwhspr | stars=1280 | pushed=2026-11-15 | os=linux | flags=-
  - Linux 原生全局听写，支持 Parakeet、Whisper、Qwen3-ASR 等多种引擎，主流发行版都能装。
  - Native system-wide dictation for Linux with Parakeet, Whisper, Qwen3-ASR and more, packaged for major distros.
- https://github.com/voquill/voquill | stars=1029 | pushed=2026-11-15 | os=win,mac,linux | flags=-
  - 跨平台 AI 语音打字：在任何桌面应用里听写，AI 清理文字稿，个人词库同步。
  - Cross-platform AI voice typing that dictates into any desktop app, cleans up the transcript and keeps a personal glossary in sync.
- https://github.com/VocaHQ/vocalinux | stars=1019 | pushed=2026-11-15 | os=linux | flags=offline
  - Linux 上 100% 离线的语音听写，在任何地方说话打字，基于 whisper.cpp 等引擎。
  - 100% offline voice dictation for Linux that types anywhere, built on whisper.cpp and other engines.
- https://github.com/tover0314-w/opentypeless | stars=684 | pushed=2026-11-15 | os=mac,win,linux | flags=-
  - Wispr Flow、Superwhisper 的开源替代：语音输入、改写和语音问答，支持自带 API Key 或本地 Ollama。
  - An open-source alternative to Wispr Flow and Superwhisper for voice input, rewriting and voice Q&A, with your own keys or local Ollama.
- https://github.com/opennookorg/betterwispr | stars=539 | pushed=2026-11-14 | os=mac | flags=offline
  - macOS 免费开源听写：按住 ⌥ 空格说话，本机用 Whisper、Parakeet 或苹果语音识别，选了云端接口才会上传。
  - Free macOS dictation: hold ⌥ Space and speak; Whisper, Parakeet or Apple speech run on your Mac, and audio leaves only if you pick a cloud option.
- https://github.com/crosswk/SayIt | stars=490 | pushed=2026-11-09 | os=win,mac | flags=cn
  - 随口说、出色写：按快捷键说话，AI 把口语整理成书面文字，直接输入到光标位置。
  - Press a shortcut and speak; AI turns casual speech into written text right at your cursor.
- https://github.com/AbhishekBarali/SpeakoFlow | stars=402 | pushed=2026-10-31 | os=win,mac,linux | flags=offline
  - 免费开源的语音输入和 AI 助手，默认本地运行，说话打字、提问回答，还能整理会议纪要。
  - Free, open-source voice typing and an AI assistant that runs locally by default, answers questions and can write up meeting notes.

## 录音、音视频转文字和字幕生成 / Transcribe recordings and make subtitles

- https://github.com/chidiwilliams/buzz | stars=22823 | pushed=2026-11-15 | os=win,mac,linux | flags=offline
  - 在自己电脑上离线转写和翻译音频，基于 OpenAI Whisper，有图形界面，最老牌的选择之一。
  - Transcribes and translates audio offline on your own computer with OpenAI Whisper, behind a simple GUI; one of the best-known options.
  - caveat: 1.4.5 is the last version for Intel Macs
- https://github.com/thewh1teagle/vibe | stars=8112 | pushed=2026-11-14 | os=win,mac,linux | flags=offline
  - 在本机转写音频和视频，界面简洁，支持多种导出格式。
  - Transcribes audio and video right on your device with a simple interface and several export formats.
- https://github.com/modelscope/FunClip | stars=6562 | pushed=2026-11-01 | os=- | flags=offline,cn
  - 阿里通义实验室的开源视频剪辑工具：用 FunASR 识别出文字稿，选中文字就能剪出对应片段并生成字幕，本地运行。
  - An open-source clipping tool from Alibaba's Tongyi lab: FunASR transcribes the video, you select text to cut the matching clips and subtitles, all locally.
- https://github.com/buxuku/SmartSub | stars=6045 | pushed=2026-11-09 | os=win,mac,linux | flags=offline,cn
  - 妙幕：视频转字幕、字幕翻译、AI 配音和字幕烧录的一站式桌面工具，用 Whisper、FunASR 等本地模型离线识别，可批量处理。
  - SmartSub, an all-in-one desktop tool for video-to-subtitles, subtitle translation, AI dubbing and burn-in, with offline Whisper or FunASR and batch processing.
- https://github.com/harry0703/AudioNotes | stars=2564 | pushed=2026-08-19 | os=- | flags=offline,cn
  - 本地把会议、访谈、课程和语音备忘转成文字，整理成 Markdown 笔记，还能针对内容提问；用 FunASR 和 Ollama，默认不发给第三方。
  - Turns meetings, interviews, lectures and voice memos into transcripts and Markdown notes you can ask questions about, locally with FunASR and Ollama.
- https://github.com/aTrainTranscription/aTrain | stars=1243 | pushed=2026-11-15 | os=win,mac,linux | flags=offline
  - 格拉茨大学研究者开发的离线转写工具，适合访谈和研究录音，自动区分说话人，不上传任何数据。
  - An offline transcription tool from University of Graz researchers for interviews and research recordings, with speaker labels and no uploads.
- https://github.com/Blue-B/WhisperSubTranslate | stars=845 | pushed=2026-10-10 | os=- | flags=offline
  - 把视频变成多语言字幕：本地用 whisper.cpp 生成字幕，再用下载的离线翻译模型或在线引擎翻译。
  - Turns any video into multilingual subtitles locally: whisper.cpp makes the SRT, then a downloaded offline model or an online engine translates it.
- https://github.com/corvo007/MioSub | stars=842 | pushed=2026-10-20 | os=- | flags=cn
  - 能读懂上下文的 AI 字幕编辑器：贴链接后自动完成下载、转录、翻译和压制，省去逐句校对机翻。
  - A context-aware AI subtitle editor that downloads, transcribes, translates and burns in subtitles from a link, so you don't proofread machine translation line by line.

## 看外语视频、玩外语游戏 / Watch foreign videos and play foreign games

- https://github.com/ramjke/Translumo | stars=5929 | pushed=2026-09-22 | os=- | flags=-
  - 实时屏幕翻译，适合游戏、视频里的硬字幕和其他画面文字。
  - Real-time screen translation for games, hardcoded video subtitles and other on-screen text.
- https://github.com/umlx5h/LLPlayer | stars=4725 | pushed=2026-11-05 | os=win | flags=-
  - 为学语言设计的播放器：双语字幕、AI 生成字幕、实时翻译和查词。
  - A media player for language learning with dual subtitles, AI-generated subtitles, real-time translation and word lookup.
- https://github.com/ciddwd/overlay-translator | stars=1320 | pushed=2026-10-30 | os=android | flags=-
  - 免 root 的安卓屏幕实时翻译，适合游戏、视觉小说和漫画，支持端侧和云端识别、离线大模型，译文直接盖在画面上。
  - No-root real-time screen translation for Android games, visual novels and comics, with on-device or cloud OCR and offline LLMs, drawn right over the screen.

## 手机和智能眼镜 / Phones and smart glasses

- https://github.com/Mentra-Community/MentraOS | stars=2425 | pushed=2026-11-14 | os=- | flags=-
  - 开源智能眼镜系统，眼镜上能看实时字幕、和 AI 对话；需要它支持的眼镜型号。
  - An open-source smart-glasses OS with live captions and AI chat on the glasses; needs a supported pair.
- https://github.com/Cyletix/CyIME | stars=1312 | pushed=2026-11-14 | os=android | flags=cn
  - 基于 Rime 的安卓中文输入法，支持离线语音输入和字幕模式，还有九键、双拼、五笔和手写。
  - A Rime-based Chinese keyboard for Android with offline voice input and a caption mode, plus T9, double pinyin, Wubi and handwriting.
- https://github.com/Nomily-Ai/nomily-app | stars=1012 | pushed=2026-11-13 | os=ios,android | flags=byok
  - 录音伴侣：从 Apple Watch、iPhone 或录音设备导入音频，用你自己的服务商转写、区分说话人和写摘要，也支持本地识别端点。
  - A recording companion that imports audio from Apple Watch, iPhone or a recorder and transcribes, labels speakers and summarizes with your own providers or a local endpoint.
- https://github.com/BryceWG/BiBi-Keyboard | stars=875 | pushed=2026-11-14 | os=android | flags=cn
  - 说点啥：安卓上的 AI 语音输入法键盘，结合语音识别和大模型，让语音输入更自然。
  - BiBi Keyboard, an Android voice keyboard that combines speech recognition and an LLM for more natural voice input.
- https://github.com/Notely-Voice/NotelyVoice | stars=824 | pushed=2026-11-12 | os=android,ios | flags=offline
  - 完全私密的 AI 语音转写和笔记应用，手机上用 Whisper 离线识别 100 多种语言，适合记课堂、会议和问诊。
  - A fully private voice transcription and notes app that runs Whisper offline on your phone in 100+ languages, for lectures, meetings and more.

## 模型与引擎（开发者） / Models and engines (for developers)

- https://github.com/openai/whisper | stars=112797 | pushed=2026-08-31 | os=- | flags=-
  - OpenAI 的通用语音识别模型，大多数工具都基于它或它的衍生版本。
  - OpenAI's general speech recognition model, the base of most tools here.
- https://github.com/ggml-org/whisper.cpp | stars=55217 | pushed=2026-11-13 | os=- | flags=-
  - Whisper 的 C/C++ 实现，CPU 和各种设备上都能高效运行。
  - A C/C++ port of Whisper that runs efficiently on CPUs and many devices.
- https://github.com/SYSTRAN/faster-whisper | stars=26775 | pushed=2026-11-12 | os=- | flags=-
  - 基于 CTranslate2 的 Whisper 加速实现。
  - A faster Whisper implementation built on CTranslate2.
- https://github.com/m-bain/whisperX | stars=25340 | pushed=2026-11-12 | os=- | flags=-
  - Whisper 加词级时间戳和说话人分离。
  - Whisper with word-level timestamps and speaker diarization.
- https://github.com/modelscope/FunASR | stars=21033 | pushed=2026-11-15 | os=- | flags=cn
  - 阿里达摩院的语音识别工具包，含流式识别、断句、标点和说话人分离，中文效果好。
  - Alibaba DAMO's speech recognition toolkit with streaming ASR, VAD, punctuation and diarization, strong on Chinese.
- https://github.com/k2-fsa/sherpa-onnx | stars=15970 | pushed=2026-11-13 | os=- | flags=-
  - 离线语音识别、合成、说话人分离等，支持手机、嵌入式和各种语言绑定。
  - Offline speech-to-text, text-to-speech, diarization and more, for phones, embedded boards and many languages.
- https://github.com/QuentinFuxa/WhisperLiveKit | stars=11253 | pushed=2026-11-14 | os=- | flags=-
  - 本地实时语音转文字服务：流式识别、说话人分离和翻译，可搭成自己的实时字幕后端。
  - A local real-time speech-to-text server with streaming ASR, diarization and translation, a backend for your own live captions.
- https://github.com/pyannote/pyannote-audio | stars=10802 | pushed=2026-11-09 | os=- | flags=-
  - 说话人分离的主流开源工具包。
  - The leading open-source toolkit for speaker diarization.
- https://github.com/QwenAudio/SenseVoice | stars=9760 | pushed=2026-09-30 | os=- | flags=cn
  - SenseVoice Small 模型：普通话、粤语、英语、日语、韩语识别，附语种和情绪识别。
  - The SenseVoice Small model for Mandarin, Cantonese, English, Japanese and Korean, with language and emotion detection.
- https://github.com/MahmoudAshraf97/whisper-diarization | stars=5676 | pushed=2026-08-15 | os=- | flags=-
  - 基于 Whisper 的转写加说话人分离脚本。
  - Whisper transcription with speaker diarization.
- https://github.com/collabora/WhisperLive | stars=4359 | pushed=2026-11-15 | os=- | flags=-
  - 接近实时的 Whisper 服务端实现。
  - A nearly-live Whisper server implementation.
- https://github.com/QwenLM/Qwen3-ASR | stars=3901 | pushed=2026-06-26 | os=- | flags=cn
  - 通义千问团队的开源语音识别模型系列。
  - Open-source speech recognition models from the Qwen team.
- https://github.com/FluidInference/FluidAudio | stars=3300 | pushed=2026-11-14 | os=- | flags=-
  - 苹果设备上的 CoreML 语音模型：识别、合成和语音检测，适合做 Mac / iOS 应用。
  - CoreML audio models for Apple devices, covering speech-to-text, TTS and voice activity detection, for Mac and iOS apps.
- https://github.com/OpenMOSS/MOSS-Transcribe-Diarize | stars=2273 | pushed=2026-10-21 | os=- | flags=-
  - 0.9B 的长音频转写模型，支持 50 多种语言，带说话人分离和时间戳。
  - A 0.9B model for long-form transcription in 50+ languages with speaker diarization and timestamps.
- https://github.com/QwenAudio/Fun-ASR | stars=1610 | pushed=2026-11-09 | os=- | flags=cn
  - Fun-ASR 语音识别模型，原生支持 Hugging Face Transformers。
  - Fun-ASR speech recognition models with native Hugging Face Transformers support.
