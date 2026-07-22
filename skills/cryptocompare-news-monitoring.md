---
name: Crypto news monitoring
description: Build a filtered, sentiment-tagged crypto news feed from the CoinDesk Data news endpoints.
api: openapi/cryptocompare-news-api-openapi.yml
operations: [getNewsSourceList, getNewsCategoryList, getNewsArticleList, getLatestNewsArticles]
generated: '2026-07-22'
method: generated
---

# Crypto news monitoring

Aggregate sentiment-tagged crypto news on `https://data-api.cryptocompare.com`
(modern) or the legacy `https://min-api.cryptocompare.com/data` surface.

## Auth

`Authorization: Apikey {key}` header or `api_key` query parameter; active
subscription required.

## Steps

1. **Discover sources** — `getNewsSourceList` (`GET /news/v1/source/list`) to
   enumerate feeds and their language/launch metadata.
2. **Discover categories** — `getNewsCategoryList` (`GET /news/v1/category/list`)
   to get the category taxonomy (asset symbols and topics).
3. **Pull articles** — `getNewsArticleList` (`GET /news/v1/article/list`) with
   `lang`, category filters, and `limit`; page backwards with `to_ts`.
   Articles carry POSITIVE / NEUTRAL / NEGATIVE sentiment.
4. **Legacy fallback** — `getLatestNewsArticles` (`GET /v2/news/`) returns the
   same aggregation on the legacy min-api surface.

## Rules

- Deduplicate by article `ID`/`GUID` when polling; poll interval should respect
  the account's per-minute credit ceiling.
- Non-empty `Err` in the envelope is a failure even on HTTP 200.
