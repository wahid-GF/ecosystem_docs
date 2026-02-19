# GoodFit Platform Data

**Your dataset. Your brand. Our intelligence.**

GoodFit powers your dataset with 296 attributes across 25 data blocks from 14+ live sources. You configure the data layer once — choosing which blocks, parameters, and quality thresholds matter for your market. Your customers access the result as your data, inside your platform. They use it to source accounts and enrich companies. They never see GoodFit.

<br>

### What your customers get

| Capability                                           | What it does                                                                                                                                           |
| ---------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [**Account Sourcing**](data-api/account-sourcing.md) | Your customers build their TAM from your dataset. They define their market, preview qualifying companies, and receive continuously refreshed accounts. |
| [**Enrichment**](data-api/enrichment.md)             | Your customers pass a company and get back up to 296 attributes. Firmographics, hiring, traffic, tech, funding, reviews — from one call.               |

Both capabilities draw from the same data blocks listed below. You configure the blocks once. Your customers use them as sourcing filters (to define which companies qualify) or receive them as enrichment fields (to learn everything about a company).

<br>

### What you configure

These blocks form your dataset. You define the parameters. Your customers query the result.

| Block                                                   | Fields | Type    |
| ------------------------------------------------------- | -----: | ------- |
| [firmographics](data-api/firmographics.md)              |     48 | Core    |
| [hiring](data-api/hiring.md)                            |     52 | Core    |
| [team](data-api/team.md)                                |     37 | Core    |
| [traffic](data-api/traffic.md)                          |     29 | Core    |
| [website\_performance](data-api/website-performance.md) |     14 | Core    |
| [funding](data-api/funding.md)                          |     10 | Core    |
| [glassdoor](data-api/glassdoor.md)                      |     10 | Core    |
| [software](data-api/software.md)                        |      9 | Core    |
| [team\_members](data-api/team-members.md)               |      8 | Dynamic |
| [technologies](data-api/technologies.md)                |      7 | Dynamic |
| [jobs](data-api/jobs.md)                                |      8 | Dynamic |
| [predictive\_labels](data-api/predictive-labels.md)     |      3 | Dynamic |
| [company\_reviews](data-api/company-reviews.md)         |      7 | Dynamic |

**Core** blocks return the same fields for every company and are included in your dataset by default.

**Dynamic** blocks accept your parameters — keywords, countries, departments, technologies, rating filters — and return signals tailored to your configuration. Each parameter combination produces distinct data points. You set these once when building your dataset. Your customers query the result.

<br>

### Partner programme

We want to understand how you need data to live in your product and we will shape delivery around that. See [Partner Patterns](introduction/partner-patterns.md) for how early integrations are taking shape, or [Getting Started](integration/getting-started.md) for the technical onboarding path.



### Don't see what you need?

The dataset is not fixed. We add new blocks, fields, sources, and custom classifiers based on partner requirements.

{% content-ref url="data-api/request.md" %}
[request.md](data-api/request.md)
{% endcontent-ref %}
