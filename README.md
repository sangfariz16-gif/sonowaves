# SonoWaves — LIVE on BNB Smart Chain (Chain ID 56)

MINT IS LIVE. Mint opened 11:18 UTC, 10 Nov 2026.

- Supply 6,666 (free 2,260 for Agent ID holders + paid 4,406 @ 0.0007 BNB flat), max 11/wallet, fuse 3→1
- Tiers: Drop Tone / Ripple Chord / Wave Harmony / Tide Boom
- Bonus token SONO: 12,000 per paid mint, max 120,000/wallet (free mints earn none)
- Mint via Binance Agentic Wallet + Agent ID (free lane Agent ID-only; paid lane public)
- Marketplace: own escrow (0% platform fee, 5% creator royalty) + Element Market entry (third-party BNB marketplace; collection searchable there by NFT contract address)
- Official X: @Sonofluidic — https://x.com/Sonofluidic
- Live page: https://sonowaves.vercel.app/

## Contracts (DEPLOYED — BSC mainnet, 2026-11-10 11:18:59 WIB)

- SONO token: 0x0D7f8dCEaDaC713F02AFCa86850F17f1f37f65BE (1B total: 540M bonus pool / 460M treasury)
- NFT: 0x8D8d7A02f7d02C6FbADc33e5Efd7cCaC7a2C8a6b (price 0.0007 BNB, mintOpen=true)
- Marketplace: 0xA9C1E5d2bDBac57C650CBE93a5B85350042cc9ba
- Owner: 0x36F3D56eAD5D1D6C2434F94DeFcEF732C5C3CbD2

Single-file site: `index.html` with the 4 tier artworks downscaled to 1024px
webp q78 and inlined as data URIs (the GitHub connector cannot push binary
files, so the images live inside the HTML instead of `assets/`). Deploy this
repo as a static site on Vercel. `assets/agent-skill.md` is the agent mint
prompt (free mintFree / paid mintPaid(n) + Agent ID checker).

Metadata: 6,666 files live at /metadata/ (repo `metadata/` folder,
extensionless files).

Migrated from Elysium (Chain ID 99901, HYPE) to BNB Smart Chain (Chain ID 56,
BNB) on 2026-11-10. The earlier Elysium draft lives in git history; Elysium
contracts were never deployed.
