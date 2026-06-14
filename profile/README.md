<div align="center">

<img src="https://raw.githubusercontent.com/Access0x1/.github/main/profile/logo.png" width="120" alt="Access0x1" />

# Access0x1

**Get any business onchain — in one drop-in.**
Open-source, non-custodial, USD-priced payments + commerce + identity. No contract code.

![License: MIT](https://img.shields.io/badge/License-MIT-0B7261?style=for-the-badge)
![Tests](https://img.shields.io/badge/tests-859%20passing-44CC11?style=for-the-badge)
![Router coverage](https://img.shields.io/badge/router-100%25%20fn%20%C2%B7%20~98%25%20lines-44CC11?style=for-the-badge)
![Slither](https://img.shields.io/badge/slither-0%20exploitable-44CC11?style=for-the-badge)
![Non-custodial](https://img.shields.io/badge/custody-none-5B21B6?style=for-the-badge)
![Base Sepolia + Arc](https://img.shields.io/badge/live-Base%20Sepolia%20%2B%20Arc%20Testnet-1D4ED8?style=for-the-badge)

[Live demo](https://access0x1.nfteria.click) · [Repo](https://github.com/Access0x1/Access0x1) · [SDK](https://github.com/Access0x1/Access0x1/tree/main/packages/react) · [Truthful self-audit](https://github.com/Access0x1/Access0x1/blob/main/AUDIT.md)

</div>

---

```bash
npx create-access0x1     # a non-custodial, USD-priced crypto checkout — live in minutes
```

## What it is
A single shared, multi-tenant router serves every merchant. Each payment is priced USD→token *inside the settlement transaction* via a Chainlink feed, an exact fee is split atomically, and net value is pushed to the merchant — all in one tx. **The contract never holds merchant funds.** What you read is what runs your money.

## What's in the box
- **Payments** — non-custodial router, USD-priced via Chainlink, atomic fee split.
- **Commerce** — subscriptions, bookings, invoices, gift cards, NFT sales — each settles through the router.
- **Identity + agents** — sign-once, budget-scoped agent sessions (ERC-7702 + ERC-6492, pre-deploy-safe); verified-human / verified-identity checkout (World ID, ENS, OIDC) stacks on top.
- **Owned ERCs** — ERC-6909 `PaymentLanes` (non-custodial receipts), ERC-7702/6492 `SessionGrant`, ERC-721 escrow.

## The proof
- **859 tests, 0 failed** · 13 headline / 45 total fuzz invariants (`fail_on_revert = true`)
- Router coverage **100% functions / ~98% lines / ~97% branches** · **Slither: 0 exploitable**
- **Deployed + verified on Base Sepolia** — router [`0xec89c9eE28AF42Ae2b917BB0bAe245EAad6E8E57`](https://base-sepolia.blockscout.com/address/0xec89c9eE28AF42Ae2b917BB0bAe245EAad6E8E57)
- **Deployed + verified on Arc Testnet (5042002)** — router [`0xA5982ea8842Eea97C6e313A5f75FD8CF72C69Aad`](https://testnet.arcscan.app/address/0xa5982ea8842eea97c6e313a5f75fd8cf72c69aad)
- **MIT**, built in public, **non-custodial by construction** (refunds can never be blocked)
- A public **[truthful self-audit](https://github.com/Access0x1/Access0x1/blob/main/AUDIT.md)** that labels every seam and gap

## Built with our sponsors (on `main`)
- **Dynamic** — email login → embedded wallet; the whole connect / sign / pay flow runs through it.
- **Chainlink** — Data Feeds price USD→token *inside the pay tx* (the price that drives settlement, not a preview).
- **ENS** — verified merchant identity (ENSIP-19) + gasless `merchant-<id>.<parent>.eth` subnames via Namestone.
- **World ID** — verified-human checkout gate (shipped on `main`).
- **Circle x402 / Gateway** — gas-free USDC settlement via EIP-3009. Arc is the lead chain — USDC is its native gas token — and all 8 contracts are **deployed + verified on Arc Testnet** alongside Base Sepolia.
- *Seams (code present, not yet in the live path): Walrus, Unlink, Blink, Uniswap payout-swap.*

## Chains
**Deployed + verified: Base Sepolia (84532) and Arc Testnet (5042002).** zkSync Sepolia is **one-command ready** (`make deploy-zksync`) but not yet broadcast. **Testnet only — no mainnet deployments and no mainnet claims.**

## Get started
```bash
npx degit Access0x1/Access0x1/templates/starter my-checkout
cd my-checkout && npm run setup
```
The generated app + contracts are **yours** — buyers pay a router you configure; nothing depends on Access0x1 infra.

---

We're **vampire coders** — open-source builders draining the closed, custodial houses onto rails nobody can lock. Casinos always had crypto; we add the accountability they never did. **#DrainTheHouse**

> Built solo at ETHGlobal NY 2026. Testnet today, and we say so — every claim is reproducible from the repo.

[**Access0x1/Access0x1**](https://github.com/Access0x1/Access0x1) — the protocol: contracts, tests, deploy scripts, the self-audit, and the starter. MIT. **Start here.**
