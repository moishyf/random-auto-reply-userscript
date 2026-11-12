# Random Auto Reply · תגובה אקראית לצ'אט

A tiny, playful Tampermonkey userscript for experimenting with quick, random replies in Google Chat and the Gmail Chat interface.

**Version in the source:** `0.4` · **Status:** experimental browser utility.

## How it works

When you type exactly **`---`** in a supported editable chat input and press **Enter**, the script replaces it with one of the built-in short replies, then dispatches a synthetic Enter event.

**Important:** Synthetic keyboard events are not guaranteed to trigger message sending in every version of Google Chat or Gmail. Check the draft before sending anything important. This is not an AI responder and does not call an AI API.

## Installation

1. Install [Tampermonkey](https://www.tampermonkey.net/) in your browser.
2. Open [the userscript file](./ChatGPT-Enhancer.user.js), click **Raw**, and follow Tampermonkey's prompt (or paste it manually into a new userscript).
3. Visit `https://chat.google.com/` or the chat interface in `https://mail.google.com/`.
4. In a chat input, type `---` and press **Enter** to test.

> The source filename is historical: despite `ChatGPT-Enhancer.user.js`, this script generates **random built-in replies**, not ChatGPT output.

## שימוש בעברית

הקלידו שלושה מקפים (`---`) בשדה ההודעה ולחצו Enter. הסקריפט מחליף אותם במשפט אקראי מתוך הרשימה בקוד. אם ההודעה אינה נשלחת אוטומטית, יש לשלוח אותה ידנית. מומלץ להשתמש בו לשיחות קלילות בלבד.

## Technical details & limitations

- Single-file script: `ChatGPT-Enhancer.user.js`.
- `@match`: Gmail and Google Chat; `@grant none`.
- Uses in-page editable elements and generated keyboard events; behavior depends on the host site's DOM and event handling.
- No third-party API key or backend is required.
- GitHub Actions checks syntax on pushes/PRs; this **does not prove compatibility** with the live chat interfaces.

## Reporting an issue

Include the browser, userscript manager and steps to reproduce, but **never publish private conversations or screenshots containing personal information**. No license is granted by this README.
