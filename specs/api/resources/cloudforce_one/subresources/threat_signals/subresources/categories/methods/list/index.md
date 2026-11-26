---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: List Threat Signals feed categories
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Signals](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals)

[Categories](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/categories)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# List Threat Signals feed categories

GET/accounts/{account\_id}/cloudforce-one/v2/threat-signals/categories

Lists the predefined categories that can be assigned to feeds.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write` `Cloudforce One Read`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20cloudforce_one.threat_signals.categories%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object { message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.categories%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

result: object { categories }

</summary>

<details>

<summary>

categories: array of object { id, description, name }

</summary>

id: string

Wire value accepted by the feed <code>category_id</code> field.

formatuuid

<a href="#">Link to this property</a>

description: string

Plain-language description of the category.

<a href="#">Link to this property</a>

name: string

Human-readable display label.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.categories%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20cloudforce_one.threat_signals.categories%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List Threat Signals feed categories

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/v2/threat-signals/categories \
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
    "categories": [
      {
        "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "description": "description",
        "name": "name"
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
    "categories": [
      {
        "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "description": "description",
        "name": "name"
      }
    ]
  },
  "success": true
}
```