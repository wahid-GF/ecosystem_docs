# Hiring

Everything about a company's current hiring activity. Total open roles, where they're hiring, keyword-matched job postings, and how much of their hiring happens outside their HQ or office locations. One of the most time-sensitive signal blocks in the dataset.

{% tabs %}
{% tab title="Keyword matches" %}

<table><thead><tr><th>Field</th><th width="322.36328125">Description</th><th>Example</th></tr></thead><tbody><tr><td>Has jobs that match</td><td>Whether open roles with keyword matches exist</td><td>true</td></tr><tr><td>Number of jobs that match</td><td>Count of open roles matching your configured keyword criteria</td><td>4</td></tr><tr><td>Percentage of jobs that match</td><td>Percentage of open roles with keyword matches relative to all open roles</td><td>18%</td></tr><tr><td>List of countries with jobs that match</td><td>Countries where open roles with keyword matches are located</td><td>United States, Germany</td></tr><tr><td>List of keywords in jobs descriptions that match</td><td>Keywords found in open role descriptions matching your configuration</td><td>data engineer, machine learning</td></tr></tbody></table>

{% endtab %}
{% tab title="Open roles" %}

<table><thead><tr><th>Field</th><th width="322.05859375">Description</th><th>Example</th></tr></thead><tbody><tr><td>Total number of open jobs</td><td>Total number of unique open roles currently listed</td><td>22</td></tr><tr><td>Open jobs in last 3 months</td><td>Count of total open roles listed in the last 3 months</td><td>35</td></tr><tr><td>Open jobs countries</td><td>List of countries where open roles are located</td><td>United States, United Kingdom, Germany</td></tr><tr><td>Open jobs countries count</td><td>Count of countries where open roles are located</td><td>3</td></tr></tbody></table>

{% endtab %}
{% tab title="Geographic distribution" %}

<table><thead><tr><th>Field</th><th width="407.40625">Description</th><th>Example</th></tr></thead><tbody><tr><td>Hiring countries outside office locations</td><td>Countries outside company office locations where jobs are published</td><td>Germany</td></tr><tr><td>Hiring countries outside office locations count</td><td>Number of countries outside company office locations where jobs are published</td><td>1</td></tr><tr><td>Jobs outside office locations count</td><td>Number of jobs in countries outside company office locations</td><td>3</td></tr><tr><td>Jobs outside office locations percentage</td><td>Percentage of jobs published in countries outside company office locations relative to all published jobs</td><td>14%</td></tr><tr><td>Jobs outside HQ count</td><td>Number of jobs in countries outside company HQ</td><td>8</td></tr><tr><td>Jobs outside HQ percentage</td><td>Percentage of jobs published outside company HQ relative to all published jobs</td><td>36%</td></tr></tbody></table>

{% endtab %}
{% endtabs %}

> **Shared fields**: Open jobs countries and Hiring countries outside office locations also appear in [Location](location.md).
