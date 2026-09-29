---
title: Skill Outputs
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Signals](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals)

[Articles](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/articles)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Skill Outputs

##### [Get Threat Signals article skill output](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/articles/subresources/skill_outputs/methods/get)

GET/accounts/{account\_id}/cloudforce-one/v2/threat-signals/articles/{article\_id}/skills/{skill\_id}/output

##### ModelsExpand Collapse

<details>

<summary>

SkillOutputGetResponse object {article\_id, custom\_skill\_version, output\_schema, 2 more }

</summary>

article\_id: string

formatuuid

<a href="#">Link to this property</a>

custom\_skill\_version: string

<a href="#">Link to this property</a>

output\_schema: string

JSON-encoded output schema of the skill. Null when the skill no longer exists.

<a href="#">Link to this property</a>

skill\_id: string

<a href="#">Link to this property</a>

custom\_output: optional unknown

Skill output. Parsed JSON when the stored output is valid JSON, otherwise the raw string.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.articles.skill_outputs%20%3E%20(model)%20skill_output_get_response%20%3E%20(schema)>)