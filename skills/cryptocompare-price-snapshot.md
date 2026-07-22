---
name: Legacy price snapshot
description: Fetch single- and multi-symbol spot prices and full tickers from the legacy min-api for dashboards and tickers.
api: openapi/cryptocompare-price-api-openapi.yml
operations: [getSingleSymbolPrice, getMultipleSymbolsPrice, getMultipleSymbolsFullPrice, getPriceHistorical]
generated: '2026-07-22'
method: generated
---

# Legacy price snapshot

Quick price reads on `https://min-api.cryptocompare.com/data` (legacy surface —
see lifecycle/cryptocompare-lifecycle.yml for the migration posture).

## Auth

`Authorization: Apikey {key}` header or `api_key` query parameter; since
2026-05-21 an active subscription is required (401 `Err.type: 2` otherwise).

## Steps

1. **Single pair** — `getSingleSymbolPrice` (`GET /price`) with `fsym=BTC`,
   `tsyms=USD,EUR` for a minimal price map.
2. **Watchlist** — `getMultipleSymbolsPrice` (`GET /pricemulti`) with
   `fsyms=BTC,ETH` for a symbol matrix.
3. **Full tickers** — `getMultipleSymbolsFullPrice` (`GET /pricemultifull`) for
   24h volume, change, and supply fields (RAW + DISPLAY blocks).
4. **Point-in-time** — `getPriceHistorical` (`GET /pricehistorical`) with `ts`
   for a historical valuation timestamp.

## Rules

- Prices default to the CCCAGG cross-exchange aggregate; pass `e={exchange}` to
  pin a single venue.
- Prefer the data-api Spot/Index endpoints for new builds; this surface is
  documented under the portal's legacy section.
- Check quota with `GET /stats/rate/limit` when polling aggressively.
