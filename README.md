# CryptoCompare (cryptocompare)

CryptoCompare (now CoinDesk Data / CCData) is a long-standing crypto market data aggregator covering 300+ exchanges, 10,000+ assets, and 300,000+ trading pairs. The platform exposes two REST API surfaces — the legacy `min-api.cryptocompare.com` and the modern `data-api.cryptocompare.com` (CoinDesk Data API) — plus a unified WebSocket streamer at `wss://streamer.cryptocompare.com/v2`.

**APIs.yml:** [apis.yml](apis.yml)

## Type
- **x-type:** company
- **x-tier:** 3 (bulk-registered from public-apis; enriched 2026-05-30)
- **source:** [public-apis/public-apis](https://github.com/public-apis/public-apis) — category: Cryptocurrency

## APIs
- **CryptoCompare min-api (Legacy)** — `https://min-api.cryptocompare.com/data` — [Documentation](https://developers.coindesk.com/documentation/legacy/Price/SingleSymbolPriceEndpoint)
- **CoinDesk Data API (CCData)** — `https://data-api.cryptocompare.com` — [Documentation](https://developers.coindesk.com/documentation/data-api/introduction)
- **CryptoCompare Streaming WebSocket** — `wss://streamer.cryptocompare.com/v2` — [Documentation](https://developers.coindesk.com/documentation/legacy-websockets/HowToConnect)
- **CryptoCompare Exchange Benchmark** — methodology / ranking — [Documentation](https://data.coindesk.com/research/exchange-benchmark)

## Tags
Cryptocurrency, Market Data, Reference Rates, News, Social, Blockchain, On-Chain, Order Book, Streaming, Index

## Artifacts

| Type | Location | Count |
|---|---|---|
| OpenAPI | [`openapi/`](openapi/) | 2 |
| AsyncAPI | [`asyncapi/`](asyncapi/) | 1 |
| JSON Schema | [`json-schema/`](json-schema/) | 10 |
| JSON Structure | [`json-structure/`](json-structure/) | 1 |
| JSON-LD | [`json-ld/`](json-ld/) | 1 |
| Examples | [`examples/`](examples/) | 5 |
| Spectral Rules | [`rules/`](rules/) | 1 |
| Vocabulary | [`vocabulary/`](vocabulary/) | 1 |
| Naftiko Capabilities | [`capabilities/`](capabilities/) | 10 |
| Plans | [`plans/`](plans/) | 1 |
| Rate Limits | [`rate-limits/`](rate-limits/) | 1 |
| FinOps | [`finops/`](finops/) | 1 |

## Authentication

CryptoCompare authenticates with a single personal API key supplied either as the `api_key` query parameter or as `Authorization: Apikey {key}`. Create / manage keys at <https://www.cryptocompare.com/cryptopian/api-keys>.

## Pricing & Rate Limits

Access is metered by monthly call credits with per-second / per-minute / per-hour / per-day ceilings.

- **Free** — 100,000 monthly credits; 30 req/s, 60 req/min, 1,200 req/hr, 10,000 req/day, 20,000 req/month; 7 days of minute history; application attribution required.
- **Commercial Starter** — 5M monthly credits; news, social, order book L1, 30 days of minute history.
- **Commercial Professional** — 25M monthly credits; full minute history (1 year), on-chain blockchain data, CoinDesk Data API (Spot, Index, Asset, News).
- **Enterprise** — Custom credits, raw trade tick history, futures and options, on-demand bulk exports, AI / ML feeds, SLA support; reference-rate licensing (CADLI, CCIX) available.

See [`plans/cryptocompare-plans-pricing.yml`](plans/cryptocompare-plans-pricing.yml), [`rate-limits/cryptocompare-rate-limits.yml`](rate-limits/cryptocompare-rate-limits.yml), and [`finops/cryptocompare-finops.yml`](finops/cryptocompare-finops.yml) for the full API Commons Plans / Rate Limits and FOCUS-aligned FinOps view.

## Streaming

A single secure WebSocket multiplexes every channel via tilde-delimited subscription strings (e.g. `5~CCCAGG~BTC~USD`):

- `0` Trade
- `2` Ticker
- `5` Aggregate Index / CCCAGG
- `8` Order Book L2 update
- `9` Order Book L2 snapshot
- `11` Full Volume
- `21` Top Tier Full Volume
- `24` OHLC Candles
- `30` Top of Order Book

Control envelopes: Welcome (20), SubscribeComplete (16), UnsubscribeComplete (17), LoadComplete (3), UnsubscribeAllComplete (18), Heartbeat (999), Unauthorized (401), RateLimit (429), ServerError (500). See [`asyncapi/cryptocompare-asyncapi.yml`](asyncapi/cryptocompare-asyncapi.yml).

## GitHub

- **Organization:** <https://github.com/CryptoCompare> (2 public repos)
  - [CryptoCompare/API](https://github.com/CryptoCompare/API) — Python wrapper
  - [CryptoCompare/CryptoCompareIOS](https://github.com/CryptoCompare/CryptoCompareIOS) — Swift / iOS wrapper
- **Research / Examples:** [CryptoCompareLTD/research](https://github.com/CryptoCompareLTD/research)

A large community of unofficial wrappers exists across Python, JavaScript, .NET, Java, Ruby, Go, Elixir, Haskell, R, PHP, and TradingView/React integrations.

## MCP & Claude Code Skills

No official or community Model Context Protocol server or Claude Code skill has been published for CryptoCompare / CoinDesk Data as of 2026-05-30. Generated Naftiko capabilities in [`capabilities/`](capabilities/) can be used as MCP-equivalent capability definitions.

## Timestamps
- **Created:** 2026-05-28
- **Modified:** 2026-05-30

## Maintainers
- **Kin Lane** — kin@apievangelist.com
