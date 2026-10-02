---
title: Add tag to Threat Signals article
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Signals](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals)

[Articles](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/articles)

[Tags](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/articles/subresources/tags)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Add tag to Threat Signals article

POST/accounts/{account\_id}/cloudforce-one/v2/threat-signals/articles/{article\_id}/tags

Applies a tag from the account’s tag catalog to a Threat Signals article.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20cloudforce_one.threat_signals.articles.tags%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

article\_id: string

formatuuid

[Link to this property](#)%20cloudforce_one.threat_signals.articles.tags%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20article_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

tag\_id: string

formatuuid

[Link to this property](#)%20cloudforce_one.threat_signals.articles.tags%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20tag_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.articles.tags%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {message, code, expected, 2 more }

</summary>

message: string

<a href="#">Link to this property</a>

code: optional number

<a href="#">Link to this property</a>

expected: optional string

<a href="#">Link to this property</a>

path: optional array of string

<a href="#">Link to this property</a>

<details>

<summary>

reason: optional "free\_custom\_feed\_limit"or "free\_custom\_skills\_disabled"or "free\_skill\_run\_disabled"or 4 more

</summary>

One of the following:

"free\_custom\_feed\_limit"

<a href="#">Link to this property</a>

"free\_custom\_skills\_disabled"

<a href="#">Link to this property</a>

"free\_skill\_run\_disabled"

<a href="#">Link to this property</a>

"free\_tier\_reconciliation\_in\_progress"

<a href="#">Link to this property</a>

"free\_tier\_reconciliation\_failed"

<a href="#">Link to this property</a>

"raw\_content\_expired"

<a href="#">Link to this property</a>

"curated\_visibility\_changed"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.articles.tags%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {applied\_by, categoryId, uuid, value }

</summary>

<details>

<summary>

applied\_by: "ai"or "analyst"or "system"

</summary>

One of the following:

"ai"

<a href="#">Link to this property</a>

"analyst"

<a href="#">Link to this property</a>

"system"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

categoryId: string

formatuuid

<a href="#">Link to this property</a>

uuid: string

formatuuid

<a href="#">Link to this property</a>

value: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.articles.tags%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20cloudforce_one.threat_signals.articles.tags%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Add tag to Threat Signals article

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/v2/threat-signals/articles/$ARTICLE_ID/tags \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "tag_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
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
      ],
      "reason": "free_custom_feed_limit"
    }
  ],
  "result": {
    "applied_by": "ai",
    "categoryId": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
    "uuid": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
    "value": "value"
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
      ],
      "reason": "free_custom_feed_limit"
    }
  ],
  "result": {
    "applied_by": "ai",
    "categoryId": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
    "uuid": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
    "value": "value"
  },
  "success": true
}
```