---
title: List Threat Signals skills
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

# List Threat Signals skills

GET/accounts/{account\_id}/cloudforce-one/v2/threat-signals/skills

Lists the default and custom skills available to the account.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write``Cloudforce One Read`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

page: optional number

minimum1

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20page%20%3E%20(schema)>)

per\_page: optional number

maximum100

minimum1

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20per_page%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

reason: optional "free\_custom\_feed\_limit"or "free\_custom\_skills\_disabled"or "free\_tier\_reconciliation\_in\_progress"or 3 more

</summary>

One of the following:

"free\_custom\_feed\_limit"

<a href="#">Link to this property</a>

"free\_custom\_skills\_disabled"

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

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {count, custom\_skills\_available, page, 3 more }

</summary>

count: number

Number of skills on this page.

<a href="#">Link to this property</a>

custom\_skills\_available: boolean

Whether the authenticated account may access custom-skill capabilities under Stakeout’s Threat Signals access-mode policy. This is a policy availability indicator, not a row-existence indicator. False for threat\_signals\_only mode; true for entitled, allowlisted, cfone\_internal, and service modes.

<a href="#">Link to this property</a>

page: number

<a href="#">Link to this property</a>

per\_page: number

<a href="#">Link to this property</a>

<details>

<summary>

skills: array of object {id, config, created\_at, 7 more }

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

<a href="#">Link to this property</a>

total\_count: number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20cloudforce_one.threat_signals.skills%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List Threat Signals skills

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/v2/threat-signals/skills \
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
      "expected": "expected",
      "path": [
        "string"
      ],
      "reason": "free_custom_feed_limit"
    }
  ],
  "result": {
    "count": 0,
    "custom_skills_available": true,
    "page": 0,
    "per_page": 0,
    "skills": [
      {
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
      }
    ],
    "total_count": 0
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
    "count": 0,
    "custom_skills_available": true,
    "page": 0,
    "per_page": 0,
    "skills": [
      {
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
      }
    ],
    "total_count": 0
  },
  "success": true
}
```