# Account Sourcing

#### What is it?

Account Sourcing allows your customers to build their TAM directly from your dataset. They define their market using the filters you have made available, preview qualifying companies, and receive a continuously refreshed set of accounts.

Your customers never need to bring their own data, scrape LinkedIn, or burn credits on a third-party provider. The accounts come from your platform, powered by the dataset you built with GoodFit.

<br>

#### Why is it useful?

Today, most platforms offer their users one of three ways to source accounts: LinkedIn scraping, an expensive third-party query, or uploading a CSV. Each of these puts the burden on the customer and means the platform feels empty on day one.

Account Sourcing turns your platform into the source of truth. Your customer describes who they sell to, and your platform delivers the accounts immediately.

With Account Sourcing, you can:

* Provide a day-one populated experience for new customers
* Replace fragile LinkedIn scraping with structured, refreshed data
* Offer dynamic filters that no other provider supports such as "companies hiring data engineers in DACH"
* Keep the dataset alive, with new companies arriving and non-qualifying companies dropping out automatically

<br>

#### How it works

You can think of it in four steps.

**1. You build the dataset.** Working with GoodFit, you define which companies are in your dataset, which attributes are included, and how Dynamic blocks are configured. This happens once, with ongoing refinement. Your customers never see this layer.

**2. Your customer defines their market.** Inside your platform, your customer specifies their ICP using the filters you have exposed — company size, geography, industry, tech stack, team composition. These map to GoodFit data block attributes behind the scenes.

**3. They preview before committing.** Before anything enters their workspace, they see total market size, a sample of qualifying companies, and validation that their criteria make sense.

**4. Accounts flow continuously.** Once published, the market is alive. New qualifying companies arrive as they enter the market. Companies that no longer qualify drop out. Your customer works a living dataset, not a static export.



#### Available filters

Every data block can be used as a sourcing filter. Here are the most common:

| Filter                | Block                          | Example                                             |
| --------------------- | ------------------------------ | --------------------------------------------------- |
| Company size          | `firmographics.employee_count` | `{ "min": 50, "max": 500 }`                         |
| Geography             | `firmographics.country`        | `{ "in": ["United States", "Germany"] }`            |
| Business model        | `firmographics.is_b2b`         | `true`                                              |
| SaaS detection        | `firmographics.is_saas`        | `true`                                              |
| GTM model             | `firmographics.gtm_model`      | `{ "contains": "Product Led" }`                     |
| Tech stack            | `technologies`                 | `{ "match": ["Salesforce"], "has_matches": true }`  |
| Hiring activity       | `hiring.open_jobs`             | `{ "min": 5 }`                                      |
| Sales team exists     | `team_members`                 | `{ "departments": ["sales"], "has_matches": true }` |
| Job keywords          | `jobs`                         | `{ "titleKeywords": ["data engineer"] }`            |
| Classification Models | `predictive_labels`            | `{ "primary_label": "Vertical SaaS" }`              |

Dynamic blocks as filters are the differentiator. These are not static fields — they are queries you defined when building your dataset, and they produce signals that no other data provider can offer as sourcing criteria.
