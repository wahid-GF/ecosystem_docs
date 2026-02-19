# Getting Started

## What is it?

Here's how you go from first call to live data in your product. We're in build partner stage, so the process is collaborative rather than prescriptive.

## What we need from you

Before anything technical happens, we need to understand three things:

* **Your use cases.** Sourcing, enrichment, or both. Are your users building TAMs, enriching CRM records, triggering workflows, or something else?
* **What data's in your product today.** Where does it come from? What's working? What's broken? What providers are you using, and what would you change?
* **How your engineering team wants to consume data.** Database access? Flat file drops to S3? API calls? We'll shape delivery around whatever's lowest-lift for you.

## How it works

{% stepper %}
{% step %}
### Discovery call
Walk us through your product, your user base, and where company data fits. We'll share what we think is possible and identify the right starting point. Usually one to two calls.
{% endstep %}
{% step %}
### Dataset configuration
With your GoodFit partnership lead, you'll define which data blocks are included, how Dynamic blocks are configured, and which attributes matter for your market. We handle the data engineering.
{% endstep %}
{% step %}
### Delivery setup
We agree on format and mechanism. Could be flat file to S3, database access, or API endpoints depending on your architecture. We configure our side. You configure ingestion on yours.
{% endstep %}
{% step %}
### Initial delivery and validation
You'll get your first data. Validate coverage, attribute quality, and schema compatibility. If something needs tweaking, we iterate. Most partners do one to two rounds of refinement.
{% endstep %}
{% step %}
### Production activation
Lock in the configuration. Activate automated refresh. Ship it to your users.
{% endstep %}
{% endstepper %}

{% content-ref url="delivery-options.md" %}
[delivery-options.md](delivery-options.md)
{% endcontent-ref %}

{% content-ref url="data-freshness-and-slas.md" %}
[data-freshness-and-slas.md](data-freshness-and-slas.md)
{% endcontent-ref %}
