# CryptoCompare

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

CryptoCompare (now CoinDesk Data / CCData, acquired by CoinDesk in late 2024) is a long-standing crypto market data aggregator covering 300+ exchanges, 10,000+ assets, and 300,000+ trading pairs. The platform exposes two REST API surfaces — the legacy min-api.cryptocompare.com (Price, Historical OHLCV, Top Lists, News, Social, Order Book, Exchanges, Blockchain) and the modern data-api.cryptocompare.com / CoinDesk Data API (Spot, Index / Reference Rates including CADLI and CCIX, Asset, News, On-Chain, Futures, Options, Overview) — plus a unified WebSocket streamer at wss://streamer.cryptocompare.com/v2 that multiplexes Trade, Ticker, CCCAGG aggregate index, Order Book L2 updates and snapshots, Full Volume, Top Tier Full Volume, OHLC Candles, and Top of Book channels. Authentication uses an API key supplied as the api_key query parameter or as an `Authorization: Apikey {key}` header. Access is metered by monthly call credits with per-second / per-minute / per-hour / per-day ceilings; the Free tier issues 100,000 monthly credits and commercial Starter / Professional / Enterprise tiers escalate credit budgets, history depth, and surface coverage (news, social, on-chain, derivatives, full streamer, on-demand bulk exports, reference-rate licensing).

**Areas:** Cryptocurrency · Market Data · Reference Rates · News · Blockchain · Onchain · Order Book · Streaming · Index · Real-Time

## CryptoCompare on APIs.io

Everything profiled for CryptoCompare is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/cryptocompare/](https://apis.io/providers/cryptocompare/)** — or go straight to one of the APIs or properties below.

### APIs (18)

- [CryptoCompare Streaming WebSocket](https://apis.io/apis/cryptocompare/streamer/) — Single secure WebSocket endpoint multiplexing every subscription via tilde-delimited subscription strings (e.g. 5~CCCAGG~BTC~USD). Channel types: Trade (0),…
- [CryptoCompare Exchange Benchmark](https://apis.io/apis/cryptocompare/exchange-benchmark/) — Quantitative ranking of integrated exchanges across Legal, KYC and Transaction Risk, Team, Data Provision, Asset Quality and Diversity, Market Quality,…
- [CryptoCompare Asset API](https://apis.io/apis/cryptocompare/cryptocompare-asset-api/) — Asset metadata, overview, supply, and reference data.
- [CryptoCompare Blockchain API](https://apis.io/apis/cryptocompare/cryptocompare-blockchain-api/) — On-chain blockchain data including history and balance distribution.
- [CryptoCompare Coins API](https://apis.io/apis/cryptocompare/cryptocompare-coins-api/) — General coin listing, mapping, and reference metadata.
- [CryptoCompare Exchanges API](https://apis.io/apis/cryptocompare/cryptocompare-exchanges-api/) — Exchange metadata and exchange-pair listings.
- [CryptoCompare Futures API](https://apis.io/apis/cryptocompare/cryptocompare-futures-api/) — Futures market data across integrated derivatives venues.
- [CryptoCompare Historical API](https://apis.io/apis/cryptocompare/cryptocompare-historical-api/) — Historical OHLCV candle data by day, hour, and minute.
- [CryptoCompare Index API](https://apis.io/apis/cryptocompare/cryptocompare-index-api/) — CoinDesk Indices (CADLI, CCIX, CCIXBE) latest tick, historical values, and composition.
- [CryptoCompare News API](https://apis.io/apis/cryptocompare/cryptocompare-news-api/) — Crypto news articles, sources, categories, and search.
- [CryptoCompare On-Chain API](https://apis.io/apis/cryptocompare/cryptocompare-on-chain-api/) — On-chain blockchain metrics aggregated across chains.
- [CryptoCompare Options API](https://apis.io/apis/cryptocompare/cryptocompare-options-api/) — Options market data across integrated derivatives venues.
- [CryptoCompare Overview API](https://apis.io/apis/cryptocompare/cryptocompare-overview-api/) — Cross-cutting overview endpoints (market cap, dominance).
- [CryptoCompare Price API](https://apis.io/apis/cryptocompare/cryptocompare-price-api/) — Real-time and historical price endpoints for single and multi-symbol queries.
- [CryptoCompare Social API](https://apis.io/apis/cryptocompare/cryptocompare-social-api/) — Social statistics for coins and assets.
- [CryptoCompare Spot API](https://apis.io/apis/cryptocompare/cryptocompare-spot-api/) — Spot market data including latest tick, historical OHLCV, trades, order book L1, and instrument metadata.
- [CryptoCompare Top Lists API](https://apis.io/apis/cryptocompare/cryptocompare-top-lists-api/) — Top list endpoints by 24h volume, market cap, exchange volume, and pair volume.
- [CryptoCompare Orderbook API](https://apis.io/apis/cryptocompare/cryptocompare-orderbook-api/) — Top-of-book order book data across integrated exchanges.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (8)

Multi-step workflows that chain operations into a business task.

- [CryptoCompare Asset Research](https://apis.io/arazzos/cryptocompare/cryptocompare-asset-research-workflow/)
- [CryptoCompare Coin Price Snapshot](https://apis.io/arazzos/cryptocompare/cryptocompare-coin-price-snapshot-workflow/)
- [CryptoCompare Coin Social Pulse](https://apis.io/arazzos/cryptocompare/cryptocompare-coin-social-pulse-workflow/)
- [CryptoCompare Exchange Discovery](https://apis.io/arazzos/cryptocompare/cryptocompare-exchange-discovery-workflow/)
- [CryptoCompare Market Cap Leaders](https://apis.io/arazzos/cryptocompare/cryptocompare-market-cap-leaders-workflow/)
- [CryptoCompare News Feed Filter](https://apis.io/arazzos/cryptocompare/cryptocompare-news-feed-filter-workflow/)
- [CryptoCompare Spot Instrument Analysis](https://apis.io/arazzos/cryptocompare/cryptocompare-spot-instrument-analysis-workflow/)
- [CryptoCompare Top Volume Deep Dive](https://apis.io/arazzos/cryptocompare/cryptocompare-top-volume-deep-dive-workflow/)

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [CryptoCompare Streaming API](https://apis.io/asyncapis/cryptocompare/cryptocompare-asyncapi/)

#### Event channels (1)

Individual events and webhooks the provider emits.

- [/](https://apis.io/channels/cryptocompare/untitled/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [coindesk](https://apis.io/servers/cryptocompare/coindesk/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Cryptocompare Agentic Access](https://apis.io/agentic-access/cryptocompare/cryptocompare-agentic-access/)

#### JSON Schema (10)

The data models the API reads and writes.

- [CCData Asset](https://apis.io/schemas/cryptocompare/cryptocompare-asset/)
- [CryptoCompare Blockchain Data Point](https://apis.io/schemas/cryptocompare/cryptocompare-blockchaindatapoint/)
- [CryptoCompare Coin List Entry](https://apis.io/schemas/cryptocompare/cryptocompare-coinlistentry/)
- [CryptoCompare Exchange](https://apis.io/schemas/cryptocompare/cryptocompare-exchange/)
- [CryptoCompare Full Ticker](https://apis.io/schemas/cryptocompare/cryptocompare-fullticker/)
- [CoinDesk Index Tick (CADLI / CCIX / CCIXBE)](https://apis.io/schemas/cryptocompare/cryptocompare-indextick/)
- [CryptoCompare News Article](https://apis.io/schemas/cryptocompare/cryptocompare-newsarticle/)
- [CryptoCompare OHLCV Candle](https://apis.io/schemas/cryptocompare/cryptocompare-ohlcvcandle/)
- [CryptoCompare Order Book Top](https://apis.io/schemas/cryptocompare/cryptocompare-orderbookl1/)
- [CryptoCompare Social Stats](https://apis.io/schemas/cryptocompare/cryptocompare-socialstats/)

#### JSON Structure (1)

Data models expressed in JSON Structure.

- [Cryptocompare Structure](https://apis.io/json-structure/cryptocompare/cryptocompare-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Cryptocompare Context](https://apis.io/jsonld/cryptocompare/cryptocompare-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [CryptoCompare Domain Vocabulary](https://apis.io/vocabularies/cryptocompare/cryptocompare-vocabulary/)

#### Examples (5)

Example requests and responses.

- [Cryptocompare Gethistoricaldailyohlcv Example](https://apis.io/examples/cryptocompare/cryptocompare-getHistoricalDailyOHLCV-example/)
- [Cryptocompare Getindexlatesttick Example](https://apis.io/examples/cryptocompare/cryptocompare-getIndexLatestTick-example/)
- [Cryptocompare Getlatestnewsarticles Example](https://apis.io/examples/cryptocompare/cryptocompare-getLatestNewsArticles-example/)
- [Cryptocompare Getsinglesymbolprice Example](https://apis.io/examples/cryptocompare/cryptocompare-getSingleSymbolPrice-example/)
- [Cryptocompare Gettoplistbytotalvolumefull Example](https://apis.io/examples/cryptocompare/cryptocompare-getTopListByTotalVolumeFull-example/)

#### Collections (20)

Postman and Open Collection request collections.

- [CoinDesk Data API (CCData) Asset API](https://apis.io/collections/cryptocompare/open-cryptocompare-asset-api/)
- [CoinDesk Data API (CCData) Asset Blockchain API](https://apis.io/collections/cryptocompare/open-cryptocompare-blockchain-api/)
- [CoinDesk Data API (CCData) Asset Coins API](https://apis.io/collections/cryptocompare/open-cryptocompare-coins-api/)
- [CoinDesk Data API (CCData)](https://apis.io/collections/cryptocompare/open-cryptocompare-data-api/)
- [CoinDesk Data API (CCData) Asset Exchanges API](https://apis.io/collections/cryptocompare/open-cryptocompare-exchanges-api/)
- [CoinDesk Data API (CCData) Asset Futures API](https://apis.io/collections/cryptocompare/open-cryptocompare-futures-api/)
- [CoinDesk Data API (CCData) Asset Historical API](https://apis.io/collections/cryptocompare/open-cryptocompare-historical-api/)
- [CoinDesk Data API (CCData) Asset Index API](https://apis.io/collections/cryptocompare/open-cryptocompare-index-api/)
- [CryptoCompare min-api (Legacy)](https://apis.io/collections/cryptocompare/open-cryptocompare-min-api/)
- [CoinDesk Data API (CCData) Asset News API](https://apis.io/collections/cryptocompare/open-cryptocompare-news-api/)
- [CoinDesk Data API (CCData) Asset On-Chain API](https://apis.io/collections/cryptocompare/open-cryptocompare-on-chain-api/)
- [CoinDesk Data API (CCData) Asset Options API](https://apis.io/collections/cryptocompare/open-cryptocompare-options-api/)
- [CoinDesk Data API (CCData) Asset Order Book API](https://apis.io/collections/cryptocompare/open-cryptocompare-order-book-api/)
- [CoinDesk Data API (CCData) Asset Overview API](https://apis.io/collections/cryptocompare/open-cryptocompare-overview-api/)
- [CoinDesk Data API (CCData) Asset Price API](https://apis.io/collections/cryptocompare/open-cryptocompare-price-api/)
- [CoinDesk Data API (CCData) Asset Social API](https://apis.io/collections/cryptocompare/open-cryptocompare-social-api/)
- [CoinDesk Data API (CCData) Asset Spot API](https://apis.io/collections/cryptocompare/open-cryptocompare-spot-api/)
- [CoinDesk Data API (CCData) Asset Top Lists API](https://apis.io/collections/cryptocompare/open-cryptocompare-top-lists-api/)
- [CoinDesk Data API (CCData)](https://apis.io/collections/cryptocompare/postman-cryptocompare-data-api/)
- [CryptoCompare min-api (Legacy)](https://apis.io/collections/cryptocompare/postman-cryptocompare-min-api/)

#### Overlays (16)

OpenAPI overlays, including conversational phrasing for each operation.

- [Cryptocompare Asset Api Overlay](https://apis.io/overlays/cryptocompare/cryptocompare-asset-api-overlay/)
- [Cryptocompare Blockchain Api Overlay](https://apis.io/overlays/cryptocompare/cryptocompare-blockchain-api-overlay/)
- [Cryptocompare Coins Api Overlay](https://apis.io/overlays/cryptocompare/cryptocompare-coins-api-overlay/)
- [Cryptocompare Exchanges Api Overlay](https://apis.io/overlays/cryptocompare/cryptocompare-exchanges-api-overlay/)
- [Cryptocompare Futures Api Overlay](https://apis.io/overlays/cryptocompare/cryptocompare-futures-api-overlay/)
- [Cryptocompare Historical Api Overlay](https://apis.io/overlays/cryptocompare/cryptocompare-historical-api-overlay/)
- [Cryptocompare Index Api Overlay](https://apis.io/overlays/cryptocompare/cryptocompare-index-api-overlay/)
- [Cryptocompare News Api Overlay](https://apis.io/overlays/cryptocompare/cryptocompare-news-api-overlay/)
- [Cryptocompare On Chain Api Overlay](https://apis.io/overlays/cryptocompare/cryptocompare-on-chain-api-overlay/)
- [Cryptocompare Options Api Overlay](https://apis.io/overlays/cryptocompare/cryptocompare-options-api-overlay/)
- [Cryptocompare Order Book Api Overlay](https://apis.io/overlays/cryptocompare/cryptocompare-order-book-api-overlay/)
- [Cryptocompare Overview Api Overlay](https://apis.io/overlays/cryptocompare/cryptocompare-overview-api-overlay/)
- [Cryptocompare Price Api Overlay](https://apis.io/overlays/cryptocompare/cryptocompare-price-api-overlay/)
- [Cryptocompare Social Api Overlay](https://apis.io/overlays/cryptocompare/cryptocompare-social-api-overlay/)
- [Cryptocompare Spot Api Overlay](https://apis.io/overlays/cryptocompare/cryptocompare-spot-api-overlay/)
- [Cryptocompare Top Lists Api Overlay](https://apis.io/overlays/cryptocompare/cryptocompare-top-lists-api-overlay/)

#### Governance rules (3)

Spectral rulesets for the provider's contracts.

- [CryptoCompare — asyncapi rules](https://apis.io/rules/cryptocompare/cryptocompare-asyncapi-spectral-rules/)
- [CryptoCompare — jsonschema rules](https://apis.io/rules/cryptocompare/cryptocompare-jsonschema-spectral-rules/)
- [CryptoCompare API Rules](https://apis.io/rules/cryptocompare/cryptocompare-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Cryptocompare Authentication](https://apis.io/security/cryptocompare/cryptocompare-authentication/)
- [Cryptocompare Domain Security](https://apis.io/security/cryptocompare/cryptocompare-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Cryptocompare Plans Pricing](https://apis.io/plans/cryptocompare/cryptocompare-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Cryptocompare Rate Limits](https://apis.io/rate-limits/cryptocompare/cryptocompare-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Cryptocompare Finops](https://apis.io/finops/cryptocompare/cryptocompare-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://data.coindesk.com/)
- [Documentation](https://developers.coindesk.com/documentation/data-api/introduction)
- [Getting started](https://developers.coindesk.com/documentation/data-api/introduction)
- [API reference](https://developers.coindesk.com/documentation/)
- [Pricing](https://developers.coindesk.com/pricing/)
- [Support](https://developers.coindesk.com/support)
- [Blog](https://data.coindesk.com/blog)
- [Terms of service](https://data.coindesk.com/terms)
- [Privacy policy](https://data.coindesk.com/privacy)
- [GitHub](https://github.com/CryptoCompare)
- [Status](https://status.coindesk.com)

## API Evangelist rating

**Kin Score 41.5** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 69.1 |
| Contract governance | 31.8 |
| Operational transparency | 26.3 |
| Developer ergonomics | 25.6 |
| Access clarity | 21.1 |

**Agent readiness 56.3** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | na |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
| Idempotency | na |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | partial |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | na |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | partial |
| Operation Distinctiveness | distinct |

**Regulatory alignment 21.3** — Securities & Market Data

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/cryptocompare/](https://apis.io/providers/cryptocompare/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for CryptoCompare: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/cryptocompare/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
