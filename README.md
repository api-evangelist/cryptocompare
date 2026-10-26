# CryptoCompare (cryptocompare)

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

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/cryptocompare/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/cryptocompare/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Cryptocurrency
- Market Data
- Reference Rates
- News
- Social
- Blockchain
- On-Chain
- Order Book
- Streaming
- Index

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-30

## APIs

### CryptoCompare min-api (Legacy)

Legacy CryptoCompare REST API. Single endpoint surface for current and historical Price, OHLCV (minute / hour / day) candles, Top Lists by 24h volume / market cap / pair volume / exchange volume, News articles with sources and categories, Social statistics, top-of-book Order Book L1, Exchanges reference data and full coin listing, and Blockchain on-chain data including transaction count, active addresses, hashrate, difficulty, and balance distribution.

- **Human URL:** [https://developers.coindesk.com/documentation/legacy/Price/SingleSymbolPriceEndpoint](https://developers.coindesk.com/documentation/legacy/Price/SingleSymbolPriceEndpoint)
- **Base URL:** `https://min-api.cryptocompare.com/data`

#### Tags

- Cryptocurrency
- Market Data
- News
- Social
- Blockchain

#### Properties

- [Documentation](https://developers.coindesk.com/documentation/legacy/Price/SingleSymbolPriceEndpoint)
- [OpenAPI](openapi/cryptocompare-min-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cryptocompare-min-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cryptocompare-min-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/cryptocompare-fullticker-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/cryptocompare-ohlcvcandle-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/cryptocompare-newsarticle-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/cryptocompare-coinlistentry-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/cryptocompare-exchange-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/cryptocompare-blockchaindatapoint-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/cryptocompare-socialstats-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/cryptocompare-orderbookl1-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](examples/cryptocompare-getSingleSymbolPrice-example.json)
- [Example](examples/cryptocompare-getHistoricalDailyOHLCV-example.json)
- [Example](examples/cryptocompare-getTopListByTotalVolumeFull-example.json)
- [Example](examples/cryptocompare-getLatestNewsArticles-example.json)
- [Sign Up](https://www.cryptocompare.com/cryptopian/api-keys)
- [Authentication](https://min-api.cryptocompare.com/documentation)

### CoinDesk Data API (CCData)

Modern, institutional-grade replacement for the legacy min-api. Consolidated surface across Spot (latest tick, instrument metadata, historical OHLCV, trades, order book L1), CoinDesk Indices and Reference Rates (CADLI, CCIX, CCIXBE) with composition endpoint, Asset metadata and supply history, News articles with full search, On-Chain metrics, Futures, Options, and Overview market cap. Standardized request and response envelope across every endpoint.

- **Human URL:** [https://developers.coindesk.com/documentation/data-api/introduction](https://developers.coindesk.com/documentation/data-api/introduction)
- **Base URL:** `https://data-api.cryptocompare.com`

#### Tags

- Cryptocurrency
- Market Data
- Reference Rates
- Index
- Spot
- Derivatives
- On-Chain
- News

#### Properties

- [Documentation](https://developers.coindesk.com/documentation/data-api/introduction)
- [OpenAPI](openapi/cryptocompare-data-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cryptocompare-data-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cryptocompare-data-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/cryptocompare-indextick-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/cryptocompare-asset-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](examples/cryptocompare-getIndexLatestTick-example.json)
- [Sign Up](https://developers.coindesk.com/pricing/)
- [Authentication](https://developers.coindesk.com/documentation/data-api/introduction)

### CryptoCompare Streaming WebSocket

Single secure WebSocket endpoint multiplexing every subscription via tilde-delimited subscription strings (e.g. 5~CCCAGG~BTC~USD). Channel types: Trade (0), Ticker (2), Aggregate Index / CCCAGG (5), Order Book L2 update (8), Order Book L2 snapshot (9), Full Volume (11), Top Tier Full Volume (21), OHLC Candles (24), and Top of Order Book (30). Control envelopes include Welcome (20), SubscribeComplete (16), UnsubscribeComplete (17), LoadComplete (3), UnsubscribeAllComplete (18), Heartbeat (999), Unauthorized (401), RateLimit (429), and ServerError (500).

- **Human URL:** [https://developers.coindesk.com/documentation/legacy-websockets/HowToConnect](https://developers.coindesk.com/documentation/legacy-websockets/HowToConnect)
- **Base URL:** `wss://streamer.cryptocompare.com/v2`

#### Tags

- Cryptocurrency
- Streaming
- WebSocket
- Order Book
- OHLCV

#### Properties

- [Documentation](https://developers.coindesk.com/documentation/legacy-websockets/HowToConnect)
- [Web Socket](wss://streamer.cryptocompare.com/v2)
- [AsyncAPI](asyncapi/cryptocompare-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/cryptocompare-data-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cryptocompare-data-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cryptocompare-min-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cryptocompare-min-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### CryptoCompare Exchange Benchmark

Quantitative ranking of integrated exchanges across Legal, KYC and Transaction Risk, Team, Data Provision, Asset Quality and Diversity, Market Quality, Security, and Negative Reports Penalty. Grade points and per-criterion splits are surfaced on the /exchanges/general endpoint of the min-api.

- **Human URL:** [https://data.coindesk.com/research/exchange-benchmark](https://data.coindesk.com/research/exchange-benchmark)
- **Base URL:** `https://data.coindesk.com/research/exchange-benchmark`

#### Tags

- Exchange Ratings
- Methodology
- Risk

#### Properties

- [Documentation](https://data.coindesk.com/research/exchange-benchmark)
- [Postman Collection](collections/cryptocompare-data-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cryptocompare-data-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cryptocompare-min-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cryptocompare-min-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Website](https://data.coindesk.com/)
- [Portal](https://developers.coindesk.com/)
- [Sign Up](https://www.cryptocompare.com/cryptopian/api-keys)
- [Pricing](https://developers.coindesk.com/pricing/)
- [Terms of Service](https://data.coindesk.com/terms)
- [Privacy Policy](https://data.coindesk.com/privacy)
- [Support](https://developers.coindesk.com/support)
- [Blog](https://data.coindesk.com/blog)
- [GitHub Organization](https://github.com/CryptoCompare)
- [SDK](https://github.com/CryptoCompare/API)
- [SDK](https://github.com/CryptoCompare/CryptoCompareIOS)
- [Public APIs Listing](https://github.com/public-apis/public-apis)
- [Spectral Rules](rules/cryptocompare-rules.yml)
- [Vocabulary](vocabulary/cryptocompare-vocabulary.yml)
- [J S O N- L D](json-ld/cryptocompare-context.jsonld)
- [JSON Structure](json-structure/cryptocompare-structure.json)
- [Plans](plans/cryptocompare-plans-pricing.yml)
- [Rate Limits](rate-limits/cryptocompare-rate-limits.yml)
- [Fin Ops](finops/cryptocompare-finops.yml)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Solutions](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
