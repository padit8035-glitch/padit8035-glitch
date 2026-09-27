# Arya Ardytia Putra

Building on-chain monitoring tools and Telegram automations. Python, TypeScript, Sui/EVM.

I mostly ship small, focused tools: polling scripts, alerting bots, and the web front-ends that sit next to them. Alert-only by default — nothing here trades on my behalf.

## Projects

| Repo | What it does | Stack |
| --- | --- | --- |
| [tele-snipe-sui](https://github.com/padit8035-glitch/tele-snipe-sui) | Telegram bot that watches X accounts and project sites for new SUI/EVM/SOL contract addresses and alerts per project | TypeScript, grammy, SQLite |
| [wallet-tracker](https://github.com/padit8035-glitch/HERMES-AGENT-FOR-ONCHAIN-WALLET-TRACKING-CRYPTO-) | Multi-wallet on-chain monitor: polls trades and ERC20 transfers, queues alerts for Telegram delivery | Python, RPC, GMGN |
| [p1-cs-percetakan](https://github.com/padit8035-glitch/p1-cs-percetakan) | Customer-service bot for a printing company: local keyword pricing with no API key, plus an LLM mode with price guardrails | JavaScript |
| [p2-quotation-rembo](https://github.com/padit8035-glitch/p2-quotation-rembo) | Quotation calculator for printing jobs: line-item pricing, order summary, printable quote | JavaScript |
| [rembo-printing-web](https://github.com/padit8035-glitch/Rembo-Printing-web-) | Single-file landing site for a commercial printing company | HTML, CSS |

## Stack

`TypeScript` · `Python` · `Node.js` · `SQLite` · `grammy` · `@mysten/sui` · `EVM RPC` · `Linux / systemd`

## Working on

- Alert pipelines for Sui and EVM with Telegram as the delivery layer
- Keeping every tool single-purpose and runnable on a cheap VPS
