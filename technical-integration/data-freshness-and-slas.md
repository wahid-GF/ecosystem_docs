# Data Freshness & SLAs

#### What is it?

This page describes how data freshness works across different sources, and what we commit to contractually.

No data point older than 30 days. In practice, high-traffic entities refresh continuously. Different attributes update at different cadences depending on source availability and query frequency.

<br>

#### Refresh cadences by source

| Source                                 | Refresh cadence               | Notes                                                                                                |
| -------------------------------------- | ----------------------------- | ---------------------------------------------------------------------------------------------------- |
| LinkedIn profiles                      | Continuous for active queries | Large companies queried frequently refresh constantly. Smaller companies refresh at minimum monthly. |
| LinkedIn Jobs / Indeed                 | Daily                         | Job data is the most time-sensitive signal we track.                                                 |
| Semrush traffic                        | Monthly                       | Traffic estimates are inherently monthly aggregations.                                               |
| Crunchbase / Dealroom                  | Weekly                        | Funding events, M\&A, and company updates.                                                           |
| BuiltWith / SimilarTech                | Weekly                        | Technology stack detection and changes.                                                              |
| G2 / Capterra / Trustpilot / Glassdoor | Weekly                        | Reviews, ratings, and software profiles.                                                             |
| Lighthouse                             | Monthly                       | Website performance metrics.                                                                         |
| GoodFit NLP                            | On crawl (continuous)         | Website classification, B2B/SaaS detection, GTM model.                                               |

For companies that get queried frequently, data refreshes happen on every crawl cycle. For less-queried companies, the refresh happens at the minimum cadence for each source — but never older than 30 days.

<br>

#### Delivery SLAs

| Metric                | Commitment                                                     |
| --------------------- | -------------------------------------------------------------- |
| Delivery timeliness   | 99.5% on-time delivery within the scheduled window             |
| Delivery completeness | 100% of configured blocks and fields present in every delivery |
| File integrity        | SHA-256 checksum provided and verified for every delivery      |
| Data freshness        | No attribute older than its documented refresh cadence         |

<br>

#### Incident handling

If a delivery is delayed or contains quality issues:

* **Detection** — GoodFit monitors every delivery pipeline automatically.
* **Notification** — Your partnership lead is notified within one hour. Critical issues trigger email alerts.
* **Resolution** — Target resolution within four hours for delivery failures, 24 hours for data quality issues.
* **Post-incident** — Written summary with root cause, impact, and preventive measures for any SLA breach.

<br>

#### Monitoring recommendations

We recommend setting up these checks on your side:

* **Delivery arrival** — alert if the expected file is not in S3 within two hours of the scheduled window
* **Record count** — alert if the manifest record count deviates more than 10% from the trailing average
* **Checksum** — verify `checksum_sha256` before processing and reject files that fail integrity checks
* **Schema version** — alert if `schema_version` changes, and review new fields before ingesting
