---
title: Delete Threat Signals feed
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

# Delete Threat Signals feed

DELETE/accounts/{account\_id}/cloudforce-one/v2/threat-signals/feeds/{feed\_id}

Unsubscribes the account from a Threat Signals feed and deletes its articles.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

feed\_id: string

formatuuid

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20feed_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20delete%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20delete%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

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

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20delete%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20cloudforce_one.threat_signals.feeds%20%3E%20(method)%20delete%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Delete Threat Signals feed

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/v2/threat-signals/feeds/$FEED_ID \
    -X DELETE \
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
      "expected": "expected",
      "path": [
        "string"
      ],
      "reason": "free_custom_feed_limit"
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