# Liam Tools — pay-per-call AI utilities (x402)

Public API: https://liam-tools-x402-lab.evangrant69420.workers.dev

## Services

- `POST /v1/numbers` — number-processing API; the gold-402 maintainer independently tested its HTTP 402 payment challenge and reported a 0.01 XRP XRPL mainnet quote.
- `POST /v1/text` — text utility.
- `POST /v1/normalize` — data normalization utility.
- `POST /v1/budget-lens` — budget analysis utility.

**Important:** Clients should inspect each endpoint's live HTTP 402 payment challenge and advertised network, recipient, and token. Do not assume every endpoint accepts the same currency or price. For operational use, payment must be verified and the service response checked after settlement. Never send money based only on a third-party listing.

### Discovery

- [Accepted gold-402 integration, PR #317](https://github.com/Haustorium12/gold-402/pull/317)
- [Liam Tools OpenAPI specification](https://liam-tools-x402-lab.evangrant69420.workers.dev/openapi.json)

### Minimal discovery probe

```bash
curl -i -X POST 'https://liam-tools-x402-lab.evangrant69420.workers.dev/v1/numbers' -H 'content-type: application/json' -d '{}'
```

An HTTP 402 reply is **not** proof that a buyer paid. No external customer sales are claimed by this document.

### Merchant integrations

Merchant Connect offers additional settlement/fulfillment plumbing as a separate service. Do not confuse Merchant Connect acceptance-test payments with independent customer revenue.

### Contact and integration requests

Open a GitHub issue in this repository describing the workflow, target chain, and requested API capability. Do not post private credentials or payment secrets in issues.
