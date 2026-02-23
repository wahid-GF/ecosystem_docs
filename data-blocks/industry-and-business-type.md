# Industry & Business Type

Everything you need to understand what a company does, who they sell to, and how they go to market. This block includes GoodFit's proprietary NLP classifications that you won't find anywhere else.

{% tabs %}
{% tab title="Industry classification" %}

<table><thead><tr><th>Field</th><th width="273.7265625">Description</th><th>Example</th></tr></thead><tbody><tr><td>LinkedIn industry</td><td>Top-level industry classification</td><td>Computer Software</td></tr><tr><td>LinkedIn specialities</td><td>List of specialties associated with the company</td><td>Cloud Computing, Data Analytics</td></tr><tr><td>Software categories</td><td>Software category classification</td><td>CRM, Marketing Automation</td></tr><tr><td>Software sub-categories</td><td>Software sub-category classification</td><td>Sales CRM, Email Marketing</td></tr><tr><td>Number of software products</td><td>Total count of software products associated with the company</td><td>2</td></tr></tbody></table>

{% endtab %}
{% tab title="AI Industry / Business Type Label" %}

You can define fully custom AI Industry / Business Type Labels during dataset setup. Tell us the labels you care about (e.g. "Vertical SaaS," "HR Tech," "Marketplace"), and GoodFit will train a model that scores every company in your dataset against those labels.

Each label returns a primary match (the best fit), all matching labels, and a probability score so your customers can filter or rank by confidence. For example, a company might return "Vertical SaaS" as the primary label with a probability of 0.87.

Below are examples of out of the box models we have pre-trained.&#x20;

<table><thead><tr><th width="222.8671875">Field</th><th>Description</th></tr></thead><tbody><tr><td>Is B2B?</td><td>B2B classification based on GoodFit's NLP analysis of the company website</td></tr><tr><td>Is B2C?</td><td>B2C classification based on GoodFit's NLP analysis of the company website</td></tr><tr><td>Is SaaS company?</td><td>SaaS classification based on GoodFit's NLP analysis of the company website</td></tr><tr><td>Is technology company?</td><td>Technology classification based on GoodFit's NLP analysis of the company website</td></tr><tr><td>Is e-commerce company?</td><td>E-commerce classification based on GoodFit's NLP analysis of the company website</td></tr><tr><td>GTM model</td><td>Product Led or Sales Assisted classification based on GoodFit's NLP analysis of the company website</td></tr><tr><td>Target user</td><td>B2B or B2C target user classification based on GoodFit's NLP analysis of the company website</td></tr></tbody></table>

{% hint style="warning" %}
AI Industry / Business Type Labels are **configurable**. You define the labels and thresholds during dataset setup. Each label you add produces its own set of results.
{% endhint %}

{% endtab %}
{% endtabs %}

> **Shared fields**: Software categories and Software sub-categories also appear in [Company Reviews](company-reviews.md).
