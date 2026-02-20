# Technologies

Technology stack detection. You define the technologies you care about during setup, and these fields tell you whether a company uses them.

{% hint style="info" %}
Technographic targeting is one of the highest-signal filters for sales teams. Partners use it to identify companies running complementary or competing tools, or to detect adoption of specific frameworks and platforms.
{% endhint %}

## Fields

| Field | Description | Example |
| --- | --- | --- |
| Has technologies that match \* | Whether matching technology was identified via company website or job descriptions | true |
| List of technologies that match \* | List of technologies identified via company website or job descriptions | Salesforce, React, AWS |

{% hint style="warning" %}
**Both fields are configurable.** Results depend on the technology list you define during dataset setup.
{% endhint %}

### How it works

You provide a list of technologies during configuration (e.g. "Salesforce", "React", "Snowflake"). GoodFit detects technologies through two channels: direct website page crawling (scanning source code, script tags, and library references) and job description analysis (parsing open roles for technology mentions). This dual approach catches technologies that might only surface in one channel.
