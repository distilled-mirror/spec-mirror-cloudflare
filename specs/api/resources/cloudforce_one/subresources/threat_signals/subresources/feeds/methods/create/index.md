---
title: Create Threat Signals feed
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

# Create Threat Signals feed

POST/accounts/{account\_id}/cloudforce-one/v2/threat-signals/feeds

Subscribes the account to a custom or curated Threat Signals feed.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

<details>

<summary>

category\_id: optional "b12a0fd6-f7b9-5393-9ef3-f888d506c550"or "d5b70eaa-626f-5761-b55b-6d9590df49fb"or "3b572d2b-890d-5286-9433-f18c85079030"or 5 more

One of the predefined Threat Signals feed categories; see GET /:account\_id/v2/threat-signals/categories.

</summary>

One of the following:

"b12a0fd6-f7b9-5393-9ef3-f888d506c550"

<a href="#">Link to this property</a>

"d5b70eaa-626f-5761-b55b-6d9590df49fb"

<a href="#">Link to this property</a>

"3b572d2b-890d-5286-9433-f18c85079030"

<a href="#">Link to this property</a>

"17f90d3b-37d3-5241-8ad4-7d6abbc2006c"

<a href="#">Link to this property</a>

"c68f28e9-7e8f-5d4b-853b-f3076893a9ee"

<a href="#">Link to this property</a>

"bb0e4a94-38ab-5c14-80a7-28cee9f4b139"

<a href="#">Link to this property</a>

"b1ef66d9-a73c-58dc-b269-22d34dfd11f4"

<a href="#">Link to this property</a>

"ab02a976-0a20-5c76-a553-7f6325afacfe"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20category_id%20%3E%20(schema)>)

curated\_feed\_id: optional string

formatuuid

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20curated_feed_id%20%3E%20(schema)>)

display\_name: optional string

maxLength255

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20display_name%20%3E%20(schema)>)

enabled: optional boolean

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20enabled%20%3E%20(schema)>)

poll\_interval\_s: optional number

maximum86400

minimum60

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20poll_interval_s%20%3E%20(schema)>)

title: optional string

maxLength255

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20title%20%3E%20(schema)>)

url: optional string

formaturi

maxLength2048

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20url%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {id, category\_id, category\_name, 12 more }

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

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Create Threat Signals feed

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/v2/threat-signals/feeds \
    -X POST \
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
  },
  "success": true
}
```