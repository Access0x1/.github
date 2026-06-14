<div align="center">

# Access0x1

**A do-it-all center to get you and your business onchain.**

Open-source, non-custodial, USD-priced payments + commerce + identity.
One drop-in. No contract code.

![License: MIT](https://img.shields.io/badge/License-MIT-0B7261?style=for-the-badge)
![Tests](https://img.shields.io/badge/tests-846%20passing-44CC11?style=for-the-badge)
![Router coverage](https://img.shields.io/badge/router%20coverage-100%25-44CC11?style=for-the-badge)
![Slither](https://img.shields.io/badge/slither-0%20exploitable-44CC11?style=for-the-badge)
![Non-custodial](https://img.shields.io/badge/custody-none-5B21B6?style=for-the-badge)

</div>

---

## What is Access0x1?

Access0x1 is an open-source, **non-custodial** way to get you and your business
onchain — accept **USD-priced** crypto payments, run real commerce on top, and
authorize agents — all with **no per-merchant contract code to write**.

A single shared, multi-tenant router serves every merchant. A payment is priced
USD-to-token *inside the settlement transaction* using a Chainlink feed, an exact
fee is split atomically, and net value is pushed to the merchant — all in one tx.
**The contract never holds merchant funds.** What you read is what runs your money.

## The one flow

```
authenticate (embedded wallet / agent)
  -> fund (any allowlisted token)
  -> pay USD-priced (Chainlink feeds, priced inside the tx)
  -> settle gas-free in USDC on Arc (Circle)
  -> receipt minted (ERC-6909 non-custodial pull receipt)
  -> value pulled to the merchant
```

Every step is a composable seam. Drop in only the pieces you need; they all run
through the same audited router.

## What's in the box

- **Payments** — one shared, non-custodial router. USD-priced via Chainlink,
  exact fee split atomically, net pushed to the merchant, all in one tx.
- **Commerce** — subscriptions, bookings, invoices, gift cards / prepaid balances,
  and zero-custody NFT sales — each a USD-priced primitive that settles straight
  through the router.
- **Identity + agents** — sign-once, budget-scoped, time-bounded agent sessions,
  including from smart accounts that aren't deployed on-chain yet.
- **Your own token** — a non-custodial factory so a business can deploy its OWN
  loyalty / credit / closed-loop token and own it in its own wallet.

## The owned ERCs

Access0x1 ships minimal, audited implementations of three ERCs that are
load-bearing to the payments + commerce + agents story:

| Standard | What we ship | Why |
|---|---|---|
| **ERC-6909** | `PaymentLanes` — multi-token non-custodial receipts, one lane per `(chainId, asset, recipient)` | receive settled value in any coin; the "pull what's yours" seam |
| **ERC-7702** | `SessionGrant` — sign once -> delegated, budget-scoped, time-bounded agent session | agent commerce without a co-sign on every spend |
| **ERC-6492** | `SessionGrant.openSessionFor` — validates signatures from counterfactual (not-yet-deployed) smart accounts | authorize before the wallet is even on-chain |

It also consumes the standard token interfaces directly: **ERC-20** for payments
and the business-owned token factory, and **ERC-721** for non-custodial NFT sales.

## The proof

Payments infrastructure is load-bearing — merchants and developers should be able
to read exactly what runs their money, not trust a black box.

- **846 tests passing** — unit, attack, and invariant suites.
- **100% router coverage**; money-path invariants proved under fuzz.
- **Slither: 0 exploitable findings.**
- **MIT licensed**, built in public.
- **Non-custodial by construction** — the router never holds merchant funds.

## Chains

**Arc (Circle)** is the lead settlement chain — gas-free USDC checkout by default —
with **Base** and **zkSync** as additional targets. Testnet only today
(Arc Testnet, Base Sepolia, zkSync Sepolia); **no mainnet deployments and no
mainnet claims.**

Built with: **Foundry · Solidity 0.8.28 · OpenZeppelin 5.x · Chainlink Data Feeds + CRE · Arc · Base · zkSync · USDC**

## Get started

Scaffold the starter (a working USD-priced checkout) straight from the repo —
no install, nothing to publish to trust:

```bash
npx degit Access0x1/Access0x1/templates/starter my-checkout
cd my-checkout
npm run setup     # installs Foundry, deps, and builds the contracts
```

The generated app and contracts are **yours** — buyers pay a router you configure,
and nothing depends on Access0x1 infrastructure.

## Explore

| Repo | What it is |
|---|---|
| [**Access0x1/Access0x1**](https://github.com/Access0x1/Access0x1) | The protocol: contracts, tests, deploy scripts, audit trail, and the starter template. MIT. **Start here.** |

Built in public. MIT. No mainnet deployments yet — testnet only.
