# Arya Ardytia Putra

Building on-chain monitoring tools, trading analytics, and Telegram automations. Python, TypeScript, Sui/EVM.

I mostly ship small, focused tools: polling scripts, analytics CLIs, alerting bots, and the web front-ends that sit next to them. Alert-only by default — nothing here trades on my behalf.

## Projects

| Repo | What it does | Stack |
| --- | --- | --- |
| [trade-journal](https://github.com/padit8035-glitch/trade-journal) | CLI that turns a raw trade log into expectancy, profit factor, R-multiples, max drawdown, and a disposition-effect check | Python, SQLite, stdlib only |
| [tele-snipe-sui](https://github.com/padit8035-glitch/tele-snipe-sui) | Telegram bot that watches X accounts and project sites for new SUI/EVM/SOL contract addresses and alerts per project | TypeScript, grammy, SQLite |
| [wallet-tracker](https://github.com/padit8035-glitch/HERMES-AGENT-FOR-ONCHAIN-WALLET-TRACKING-CRYPTO-) | Multi-wallet on-chain monitor: polls trades and ERC20 transfers, queues alerts for Telegram delivery | Python, RPC, GMGN |
| [p1-cs-percetakan](https://github.com/padit8035-glitch/p1-cs-percetakan) | Customer-service bot for a printing company: local keyword pricing with no API key, plus an LLM mode with price guardrails | JavaScript |
| [p2-quotation-rembo](https://github.com/padit8035-glitch/p2-quotation-rembo) | Quotation calculator for printing jobs: line-item pricing, order summary, printable quote | JavaScript |
| [rembo-printing-web](https://github.com/padit8035-glitch/Rembo-Printing-web-) | Single-file landing site for a commercial printing company | HTML, CSS |

## Notes on how I build

- **Zero dependencies where the standard library will do.** `trade-journal` has no `pip install`, no lockfile, and runs on three Python versions in CI.
- **The maths is the product.** Analytics are pure functions with no I/O, so the risk calculations are tested directly rather than through a database.
- **Validate at the boundary.** CSV rows are checked on import; bad rows are reported by line number and skipped, never inserted silently.
- **Tests are plain asserts.** No framework, no fixtures — just the checks that fail if the maths breaks.

## Stack

`Python` · `TypeScript` · `Node.js` · `SQLite` · `grammy` · `@mysten/sui` · `EVM RPC` · `Linux / systemd`

## Working on

- Alert pipelines for Sui and EVM with Telegram as the delivery layer
- Behavioural metrics for discretionary trading (cutting winners early is measurable)
- Keeping every tool single-purpose and runnable on a cheap VPS
