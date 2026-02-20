# Common Use Cases

## What is it?

How partners are thinking about GoodFit data in their products. These patterns come from live conversations. They show the range of what's possible, not a prescriptive playbook.

{% hint style="info" %}
**Meet Sarah.** She runs product at a GTM platform. Her users import CSVs, scrape LinkedIn, or buy expensive credits from a data vendor. She wants company data to feel native, like her platform built it. The patterns below show how partners like Sarah are thinking about GoodFit.
{% endhint %}

## Pattern 1: Account sourcing

A GTM workflow platform wants to offer a native "Build Your TAM" experience. Today, their users scrape LinkedIn, query an expensive third-party provider, or import CSVs that are stale on arrival. The platform feels empty on day one.

With GoodFit, the partner offers an account finder powered by the sourcing engine. Users define criteria using filters the partner has configured: department size, geography, industry, tech stack, hiring activity. Results flow continuously. New qualifying companies show up. Companies that no longer qualify drop out.

What makes this different from bolting on a standard data provider is the filters. Users can source based on "companies hiring data engineers in DACH" or "companies with VP-level sales leadership." These are live queries against configured data groups, not static fields.

The partner defines which data groups and parameters matter. GoodFit configures the dataset. The partner builds the UI. Users query the dataset like it's native.

## Pattern 2: Identity resolution and data hygiene

A platform is building identity resolution: unifying a customer's CRM data, product analytics, and other first-party data into a single company view. Once unified, the next step is filling in the gaps. They need a data partner who can handle both basic firmographics and deeper signals without costing a fortune per record.

With GoodFit, the partner triggers enrichment when a company record is created or unified. One call returns 100s of attributes. Basic company data (name, size, geography, industry) plus signals that commodity providers miss: hiring velocity, team composition, traffic trends, technology stack, NLP classifications.

Better data at a more sustainable cost, plus proprietary signals that didn't exist in their old stack.

## Pattern 3: AI-powered account intelligence

A conversational intelligence platform wants to go beyond call recording. Their vision: when a user onboards, the platform understands their ICP from existing customers and pipeline, then proactively suggests accounts worth pursuing. Think Spotify recommendations, but for target accounts.

With GoodFit, the platform gets the structured data layer that makes this possible. GoodFit provides the universe of companies with deep attributes. The partner's AI models consume those attributes, identify patterns in existing customers, and surface net-new companies that match.

What makes this different from CRM data alone is breadth. CRM data tells you about companies you've already touched. GoodFit tells you about the 25M+ you haven't, including niche verticals where standard providers have minimal coverage.

## Pattern 4: Signal-based workflows

A platform lets users build automated workflows: "every Monday, find accounts that match X, enrich with Y, push to Z." The workflows are powerful, but only as good as the data feeding them. Today, the data options are limited and expensive.

With GoodFit, the partner exposes data groups as workflow triggers and filters. Not just "this company has 200 employees" but "this company is hiring 47 people, 34% remote, with 12 open sales roles and jobs posted outside their HQ country." Those signals become workflow inputs.

Users build automations using attributes they don't even know are powered by GoodFit. The data refreshes on cadence. The workflows fire on change.

## Common themes

Every conversation with prospective partners surfaces the same things:

* **Fragmented data stacks.** Everyone's tried at least two providers. None alone covers the breadth of data users actually need.
* **Native experience matters.** Nobody wants their customers to see a third-party logo or get redirected to another platform. The data needs to live inside the product.
* **Engineering capacity is limited.** Partners have product roadmaps to execute. Data engineering is a distraction. They want someone else to handle identity resolution, source management, refresh logic, and quality.
* **Custom signals are the differentiator.** Basic firmographics are table stakes. What gets partners interested is the GoodFit NLP layer and the ability to configure data groups with parameters specific to their market.

{% content-ref url="../technical-integration/getting-started.md" %}
[getting-started.md](../technical-integration/getting-started.md)
{% endcontent-ref %}
