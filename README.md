# SonoWaves — preview site (BNB Smart Chain, Chain ID 56)

Preview only — mint is disabled, no contracts are deployed.

- Supply 6,666 (free 2,260 for Agent ID holders + paid 4,406 @ 0.0007 BNB flat), max 11/wallet, fuse 3→1
- Tiers: Drop Tone / Ripple Chord / Wave Harmony / Tide Boom
- Bonus token SONO: 12,000 per paid mint, max 120,000/wallet (free mints earn none)
- Mint via Binance Agentic Wallet + Agent ID (free lane Agent ID-only; paid lane public)
- Marketplace: placeholder section only — no contract, no listings yet. Also listed: Element Market entry (third-party BNB marketplace; collection appears there automatically after deploy, link activates after deploy, no extra contract cost)
- Official X: @Sonofluidic — https://x.com/Sonofluidic

Single-file site: `index.html` with the 4 tier artworks inlined as data URIs
(the GitHub connector cannot push binary files, so the images live inside the
HTML instead of `assets/`). Deploy this repo as a static site on Vercel.

Migrated from Elysium (Chain ID 99901, HYPE) to BNB Smart Chain (Chain ID 56,
BNB) on 2026-11-10. Previous Elysium preview lives in git history (commit
90dafbc); Elysium contracts were never deployed.

Step 2 (2026-11-10): metadata 6,666 files live at /metadata/ (repo `metadata/` folder, extensionless, like PanduAGENT). Predicted addresses updated to the Step-1 values: SONO 0x0D7f8dCEaDaC713F02AFCa86850F17f1f37f65BE, NFT 0x8D8d7A02f7d02C6FbADc33e5Efd7cCaC7a2C8a6b, Marketplace 0xA9C1E5d2bDBac57C650CBE93a5B85350042cc9ba (NOT deployed). Contracts are FROZEN — no more source edits.
