<!-- section:intro -->
上网课、开会、看外语直播、写东西，都离不开把声音变成文字。过去几个月，开源的语音转文字工具更新得很快：有的给任何正在播放的声音加实时双语字幕，有的不往会议里塞机器人就能写纪要，有的按住快捷键说话就能代替打字，很多还能完全在自己电脑上运行，录音不上传。

这份清单按用途整理这些工具，标明每个工具支持什么系统、能不能完全本地运行、要不要自备 API Key，以及是否中文友好。

<!-- section:pick -->
## 按用途找工具

| 你想做什么 | Windows | Mac | 手机 |
|---|---|---|---|
| 网课、直播、外语视频加实时双语字幕 | [LiveCaptions-Translator](https://github.com/SakiRinn/LiveCaptions-Translator)、[知了](https://github.com/wquguru/cicada)、[声稿](https://github.com/niyongsheng/AudioScript) | [知了](https://github.com/wquguru/cicada)、[声稿](https://github.com/niyongsheng/AudioScript)、[v2s](https://github.com/franklioxygen/v2s) | [同传字幕](https://github.com/KorenKrita/simul-subtitle)、[Mimi](https://github.com/yuxino/Mimi)（Android） |
| 开会自动出纪要 | [Meetily](https://github.com/Zackriya-Solutions/meetily)、[听过](https://github.com/tancheng33/tingo)（中文会议） | [Meetily](https://github.com/Zackriya-Solutions/meetily)、[Muesli](https://github.com/Muesli-HQ/muesli)、[Yogurt](https://github.com/FrigadeHQ/yogurt) | [Nomily](https://github.com/Nomily-Ai/nomily-app)（导入录音） |
| 说话代替打字 | [CapsWriter-Offline](https://github.com/HaujetZhao/CapsWriter-Offline)（中文）、[Handy](https://github.com/cjpais/Handy) | [Handy](https://github.com/cjpais/Handy)、[Type4Me](https://github.com/joewongjc/type4me)（中文）、[VoiceInk](https://github.com/Beingpax/VoiceInk) | [说点啥](https://github.com/BryceWG/BiBi-Keyboard)（Android） |
| 录音、视频转文字或出字幕 | [Buzz](https://github.com/chidiwilliams/buzz)、[妙幕](https://github.com/buxuku/SmartSub) | [Buzz](https://github.com/chidiwilliams/buzz)、[Vibe](https://github.com/thewh1teagle/vibe)、[妙幕](https://github.com/buxuku/SmartSub) | [Notely Voice](https://github.com/Notely-Voice/NotelyVoice) |
| 访谈、研究录音，要区分说话人 | [aTrain](https://github.com/aTrainTranscription/aTrain) | [aTrain](https://github.com/aTrainTranscription/aTrain) | — |

<!-- section:rules -->
## 用之前先知道

> [!IMPORTANT]
> - **本地还是云端。** 标 🔒 的可以完全在你的设备上运行，录音不上传；标 🔑 的需要你自己的 API Key，音频或文字会发给你选的服务商，可能产生费用。
> - **录音先打招呼。** 很多国家和地区要求录音前征得参与者同意，公司和学校也可能有自己的规定。开会、上课录音转写之前，先告诉大家。
> - **电脑配置。** 本地模型可能比较吃内存和显卡。一些 Mac 应用的本地模式只支持 Apple 芯片（如 MacParakeet，知了在 Apple 芯片上才全程本机识别，Buzz 新版也不再支持 Intel Mac）；Meetily 的 Windows 安装包需要支持 AVX2 的 CPU；没有独立显卡可以试只用 CPU 的 hayamimi 或较小的模型。
> - **中文场景。** 优先看标了 🀄 的工具，其中不少用阿里的 FunASR、SenseVoice 或 Qwen3-ASR 模型。Tingo 的作者提到，FunASR 处理中文标点、数字和人名比通用的英文方案好。

本清单不收录标榜“隐身”的面试、考试作弊助手，也不收录以偷录、侵犯隐私为卖点的工具。

<!-- section:faq -->
## 常见问题

**哪个识别最准？**
取决于语言、口音和录音质量，这份清单没有做统一测评。中文可以先试 FunASR、SenseVoice 系的工具，英文场景最常见的是基于 Whisper 和 Parakeet 的工具。

**能识别腾讯会议、Zoom 里对方的声音吗？**
大部分实时字幕和会议纪要工具直接录电脑的系统声音，不用往会议里加机器人，对方说话也能识别，知了、Yogurt、Tingo 的 README 都写明了这一点。手机系统一般不允许录其他应用的通话声音，知了建议开外放用“面对面”模式。

**要花钱吗？**
这里都是开源项目，本地运行不花钱；用云端接口要按服务商的价格付费。VoiceInk 的官网编译版收费，源码可以自己编译。

**星标数多久更新一次？**
每周一由 GitHub Actions 自动刷新并重新排序，链接每周检查一次。

<!-- section:finder -->
## 让 AI 助手帮你挑

这份清单也是一个 skill。把仓库里的 [`skills/transcription-finder`](skills/transcription-finder) 文件夹装进你的 AI 助手（或运行 `npx skills add DU8866-nice/awesome-ai-transcription`），然后问它：

> 我在澳洲读研，用 Windows 笔记本，想给英文网课加中文实时字幕，最好不花钱，用哪个？

它会按你的系统、用途、预算和隐私要求，从清单里挑两三个并说明理由，同时提醒录音要先征得同意。

<!-- section:contributing -->
## 参与贡献

欢迎推荐项目或纠错：[提交 Issue](https://github.com/DU8866-nice/awesome-ai-transcription/issues/new/choose)，或者修改 [`data/tools.yaml`](data/tools.yaml) 后提 PR，详见[贡献指南](CONTRIBUTING.md)。README 由脚本生成，请不要直接改它。
