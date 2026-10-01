# Audio guide

## How it works
- When a driver taps **Read this page**, the page plays a recorded file if one exists for that language and page.
- If no file exists, or the file fails to load, the page uses the voice already on the driver's phone.
- Both read the same text, so you can launch with phone voices and add recordings language by language.
- You do not edit any code. Add the MP3 files to the repository and the page finds them.

## Why a recording sounds more human
Phone voices are built into each phone. The page already picks the best one available and reads in short sentences with pauses, but some phones only have basic voices, especially for Romanian and Polish. A recording by a native speaker is the only way to guarantee a human sound on every phone.

## Files
Put files in these folders, with these exact names:

| Page | File name |
|---|---|
| Welcome | s2.mp3 |
| Rules 1 to 10 | s3.mp3 |
| Rules 11 to 19 | s4.mp3 |
| Goods-In instructions | s5.mp3 |
| Acknowledgement | s6.mp3 |
| Done | s7.mp3 |

Folders: `audio/en`, `audio/fr`, `audio/ro`, `audio/pl`, `audio/ru`. That is 6 files per language.

`audio-scripts.csv` has the exact text for every file. Read it word for word.

## Before you record
- Record a language only after its translation is signed off. If the text changes later, that file must be recorded again.
- Do not record from the draft translations.

## Who records
Best for safety wording: a native speaker, ideally someone who knows the site and the terms. A text-to-speech service can also work, but check its licence allows workplace use, and have a native speaker listen to every file. I cannot generate native-quality audio for these languages myself.

## Recording settings
- MP3, mono, about 64 kbps, 22 or 44 kHz.
- Slow, clear pace. A short pause between rules. No music.
- Aim for under 1.5 MB per file so it loads on mobile data.

## Testing
1. Open the live page and choose the language.
2. Tap **Read this page** on each of the 6 pages. The recorded voice should play, not the phone voice.
3. Tap **Stop**. It must stop at once.
4. Change language mid-play. Nothing should keep playing.
5. Check on Android and iPhone, on mobile data and Wi-Fi.
6. Rename one file and confirm the page falls back to the phone voice for that page.

## Caching
Browsers can keep an old MP3 for a short time after you replace it. After replacing a file, test on a phone you have not used before, or clear the browser cache.
