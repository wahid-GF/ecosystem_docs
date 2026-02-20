# Company Reviews

Customer-facing reviews and ratings. You define the keywords you care about during setup, and these fields tell you whether any reviews mention those terms and how many match.

{% hint style="info" %}
Review keyword matching lets partners surface companies whose customers are talking about specific topics — pain points, competitor mentions, feature requests, or product categories. It's a powerful intent signal.
{% endhint %}

## Fields

| Field | Description | Example |
| --- | --- | --- |
| Has reviews that match \* | Whether a review with a keyword match exists | true |
| Number of reviews that match \* | Count of reviews matching your configured keyword criteria | 12 |

{% hint style="warning" %}
**Both fields are configurable.** Results depend entirely on the keywords you define during dataset setup. No keywords configured means no results returned.
{% endhint %}

### How it works

You provide a list of keywords during configuration. GoodFit scans customer-facing reviews for each company and returns matches against your terms. For example, if you configure keywords like "slow onboarding" or "API integration", you'll see which companies have reviews mentioning those phrases.
