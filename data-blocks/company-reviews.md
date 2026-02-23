# Company Reviews

Customer-facing reviews and ratings across review platforms. This block covers keyword-matched review signals, review counts, ratings, and software feature mentions. You define the keywords you care about during setup.

{% hint style="info" %}
Review keyword matching lets partners surface companies whose customers are talking about specific topics — pain points, competitor mentions, feature requests, or product categories. It's a powerful intent signal.
{% endhint %}

{% tabs %}
{% tab title="Software reviews" %}
<table><thead><tr><th>Field</th><th width="372.72265625">Description</th><th>Example</th></tr></thead><tbody><tr><td>Has software features that match</td><td>Whether features matching your configured keywords exist across review platforms</td><td>true</td></tr><tr><td>Has software reviews that match</td><td>Whether reviews matching your configured keywords exist</td><td>true</td></tr><tr><td>List of keywords in software reviews that match</td><td>Keywords found in reviews matching your configuration</td><td>API integration, ease of use</td></tr><tr><td>Number of software reviews</td><td>Count of customer reviews on the company's profile across review platforms</td><td>234</td></tr><tr><td>Average software reviews rating</td><td>Overall review rating on the company's profile across review platforms</td><td>4.5</td></tr></tbody></table>
{% endtab %}

{% tab title="Keyword matches" %}
<table><thead><tr><th>Field</th><th width="372.72265625">Description</th><th>Example</th></tr></thead><tbody><tr><td>Has reviews that match</td><td>Whether a review with a keyword match exists</td><td>true</td></tr><tr><td>Number of reviews that match</td><td>Count of reviews matching your configured keyword criteria</td><td>12</td></tr></tbody></table>

{% hint style="warning" %}
**Both fields are configurable.** Results depend entirely on the keywords you define during dataset setup. No keywords configured means no results returned.
{% endhint %}
{% endtab %}
{% endtabs %}

### How it works

You provide a list of keywords during configuration. GoodFit scans customer-facing reviews for each company and returns matches against your terms. For example, if you configure keywords like "slow onboarding" or "API integration", you'll see which companies have reviews mentioning those phrases.

> **Shared fields**: Software categories and Software sub-categories also appear in [Industry & Business Type](industry-and-business-type.md).
