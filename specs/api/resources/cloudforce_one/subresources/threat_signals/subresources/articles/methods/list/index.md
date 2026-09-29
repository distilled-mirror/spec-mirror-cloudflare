---
title: List Threat Signals articles
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Signals](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals)

[Articles](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_signals/subresources/articles)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List Threat Signals articles

GET/accounts/{account\_id}/cloudforce-one/v2/threat-signals/articles

Lists articles from the account’s Threat Signals feeds.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write``Cloudforce One Read`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

article\_id: optional array of string

Repeatable article UUID filter. Returns the union of matching account-owned articles; use this to list every Threat Signals article referenced by an indicator’s sources.

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20article_id%20%3E%20(schema)>)

cursor: optional string

Opaque cursor from a previous response’s `next_cursor`. When provided, pagination, ordering, totals, and article filters come from the cursor. Sending `per_page`, `sort`, `include_total`, or any article filter alongside it returns a 400 `CursorFilterConflictError`.

minLength1

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20cursor%20%3E%20(schema)>)

feed\_category: optional string

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20feed_category%20%3E%20(schema)>)

feed\_id: optional string

formatuuid

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20feed_id%20%3E%20(schema)>)

fetched\_after: optional string

formatdate-time

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20fetched_after%20%3E%20(schema)>)

fetched\_before: optional string

formatdate-time

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20fetched_before%20%3E%20(schema)>)

include\_total: optional boolean

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20include_total%20%3E%20(schema)>)

per\_page: optional number

maximum100

minimum1

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20per_page%20%3E%20(schema)>)

published\_after: optional string

formatdate-time

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20published_after%20%3E%20(schema)>)

published\_before: optional string

formatdate-time

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20published_before%20%3E%20(schema)>)

read: optional boolean

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20read%20%3E%20(schema)>)

search: optional string

maxLength500

minLength1

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20search%20%3E%20(schema)>)

sort: optional string

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20sort%20%3E%20(schema)>)

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

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20source_type%20%3E%20(schema)>)

Deprecatedtag: optional string

Legacy human-readable tag-value filter. Ignored when tag\_id is supplied; prefer tag\_id.

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20tag%20%3E%20(schema)>)

<details>

<summary>

tag\_applied\_by: optional "ai"or "analyst"or "system"

Assignment provenance filter. When combined with tag\_id or tag\_category\_id, the matching assignment must have this provenance.

</summary>

One of the following:

"ai"

<a href="#">Link to this property</a>

"analyst"

<a href="#">Link to this property</a>

"system"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20tag_applied_by%20%3E%20(schema)>)

Deprecatedtag\_category: optional string

Legacy category-name disambiguator for tag. It has no effect without tag; prefer tag\_category\_id.

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20tag_category%20%3E%20(schema)>)

tag\_category\_id: optional array of string

Repeatable tag-category UUID filter. An article matches any selected category; when tag\_id is also present, the tag and category groups are ANDed.

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20tag_category_id%20%3E%20(schema)>)

tag\_id: optional array of string

Repeatable tag UUID filter. An article matches any selected tag.

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20tag_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

result: object {articles, has\_more, next\_cursor, 2 more }

</summary>

<details>

<summary>

articles: array of object {id, dataset\_id, event\_id, 10 more }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

dataset\_id: string

Threat Events dataset identifier for the article redirect. Null when the account feeds dataset mapping is unavailable.

<a href="#">Link to this property</a>

event\_id: string

Threat Events event identifier associated with this article for a UI redirect. Null when no event has been linked.

<a href="#">Link to this property</a>

feed\_display\_name: string

<a href="#">Link to this property</a>

feed\_id: string

formatuuid

<a href="#">Link to this property</a>

fetched\_at: string

<a href="#">Link to this property</a>

link: string

<a href="#">Link to this property</a>

published\_at: string

<a href="#">Link to this property</a>

read: boolean

<a href="#">Link to this property</a>

read\_at: string

<a href="#">Link to this property</a>

summary: string

Persisted enrichment summary. Null until enrichment produces a summary.

<a href="#">Link to this property</a>

<details>

<summary>

tags: array of object {applied\_by, categoryId, uuid, value }

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

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

has\_more: boolean

<a href="#">Link to this property</a>

next\_cursor: string

<a href="#">Link to this property</a>

total\_count: number

<a href="#">Link to this property</a>

total\_count\_is\_exact: boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List Threat Signals articles

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/v2/threat-signals/articles \
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
    "articles": [
      {
        "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "dataset_id": "dataset_id",
        "event_id": "event_id",
        "feed_display_name": "feed_display_name",
        "feed_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "fetched_at": "fetched_at",
        "link": "link",
        "published_at": "published_at",
        "read": true,
        "read_at": "read_at",
        "summary": "summary",
        "tags": [
          {
            "applied_by": "ai",
            "categoryId": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
            "uuid": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
            "value": "value"
          }
        ],
        "title": "title"
      }
    ],
    "has_more": true,
    "next_cursor": "next_cursor",
    "total_count": 0,
    "total_count_is_exact": true
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
    "articles": [
      {
        "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "dataset_id": "dataset_id",
        "event_id": "event_id",
        "feed_display_name": "feed_display_name",
        "feed_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "fetched_at": "fetched_at",
        "link": "link",
        "published_at": "published_at",
        "read": true,
        "read_at": "read_at",
        "summary": "summary",
        "tags": [
          {
            "applied_by": "ai",
            "categoryId": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
            "uuid": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
            "value": "value"
          }
        ],
        "title": "title"
      }
    ],
    "has_more": true,
    "next_cursor": "next_cursor",
    "total_count": 0,
    "total_count_is_exact": true
  },
  "success": true
}
```