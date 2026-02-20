# Industry & Business Type

Everything you need to understand what a company does, who they sell to, and how they go to market. This group includes GoodFit's proprietary NLP classifications that you won't find anywhere else.

{% hint style="info" %}
Partners use these fields to build vertical market filters. The NLP classifications (B2B, SaaS, GTM model) are exclusive to GoodFit and aren't available from standard firmographic providers.
{% endhint %}

## Industry classification

| Field | Description | Example |
| --- | --- | --- |
| LinkedIn industry | Top-level industry classification | Computer Software |
| LinkedIn specialities | List of specialties associated with the company | Cloud Computing, Data Analytics |
| Software categories | Software category classification | CRM, Marketing Automation |
| Software sub-categories | Software sub-category classification | Sales CRM, Email Marketing |

## GoodFit NLP classifications

| Field | Description | Example |
| --- | --- | --- |
| Is B2B? | B2B classification based on GoodFit's NLP analysis of the company website | true |
| Is B2C? | B2C classification based on GoodFit's NLP analysis of the company website | false |
| Is SaaS company? | SaaS classification based on GoodFit's NLP analysis of the company website | true |
| Is technology company? | Technology classification based on GoodFit's NLP analysis of the company website | true |
| Is e-commerce company? | E-commerce classification based on GoodFit's NLP analysis of the company website | false |
| GTM model | Product Led or Sales Assisted classification based on GoodFit's NLP analysis of the company website | Product Led |
| Target user | B2B or B2C target user classification based on GoodFit's NLP analysis of the company website | B2B |

## Custom classification models

You can define fully custom classification models during dataset setup. Tell us the labels you care about (e.g. "Vertical SaaS," "HR Tech," "Marketplace"), and GoodFit will train a model that scores every company in your dataset against those labels.

Each model returns a primary label (the best match), all matching labels, and a probability score so your customers can filter or rank by confidence. For example, a company might return "Vertical SaaS" as the primary label with a probability of 0.87.

{% hint style="warning" %}
Classification models are **configurable**. You define the models, labels, and thresholds during dataset setup. Each model you add produces its own set of results.
{% endhint %}

> **Shared fields**: Software categories and Software sub-categories also appear in [Software Products](software-products.md).
