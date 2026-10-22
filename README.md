<p align="center"><img src="assets/mimo_mascot_logo_transparent.png" width="96" alt="MIMO mascot"></p>
<h1 align="center">MIMO Exchange</h1>
<p align="center">A non-custodial trading terminal for Robinhood Chain.</p>
<p align="center"><a href="https://mimotrade.io">mimotrade.io</a> · <a href="web/README.md">Documentation</a> · <a href="SECURITY.md">Report a vulnerability</a></p>

![The MIMO trade terminal](web/public/screens/trade.png)

MIMO trades crypto, Robinhood Stock Tokens and new launches on Robinhood Chain (chain ID 4663) through Uniswap v2, v3 and v4. Your wallet signs every transaction. MIMO never holds keys or funds, and charges no fee of its own.

## What it does

- **Swaps through Uniswap's own contracts.** The best of direct and two-hop routes through WETH and USDG, with the pool fee, price impact and minimum received shown before you sign.
- **A check before every signature.** Each transaction is decoded against its quote and simulated; anything that does not match is refused before your wallet sees it.
- **Risk flags on every token.** Source verification, owner powers, a honeypot and tax simulation, Stock Token authenticity, liquidity and pool age.
- **Live prices.** Every price moves with its token's own pool on chain.
- **Orders that wait for you.** Limit, stop and OCO orders and DCA or grid bots ask your wallet when their price is reached.
- **Telegram companion.** Prices, new-pool alerts and a read-only portfolio.

## Stack

Next.js 16, React 19, TypeScript, viem and wagmi, Tailwind CSS 4, SQLite. Ships as one Docker container.

## Run it locally

```bash
cd web
npm ci
npm run dev   # http://localhost:3210
npm test
```

## Status

Private beta at [mimotrade.io](https://mimotrade.io). MIMO is not affiliated with Robinhood. A Robinhood Stock Token is a token issued by Robinhood Assets (Jersey) Limited, not the share itself. Nothing here is investment advice.
