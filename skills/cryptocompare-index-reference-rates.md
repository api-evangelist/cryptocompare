---
name: CoinDesk index reference rates
description: Read CADLI/CCIX reference-rate ticks, historical values, and index composition for mark-to-market and settlement.
api: openapi/cryptocompare-index-api-openapi.yml
operations: [getIndexLatestTick, getIndexHistoricalDaily, getIndexHistoricalHourly, getIndexHistoricalMinute, getIndexComposition]
generated: '2026-07-22'
method: generated
---

# CoinDesk index reference rates

Value digital-asset positions against the CoinDesk index family (CADLI, CCIX,
CCCAGG) on `https://data-api.cryptocompare.com`.

## Auth

`Authorization: Apikey {key}` header or `api_key` query parameter; active
subscription required.

## Steps

1. **Latest reference rate** — `getIndexLatestTick`
   (`GET /index/cc/v1/latest/tick`) with `market` set to the index family
   (e.g. `cadli`) and `instruments` (e.g. `BTC-USD`).
2. **Historical marks** — `getIndexHistoricalDaily`
   (`GET /index/cc/v1/historical/days`) for end-of-day marks; drop to
   `getIndexHistoricalHourly` / `getIndexHistoricalMinute` for intraday
   valuation points. Page backwards with `limit` + `to_ts`.
3. **Composition** — `getIndexComposition`
   (`GET /index/cc/v1/latest/instrument/composition`) to audit constituent
   exchanges/weights behind a rate before using it for settlement.

## Rules

- Pick the index deliberately: CADLI is the regulated CoinDesk reference rate
  family; CCCAGG is the legacy cross-exchange aggregate.
- Check `Err` in the envelope on every response; 401 means the key/subscription
  lapsed (free tier retired 2026-05-21).
