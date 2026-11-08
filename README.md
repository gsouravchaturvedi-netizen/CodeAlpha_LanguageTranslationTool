# Language Translation Tool (FastLight)

CodeAlpha internship project. Type or speak text, choose the source and target languages, and get the translation instantly.
Everything runs in the browser from a single file, `index.html`. No installation, no server, no sign-in.

## Features

- 110 languages plus auto-detect, swap button, instant translation while typing
- Voice input (microphone) and text-to-speech with voice and speed options
- Copy, paste, share, saved phrases, translation history and CSV export
- Dark mode, four color themes, high contrast, text sizes
- Animated backgrounds and your own wallpapers
- Works on phones and laptops

## Task requirements

| Requirement | Where it is done |
|---|---|
| User interface to enter text and choose source and target languages | Two text boxes with source and target language menus, auto-detect and a swap button |
| Use a translation API | The free [MyMemory](https://mymemory.translated.net) translation API |
| Send the text and get the translated response | `translateChunk()` in `index.html` sends the text with `fetch` and reads the JSON reply |
| Display the translated text clearly | Result box on the right, updated as you type, with a loading indicator and clear error messages |
| Optional: copy button | **Copy** button under the result |
| Optional: text-to-speech | **Listen** button (browser speech synthesis), plus voice and speed options |

## Run it

Open `index.html` in Chrome or Edge. That is all.

## Put it online with GitHub Pages (free)

1. In this repository open **Settings > Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**, select the `main` branch and the `/ (root)` folder, then **Save**.
3. After a minute your site is live at `https://YOUR-USERNAME.github.io/CodeAlpha_LanguageTranslationTool/`.

## Good to know

- Translations come from MyMemory, which allows about 5,000 characters per day without a key. If the limit is reached, try again tomorrow.
- The text you type is sent to MyMemory to be translated. History and saved phrases stay only in your browser.
- Voice input needs Chrome or Edge and a microphone. Spoken output needs a voice for that language on your device (Microsoft Edge has the most).
- The **Report** button opens an email to the address set as `REPORT_EMAIL` near the end of `index.html`. Change it to your own address.

## Tech

HTML, CSS and JavaScript only: Fetch API, Web Speech API (recognition and synthesis), IndexedDB (your own wallpapers) and localStorage (settings, history).
