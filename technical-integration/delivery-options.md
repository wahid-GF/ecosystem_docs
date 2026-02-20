---
hidden: true
---

# Delivery Options

## What is it?

Delivery options define how GoodFit data gets into your product. The right method depends on your architecture, your team's capacity, and what you're building. We support multiple approaches and can shape new ones.

### Why does this matter?

The wrong delivery method creates engineering drag. The right one disappears into your existing stack. Pick based on your architecture, not on what sounds newest.

## Choosing the right option

<table data-view="cards">
<thead><tr>
  <th></th>
  <th></th>
</tr></thead>
<tbody>
<tr>
  <td><strong>Flat File (S3)</strong></td>
  <td>Batch delivery, daily or weekly. Best for data warehouse architectures and MVPs. Lowest engineering lift.</td>
</tr>
<tr>
  <td><strong>Database Access</strong></td>
  <td>Near real-time, full SQL-style queries. Best for partners who want query flexibility or real-time filtering.</td>
</tr>
<tr>
  <td><strong>API Endpoints</strong></td>
  <td>Real-time enrichment and sourcing. Structured endpoints, event-driven. Best for API-first architectures.</td>
</tr>
</tbody>
</table>

{% hint style="info" %}
You're not locked in. Start with flat files. Move to API when you're ready. Run both in parallel during migration. The underlying dataset is the same regardless of delivery method.
{% endhint %}

## Option 1: Flat file delivery (S3)

Best for MVP integrations, data warehouse architectures, and teams that want full control over ingestion.

GoodFit delivers structured files to an S3 bucket on a configured cadence. You pick them up and process them however you want.

```
s3://{bucket}/{partner_prefix}/
├── enrichment/
│   ├── enriched_2026-02-15.csv
│   └── enriched_2026-02-15_manifest.json
└── sourcing/
    ├── sourced_2026-02-15.csv
    └── sourced_2026-02-15_manifest.json
```

Supported formats: CSV (UTF-8), Parquet, and JSON Lines.

{% hint style="info" %}
Every delivery includes a `manifest.json` with record count, field list, checksum, and schema version. Use it for automated quality checks.
{% endhint %}

This is how most partners start. Lowest-lift integration, no API dependencies, no rate limits. Your existing data infrastructure handles ingestion.

## Option 2: Database access

Best for partners who want query flexibility, real-time filtering, or to build their own query layer on top of the dataset.

GoodFit gives you access to a configured dataset in a queryable format. You run the queries. We maintain the data.

More flexibility than flat files. You can build dynamic filtering, faceted search, and real-time lookups without waiting for a file delivery.

Database access is available for build partners. We'll shape the details around what you need: hosted database, replicated dataset, or query API.

## Option 3: API endpoints

Best for real-time enrichment, on-demand sourcing, and event-driven architectures.

Structured API endpoints for sourcing (`POST /v1/markets`) and enrichment (`POST /v1/enrich`). Your platform calls GoodFit in real-time. Results come back structured and typed.

See [Account Sourcing](../what-your-customers-get/account-sourcing.md) and [Enrichment](../what-your-customers-get/enrichment.md) for more detail.

## Schema mapping

GoodFit field names follow the data group structure documented in this portal, for example `firmographics.employee_count` or `hiring.open_jobs`. Your internal schema will use different names.

We'll work with your engineering team to define a mapping. Common patterns:

{% tabs %}
{% tab title="Direct mapping" %}
```json
{
  "firmographics.company_name": "account_name",
  "firmographics.employee_count": "num_employees",
  "firmographics.country": "hq_country",
  "hiring.open_jobs": "active_job_postings"
}
```
{% endtab %}

{% tab title="Transform mapping" %}
```json
{
  "firmographics.revenue_range": {
    "target": "revenue_tier",
    "transform": {
      "$1M-$5M": "SMB",
      "$5M-$10M": "Mid-Market",
      "$10M-$50M": "Mid-Market",
      "$50M-$100M": "Enterprise",
      "$100M+": "Enterprise"
    }
  }
}
```
{% endtab %}
{% endtabs %}

{% content-ref url="data-freshness-and-slas.md" %}
[data-freshness-and-slas.md](data-freshness-and-slas.md)
{% endcontent-ref %}
