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

SkillOutputGetResponse object {article\_id, custom\_output, custom\_output\_parse\_status, 4 more }

</summary>

article\_id: string

Article UUID that received the skill output.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

custom\_output: stringor numberor booleanor 2 more

Untrusted model output: parsed JSON when the stored completion text is valid JSON, otherwise raw text. Consumers must safely render or escape it.

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

boolean

<a href="#">Link to this property</a>

array of unknown

<a href="#">Link to this property</a>

map\[unknown]

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

custom\_output\_parse\_status: "parsed"or "invalid\_json"

Whether custom\_output was parsed from the stored completion text.

</summary>

One of the following:

"parsed"

<a href="#">Link to this property</a>

"invalid\_json"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

custom\_output\_validation\_status: "valid"or "invalid\_json"or "schema\_invalid"or "unknown"

Non-blocking validation classification for untrusted model output. <code>unknown</code> is retained only for historical rows.

</summary>

One of the following:

"valid"

<a href="#">Link to this property</a>

"invalid\_json"

<a href="#">Link to this property</a>

"schema\_invalid"

<a href="#">Link to this property</a>

"unknown"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

custom\_skill\_version: string

Custom Skill version that produced the output. Null when historical metadata is unavailable.

<a href="#">Link to this property</a>

output\_schema: string

JSON-encoded output schema. Null when historical skill metadata is unavailable.

<a href="#">Link to this property</a>

skill\_id: string

Custom Skill UUID that produced the output.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.articles.skill_outputs%20%3E%20(model)%20skill_output_get_response%20%3E%20(schema)>)