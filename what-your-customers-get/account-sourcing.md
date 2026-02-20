# Account Sourcing

## What is it?

Account Sourcing lets your customers build their TAM straight from your dataset. They define their market using filters you've set up, preview the companies that qualify, and get a set of accounts that refreshes on its own.

No scraping LinkedIn. No third-party credits. The accounts come from your platform, powered by the dataset you built with GoodFit.

## Why is it useful?

Long gone are the days where your users had to scrape LinkedIn, pay for expensive third-party queries, or upload stale CSVs. All three put the burden on the customer, and the platform feels empty on day one.

Account Sourcing turns your platform into the source of truth. A customer describes who they sell to, and your platform delivers the accounts right away.

Here's what that unlocks:

* New customers get a populated experience from day one
* Structured, refreshed data replaces fragile LinkedIn scraping
* You can offer filters no other provider supports, like "companies hiring data engineers in DACH"
* The dataset stays alive as new companies arrive and non-qualifying ones drop out

## How it works

{% stepper %}
{% step %}
### Build the dataset
You work with GoodFit to define which companies are included, which attributes matter, and how configurable groups are set up. You do this once, then refine over time. Your customers never see this layer.
{% endstep %}
{% step %}
### Customers define their market
Inside your platform, they set their ICP using the filters you've exposed: company size, geography, industry, tech stack, team composition. Behind the scenes, these map to GoodFit data group attributes.
{% endstep %}
{% step %}
### They preview before committing
Before anything hits their workspace, they see total market size, a sample of qualifying companies, and validation that their criteria make sense.
{% endstep %}
{% step %}
### Accounts flow continuously
Once published, the market is alive. New qualifying companies show up. Companies that no longer qualify drop out. Your customers work a living dataset, not a static export.
{% endstep %}
{% endstepper %}

## Available filters

<details>
<summary>View all available filters</summary>

Every data group can be used as a sourcing filter. Here are the most common:

| Filter | Group | Example |
| --- | --- | --- |
| Company size | [Company Information](../what-you-configure/company-information.md) | `{ "min": 50, "max": 500 }` |
| Geography | [Location](../what-you-configure/location.md) | `{ "in": ["United States", "Germany"] }` |
| Business model | [Industry & Business Type](../what-you-configure/industry-and-business-type.md) | `true` |
| SaaS detection | [Industry & Business Type](../what-you-configure/industry-and-business-type.md) | `true` |
| GTM model | [Industry & Business Type](../what-you-configure/industry-and-business-type.md) | `{ "contains": "Product Led" }` |
| Funding stage | [Funding](../what-you-configure/funding.md) | `{ "in": ["Series A", "Series B"] }` |
| Tech stack | [Technologies](../what-you-configure/technologies.md) | `{ "match": ["Salesforce"], "has_matches": true }` |
| Hiring activity | [Hiring](../what-you-configure/hiring.md) | `{ "min": 5 }` |
| Team composition | [Team](../what-you-configure/team.md) | `{ "departments": ["sales"], "has_matches": true }` |
| Job keywords | [Hiring](../what-you-configure/hiring.md) | `{ "titleKeywords": ["data engineer"] }` |
| Traffic volume | [Website Traffic](../what-you-configure/website-traffic.md) | `{ "min": 50000 }` |
| Classification model | [Industry & Business Type](../what-you-configure/industry-and-business-type.md) | `{ "primary_label": "Vertical SaaS" }` |

</details>

{% hint style="success" %}
Configurable groups as filters are the differentiator. These aren't static fields. They're queries you defined when building your dataset, producing signals no other provider can offer as sourcing criteria.
{% endhint %}

{% content-ref url="enrichment.md" %}
[enrichment.md](enrichment.md)
{% endcontent-ref %}

{% content-ref url="../technical-integration/delivery-options.md" %}
[delivery-options.md](../technical-integration/delivery-options.md)
{% endcontent-ref %}
