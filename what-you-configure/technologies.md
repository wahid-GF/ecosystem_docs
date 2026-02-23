# Technologies

Custom technology stack detection. You define the technologies you care about during setup, and GoodFit tells you which companies in your dataset use them.

{% hint style="info" %}
Technographic targeting is one of the highest-signal filters for sales teams. Partners use it to identify companies running complementary or competing tools, or to detect adoption of specific frameworks and platforms.
{% endhint %}

## How it works

You provide a list of technologies during configuration (e.g. "Salesforce", "React", "Snowflake"). GoodFit detects technologies through two channels: direct website page crawling (scanning source code, script tags, and library references) and job description analysis (parsing open roles for technology mentions). This dual approach catches technologies that might only surface in one channel.

For each company, you'll know whether they use any of your configured technologies and which ones were detected. Results update as websites change and new job descriptions are published.

{% hint style="warning" %}
**This is a configurable package.** Results depend entirely on the technology list you define during dataset setup. No technologies configured means no results returned.
{% endhint %}
