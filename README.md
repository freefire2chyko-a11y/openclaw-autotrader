# OpenClaw AutoTrader

Public-facing tracking repo for `Tiger Pocket Agent`, containing only sanitized monitoring cards and daily review notes.

[简体中文说明](./README.zh-CN.md)

## Naming

- Primary repo name: `openclaw-autotrader`
- Positioning: OpenClaw + Fully Automated Live Trading
- Short stream title: `OpenClaw AutoTrader Daily`

Alternative names:

- `tigerpocket-openclaw-autotrader`
- `openclaw-live-autotrader`
- `openclaw-trading-bot`

## Purpose

This repo is designed for a daily livestream workflow:

- publish a sanitized public monitoring card
- publish a sanitized daily report and recap
- keep livestream-friendly public updates in one place
- avoid uploading private trading details, identity data, and code internals

## Recommended Structure

```text
.
├── README.md
├── README.zh-CN.md
├── .gitignore
├── docs/
│   ├── public-monitor/
│   │   ├── README.md
│   │   └── 2026/
│   │       └── 2026-03-11.md
│   ├── daily-reports/
│   │   ├── README.md
│   │   └── 2026/
│   │       └── 2026-03-11.md
│   ├── weekly-recaps/
│   └── incidents/
├── logs/
│   ├── README.md
│   └── .gitkeep
├── strategies/
│   └── README.md
├── configs/
│   └── .env.example
└── scripts/
    └── README.md
```

## What Gets Published

Published to GitHub:

- `docs/public-monitor/YYYY/YYYY-MM-DD.md`
- `docs/daily-reports/YYYY/YYYY-MM-DD.md`

Never publish:

- account balances
- prices, quantities, costs, or PnL amounts
- order ids or broker metadata
- token usage or model chain
- identity data, secrets, local paths, or implementation details

## Where The Public Card Is Updated

Update public monitoring cards in:

- `docs/public-monitor/YYYY/YYYY-MM-DD.md`

Example:

- `docs/public-monitor/2026/2026-03-11.md`

## Where To Update The Daily Report

Update daily reports in:

- `docs/daily-reports/YYYY/YYYY-MM-DD.md`

Example:

- `docs/daily-reports/2026/2026-03-11.md`

This keeps reports easy to browse by year and easy to surface during livestreams.

## Logs Policy

This repo should not carry raw runtime logs.

Use `logs/` only as a reminder that runtime logs stay local and private.

## Daily Report Template

Each daily report should include:

1. Market context
2. Public status snapshot
3. Public action summary
4. Review of plan vs execution
5. Risk or anomaly note
6. Next-session watch items

## Livestream Workflow

1. Local trading system produces the full private monitor card and report
2. The GitHub tracking agent strips sensitive fields
3. A public card is written into `docs/public-monitor/YYYY/YYYY-MM-DD.md`
4. A public daily review is written into `docs/daily-reports/YYYY/YYYY-MM-DD.md`
5. The repo commits and pushes only those public markdown files

## Suggested Next Steps

If you want, the next iteration can add:

- GitHub Actions to validate public report format
- a dashboard page for recent public updates
- a small site index for livestream browsing
