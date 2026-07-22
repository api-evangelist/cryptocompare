---
name: CryptoCompare spot market analysis
description: Discover markets and instruments, then pull latest tick and historical OHLCV for a spot pair on the CoinDesk Data API.
api: openapi/cryptocompare-spot-api-openapi.yml
operations: [getSpotMarketsList, getSpotInstrumentMetadata, getSpotLatestTick, getSpotHistoricalDaily, getSpotHistoricalTrades]
generated: '2026-07-22'
method: generated
---

# CryptoCompare spot market analysis

Analyze a spot trading pair end-to-end on `https://data-api.cryptocompare.com`.

## Auth

Every call requires an API key under an active subscription (the free tier was
retired 2026-05-21). Send `Authorization: Apikey {key}` (preferred) or
`api_key={key}` as a query parameter. Unauthenticated calls return HTTP 401 with
`{"Data":{},"Err":{"type":2,"message":"API key required..."}}`.

## Steps

1. **List markets** — `getSpotMarketsList` (`GET /spot/v2/markets`) to see the
   integrated venues (e.g. `coinbase`, `kraken`).
2. **Resolve the instrument** — `getSpotInstrumentMetadata`
   (`GET /spot/v1/markets/instruments`) with `market` and `instruments`
   (e.g. `BTC-USD`) to confirm mapping and status.
3. **Latest tick** — `getSpotLatestTick` (`GET /spot/v1/latest/tick`) with
   `market` + `instruments` for current price and 24h fields.
4. **History** — `getSpotHistoricalDaily` (`GET /spot/v1/historical/days`) with
   `market`, `instrument`, `limit`, and page backwards with `to_ts` set to the
   earliest `TIMESTAMP` of the prior response.
5. **Trades (optional)** — `getSpotHistoricalTrades`
   (`GET /spot/v1/historical/trades`) for tick-level detail.

## Rules

- Responses arrive in a `{"Data": ..., "Err": {}}` envelope — treat a non-empty
  `Err` as failure even on HTTP 200, and honor `Err.http_status_code`.
- All operations are read-only GETs; retry on 429 only after the per-interval
  window resets (see rate-limits/cryptocompare-rate-limits.yml).
