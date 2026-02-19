# GoodFit Platform Data

**Your platform. Your configuration. Our intelligence.**

GoodFit powers your dataset with hundreds attributes across 25 data blocks from dozens of live sources. You configure the data layer once choosing which blocks, parameters, and quality thresholds matter for your market. Your customers access the result as your data, inside your platform. They use it to source accounts and enrich companies. They never see GoodFit.

<br>

### What your customers get

| Capability                                           | What it does                                                                                                                                           |
| ---------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [**Account Sourcing**](data-api/account-sourcing.md) | Your customers build their TAM from your dataset. They define their market, preview qualifying companies, and receive continuously refreshed accounts. |
| [**Enrichment**](data-api/enrichment.md)             | Your customers pass a company and get back up to 296 attributes. Firmographics, hiring, traffic, tech, funding, reviews from one provider.             |

Both capabilities draw from the same data blocks listed below. You configure the blocks once. Your customers use them as sourcing filters (to define which companies qualify) or receive them as enrichment fields (to learn everything about a company).

<br>

### What you configure

These blocks form your dataset. You define the parameters. Your customers query the result.

<table><thead><tr><th width="296.1171875">Block</th><th align="right">Fields</th><th>Type</th></tr></thead><tbody><tr><td><a href="data-api/firmographics.md">Firmographics</a></td><td align="right">48</td><td>Core</td></tr><tr><td><a href="data-api/hiring.md">Hiring</a></td><td align="right">52</td><td>Dynamic</td></tr><tr><td><a href="data-api/team.md">Team</a></td><td align="right">37</td><td>Dynamic</td></tr><tr><td><a href="data-api/website-performance.md">Site Performance</a></td><td align="right">14</td><td>Core</td></tr><tr><td><a href="data-api/glassdoor.md">Employee Sentiment</a></td><td align="right">10</td><td>Core</td></tr><tr><td><a href="data-api/software.md">Software</a></td><td align="right">9</td><td>Core</td></tr><tr><td><a href="data-api/technologies.md">Technographics</a></td><td align="right">7</td><td>Dynamic</td></tr><tr><td><a href="data-api/predictive-labels.md">Classification Language Models</a></td><td align="right">3</td><td>Dynamic</td></tr><tr><td><a href="data-api/company-reviews.md">Reviews</a></td><td align="right">7</td><td>Dynamic</td></tr></tbody></table>

**Core** blocks return the same fields for every company and are included in your dataset.

**Dynamic** blocks accept your parameters - keywords, countries, departments, technographics, rating filters - for a tailored configuration. Each parameter combination produces distinct data points and sourcing results. You set these once when building your dataset. Your customers query the result.

<br>

### Partner Program

We want to understand how you need data to live in your product and we will shape delivery around that. See [Partner Patterns](introduction/partner-patterns.md) for how early integrations are taking shape, or [Getting Started](integration/getting-started.md) for the technical onboarding path.



### Don't see what you need?

The dataset is not fixed. We add new blocks, fields, sources, and custom classifiers based on partner requirements.

{% content-ref url="data-api/request.md" %}
[request.md](data-api/request.md)
{% endcontent-ref %}
