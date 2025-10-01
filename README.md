# Leads tracker

A minimal Chrome extension popup that lets you save the current tab URL or any text input into localStorage and view saved leads.

## Files
- [index.html](index.html) — popup UI
- [index.css](index.css) — styles for the popup
- [index.js](index.js) — main logic (see functions/variables below)
- [manifest.json](manifest.json) — Chrome extension manifest
- [icon.png](icon.png) — extension icon

## Key symbols
- [`myLeads`](index.js) — array that stores saved leads
- [`render`](index.js) — renders `myLeads` into the popup UI
- [`tabBtn`](index.js) — "SAVE TAB" button event (saves active tab URL)
- [`inputBtn`](index.js) — "SAVE INPUT" button event (saves input text)
- [`deleteBtn`](index.js) — "DELETE ALL" button event (clears storage)

## Install / Run (for development)
1. Open Chrome and go to chrome://extensions
2. Enable "Developer mode"
3. Click "Load unpacked" and select the project folder (the folder containing [manifest.json](manifest.json))
4. Click the extension icon to open the popup ([index.html](index.html))

## Usage
- Type any text in the input and click SAVE INPUT to save it to `myLeads`.
- Click SAVE TAB to save the current tab's URL (requires the `tabs` permission from [manifest.json](manifest.json)).
- Click DELETE ALL to clear saved leads.

Data is persisted in localStorage under the key `"myLeads"`.

## Notes
- Rendering and DOM updates are handled in [`render`](index.js).
- You can inspect the popup console via the Chrome extension popup inspector for debugging.

## License
Simple demo project — use and modify as needed.