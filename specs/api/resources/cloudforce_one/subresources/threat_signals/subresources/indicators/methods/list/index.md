---
title: List Threat Signals article indicators
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Signals](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals)

[Indicators](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/indicators)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List Threat Signals article indicators

GET/accounts/{account\_id}/cloudforce-one/v2/threat-signals/indicators

Lists indicators of compromise extracted from the account’s Threat Signals articles.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write``Cloudforce One Read`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20cloudforce_one.threat_signals.indicators%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

article\_id: optional string

formatuuid

[Link to this property](#)%20cloudforce_one.threat_signals.indicators%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20article_id%20%3E%20(schema)>)

cursor: optional string

minLength1

[Link to this property](#)%20cloudforce_one.threat_signals.indicators%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20cursor%20%3E%20(schema)>)

feed\_id: optional string

formatuuid

[Link to this property](#)%20cloudforce_one.threat_signals.indicators%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20feed_id%20%3E%20(schema)>)

include\_total: optional boolean

[Link to this property](#)%20cloudforce_one.threat_signals.indicators%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20include_total%20%3E%20(schema)>)

per\_page: optional number

maximum100

minimum1

[Link to this property](#)%20cloudforce_one.threat_signals.indicators%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20per_page%20%3E%20(schema)>)

search: optional string

NFC-normalized and trimmed, case-insensitive literal substring search of indicator values. Requires 3–500 Unicode code points; the upper code-point bound is described here because OpenAPI string length cannot precisely express it without imposing UTF-16 semantics.

[Link to this property](#)%20cloudforce_one.threat_signals.indicators%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20search%20%3E%20(schema)>)

sort: optional string

[Link to this property](#)%20cloudforce_one.threat_signals.indicators%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20sort%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.indicators%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

result: object {indicators, pagination }

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

[Link to this property](#)%20cloudforce_one.threat_signals.indicators%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20cloudforce_one.threat_signals.indicators%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List Threat Signals article indicators

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/v2/threat-signals/indicators \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "errors": [
    {
      "message": "message"
    }
  ],
  "result": {
    "indicators": [
      {
        "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "article_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "article_title": "article_title",
        "dataset_id": "dataset_id",
        "feed_display_name": "feed_display_name",
        "feed_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "type": "type",
        "value": "value"
      }
    ],
    "pagination": {
      "count": 0,
      "cursor": "cursor",
      "has_more": true,
      "page": 1,
      "per_page": 1,
      "total_count": 0,
      "total_count_is_exact": true
    }
  },
  "success": true
}
```

##### Returns Examples

200 example

```
{
  "errors": [
    {
      "message": "message"
    }
  ],
  "result": {
    "indicators": [
      {
        "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "article_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "article_title": "article_title",
        "dataset_id": "dataset_id",
        "feed_display_name": "feed_display_name",
        "feed_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "type": "type",
        "value": "value"
      }
    ],
    "pagination": {
      "count": 0,
      "cursor": "cursor",
      "has_more": true,
      "page": 1,
      "per_page": 1,
      "total_count": 0,
      "total_count_is_exact": true
    }
  },
  "success": true
}
```