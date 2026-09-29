---
title: Search Threat Signals articles using AI Search
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Signals](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Search Threat Signals articles using AI Search

GET/accounts/{account\_id}/cloudforce-one/v2/threat-signals/search

Searches the account’s Threat Signals articles using keyword and semantic retrieval.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write``Cloudforce One Read`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20cloudforce_one.threat_signals%20%3E%20(method)%20search%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

query: string

maxLength1000

minLength1

[Link to this property](#)%20cloudforce_one.threat_signals%20%3E%20(method)%20search%20%3E%20(params)%20default%20%3E%20(param)%20query%20%3E%20(schema)>)

feed\_id: optional string

formatuuid

[Link to this property](#)%20cloudforce_one.threat_signals%20%3E%20(method)%20search%20%3E%20(params)%20default%20%3E%20(param)%20feed_id%20%3E%20(schema)>)

<details>

<summary>

max\_results: optional ""or string

</summary>

One of the following:

""

<a href="#">Link to this property</a>

string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals%20%3E%20(method)%20search%20%3E%20(params)%20default%20%3E%20(param)%20max_results%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals%20%3E%20(method)%20search%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

result: object {count, results }

</summary>

count: number

Number of unique article candidates returned in this response. Equal to results.length.

minimum0

<a href="#">Link to this property</a>

<details>

<summary>

results: array of object {article\_id, dataset\_id, event\_id, 3 more }

</summary>

article\_id: string

formatuuid

<a href="#">Link to this property</a>

dataset\_id: string

formatuuid

<a href="#">Link to this property</a>

event\_id: string

formatuuid

<a href="#">Link to this property</a>

feed\_id: string

formatuuid

<a href="#">Link to this property</a>

score: number

<a href="#">Link to this property</a>

text: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals%20%3E%20(method)%20search%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20cloudforce_one.threat_signals%20%3E%20(method)%20search%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Search Threat Signals articles using AI Search

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/v2/threat-signals/search \
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
    "count": 0,
    "results": [
      {
        "article_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "dataset_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "event_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "feed_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "score": 0,
        "text": "text"
      }
    ]
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
    "count": 0,
    "results": [
      {
        "article_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "dataset_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "event_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "feed_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "score": 0,
        "text": "text"
      }
    ]
  },
  "success": true
}
```