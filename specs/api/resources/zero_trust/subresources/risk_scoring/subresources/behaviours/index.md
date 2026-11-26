---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Behaviours
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Risk Scoring](https://developers.cloudflare.com/api/resources/zero_trust/subresources/risk_scoring)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Behaviours

##### [Get all behaviors and associated configuration](https://developers.cloudflare.com/api/resources/zero_trust/subresources/risk_scoring/subresources/behaviours/methods/get)

GET/accounts/{account\_id}/zt\_risk\_scoring/behaviors

##### [Update configuration for risk behaviors](https://developers.cloudflare.com/api/resources/zero_trust/subresources/risk_scoring/subresources/behaviours/methods/update)

PUT/accounts/{account\_id}/zt\_risk\_scoring/behaviors

##### ModelsExpand Collapse

<details>

<summary>

BehaviourGetResponse object { behaviors }

Risk behaviors, keyed by behavior ID.

</summary>

<details>

<summary>

behaviors: map\[object { description, enabled, name, 2 more } ]

Risk behaviors, keyed by behavior ID.

</summary>

description: string

Explains what the behavior detects.

<a href="#">Link to this property</a>

enabled: boolean

Whether the behavior counts toward the risk score.

<a href="#">Link to this property</a>

name: string

Display name of the behavior.

<a href="#">Link to this property</a>

points: number

Risk score points of a behavior.

maximum100

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

risk\_level: "info" or "low" or "medium" or "high"

Risk level of a behavior or an event.

</summary>

One of the following:

"info"

<a href="#">Link to this property</a>

"low"

<a href="#">Link to this property</a>

"medium"

<a href="#">Link to this property</a>

"high"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.risk_scoring.behaviours%20%3E%20(model)%20behaviour_get_response%20%3E%20(schema)>)

<details>

<summary>

BehaviourUpdateResponse object { behaviors }

Risk behaviors, keyed by behavior ID.

</summary>

<details>

<summary>

behaviors: map\[object { description, enabled, name, 2 more } ]

Risk behaviors, keyed by behavior ID.

</summary>

description: string

Explains what the behavior detects.

<a href="#">Link to this property</a>

enabled: boolean

Whether the behavior counts toward the risk score.

<a href="#">Link to this property</a>

name: string

Display name of the behavior.

<a href="#">Link to this property</a>

points: number

Risk score points of a behavior.

maximum100

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

risk\_level: "info" or "low" or "medium" or "high"

Risk level of a behavior or an event.

</summary>

One of the following:

"info"

<a href="#">Link to this property</a>

"low"

<a href="#">Link to this property</a>

"medium"

<a href="#">Link to this property</a>

"high"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.risk_scoring.behaviours%20%3E%20(model)%20behaviour_update_response%20%3E%20(schema)>)