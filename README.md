# Partner Data Platform

**Your dataset. Your brand. Our intelligence.**

GoodFit powers your dataset with 296 attributes across 25 data blocks from 14+ live sources. You configure the data layer once — choosing which blocks, parameters, and quality thresholds matter for your market. Your customers access the result as your data, inside your platform. They use it to source accounts and enrich companies. They never see GoodFit.

<br>

### What your customers get

| Capability | What it does | Endpoint |
| --- | --- | --- |
| [**Account Sourcing**](data-api/account-sourcing.md) | Your customers build their TAM from your dataset. They define their market, preview qualifying companies, and receive continuously refreshed accounts. | `POST /v1/markets` |
| [**Enrichment**](data-api/enrichment.md) | Your customers pass a company and get back up to 296 attributes. Firmographics, hiring, traffic, tech, funding, reviews — from one call. | `POST /v1/enrich` |

Both capabilities draw from the same data blocks listed below. You configure the blocks once. Your customers use them as sourcing filters (to define which companies qualify) or receive them as enrichment fields (to learn everything about a company).

<br>

### What you configure

These blocks form your dataset. You define the parameters. Your customers query the result.

| Block | Fields | Type | Source |
| --- | ---: | --- | --- |
| [firmographics](data-api/firmographics.md) | 48 | Core | LinkedIn, Crunchbase, GoodFit NLP |
| [hiring](data-api/hiring.md) | 52 | Core | LinkedIn Jobs, Indeed |
| [team](data-api/team.md) | 37 | Core | LinkedIn |
| [traffic](data-api/traffic.md) | 29 | Core | Semrush |
| [website\_performance](data-api/website-performance.md) | 14 | Core | Lighthouse |
| [funding](data-api/funding.md) | 10 | Core | Crunchbase, Dealroom |
| [glassdoor](data-api/glassdoor.md) | 10 | Core | Glassdoor |
| [software](data-api/software.md) | 9 | Core | G2, Capterra |
| [team\_members](data-api/team-members.md) | 8 | You Configure | LinkedIn |
| [technologies](data-api/technologies.md) | 7 | You Configure | BuiltWith, SimilarTech |
| [jobs](data-api/jobs.md) | 8 | You Configure | LinkedIn Jobs, Indeed |
| [predictive\_labels](data-api/predictive-labels.md) | 3 | You Configure | GoodFit NLP |
| [company\_reviews](data-api/company-reviews.md) | 7 | You Configure | Trustpilot |

**Core** blocks return the same fields for every company and are included in your dataset by default.

**You Configure** blocks accept your parameters — keywords, countries, departments, technologies, rating filters — and return signals tailored to your configuration. Each parameter combination produces distinct data points. You set these once when building your dataset. Your customers query the result.

<br>

### Data freshness

No data point older than 30 days. In practice, high-traffic entities refresh continuously. Different attributes update at different cadences depending on source availability and query frequency.

| Source | Refresh cadence |
| --- | --- |
| LinkedIn profiles | Continuous for active queries |
| LinkedIn Jobs / Indeed | Daily |
| Semrush traffic | Monthly |
| Crunchbase / Dealroom | Weekly |
| BuiltWith / SimilarTech | Weekly |
| G2 / Capterra / Trustpilot / Glassdoor | Weekly |
| Lighthouse | Monthly |
| GoodFit NLP | On crawl (continuous) |

<br>

### Build partner programme

We are in build partner stage for the white label offering. That means flexibility — we want to understand how you need data to live in your product and we will shape delivery around that.

See [Partner Patterns](introduction/partner-patterns.md) for how early integrations are taking shape, or [Getting Started](integration/getting-started.md) for the technical onboarding path.

<br>

### Don't see what you need?

The dataset is not fixed. We add new blocks, fields, sources, and custom classifiers based on partner requirements.

{% content-ref url="data-api/request.md" %}
[Request a data point](data-api/request.md)
{% endcontent-ref %}
