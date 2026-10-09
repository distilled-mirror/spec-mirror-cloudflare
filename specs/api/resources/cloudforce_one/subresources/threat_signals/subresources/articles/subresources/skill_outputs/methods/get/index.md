---
title: Get Threat Signals article skill output
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Signals](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals)

[Articles](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/articles)

[Skill Outputs](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/articles/subresources/skill_outputs)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Get Threat Signals article skill output

GET/accounts/{account\_id}/cloudforce-one/v2/threat-signals/articles/{article\_id}/skills/{skill\_id}/output

Retrieves the stored output of a skill for a Threat Signals article.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write``Cloudforce One Read`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20cloudforce_one.threat_signals.articles.skill_outputs%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

article\_id: string

formatuuid

[Link to this property](#)%20cloudforce_one.threat_signals.articles.skill_outputs%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20article_id%20%3E%20(schema)>)

skill\_id: string

[Link to this property](#)%20cloudforce_one.threat_signals.articles.skill_outputs%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20skill_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.articles.skill_outputs%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {message, code, custom\_feed\_count, 4 more }

</summary>

message: string

<a href="#">Link to this property</a>

code: optional number

<a href="#">Link to this property</a>

custom\_feed\_count: optional number

The current count of custom feeds for the account.

minimum0

<a href="#">Link to this property</a>

custom\_feed\_limit: optional number

The custom feed limit for the account.

minimum0

<a href="#">Link to this property</a>

expected: optional string

<a href="#">Link to this property</a>

path: optional array of string

<a href="#">Link to this property</a>

<details>

<summary>

reason: optional "threat\_signals\_feed\_limit"or "free\_custom\_skills\_disabled"or "free\_skill\_run\_disabled"or 4 more

</summary>

One of the following:

"threat\_signals\_feed\_limit"

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

[Link to this property](#)%20cloudforce_one.threat_signals.articles.skill_outputs%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {article\_id, custom\_output, custom\_output\_parse\_status, 4 more }

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

[Link to this property](#)%20cloudforce_one.threat_signals.articles.skill_outputs%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20cloudforce_one.threat_signals.articles.skill_outputs%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Get Threat Signals article skill output

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/v2/threat-signals/articles/$ARTICLE_ID/skills/$SKILL_ID/output \
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
  "messages": [
    {
      "message": "message",
      "code": 0,
      "custom_feed_count": 0,
      "custom_feed_limit": 0,
      "expected": "expected",
      "path": [
        "string"
      ],
      "reason": "threat_signals_feed_limit"
    }
  ],
  "result": {
    "article_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
    "custom_output": "string",
    "custom_output_parse_status": "parsed",
    "custom_output_validation_status": "valid",
    "custom_skill_version": "custom_skill_version",
    "output_schema": "output_schema",
    "skill_id": "skill_id"
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
      "custom_feed_count": 0,
      "custom_feed_limit": 0,
      "expected": "expected",
      "path": [
        "string"
      ],
      "reason": "threat_signals_feed_limit"
    }
  ],
  "result": {
    "article_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
    "custom_output": "string",
    "custom_output_parse_status": "parsed",
    "custom_output_validation_status": "valid",
    "custom_skill_version": "custom_skill_version",
    "output_schema": "output_schema",
    "skill_id": "skill_id"
  },
  "success": true
}
```