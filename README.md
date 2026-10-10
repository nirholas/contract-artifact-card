# Contract Artifact Card

<!-- three.ws:badges -->
[![GitHub stars](https://img.shields.io/github/stars/nirholas/contract-artifact-card?style=flat&logo=github)](https://github.com/nirholas/contract-artifact-card/stargazers) [![Last commit](https://img.shields.io/github/last-commit/nirholas/contract-artifact-card?style=flat)](https://github.com/nirholas/contract-artifact-card/commits) [![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat)](https://github.com/nirholas/contract-artifact-card/pulls) [![AI agent friendly](https://img.shields.io/badge/AI%20agents-AGENTS.md%20%2B%20llms.txt-6d5dfc?style=flat)](https://github.com/nirholas/contract-artifact-card/blob/HEAD/AGENTS.md)
<!-- /three.ws:badges -->


Generate a clean, shareable contract deployment and permissions card.

## Why this exists

Solana transaction v1 raises the maximum transaction size from 1,232 to 4,096 bytes. Contract Artifact Card explores a focused consumer use of that space while making the wire budget visible.

## Working features

- Responsive monochrome product UI with deterministic payload generation
- Live UTF-8 byte meter, v1 fit estimate, and legacy transaction comparison
- Wallet Standard discovery and v1 capability reporting, plus EIP-1193 wallet connection
- Copy and download flows with no server, account, analytics, or custody
- Dependency-free production build and Cloudflare Workers static configuration
- Product contract test, security headers, security policy, and architecture docs

## Status

This is a functional product prototype, not an audited transaction broadcaster. It intentionally stops at payload generation so users cannot mistake experimental sizing logic for a reviewed signing flow. Integrate the generated artifact with [First](https://github.com/nirholas/first-onchain) or a reviewed `@solana/kit >= 8` v1 sender.

## Run

```bash
npm test
npm run build
npm run dev
```

Open http://localhost:4173. To deploy after authenticating Wrangler, run `npm run deploy`.

## Transaction v1 rules

- Use transaction version 1 to access the 4,096-byte ceiling.
- Set compute-unit and loaded-accounts-data-size limits explicitly; v1 defaults both to zero.
- Check `supportedTransactionVersions.has(1)` before asking a wallet to sign.
- Readers must set `maxSupportedTransactionVersion: 1`.
- Read sponsor and indexer limits from `transactionConfig`, not Compute Budget instructions.
- V1 supports 64 inline addresses, rejects duplicates, and does not use address lookup tables.

See [docs/PRODUCT.md](docs/PRODUCT.md) for product boundaries and extension points.

## License

MIT

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=nirholas/contract-artifact-card&type=Date)](https://www.star-history.com/#nirholas/contract-artifact-card&Date)

<!-- three.ws:growth -->
## Support the project

If contract-artifact-card saves you time, **[star it on GitHub](https://github.com/nirholas/contract-artifact-card)**. Stars are how other developers and AI agents find the repositories worth trusting, and they cost you one click.

Know someone who would use it? [Post on X](https://twitter.com/intent/tweet?text=contract-artifact-card%3A%20Generate%20a%20clean%2C%20shareable%20contract%20deployment%20and%20permissions%20card&url=https%3A%2F%2Fgithub.com%2Fnirholas%2Fcontract-artifact-card) · [Share on Bluesky](https://bsky.app/intent/compose?text=contract-artifact-card%3A%20Generate%20a%20clean%2C%20shareable%20contract%20deployment%20and%20permissions%20card%20https%3A%2F%2Fgithub.com%2Fnirholas%2Fcontract-artifact-card) · [Share on LinkedIn](https://www.linkedin.com/sharing/share-offsite/?url=https%3A%2F%2Fgithub.com%2Fnirholas%2Fcontract-artifact-card) · [Submit to Hacker News](https://news.ycombinator.com/submitlink?u=https%3A%2F%2Fgithub.com%2Fnirholas%2Fcontract-artifact-card&t=contract-artifact-card%3A%20Generate%20a%20clean%2C%20shareable%20contract%20deployment%20and%20permissions%20card) · [Share on Reddit](https://www.reddit.com/submit?url=https%3A%2F%2Fgithub.com%2Fnirholas%2Fcontract-artifact-card&title=contract-artifact-card%3A%20Generate%20a%20clean%2C%20shareable%20contract%20deployment%20and%20permissions%20card)

## Built for AI agents too

Coding agents and LLM tooling can read this repo directly: [AGENTS.md](./AGENTS.md), [llms.txt](./llms.txt), [llms-full.txt](./llms-full.txt). Point an agent at `https://github.com/nirholas/contract-artifact-card` and it has the context it needs.

## More from the same author

- [All repositories by nirholas](https://github.com/nirholas/nirholas#readme): the full catalog, grouped by topic
- [three.ws](https://three.ws): the platform for 3D AI agents with Solana wallets, a skill marketplace and x402 payments
- Questions or ideas: [open an issue](https://github.com/nirholas/contract-artifact-card/issues) or [start a discussion](https://github.com/nirholas/contract-artifact-card/discussions)

## Contributors

[![Contributors](https://contrib.rocks/image?repo=nirholas/contract-artifact-card)](https://github.com/nirholas/contract-artifact-card/graphs/contributors)

<!-- /three.ws:growth -->
