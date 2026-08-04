# Morpho

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Morpho is an open DeFi credit network enabling permissionless lending and borrowing of digital assets across Ethereum, Base, Arbitrum, and other supported chains. The Morpho API provides a GraphQL-based interface to access comprehensive onchain and offchain data from the Morpho ecosystem in real time.

## APIs

| API | Description |
|-----|-------------|
| [Markets API](https://docs.morpho.org/tools/offchain/api/morpho/) | Query market parameters, supply/borrow state, APYs, oracles, and risk indicators |
| [Vaults API](https://docs.morpho.org/tools/offchain/api/morpho-vaults/) | Retrieve vault metrics, depositor positions, APY, allocation, and earnings |
| [Positions API](https://docs.morpho.org/tools/offchain/api/morpho/) | User-level collateral, borrow, and supply positions across markets and vaults |
| [Liquidations API](https://docs.morpho.org/tools/offchain/api/morpho/) | Historical liquidation events with seized assets, repaid amounts, and bad debt |
| [Rewards API](https://docs.morpho.org/tools/offchain/api/get-started/) | Supply and borrow reward APRs and campaign data across markets |
| [Public Allocator API](https://docs.morpho.org/tools/offchain/api/public-allocator/) | Reallocatable liquidity, flow caps, and vault reallocation history |
| [Historical API](https://docs.morpho.org/tools/offchain/api/get-started/) | Time-series APY, supply/borrow volumes, and asset price data |

## GraphQL Endpoint

```
https://api.morpho.org/graphql
```

No authentication or API key required. Rate limit: 5,000 requests per 5 minutes.

## Resources

- [Documentation](https://docs.morpho.org/)
- [Developer Portal](https://developers.morpho.org/)
- [GraphQL Playground](https://api.morpho.org/graphql)
- [SDK](https://docs.morpho.org/tools/offchain/sdks/get-started/)
- [GitHub](https://github.com/morpho-org)
- [Blog](https://morpho.org/blog/)
- [Support](https://help.morpho.org/)
- [Discord](https://discord.gg/morpho)

## Maintainer

**Kin Lane** — kin@apievangelist.com
