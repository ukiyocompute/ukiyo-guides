# Ukiyo guides

## 1. Agents paying with x402 or MPP, no account

Buy GPU blocks at `POST https://pay.u-kiyo.ai/api/machine/gpu-blocks` or jobs at `POST https://pay.u-kiyo.ai/api/machine/gpu-jobs`. Use any standard x402 v2 exact USDC client on Base, or an MPP client for Solana USDC or Tempo USDC.e. No signup or API key is required.

Read [pricing](https://pay.u-kiyo.ai/api/pricing), send the purchase details, current legal acceptance and a P-256 recovery public key, then retry the same URL and body with the standard payment header. Save the returned access token and retain the recovery private key. Read the [complete payment, recovery and Bazaar guide](https://docs.u-kiyo.ai/connect/machine-payments) before paying.

Cloudflare operators: raise the default $0.10 payment cap to cover the approved quote ($5 minimum); `maxPaymentValue: 5_000_000n` covers $5 USDC. Keep a cumulative budget. Live ghost/stall fallback replaces failed provider instances within the purchased specifications and budget, confirms destruction before replacement, and issues exactly-once service credit if provisioning fails. Anonymous cards and inference are unavailable.

## 2. Agents and developers using the API with an account

The existing API-key/account-balance flow is unchanged: CLI `ukiyo` 0.2.5, local MCP `ukiyo-mcp` 0.2.0 and pinned Skill `ukiyo-compute` 1.0.1. These are existing release downloads, not new npm releases. The account instructions below apply to this path. Skill 1.0.1's immutable artifact references CLI 0.2.2; keep the separately installed CLI 0.2.5. See the full guide for artifact links and checksums.


Step-by-step guides for getting real work done on Ukiyo GPUs: training, inference, notebooks and more. Each guide lives in its own folder with a README and any code it needs.

New guides are added here as they're published. For product documentation, see [docs.u-kiyo.ai](https://docs.u-kiyo.ai).

## Guides

_Coming soon._

<!-- Add one line per guide, newest first:
- [Guide title](folder-name/): one-sentence summary.
-->

## Guide layout

```text
folder-name/
  README.md      the guide: what you'll build, cost estimate, steps
  ...            scripts or config the guide uses
```

## Get started

- [Ukiyo CLI](https://github.com/ukiyocompute/ukiyo-cli): rent a GPU from your terminal
- [Ukiyo MCP server](https://github.com/ukiyocompute/ukiyo-mcp) · [Agent skill](https://github.com/ukiyocompute/ukiyo-skill) · [API](https://github.com/ukiyocompute/ukiyo-api)
- [Live GPU prices](https://u-kiyo.ai/gpu/)

## License

[MIT](LICENSE) © 2026 Ukiyo Compute LLC.
