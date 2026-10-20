<div align="center">

<img src="https://raw.githubusercontent.com/Access0x1/.github/main/profile/logo.png" width="120" alt="Access0x1" />

# Access0x1

**Get any business — or its agent — onchain, in one drop-in.**
Non-custodial, USD-priced payments + commerce + identity. No contract code.

![Live on Base mainnet](https://img.shields.io/badge/Base%20mainnet-live-0B7261?style=for-the-badge)
![Non-custodial](https://img.shields.io/badge/custody-none-5B21B6?style=for-the-badge)
![Safe-owned](https://img.shields.io/badge/owned%20by-2--of--3%20Safe-1D4ED8?style=for-the-badge)

[Mainnet proof](https://access0x1.com/mainnet) · [Security](https://access0x1.com/security) · [Status](https://access0x1.com/status) · [Support](https://t.me/access0x1) · [Test network](https://access0x1.click)

</div>

---

## What it is

One shared router serves every merchant. Each payment is USD-priced *inside the
settlement transaction* via a Chainlink feed, an exact fee is split atomically
(`net + fee == gross`), and net value lands at the merchant in the same tx —
**the contract never holds merchant funds.** What you read is what runs your money.

Live on **Base mainnet** since 2026-10-20: eleven modules, every one owned by a
2-of-3 multisig Safe, upgrades only by that Safe, source verified on Basescan.
Fees on chain: 1% per payment (30 cent minimum), 2% for the extra-service modules.

## The proof

- The first three real USDC settlements on Base each split exactly (merchant net plus fee
  equals gross) and left the router at zero. The transactions are on
  **[access0x1.com/mainnet](https://access0x1.com/mainnet)**.
- The router proxy is [`0xe92244e3368561faf21648146511DeDE3a475EB5`](https://basescan.org/address/0xe92244e3368561faf21648146511DeDE3a475EB5),
  and the same CREATE3 address answers on **eleven test networks**, so you can rehearse with
  test funds at [access0x1.click](https://access0x1.click) first.
- Thousands of Foundry tests, fuzz and invariant suites, and symbolic proofs, behind every
  release. Ethereum and Unichain mainnet are coming next.

## Built with, at ETHGlobal Lisbon 2026

**Uniswap** (a real swap landed through the shipped rail during the event —
[fill == quote, to the wei](https://sepolia.etherscan.io/tx/0x936acc13fd35032da86aa7075608131f3c39addb9198d7d5877e54ff51a24e69) —
plus a v4 hook that turns swaps into attributable receipts) ·
**0G** (the assistant answers on 0G Compute, badge visible) ·
**World** (an AgentKit admission gate in front of the paying agent) ·
**ENS** (a payment resolver, and an agent identity that publishes its own
inference choice onchain).

## In the stack either way

**Dynamic · Chainlink · Circle (USDC, Arc, x402) · MetaMask · Walrus** — not all
of them sponsor every event we build at. We like them, we run on them regardless.

---

> Built at ETHGlobal NY 2026; extended at ETHGlobal Lisbon 2026.
> Every claim here has a public proof: [access0x1.com/mainnet](https://access0x1.com/mainnet).
