# Tickerbook

A stock tracker that runs in the browser and installs on your phone as a PWA. It is an independent app inspired by popular Android stock trackers such as JStock.

**Version 1.1.0** (see [CHANGELOG.md](CHANGELOG.md))

## Features

- **Watchlists**: several lists, sorting, and a detail page with a price chart, day range, volume and your position.
- **Portfolio**: buy, sell, dividend and cash records. Shows cost basis, realised and unrealised gain, dividends, fees and cash balance (average-cost method).
- **Price alerts**: above or below a price, checked on every price update, with optional browser notifications.
- **Price sources**: manual entry, a simulated demo feed, or live quotes from [Finnhub](https://finnhub.io/) with your own free API key.
- **Backup and restore**: copy your data as JSON and paste it back later.
- **Offline shell** and light/dark themes.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app (HTML, CSS and JavaScript in one file) |
| `manifest.webmanifest` | Name, colours and icons used when installed |
| `sw.js` | Service worker that caches the app for offline use |
| `icon-192.png`, `icon-512.png` | App icons |
| `CHANGELOG.md` | Release history |

## Host it on GitHub Pages

1. Put all the files in a repository, either at the root or in a folder such as `docs/`.
2. In the repository go to **Settings > Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, pick your branch and the folder (`/ (root)` or `/docs`), then save.
4. After a minute the app is live at `https://<your-username>.github.io/<repository>/`.

All paths in the app are relative, so it works from a repository sub-path.

## Install on your phone

Open the GitHub Pages address in Chrome on Android, open the menu and choose **Add to Home screen** (or **Install app**). On iPhone use Safari, then **Share > Add to Home Screen**.

## Live prices with Finnhub

1. Create a free account at finnhub.io and copy your API key.
2. In the app open **More**, set **Price source** to **Finnhub (live)**, and paste the key.
3. Add stocks by symbol. The price and company name are fetched for you.

Notes:
- Finnhub's free plan covers US stocks. For other markets, add the stock by hand and use manual prices.
- The key is stored in your browser only and is sent only to finnhub.io.
- The free plan allows about 60 calls a minute. With a long watchlist, choose a longer update interval.

## Your data

Everything is stored in your browser (`localStorage`) on the device you use. Nothing is uploaded. Clearing site data erases it, so use **More > Backup** now and then. Backups can be restored on any device.

## Updating

Replace the files in your repository with the new ones and commit. Installed copies pick up the new version the next time the app is opened online, after one reload.

## Versioning

The version appears in three places and should be changed together on each release:

1. `VERSION` in `index.html` (shown under More > About)
2. `CACHE` and the comment at the top of `sw.js`
3. The heading in `CHANGELOG.md` and the version line in this README

## Disclaimer

Prices may be delayed or wrong. Nothing here is investment advice.
