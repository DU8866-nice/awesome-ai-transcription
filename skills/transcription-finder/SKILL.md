---
name: transcription-finder
description: Recommends open-source speech-to-text tools from the Awesome AI Transcription list for live captions, real-time interpreting, AI meeting notes, dictation and transcribing recordings, matched to the user's system, language, budget and privacy needs. Use when someone asks which tool to use for subtitles, captions, meeting minutes, voice typing or transcription.
---

# Transcription Finder

Help the user pick a few tools from the Awesome AI Transcription list.

## Data

- The catalog is in `references/catalog.md`. Each entry lists the repo URL, stars, last push date, supported systems (`os`), flags (`offline` runs fully local, `byok` needs the user's own API key, `cn` Chinese-friendly: Chinese UI or docs, or built for Chinese use) and a short description in Chinese and English.
- If you can read the web, the latest version is at https://github.com/DU8866-nice/awesome-ai-transcription (`data/tools.yaml` and `data/stats.json`). Prefer it when it is newer than the bundled catalog.
- Only recommend entries that are in the catalog. Do not invent projects, star counts or features.

## Steps

1. Find out, from the conversation or with at most two short questions:
   - the task: live captions or translation, meeting notes, dictation, transcribing files or subtitles, watching foreign videos;
   - the system: Windows, macOS (Apple Silicon or Intel), Linux, Android or iPhone;
   - the language, especially whether Chinese matters;
   - whether audio must stay on the device, and whether they are willing to pay for a cloud API.
2. Pick two or three entries that fit, preferring recently updated ones, `offline` entries when privacy matters and `cn` entries for Chinese users. Say why each fits in one sentence.
3. Mention any caveat shown in the catalog, such as required OS versions, paid official builds or English-only support.
4. Remind them briefly to tell people before recording a meeting or class, since many places require consent.
5. Do not recommend tools for secret recording or for cheating in interviews or exams. The list does not include them.

## Output

Reply in the user's language. Keep it short: the picks with links and one-line reasons, then the consent reminder in one line.
