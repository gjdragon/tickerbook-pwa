# Changelog

All notable changes to Tickerbook. Versions follow [Semantic Versioning](https://semver.org/).

## 1.1.0 - 2026-10-16

### Added
- Adding a stock with the Finnhub price source now looks up the live price and company name from the symbol. No price needs to be typed.
- A price box appears only when a lookup fails (unknown symbol, a non-US symbol on Finnhub's free plan, or no network), so a stock can still be added by hand.
- Version number shown under More > About.

### Changed
- The service worker cache is now named after the app version, so each release replaces the previous offline copy.

## 1.0.0 - 2026-10-16

First release.

### Added
- Watchlists: multiple lists, sorting by added order, symbol, change % or price, and a detail page with price chart (1M, 3M, 6M, All), day range and volume.
- Portfolio: buy, sell, dividend and cash records, with cost basis, realised and unrealised gain, fees and cash balance using the average-cost method.
- Price alerts: notify when a price goes above or below a level, checked on every price update, with optional browser notifications.
- Price sources: manual entry, a simulated demo feed, and Finnhub live quotes with your own API key.
- Settings: currency symbol, red-up or green-up colours, update interval.
- Backup and restore by copying and pasting your data as JSON.
- Installable PWA with offline app shell, light and dark themes.
