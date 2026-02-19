# Account Sourcing

## What is it?

Account Sourcing lets your customers build their TAM directly from your dataset. They define their market using filters you've configured, preview qualifying companies, and get a continuously refreshed set of accounts.

No scraping LinkedIn. No third-party credits. The accounts come from your platform, powered by the dataset you built with GoodFit.

## Why is it useful?

Most platforms today give users three ways to source accounts: LinkedIn scraping, an expensive third-party query, or uploading a CSV. All three put the burden on the customer, and the platform feels empty on day one.

Account Sourcing turns your platform into the source of truth. A customer describes who they sell to, and your platform delivers the accounts immediately.

With Account Sourcing, you can:

* Give new customers a populated experience from day one
* Replace fragile LinkedIn scraping with structured, refreshed data
* Offer dynamic filters no other provider supports, like "companies hiring data engineers in DACH"
* Keep the dataset alive as new companies arrive and non-qualifying ones drop out

## How it works

Four steps.

**1. You build the dataset.** With GoodFit, you define which companies are included, which attributes matter, and how Dynamic blocks are configured. This happens once, with ongoing refinement. Customers never see this layer.

**2. Customers define their market.** Inside your platform, they specify their ICP using the filters you've exposed: company size, geography, industry, tech stack, team composition. These map to GoodFit data block attributes behind the scenes.

**3. They preview before committing.** Before anything enters their workspace, they see total market size, a sample of qualifying companies, and validation that their criteria make sense.

**4. Accounts flow continuously.** Once published, the market is alive. New qualifying companies arrive. Companies that no longer qualify drop out. Customers work a living dataset, not a static export.

## Available filters

Every data block can be used as a sourcing filter. Here are the most common:

| Filter                | Block                          | Example                                             |
| --------------------- | ------------------------------ | --------------------------------------------------- |
| Company size          | `firmographics.employee_count` | `{ "min": 50, "max": 500 }`                         |
| Geography             | `firmographics.country`        | `{ "in": ["United States", "Germany"] }`            |
| Business model        | `firmographics.is_b2b`         | `true`                                              |
| SaaS detection        | `firmographics.is_saas`        | `true`                                              |
| GTM model             | `firmographics.gtm_model`      | `{ "contains": "Product Led" }`                     |
| Funding stage         | `funding.last_funding_stage`   | `{ "in": ["Series A", "Series B"] }`               |
| Tech stack            | `technologies`                 | `{ "match": ["Salesforce"], "has_matches": true }`  |
| Hiring activity       | `hiring.open_jobs`             | `{ "min": 5 }`                                      |
| Sales team exists     | `team_members`                 | `{ "departments": ["sales"], "has_matches": true }` |
| Job keywords          | `jobs`                         | `{ "titleKeywords": ["data engineer"] }`            |
| Traffic volume        | `traffic.all_domains_visits`   | `{ "min": 50000 }`                                  |
| Classification Model  | `classification_model`         | `{ "primary_label": "Vertical SaaS" }`              |

{% hint style="success" %}
Dynamic blocks as filters are the differentiator. These aren't static fields. They're queries you defined when building your dataset, producing signals no other provider can offer as sourcing criteria.
{% endhint %}

{% content-ref url="enrichment.md" %}
[enrichment.md](enrichment.md)
{% endcontent-ref %}

{% content-ref url="../technical-integration/delivery-options.md" %}
[delivery-options.md](../technical-integration/delivery-options.md)
{% endcontent-ref %}
