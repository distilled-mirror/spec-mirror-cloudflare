---
title: Create Threat Signals skill
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Signals](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals)

[Skills](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/skills)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Create Threat Signals skill

POST/accounts/{account\_id}/cloudforce-one/v2/threat-signals/skills

Creates a custom AI skill for the account.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

name: string

maxLength100

minLength1

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20name%20%3E%20(schema)>)

output\_schema: string

maxLength4096

minLength1

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20output_schema%20%3E%20(schema)>)

prompt: string

maxLength4000

minLength1

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20prompt%20%3E%20(schema)>)

<details>

<summary>

type: "summary"or "tags"

</summary>

One of the following:

"summary"

<a href="#">Link to this property</a>

"tags"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20type%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {id, config, created\_at, 7 more }

</summary>

id: string

<a href="#">Link to this property</a>

config: string

JSON-encoded skill configuration. Always null for default skills.

<a href="#">Link to this property</a>

created\_at: string

<a href="#">Link to this property</a>

is\_active: number

1 when active, 0 when inactive.

<a href="#">Link to this property</a>

name: string

<a href="#">Link to this property</a>

output\_schema: string

JSON-encoded JSON Schema the skill output must satisfy.

<a href="#">Link to this property</a>

prompt: string

<a href="#">Link to this property</a>

<details>

<summary>

source: "default"or "custom"

<code>default</code> for Cloudforce One managed skills (read-only), <code>custom</code> for account skills.

</summary>

One of the following:

"default"

<a href="#">Link to this property</a>

"custom"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

type: string

<a href="#">Link to this property</a>

updated\_at: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Create Threat Signals skill

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/v2/threat-signals/skills \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "name": "x",
          "output_schema": "x",
          "prompt": "x",
          "type": "summary"
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
    "id": "id",
    "config": "config",
    "created_at": "created_at",
    "is_active": 0,
    "name": "name",
    "output_schema": "output_schema",
    "prompt": "prompt",
    "source": "default",
    "type": "summary",
    "updated_at": "updated_at"
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
    "id": "id",
    "config": "config",
    "created_at": "created_at",
    "is_active": 0,
    "name": "name",
    "output_schema": "output_schema",
    "prompt": "prompt",
    "source": "default",
    "type": "summary",
    "updated_at": "updated_at"
  },
  "success": true
}
```