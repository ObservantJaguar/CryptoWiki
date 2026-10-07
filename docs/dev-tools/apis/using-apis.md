---
layout: default
title: Using APIs in practice
parent: Node APIs and indexers
grand_parent: Tools
---

# Using APIs in practice

Practical patterns for production data access: how to structure queries, handle rate limits, and choose between hosted APIs, indexers, and your own node.

## Choosing a data source

| Need | Recommended |
|---|---|
| Raw `eth_*`/chain data, quick prototyping | Hosted node API (or local node) |
| Rich, typed, queryable domain data | The Graph subgraph |
| Maximum trustlessness, compliance | Your own full node |
| Historical/archive data at scale | Archive provider or Erigon archive node |

## Common pitfalls

- **Rate limits** — hosted providers cap requests; add caching and backoff.
- **Single point of failure** — use provider failover (multiple RPC URLs) in production.
- **Websocket disconnects** — handle reconnection logic for subscriptions.
- **Data freshness** — wait for finality (`safe`/`finalized`) before reacting; avoid relying on `latest` for irreversible actions.
- **Indexer lag** — subgraphs index asynchronously; check sync status before trusting query results.

## Best practices

- **Cache** historical data locally to reduce redundant RPC calls.
- **Batch** requests where the API supports it (e.g. `eth_getLogs` ranges, multicall).
- **Monitor** error rates and latency; alert on anomalies.
- **Provide graceful degradation** when a provider is down.

## See also

- [RPC transactions]({{ 'guides/rpc-transaction' | relative_url }}) — calling your own node.
- [Node software]({{ 'nodes' | relative_url }}) — running infrastructure yourself.
- [Providing APIs]({{ 'dev-tools/apis/thegraph' | relative_url }}) and [Hosted APIs]({{ 'dev-tools/apis/hosted-apis' | relative_url }}).