# Delivery Options

## What is it?

Delivery options define how GoodFit data gets into your product. The right method depends on your architecture, your team's capacity, and what you're building. We support multiple approaches and can shape new ones.

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

GoodFit provides access to a configured dataset in a queryable format. You run the queries. We maintain the data.

More flexibility than flat files. You can build dynamic filtering, faceted search, and real-time lookups without waiting for a file delivery.

Database access is available for build partners. The specifics (hosted database, replicated dataset, query API) are shaped by partner requirements.

## Option 3: API endpoints

Best for real-time enrichment, on-demand sourcing, and event-driven architectures.

Structured API endpoints for sourcing (`POST /v1/markets`) and enrichment (`POST /v1/enrich`). Your platform calls GoodFit in real-time. Results come back structured and typed.

See [Account Sourcing](../what-your-customers-get/account-sourcing.md) and [Enrichment](../what-your-customers-get/enrichment.md) for more detail.

## Choosing the right option

| Question                       | Flat file                | Database               | API                  |
| ------------------------------ | ------------------------ | ---------------------- | -------------------- |
| How quickly do you need data?  | Batch (daily/weekly)     | Near real-time         | Real-time            |
| Do you have a data warehouse?  | Yes, pipe it in          | Maybe, we can host     | Not needed           |
| How much query flexibility?    | You query your warehouse | Full SQL-style queries | Structured endpoints |
| Engineering lift to integrate? | Low                      | Medium                 | Medium               |
| Best for MVP?                  | Yes                      | Depends                | If API-first         |

{% hint style="info" %}
You're not locked in. Start with flat files. Move to API when you're ready. Run both in parallel during migration. The underlying dataset is the same regardless of delivery method.
{% endhint %}

## Schema mapping

GoodFit field names follow the data block structure documented in this portal, for example `firmographics.employee_count` or `hiring.open_jobs`. Your internal schema will use different names.

We work with your engineering team to define a mapping. Common patterns:

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
