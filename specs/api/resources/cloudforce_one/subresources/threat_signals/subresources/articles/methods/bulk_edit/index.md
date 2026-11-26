---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Bulk update Threat Signals article read status
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Signals](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals)

[Articles](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/articles)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Bulk update Threat Signals article read status

PATCH/accounts/{account\_id}/cloudforce-one/v2/threat-signals/articles

Marks up to 50 Threat Signals articles as read or unread.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20bulk_edit%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

article\_ids: array of string

Array of article UUIDs to mark (1-50).

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20bulk_edit%20%3E%20(params)%200%20%3E%20(param)%20article_ids%20%3E%20(schema)>)

read: boolean

True to mark read, false to mark unread.

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20bulk_edit%20%3E%20(params)%200%20%3E%20(param)%20read%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object { message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20bulk_edit%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object { message, code, expected, path }

</summary>

message: string

<a href="#">Link to this property</a>

code: optional number

<a href="#">Link to this property</a>

expected: optional string

<a href="#">Link to this property</a>

path: optional array of string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20bulk_edit%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object { updated\_count }

</summary>

updated\_count: number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20bulk_edit%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20bulk_edit%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Bulk update Threat Signals article read status

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/v2/threat-signals/articles \
    -X PATCH \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "article_ids": [
            "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
          ],
          "read": true
        }'
```

200 example

```
{
  "errors": [
    {
      "message": "message"
    }
  ],
  "messages": [
    {
      "message": "message",
      "code": 0,
      "expected": "expected",
      "path": [
        "string"
      ]
    }
  ],
  "result": {
    "updated_count": 0
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
  "messages": [
    {
      "message": "message",
      "code": 0,
      "expected": "expected",
      "path": [
        "string"
      ]
    }
  ],
  "result": {
    "updated_count": 0
  },
  "success": true
}
```