# Grey Black White

A minimal Microsoft Edge theme with a **pure black title bar and window frame**, a **#333333 toolbar**, and a **custom 1920×1080 new-tab image**.

![New tab background preview](docs/preview-background.jpg)

## Features

- Pure black (`#000000`) title bar, window frame, and window controls.
- `#333333` toolbar, address bar, and bookmarks bar.
- White page surface with dark, readable text.
- Custom new-tab background artwork (`theme/images/grey-black-white-ntp.png`).
- Theme-only: no scripts, no content scripts, no permissions, no data collection.

## Colors

| Area | Color |
| --- | --- |
| Title bar / window frame | `#000000` |
| Window controls | `#000000` |
| Toolbar / address bar / bookmarks bar | `#333333` |
| Toolbar text and icons | `#FFFFFF` |
| Page surface | `#FFFFFF` |
| Page text | `#1A1A1A` |
| New-tab background | custom image |

## Download

- GitHub release: https://github.com/DYouAn/grey-black-white/releases/latest
- Repository: https://github.com/DYouAn/grey-black-white

## Install (developer / unpacked)

1. Download `dist/Grey-Black-White-v2.3.0.zip` (or use the `theme/` folder directly).
2. Unzip it.
3. Open `edge://extensions/` in Microsoft Edge.
4. Enable **Developer mode**.
5. Click **Load unpacked** and select the folder containing `manifest.json`.
6. If needed, open **Settings → Appearance → Theme** and choose **Grey Black White**.

## Show the new-tab image

After installing:

1. Open a new tab.
2. Click the gear icon (page settings).
3. Set **Background** to **Theme**.
4. If a custom background was selected before, choose **No image** once and refresh the new tab.

Edge's built-in “Customize Edge → Image themes” can apply a colour theme sampled from the image and override this theme. If that happens, re-select **Grey Black White** under `edge://settings/appearance`.

## Privacy

This theme only supplies static colours and one image to Edge. It contains no scripts, makes no network requests, requests no permissions, and does not collect or share data.

See [privacy-policy.md](privacy-policy.md) or the hosted HTML version:

https://dyouan.github.io/grey-black-white/privacy-policy.html

## Repository layout

```
theme/                 Manifest + icon + new-tab image (load unpacked)
docs/                  Preview images and store screenshots
dist/                  Store-ready package for GitHub Releases
store/                 Edge Add-ons listing copy and publishing guide
privacy-policy.*       Policy text for the store / GitHub Pages
```

## Publishing to the Edge Add-ons store

The package in `dist/Grey-Black-White-v2.3.0.zip` has `manifest.json` at its root and is ready for Partner Center upload. See [store/publishing-guide-zh.md](store/publishing-guide-zh.md) and [store/listing.md](store/listing.md).

## Artwork

See [ASSETS.md](ASSETS.md). The new-tab artwork was supplied by the project owner; no license is granted for the artwork.
