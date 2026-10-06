---
title: List Threat Signals feeds
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Signals](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals)

[Feeds](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/feeds)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List Threat Signals feeds

GET/accounts/{account\_id}/cloudforce-one/v2/threat-signals/feeds

Lists the account’s Threat Signals feed subscriptions.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write``Cloudforce One Read`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

category: optional string

maxLength100

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20category%20%3E%20(schema)>)

enabled: optional boolean

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20enabled%20%3E%20(schema)>)

limit: optional number

maximum100

minimum1

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20limit%20%3E%20(schema)>)

page: optional number

minimum1

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20page%20%3E%20(schema)>)

per\_page: optional number

maximum100

minimum1

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20per_page%20%3E%20(schema)>)

sort: optional string

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20sort%20%3E%20(schema)>)

<details>

<summary>

source\_type: optional "curated"or "custom"

</summary>

One of the following:

"curated"

<a href="#">Link to this property</a>

"custom"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20source_type%20%3E%20(schema)>)

status: optional string

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20status%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {count, custom\_feed\_count, custom\_feed\_limit, 4 more }

</summary>

count: number

Number of feeds on this page.

<a href="#">Link to this property</a>

custom\_feed\_count: number

The current count of custom feeds for the account.

minimum0

<a href="#">Link to this property</a>

custom\_feed\_limit: number

The resolved custom feed limit for the account.

minimum0

<a href="#">Link to this property</a>

<details>

<summary>

feeds: array of object {id, category\_id, category\_name, 12 more }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

category\_id: string

Feed category identifier. Null when unset.

<a href="#">Link to this property</a>

category\_name: string

Display name of the feed category. Null when unset or unresolvable.

<a href="#">Link to this property</a>

created\_at: string

<a href="#">Link to this property</a>

curated\_feed\_id: string

Curated catalog feed this subscription was created from. Null for custom feeds.

<a href="#">Link to this property</a>

display\_name: string

<a href="#">Link to this property</a>

enabled: boolean

<a href="#">Link to this property</a>

last\_polled\_at: string

<a href="#">Link to this property</a>

poll\_interval\_s: number

<a href="#">Link to this property</a>

source\_type: string

<code>custom</code> for a feed added by URL, <code>curated</code> for a curated catalog feed.

<a href="#">Link to this property</a>

status: string

Polling health: <code>active</code>, or <code>error</code> after a failed poll.

<a href="#">Link to this property</a>

subscribed\_at: string

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

updated\_at: string

<a href="#">Link to this property</a>

url: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

page: number

<a href="#">Link to this property</a>

per\_page: number

<a href="#">Link to this property</a>

total\_count: number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List Threat Signals feeds

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/v2/threat-signals/feeds \
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
    "count": 0,
    "custom_feed_count": 0,
    "custom_feed_limit": 0,
    "feeds": [
      {
        "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "category_id": "category_id",
        "category_name": "category_name",
        "created_at": "created_at",
        "curated_feed_id": "curated_feed_id",
        "display_name": "display_name",
        "enabled": true,
        "last_polled_at": "last_polled_at",
        "poll_interval_s": 0,
        "source_type": "custom",
        "status": "active",
        "subscribed_at": "subscribed_at",
        "title": "title",
        "updated_at": "updated_at",
        "url": "url"
      }
    ],
    "page": 0,
    "per_page": 0,
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
    "count": 0,
    "custom_feed_count": 0,
    "custom_feed_limit": 0,
    "feeds": [
      {
        "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "category_id": "category_id",
        "category_name": "category_name",
        "created_at": "created_at",
        "curated_feed_id": "curated_feed_id",
        "display_name": "display_name",
        "enabled": true,
        "last_polled_at": "last_polled_at",
        "poll_interval_s": 0,
        "source_type": "custom",
        "status": "active",
        "subscribed_at": "subscribed_at",
        "title": "title",
        "updated_at": "updated_at",
        "url": "url"
      }
    ],
    "page": 0,
    "per_page": 0,
    "total_count": 0
  },
  "success": true
}
```