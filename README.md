<div align="center">

# 🗿 Concrete Community Tools

**Independent, community-built tools for [Concrete Protocol](https://concrete.xyz)**

A wallet tracker, a builder suite, and a field guide — built to make the protocol easier to use, understand, and explore.

[![Concrete Tracker](https://img.shields.io/badge/Live-Concrete%20Tracker-2f6fed?style=for-the-badge)](https://concrete-tracker-seven.vercel.app)
[![Builder Suite](https://img.shields.io/badge/Live-Builder%20Suite-c9a227?style=for-the-badge)](https://concrete-builder-suite.vercel.app)
[![Concrete Academy](https://img.shields.io/badge/Live-Concrete%20Academy-6b6b6b?style=for-the-badge)](https://concrete-academy.vercel.app)

![Status](https://img.shields.io/badge/status-active-brightgreen)
![Unofficial](https://img.shields.io/badge/affiliation-unofficial%20%2F%20community-lightgrey)
![License](https://img.shields.io/badge/license-MIT-blue)

</div>

---

## ⚠️ Independence notice

These are **unofficial, community-built projects**. They are not made, maintained, or endorsed by Blueprint Finance or the Concrete team. Nothing here ever asks for a seed phrase, private key, or wallet connection. Where numbers are shown — TVL, APY, funding rounds — they're either read live on-chain, pulled live from DefiLlama's public API, or hand-verified against Concrete's own public announcements. Anything hypothetical (like airdrop modeling) is labeled clearly as such. **Always confirm anything financially material directly on [app.concrete.xyz](https://app.concrete.xyz).**

---

## 📖 Table of Contents

- [Overview](#-overview)
- [1. Concrete Tracker](#1--concrete-tracker)
- [2. Concrete Builder Suite](#2--concrete-builder-suite)
- [3. Concrete Academy](#3--concrete-academy)
- [Why three separate tools](#-why-three-separate-tools)
- [Tech notes](#-tech-notes)
- [Feedback](#-feedback)
- [License](#-license)

---

## 🧭 Overview

| Tool | What it's for | Link |
|---|---|---|
| 📍 **Concrete Tracker** | Read your live vault positions & points, no wallet-connect | [Launch →](https://concrete-tracker-seven.vercel.app) |
| 🧰 **Concrete Builder Suite** | AI assistant, vault optimizer, docs guide, arcade game | [Launch →](https://concrete-builder-suite.vercel.app) |
| 📚 **Concrete Academy** | A field-guide-style course on how Concrete actually works | [Launch →](https://concrete-academy.vercel.app) |

---

## 1. 📍 Concrete Tracker

> A wallet-first, read-only dashboard for Concrete vault positions.

**Live:** https://concrete-tracker-seven.vercel.app

### Features
- ✅ Live vault positions — Ethereum + Arbitrum, read directly from each vault's on-chain ERC-4626 interface (no indexer, no cache)
- ✅ Concrete Points balance + leaderboard
- ✅ Multi-wallet comparison, side by side
- ✅ Shareable public profile links (`/w/0xYourAddress`)
- ✅ CSV / JSON / PDF export + auto-generated share cards
- ✅ Share-price alerts (browser + webhook)
- ✅ **Live Vaults dashboard** — every known vault, live TVL/share price/APY
- ✅ **Vault Optimizer + Earning Prediction** chart
- ✅ Hypothetical airdrop allocation estimator (based on your real points)

<details>
<summary><strong>How it works</strong></summary>

<br>

Every read happens live, at request time, straight from the chain — calling each vault's `name`, `symbol`, `totalAssets`, `totalSupply`, `balanceOf`, and `convertToAssets` over a public RPC. No database caching your position, no scheduled indexer, no wallet-connect step. Nothing is ever signed and no approval is ever requested — it only reads public on-chain state.

</details>

### Who it's for
Anyone tracking their own Concrete position, multiple wallets, or a team/DAO treasury that wants an audit-ready, read-only view.

---

## 2. 🧰 Concrete Builder Suite

> A hub of tools, an AI assistant, and a game — different ways into the ecosystem.

**Live:** https://concrete-builder-suite.vercel.app

| Tool | Description |
|---|---|
| 🤖 **Concrete Assistant** | AI chatbot for real-time protocol Q&A — APYs, liquidation protection, borrowing, onboarding |
| 📊 **Vault Optimizer** | Risk-adjusted yield comparison across Concrete's multi-asset vaults |
| 📖 **System Guide** | Interactive knowledge base covering vaults, borrowing, liquidation protection & points |
| 🎮 **Moai Saves: DeFi Rescue** | Browser arcade game teaching Concrete's mechanics through gameplay — catch depositors, block liquidators, climb the Hall of Stone leaderboard |
| 🧭 **Concrete Run** | Zero-friction portal linking directly into `app.concrete.xyz` and `points.concrete.xyz` |

### Why it exists
Different people engage differently — some want a dashboard, some want a chatbot, some learn best by playing something. Builder Suite covers more of those entry points instead of assuming one format fits everyone.

---

## 3. 📚 Concrete Academy

> An unofficial field guide to how Concrete is built — with live data baked in.

**Live:** https://concrete-academy.vercel.app

### How the learning format works
1. **Read a drawing** — plain-language explainer of one part of the protocol
2. **Pass inspection** — three quick checks per sheet
3. **Earn your standing** — Apprentice → Architect, tracked locally in your browser only

### Live data (not a snapshot)
- 📡 Live official X feeds — `@ConcreteXYZ`, `@Blueprint_DeFi`
- 📈 Live TVL & chain data from DefiLlama's public API
- 📰 Live-updating milestone history since Blueprint Finance's 2022 founding

### Toolkit inside Academy
- 💰 **Vault Yield Calculator** — real vault, live APY, your hypothetical deposit
- 🏆 **Vault Optimizer** — ranks every live vault by current APY
- 🔍 **Vault Explorer** — side-by-side custody & withdrawal comparison
- 💸 **Funding Trail** — every disclosed round since 2022, charted
- 🎲 **Airdrop Allocation Checker** *(hypothetical, unofficial — Concrete has not announced a token)*

### Who it's for
Anyone who wants to actually understand Concrete's mechanics with real numbers, instead of piecing it together from threads.

---

## 🤔 Why three separate tools

Different people want different things from a protocol they're spending time in — raw position data, decision-support tools, or a proper way to learn the system. Keeping each tool focused on one job let each one stay simple instead of building one bloated app.

---

## 🛠 Tech notes

- All three are static/serverless deployments on Vercel.
- On-chain reads use standard read-only RPC calls — no wallet connection is ever requested.
- Live data sources: public RPC endpoints (chain reads), DefiLlama's public API (TVL/APY), and Concrete's own official X/blog feeds.
- No user wallet, points, or personal data is stored server-side by any of these tools.

---

## 💬 Feedback

Bug reports, feature requests, and general feedback are always welcome — open an issue in this repo, or reach out on X.

---

## 📄 License

MIT — see [LICENSE](./LICENSE).

<div align="center">

Built independently for the Concrete community. Not affiliated with Blueprint Finance.

</div>
