---
title: Indicators
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Signals](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Indicators

##### [List Threat Signals article indicators](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/indicators/methods/list)

GET/accounts/{account\_id}/cloudforce-one/v2/threat-signals/indicators

##### ModelsExpand Collapse

<details>

<summary>

IndicatorListResponse object {indicators, pagination }

</summary>

<details>

<summary>

indicators: array of object {id, article\_id, article\_title, 5 more }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

article\_id: string

formatuuid

<a href="#">Link to this property</a>

article\_title: string

<a href="#">Link to this property</a>

dataset\_id: string

Threat Events dataset identifier for navigating from this indicator. Null when the account feeds dataset mapping is unavailable.

<a href="#">Link to this property</a>

feed\_display\_name: string

<a href="#">Link to this property</a>

feed\_id: string

formatuuid

<a href="#">Link to this property</a>

type: string

<a href="#">Link to this property</a>

value: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

pagination: object {count, cursor, has\_more, 4 more }

</summary>

count: number

minimum0

<a href="#">Link to this property</a>

cursor: string

<a href="#">Link to this property</a>

has\_more: boolean

<a href="#">Link to this property</a>

page: number

Ordinal of this cursor page; not a total-results offset.

minimum1

<a href="#">Link to this property</a>

per\_page: number

maximum100

minimum1

<a href="#">Link to this property</a>

total\_count: number

minimum0

<a href="#">Link to this property</a>

total\_count\_is\_exact: boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.indicators%20%3E%20(model)%20indicator_list_response%20%3E%20(schema)>)