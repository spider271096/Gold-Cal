# FundedNext XAUUSD Risk Calculator

A single-file calculator (plain HTML, CSS and JavaScript, no dependencies) for a **$6,000 FundedNext Stellar 2-Step** MT5 account, trading **XAUUSD only**.

## What it does

- Enter direction (BUY or SELL) and entry price.
- Stop loss is set **$12** from entry and take profit **$24** from entry (1:2).
- Lot size is calculated automatically and rounded **down** to the MT5 lot step, so the estimated stop-loss loss plus entered costs stays within **$18**.
- Shows estimated costs, net loss at SL and net profit at TP.
- Daily risk tracker for the personal rules below.

## Rules used

| Rule | Value |
|---|---|
| Risk per trade (costs included) | $18 |
| Max trades per day | 2 |
| Personal daily hard stop | -$40 |
| Stop after consecutive losses | 2 |
| Firm daily loss limit | $300 |
| Firm maximum loss (static) | $600 |
| Static account floor | $5,400 |
| Phase 1 / Phase 2 target | $480 / $300 |

The firm values come from the FundedNext plan page for this account. Always confirm them on your own dashboard.

## Assumptions to verify

- Contract size is assumed to be **100** for XAUUSD. Check the symbol specification in your MT5.
- Default lot step is 0.01. Spread, slippage and commission default to 0, so enter your real values for accurate sizing.
- The tracker is manual. It does not connect to MT5.

## Run locally

Download `index.html` and open it in any browser.

## Install on a phone

The site is an installable web app and works offline after the first visit.

1. Open the GitHub Pages link in Chrome.
2. Menu > **Install app** (or **Add to Home screen**).

Files: `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`. Keep them all in the repository root.

## Deploy with GitHub Pages

1. Push `index.html` and `README.md` to a repository.
2. Open **Settings > Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
4. The site goes live at `https://<your-username>.github.io/<repository-name>/` after a minute.

## Disclaimer

This is a personal calculation aid, not financial advice. Trading carries risk of loss. Fills, spread and slippage can make actual results differ from the estimates.
