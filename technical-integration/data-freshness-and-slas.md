---
hidden: true
---

# Data Freshness & SLAs

## What is it?

How data freshness works across different sources, and what we commit to contractually.

{% hint style="success" %}
No data point older than 30 days. In practice, high-traffic entities refresh continuously. Different attributes update at different cadences depending on source availability and query frequency.
{% endhint %}

### Why does this matter?

Stale data erodes trust. If your customers see a company listed as "50 employees" when it's actually 500, they stop trusting your platform. Freshness isn't a nice-to-have; it's what separates a live dataset from a static dump.

## Refresh cadences

| Data category | Refresh cadence | Notes |
| --- | --- | --- |
| Company profiles & firmographics | Continuous for active queries | Large companies refresh constantly. Smaller ones at minimum monthly. |
| Job postings & hiring activity | Daily | Most time-sensitive signal we track. |
| Website traffic estimates | Monthly | Inherently monthly aggregations. |
| Funding & investment data | Weekly | Funding events, M&A, and company updates. |
| Technology detection | Weekly | Tech stack detection and changes. |
| Software reviews & ratings | Weekly | Product reviews and rating data. |
| Employee sentiment | Weekly | Employee reviews, ratings, and sentiment. |
| Company reviews | Weekly | Customer-facing reviews and ratings. |
| Website performance | Monthly | Speed and performance metrics. |
| Business classification & NLP | On crawl (continuous) | B2B/SaaS detection, GTM model, custom classifiers. |

For companies that get queried a lot, data refreshes on every crawl cycle. For less-queried companies, it refreshes at the minimum cadence for each source, but never older than 30 days.

## Delivery SLAs

| Metric                | Commitment                                                     |
| --------------------- | -------------------------------------------------------------- |
| Delivery timeliness   | 99.5% on-time delivery within the scheduled window             |
| Delivery completeness | 100% of configured blocks and fields present in every delivery |
| File integrity        | SHA-256 checksum provided and verified for every delivery      |
| Data freshness        | No attribute older than its documented refresh cadence         |

## Incident handling

If a delivery is delayed or has quality issues:

* **Detection**: We monitor every delivery pipeline automatically.
* **Notification**: Your partnership lead gets notified within one hour. Critical issues trigger email alerts.
* **Resolution**: We target four hours for delivery failures, 24 hours for data quality issues.
* **Post-incident**: Written summary with root cause, impact, and preventive measures for any SLA breach.

## Monitoring recommendations

We'd recommend setting up these checks on your side:

{% stepper %}
{% step %}
#### Delivery arrival
Alert if the expected file isn't in S3 within two hours of the scheduled window.
{% endstep %}
{% step %}
#### Record count
Alert if the manifest record count deviates more than 10% from the trailing average.
{% endstep %}
{% step %}
#### Checksum
Verify `checksum_sha256` before processing and reject files that fail integrity checks.
{% endstep %}
{% step %}
#### Schema version
Alert if `schema_version` changes, and review new fields before ingesting.
{% endstep %}
{% endstepper %}
