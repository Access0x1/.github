<div align="center">

<img src="https://raw.githubusercontent.com/Access0x1/.github/main/profile/logo.png" width="120" alt="Access0x1" />

# Access0x1

**Get any business — or its agent — onchain, in one drop-in.**
Open-source, non-custodial, USD-priced payments + commerce + identity. No contract code.

![License: MIT](https://img.shields.io/badge/License-MIT-0B7261?style=for-the-badge)
![Non-custodial](https://img.shields.io/badge/custody-none-5B21B6?style=for-the-badge)
![One address, 8 testnets](https://img.shields.io/badge/one%20CREATE3%20address-9%20testnets-1D4ED8?style=for-the-badge)

[Live app](https://access0x1.click) · [Repo](https://github.com/Access0x1/Access0x1) · [SDK](https://github.com/Access0x1/Access0x1/tree/main/packages/react) · [Truthful self-audit](https://github.com/Access0x1/Access0x1/blob/main/AUDIT.md)

</div>

---

## What it is

One shared router serves every merchant. Each payment is USD-priced *inside the
settlement transaction* via a Chainlink feed, an exact fee is split atomically
(`net + fee == gross`), and net value lands at the merchant in the same tx —
**the contract never holds merchant funds.** What you read is what runs your money.

```bash
npx degit Access0x1/Access0x1/templates/starter my-checkout   # the whole stack, yours
```

## The proof

- The same **CREATE3** router — [`0xe92244e3368561faf21648146511DeDE3a475EB5`](https://sepolia.basescan.org/address/0xe92244e3368561faf21648146511DeDE3a475EB5) —
  serves **nine testnets** (7 source-verified), with registered merchants and settled
  payments you can read on-chain.
- Test counts are **CI-enforced on the [repo badges](https://github.com/Access0x1/Access0x1#readme)** —
  read them there, fresh, over 2,000 Foundry tests strong plus the web suite.
- A public **[truthful self-audit](https://github.com/Access0x1/Access0x1/blob/main/AUDIT.md)**
  labels every seam and gap. **Testnet-only today — mainnet is a post-audit
  decision, not a claim.**

## Building with, this weekend — ETHGlobal Lisbon 2026

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

> Built solo at ETHGlobal NY 2026; extended live at ETHGlobal Lisbon 2026.
> Every claim is reproducible from the repo.

[**Access0x1/Access0x1**](https://github.com/Access0x1/Access0x1) — contracts,
tests, deploy scripts, the self-audit, and the starter. MIT. **Start here.**
