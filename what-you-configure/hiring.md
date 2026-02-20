# Hiring

Everything about a company's current hiring activity. Total open roles, where they're hiring, keyword-matched job postings, and how much of their hiring happens outside their HQ or office locations. One of the most time-sensitive signal groups in the dataset.

{% hint style="info" %}
Hiring data refreshes daily — the fastest cadence in the dataset. Partners use it to detect growth, expansion into new markets, and technology adoption in near real-time.
{% endhint %}

## Keyword matches

| Field | Description | Example |
| --- | --- | --- |
| Has jobs that match | Whether open roles with keyword matches exist | true |
| Number of jobs that match | Count of open roles matching your configured keyword criteria | 4 |
| Percentage of jobs that match | Percentage of open roles with keyword matches relative to all open roles | 18% |
| List of countries with jobs that match | Countries where open roles with keyword matches are located | United States, Germany |
| List of keywords in jobs descriptions that match | Keywords found in open role descriptions matching your configuration | data engineer, machine learning |

## Open roles

| Field | Description | Example |
| --- | --- | --- |
| Total number of open jobs | Total number of unique open roles currently listed | 22 |
| Open jobs in last 3 months | Count of total open roles listed in the last 3 months | 35 |
| Open jobs countries | List of countries where open roles are located | United States, United Kingdom, Germany |
| Open jobs countries count | Count of countries where open roles are located | 3 |

## Geographic distribution

| Field | Description | Example |
| --- | --- | --- |
| Hiring countries outside office locations | Countries outside company office locations where jobs are published | Germany |
| Hiring countries outside office locations count | Number of countries outside company office locations where jobs are published | 1 |
| Jobs outside office locations count | Number of jobs in countries outside company office locations | 3 |
| Jobs outside office locations percentage | Percentage of jobs published in countries outside company office locations relative to all published jobs | 14% |
| Jobs outside HQ count | Number of jobs in countries outside company HQ | 8 |
| Jobs outside HQ percentage | Percentage of jobs published outside company HQ relative to all published jobs | 36% |

> **Shared fields**: Open jobs countries and Hiring countries outside office locations also appear in [Location](location.md).
