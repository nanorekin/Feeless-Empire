# Feeless Empire

A free, single-file idle/incremental game. Build a block-processing empire, watch it tick up on its own, and keep earning even while the tab (or your browser) is closed.

## Play

- **Tap** the pickaxe to process transactions by hand, or spend blocks on **generators** that process them automatically, every second, forever. Each generator gets a little pricier the more you own, so spreading out beats stacking just one kind.
- **Offline progress:** your empire keeps producing at its last known rate while you're away, and credits it back the moment you return (capped at a few hours by default — stretchable with Research). There's no penalty for closing the tab.
- **Fork the chain:** once you've built up a solid lifetime total, reset your blocks and generators back to zero in exchange for permanent **Genesis Shards** — each one worth +2% production, forever, through every future fork.
- **Research:** spend Genesis Shards on permanent upgrades (global production, click power, a longer offline cap, a head start after each fork) that stick around no matter how many times you fork.
- **Get more shards:** forking is always enough on its own — nothing here is paywalled. Tipping XNO (same tip card as every other Feeless game) is an optional way to speed that up or say thanks; it has no effect on production rates or odds.
- A **"How to play"** section on the page explains the loop in plain language.

## Numbers

Big numbers are formatted with standard suffixes (K, M, B, T, Qa, Qi, Sx, Sp, Oc, No, Dc, Ud, Dd). Progress — blocks, generator counts, shards, research levels, and the offline timestamp — is stored in `localStorage`, so it's local to one browser, same as every other game's supporter unlock.

## Deploy on GitHub Pages

1. Create a new repository, for example `feeless-empire`.
2. Upload `index.html` and `README.md` to the root of the repository.
3. Open **Settings > Pages**, set the source to **Deploy from a branch**, choose `main` and `/ (root)`, then save.
4. After a minute the game is live at `https://<your-username>.github.io/feeless-empire/`.
5. Add it to the Feeless Arcade hub's `GAMES` list once it's live.

## Donations

The tip card works the same way as the other Feeless games:

- A `nano:` payment link with the chosen amount, shown as a QR code and an **Open in wallet** button.
- A **Copy address** button.
- An **I've sent it, check** button that asks public Nano nodes whether a matching payment arrived, then credits Genesis Shards (currently 15 shards per 1 XNO tipped).

To use a different wallet, change `NANO_ADDRESS` near the top of the script in `index.html`. The shard-per-XNO rate is the `SHARDS_PER_XNO` constant right below it. If the public RPC endpoints in `RPCS` ever block browser requests, point them at your own proxy.

Add `?selftest` to the URL to expose a `window.__fe` object for automated tests.
