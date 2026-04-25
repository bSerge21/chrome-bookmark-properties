# Bookmark Properties — Chrome Extension

A Chrome side panel extension that shows detailed properties of your bookmarks: creation date, modification date, last used date, folder path, and more.

## Features

- **Drag & drop** — drag any bookmark from the bookmarks bar or bookmarks manager onto the drop zone to instantly see its properties
- **Recent bookmarks** — shows the 30 most recently added bookmarks
- **Search** — search bookmarks by title or URL
- **Properties** — shows ID, creation date, modification date, last used date, domain, folder path, position
- **Edit** — rename or change the URL of a bookmark directly from the panel
- **Stats** — total bookmark and folder count, number of unique domains, oldest bookmarks

## Why

Chrome's built-in bookmarks manager does not show when a bookmark was created or any other metadata. This extension fills that gap.

## Installation

Since this extension is not published on the Chrome Web Store, install it manually:

1. Download or clone this repository
2. Open Chrome and go to `chrome://extensions/`
3. Enable **Developer mode** (toggle in the top right)
4. Click **Load unpacked** and select the folder containing the extension files
5. Click the extension icon in the toolbar to open the side panel

## Usage

- **Drag & drop** — open `chrome://bookmarks` or any page with a bookmarks bar, then drag a bookmark onto the "Drag bookmark here" zone in the panel
- **Search** — switch to the Search tab and type a title or URL
- **Recent** — the Recent tab shows your latest bookmarks; click any to view its properties
- **Edit** — in the Properties tab, change the title or URL and click Save

## Files

```
manifest.json     — extension manifest (MV3)
background.js     — service worker (opens side panel on toolbar click)
sidepanel.html    — side panel UI
sidepanel.js      — all logic (bookmark API calls, rendering, drag & drop)
icons/            — extension icons
```

## Permissions

- `bookmarks` — read and update bookmark data
- `sidePanel` — display the side panel
- `storage` — reserved for future use
- `tabs` — open bookmarks in a new tab

## License

MIT
