# Worksop Driver Safety Pilot

Static page for GitHub Pages. English, French, Romanian, Polish and Russian.

## Source of truth
The English rules and the Goods-In driver instructions follow the gatehouse sheets, which are accepted by management and H&S. Do not change English wording without the same approval.

## Files
- `index.html`: the whole app, one file. All text for all languages is inside it.
- `404.html`: page shown for wrong addresses. The repository already has a `.nojekyll` file, so nothing else is needed.
- `audio/`, `audio-scripts.csv`, `AUDIO_GUIDE.md`: optional recorded voice. See the guide.
- `voice-test.html`: testing page that lists the voices on a phone. Delete it before the QR goes live.
- `translation-review.csv`: sheet for the independent translation reviewers. Not needed for hosting, so remove it from the public repository after review if you prefer.
- `TRANSLATION_REVIEW.md`, `PRELAUNCH_CHECKLIST.md`: working notes. Same advice applies.

## Language release control
Near the top of the script in `index.html` is this line:

    const REVIEWED={en:true,fr:false,ro:false,pl:false,ru:false};

Drivers can only choose a language set to `true`. Change a language to `true` only after a reviewer has signed it off in the review sheet.

Reviewers open the live address with `?review=1` on the end to test the unreviewed drafts. Those pages show a red DRAFT banner.

## Publish
1. Create the repository under a company-owned GitHub account or organisation, if your IT team agrees. On the Free plan the repository must be public, and the published page is public on the internet either way.
2. Upload every file from this folder to the repository root.
3. In Settings > Pages, choose Deploy from a branch, select `main` and `/ (root)`, then save.
4. Open the exact address GitHub gives you on a phone. Test before making any QR code.
5. Keep a downloaded copy of each release.

## Controls
- Do not upload the source PDFs.
- Do not add analytics, credentials, internal links or employee contact details.
- Change the version label on the welcome page (`Pilot 1.9` in `index.html`) with every release so you can tell which version a printed QR points to.

## Voice playback
- Plays a recorded MP3 for a page when one exists in `audio/<language>/` (see `AUDIO_GUIDE.md`).
- Otherwise uses the voices already installed on the driver's phone. The page picks the most natural-sounding voice the phone has for the language (it prefers voices named Natural, Neural, Enhanced, Premium or Google, and avoids basic ones), reads one sentence at a time, and pauses between sentences and rules.
- Availability of phone voices varies by phone and language. Test every language on real Android and iPhone devices.
- Printed and colleague-assisted fallbacks stay in place.
- If a phone has no voice for the chosen language and no recording exists, the page says so in that language and tells the driver to ask Goods-In.
