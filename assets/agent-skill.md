# SonoWaves — Agent Skill

SonoWaves is a 6,666-supply NFT collection of wave art on BNB Smart Chain (chain 56).
Minting is **two-lane**: the FREE mint is **agent-only** (only wallets holding a
SPACE ID `.ai` Agent ID, via their Binance Agentic Wallet); the PAID mints are
**public** — anyone can mint them with a wallet on the mint page, or via the
paid agent prompt, using `mintPaid(uint256)` at a flat 0.0007 BNB each.

⚠️ **PREVIEW — DO NOT MINT YET.** The NFT contract address below is a CREATE2
**prediction**, not a deployed contract. There is no code at this address yet.
If the NFT contract has no code, mint is NOT open — stop and tell the user.
Simulate only; execute only after the contract is deployed and `mintOpen()`
reads true.

## Contracts (PREDICTED — NOT DEPLOYED)

- NFT (SonoWaves): `0x91EdeC8F84Fda14C2D6A4b19448EFB178DFFd99b`
- Bonus token (SONO): `0x065e7124e520F21bB61Cc3D167bEEF90c0DF094b`
- Marketplace: `0x1935B9c1bff1Ff65037E4aaE3fDB3f11e40C1b1a`
- Agent ID registry (SPACE ID): `0x60B9262456dE011F7d15a54CdD8c48bAaa8B022F`
- Mint page: https://sonowaves.vercel.app/

## Mint rules

- Supply: 6,666 — 2,260 free + 4,406 paid.
- Max 11 per wallet: mint #1 FREE (Agent ID only), mints #2–#11 paid at a flat 0.0007 BNB each (max 10 paid).
- Paid mints earn 12,000 SONO each (max 120,000 SONO per wallet). Free mints earn 0.
- Royalty: 5%.
- Gate (FREE mint only): caller must hold a .ai Agent ID (registry balanceOf > 0), claimed through the Binance Agentic Wallet. Checked on-chain — no ID, no free mint.
- Paid mints: PUBLIC — no Agent ID needed, via `mintPaid(uint256)`.
- Fuse: burn 3 waves of one tier to receive 1 of the next tier (Drop Tone → Ripple Chord → Wave Harmony → Tide Boom). Deterministic, no randomness.

## How to mint (for the user's agent)

1. Confirm the user's wallet holds a .ai Agent ID:
   `balanceOf(<wallet>)` on the registry above must be > 0.
2. Confirm the contract is deployed AND mint is open: the NFT contract must
   have code, and `mintOpen()` on it must be true. If there is no code yet,
   mint is NOT open — stop and tell the user. Do not execute anything.
3. FREE mint (mint #1) — use this prompt:
   "Use my Binance Agentic Wallet on BSC (chain 56) to call mintFree() on the SonoWaves contract 0x91EdeC8F84Fda14C2D6A4b19448EFB178DFFd99b and mint my FREE SonoWaves (mint #1, Agent ID required). My wallet holds a .ai Agent ID and has not claimed its free mint yet. Mint is open. Simulate first, then execute."
4. Paid mints — `mintPaid(n)` for n = 1–10 at 0.0007 BNB each (total n × 0.0007 BNB),
   each earning 12,000 SONO. Prompt pattern:
   "Use my Binance Agentic Wallet on BSC (chain 56) to call mintPaid(n) on the SonoWaves contract 0x91EdeC8F84Fda14C2D6A4b19448EFB178DFFd99b and mint n SonoWaves for [n × 0.0007] BNB in total (public mint — no Agent ID needed). Simulate first, then execute."
   Simulate first, then execute. Never overpay beyond 0.0007 BNB per wave.
5. After the mint, report the token ID(s).

## SONO bonus token

- Name SONO, symbol SONO. Bonus only: 12,000 SONO per paid mint, max 120,000 SONO per wallet.
- SONO is earned by paid minting only — never sold separately by this project, and carries no promise of value. Total supply / pool split is not yet confirmed — do not quote any.

## Marketplace

- Fixed-price escrow market (0% platform fee, 5% creator royalty), deployed last, after mint opens.
- The marketplace is not live yet. Do not list or buy until its official link is published on the mint page.
