# Account Sourcing

## What is it?

Account Sourcing lets your customers build their market and source accounts straight from your dataset. They define their market using filters you've set up, preview the companies that qualify, and get a set of accounts that refreshes on its own.

No scraping LinkedIn. No third-party credits. The accounts come from your platform, powered by the dataset you built with GoodFit.

## Why is it useful?

Scraping LinkedIn, paying for expensive third-party queries, or syncing stale CRM data/CSVs. All three put the burden on the customer, and leave the platform empty on day one.

Account Sourcing turns your platform into the source of truth. A customer determines who they sell to across any definition you allow within the platform., For you to then dynamically deliver the accounts as and when required.

Unlocks:

* New customers get a populated experience from day one
* You can offer filters no other provider supports, like "B2B SaaS companies hiring data engineers in DACH and use kubernetes"
* The dataset remains dynamic as new companies arrive and non-qualifying ones drop out
* Identity resolution resolved across a breadth of data sources

## How it works

{% stepper %}
{% step %}
#### Build the dataset

Work with GoodFit to define which companies are included, which attributes matter, and how segments are configured. Done once, refined over time. Your customers never see this layer.
{% endstep %}

{% step %}
#### Customers define their market

Inside your platform, customers set their ICP using any filters you've exposed: hiring velocity, geography, customer reviews, tech stack, team composition, and more. Behind the scenes, these map directly to GoodFit data blocks.
{% endstep %}

{% step %}
#### Accounts flow continuously

Once published, the market stays live. New companies appear the moment they qualify. Companies that no longer fit drop off automatically. This powers whatever sourcing and market sizing workflows you want to build into your platform.
{% endstep %}
{% endstepper %}

## Available filters

<details>

<summary>View all available filters</summary>

Every data group can be used as a sourcing filter. Here are the most common:

| Filter               | Group                                                                           | Example                                             |
| -------------------- | ------------------------------------------------------------------------------- | --------------------------------------------------- |
| Company size         | [Company Information](../what-you-configure/company-information.md)             | `{ "min": 50, "max": 500 }`                         |
| Geography            | [Location](../what-you-configure/location.md)                                   | `{ "in": ["United States", "Germany"] }`            |
| Business model       | [Industry & Business Type](../what-you-configure/industry-and-business-type.md) | `true`                                              |
| SaaS detection       | [Industry & Business Type](../what-you-configure/industry-and-business-type.md) | `true`                                              |
| GTM model            | [Industry & Business Type](../what-you-configure/industry-and-business-type.md) | `{ "contains": "Product Led" }`                     |
| Funding stage        | [Funding](../what-you-configure/funding.md)                                     | `{ "in": ["Series A", "Series B"] }`                |
| Tech stack           | [Technologies](../what-you-configure/technologies.md)                           | `{ "match": ["Salesforce"], "has_matches": true }`  |
| Hiring activity      | [Hiring](../what-you-configure/hiring.md)                                       | `{ "min": 5 }`                                      |
| Team composition     | [Team](../what-you-configure/team.md)                                           | `{ "departments": ["sales"], "has_matches": true }` |
| Job keywords         | [Hiring](../what-you-configure/hiring.md)                                       | `{ "titleKeywords": ["data engineer"] }`            |
| Traffic volume       | [Website Traffic](../what-you-configure/website-traffic.md)                     | `{ "min": 50000 }`                                  |
| Classification model | [Industry & Business Type](../what-you-configure/industry-and-business-type.md) | `{ "primary_label": "Vertical SaaS" }`              |

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
