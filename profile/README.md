<div align="center">
  <img src="https://raw.githubusercontent.com/Access0x1/.github/main/profile/logo.png" width="120" alt="Access0x1">

# Access0x1

**The payment router that never holds the money.**

[access0x1.com](https://access0x1.com) · [Public payment record](https://access0x1.com/mainnet) · [Security](https://access0x1.com/security) · [Status](https://access0x1.com/status) · [Support on Telegram](https://t.me/access0x1)

</div>

---

A customer pays a business in USDC. The price is set in dollars and converted inside the transaction with a Chainlink price feed. The fee is split in that same transaction, so the business is paid at once and the router keeps nothing: what the business receives plus the fee always equals what the customer paid.

### Live

| | |
|---|---|
| Networks | Base · Ethereum · Unichain · Arc |
| Router (same address on each) | [`0xe92244e3368561faf21648146511DeDE3a475EB5`](https://basescan.org/address/0xe92244e3368561faf21648146511DeDE3a475EB5) |
| Owner | 2-of-3 Safe [`0xF025EC0bB828dbFD896c22142a323dD8606F9A91`](https://basescan.org/address/0xF025EC0bB828dbFD896c22142a323dD8606F9A91). Upgrades happen only through the Safe. |

### How the code is held to account

Unit, fuzz and invariant tests in Foundry on every money path, symbolic proofs with Halmos, mutation testing, and static analysis with Slither and Aderyn.

### Open source

- **[access0x1-snap](https://github.com/Access0x1/access0x1-snap)**: a MetaMask Snap that shows who you are paying, the fee and what the business receives, before you sign.

Access0x1 is built by [SebasTN Inc.](https://github.com/SebasTN-Inc), New York.
