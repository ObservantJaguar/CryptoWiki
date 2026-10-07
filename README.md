# CoreStratum Crypto Wiki

A self-hosted, GitHub Pages–based technical reference wiki on cryptocurrencies, blockchains, and decentralized finance. Built with **Jekyll + Just the Docs**.

## Structure

The wiki is organized into three classes:

- **Theory** — concepts and mathematics (blockchain fundamentals, consensus, cryptography, wallets/keys, history, regulation).
- **Tools** — an encyclopedia of node software, wallets, explorers, DeFi instruments, and developer tooling.
- **Practice** — hand-on guides for running nodes, managing keys, RPC transactions, smart contracts, validators, and security.

## Layout

```
docs/                 <- GitHub Pages source
├── _config.yml       <- Pages config (remote_theme)
├── _config_local.yml <- local build config (theme)
├── index.md          <- home
├── sections/         <- Theory / Tools / Practice
├── theory/           <- fundamentals, consensus, cryptography, wallets-keys, history, regulation
├── nodes/            <- bitcoin, ethereum, alt-nodes
├── wallets/          <- hardware, software, custody
├── explorers/        <- block-explorers, on-chain-analytics
├── defi/             <- dex, aggregation, stablecoins
├── dev-tools/        <- frameworks, libraries, apis
├── staking-mining/   <- staking, mining
└── guides/           <- practical walkthroughs
```

## Local development

```bash
bundle install        # in docs/
bundle exec jekyll serve --source docs --destination docs/_site \
  --config docs/_config.yml,docs/_config_local.yml
```

Then open `http://127.0.0.1:4000/CryptoWiki/`.

## Publishing

GitHub Pages is set to build from branch `main`, folder `/docs`. Push to `main` and Pages rebuilds automatically.

## Content notes

- Technical reference only — **not** financial/investment advice.
- Official links only; proprietary products are labeled as such.
- Plain ASCII diagrams (no box-drawing characters) to keep files UTF-8 safe.