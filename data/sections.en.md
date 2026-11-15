<!-- section:intro -->
Online classes, meetings, foreign-language streams and writing all depend on turning speech into text. Open-source speech-to-text tools have moved fast in the past few months: some add live bilingual captions to anything that's playing, some write meeting notes without putting a bot in the call, some let you hold a key and speak instead of typing, and many run entirely on your own computer so recordings never leave it.

This list sorts these tools by task and shows, for each one, the systems it supports, whether it runs fully local, whether it needs your own API key and whether it is Chinese-friendly.

<!-- section:pick -->
## Find a tool by task

| What you want | Windows | Mac | Phone |
|---|---|---|---|
| Live bilingual captions for classes, streams and foreign videos | [LiveCaptions-Translator](https://github.com/SakiRinn/LiveCaptions-Translator), [Cicada](https://github.com/wquguru/cicada), [AudioScript](https://github.com/niyongsheng/AudioScript) | [Cicada](https://github.com/wquguru/cicada), [AudioScript](https://github.com/niyongsheng/AudioScript), [v2s](https://github.com/franklioxygen/v2s) | [Simul Subtitle](https://github.com/KorenKrita/simul-subtitle), [Mimi](https://github.com/yuxino/Mimi) (Android) |
| Automatic meeting notes | [Meetily](https://github.com/Zackriya-Solutions/meetily), [Tingo](https://github.com/tancheng33/tingo) (Chinese meetings) | [Meetily](https://github.com/Zackriya-Solutions/meetily), [Muesli](https://github.com/Muesli-HQ/muesli), [Yogurt](https://github.com/FrigadeHQ/yogurt) | [Nomily](https://github.com/Nomily-Ai/nomily-app) (imports recordings) |
| Speak instead of typing | [CapsWriter-Offline](https://github.com/HaujetZhao/CapsWriter-Offline) (Chinese), [Handy](https://github.com/cjpais/Handy) | [Handy](https://github.com/cjpais/Handy), [Type4Me](https://github.com/joewongjc/type4me) (Chinese), [VoiceInk](https://github.com/Beingpax/VoiceInk) | [BiBi Keyboard](https://github.com/BryceWG/BiBi-Keyboard) (Android) |
| Transcribe recordings or make subtitles | [Buzz](https://github.com/chidiwilliams/buzz), [SmartSub](https://github.com/buxuku/SmartSub) | [Buzz](https://github.com/chidiwilliams/buzz), [Vibe](https://github.com/thewh1teagle/vibe), [SmartSub](https://github.com/buxuku/SmartSub) | [Notely Voice](https://github.com/Notely-Voice/NotelyVoice) |
| Interviews and research recordings with speaker labels | [aTrain](https://github.com/aTrainTranscription/aTrain) | [aTrain](https://github.com/aTrainTranscription/aTrain) | — |

<!-- section:rules -->
## Good to know

> [!IMPORTANT]
> - **Local or cloud.** Tools marked 🔒 can run entirely on your device, so recordings are not uploaded. Tools marked 🔑 need your own API key, send audio or text to the provider you choose, and may cost money.
> - **Ask before you record.** Many countries and regions require consent from everyone being recorded, and companies and schools may have their own rules. Tell people before you record and transcribe a meeting or class.
> - **Hardware.** Local models can be heavy on memory and GPU. Some Mac apps only run locally on Apple Silicon (MacParakeet, for example; Cicada is fully on-device only there, and newer Buzz releases dropped Intel Macs); Meetily's Windows installer needs an AVX2 CPU; without a dedicated GPU, try the CPU-only hayamimi or a smaller model.
> - **Chinese.** Start with tools marked 🀄; many use Alibaba's FunASR, SenseVoice or Qwen3-ASR models. The Tingo author notes FunASR handles Chinese punctuation, numbers and names better than general English-first models.

This list does not include "stealth" interview or exam cheating assistants, or tools pitched at secret recording or invading privacy.

<!-- section:faq -->
## FAQ

**Which one is most accurate?**
It depends on the language, accent and recording quality, and this list has not run a common benchmark. For Chinese, start with FunASR or SenseVoice-based tools; for English, tools built on Whisper and Parakeet are the most common.

**Can it hear the other people on Zoom or Teams?**
Most live caption and meeting-note tools record the computer's system audio, so they hear everyone without adding a bot to the call; the Cicada, Yogurt and Tingo READMEs all say so. Phones generally don't allow recording other apps' call audio, and Cicada suggests using speaker mode with its face-to-face mode.

**Does it cost anything?**
Everything here is open source and free to run locally; cloud APIs are billed by the provider. VoiceInk's official builds are paid, but you can build it from source.

**How often are stars updated?**
Every Monday GitHub Actions refreshes the stars and re-sorts the list, and links are checked weekly.

<!-- section:finder -->
## Let your AI agent pick

This list is also a skill. Install the [`skills/transcription-finder`](skills/transcription-finder) folder in your AI agent (or run `npx skills add DU8866-nice/awesome-ai-transcription`) and ask:

> I'm on a Windows laptop and want free live English captions for my online lectures. Which tool should I use?

It picks two or three entries for your system, task, budget and privacy needs, explains why, and reminds you to get consent before recording.

<!-- section:contributing -->
## Contributing

Suggestions and corrections are welcome: [open an issue](https://github.com/DU8866-nice/awesome-ai-transcription/issues/new/choose), or edit [`data/tools.yaml`](data/tools.yaml) and send a PR. See the [contributing guide](CONTRIBUTING.md). The README is generated by a script, so please don't edit it directly.
