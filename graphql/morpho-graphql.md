# Morpho GraphQL API

The Morpho GraphQL API is the primary offchain data interface for the Morpho DeFi credit protocol. It exposes comprehensive real-time and historical data covering Morpho Blue lending markets, MetaMorpho vaults (V1 and V2), user positions, collateral, liquidations, rewards, oracle configurations, public allocator state, and curators across Ethereum, Base, Arbitrum, and all other supported EVM chains. The schema includes 299 types spanning markets, vaults, positions, transactions, and analytics time-series.

**Endpoint:** https://api.morpho.org/graphql

**Authentication:** None required. The API is publicly accessible without API keys or authentication headers.

**Documentation:** https://docs.morpho.org/tools/offchain/api/get-started/

**Playground:** https://api.morpho.org/graphql (GraphQL introspection and sandbox available)

**References:**
- Documentation: https://docs.morpho.org/tools/offchain/api/morpho/
- GettingStarted: https://docs.morpho.org/tools/offchain/api/get-started/
- VaultsAPI: https://docs.morpho.org/tools/offchain/api/morpho-vaults/
- PublicAllocatorAPI: https://docs.morpho.org/tools/offchain/api/public-allocator/
- SubgraphsDocs: https://docs.morpho.org/tools/offchain/subgraphs/
- GitHubOrg: https://github.com/morpho-org

## Key Types

- **Market** — Morpho Blue lending market with params (loan asset, collateral, LLTV, oracle, IRM), state (supply/borrow/collateral amounts and USD values, utilization), APY aggregates, warnings, oracle info, and bad debt tracking.
- **Vault** (MetaMorpho V1) — ERC-4626 vault with allocation queue, supply/withdraw queues, curator, guardian, fee, timelock, and historical state.
- **VaultV2** (MetaMorpho V2) — Next-generation vault with adapter registry, gates configuration, performance/management fees, sentinel, timelock, and VaultV2Caps per adapter.
- **MarketPosition** — A user's position in a specific market (collateral supplied, shares/assets borrowed, USD values, health factor context).
- **VaultPosition** — A user's deposit in a MetaMorpho vault (shares, assets, USD value, PnL, ROE).
- **Transaction** / **MarketTransaction** / **VaultV1Transaction** / **VaultV2Transaction** — On-chain event records including liquidations, transfers, deposits, and withdrawals with block and timestamp data.
- **PublicAllocator** — Configuration and reallocation history for the Morpho Public Allocator, including flow caps per vault-market pair.
- **Asset** — ERC-20 token metadata with price data and yield information.
- **Oracle** — Oracle configuration (Chainlink, ChainlinkV2, Custom) with feed addresses and accuracy metrics.
- **Curator** — Vault curator metadata including social links and managed vault list.
- **User** — Aggregated user state across all market and vault positions.

## Pagination

All paginated types (e.g., `PaginatedMarkets`, `PaginatedVaultV2s`) use `PageInfo` with `hasNextPage`, `endCursor` for cursor-based pagination.

## Time-Series

Historical queries accept `TimeseriesOptions` with `startTimestamp`, `endTimestamp`, and `interval` (HOUR, DAY, WEEK, MONTH, QUARTER, YEAR). Data points are returned as `BigIntDataPoint`, `FloatDataPoint`, or `IntDataPoint` with `x` (timestamp) and `y` (value) fields.
