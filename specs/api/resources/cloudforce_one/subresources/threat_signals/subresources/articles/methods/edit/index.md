---
title: Update Threat Signals article read status
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

# Update Threat Signals article read status

PATCH/accounts/{account\_id}/cloudforce-one/v2/threat-signals/articles/{article\_id}

Marks a Threat Signals article as read or unread.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20edit%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

article\_id: string

formatuuid

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20edit%20%3E%20(params)%20default%20%3E%20(param)%20article_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

read: boolean

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20edit%20%3E%20(params)%200%20%3E%20(param)%20read%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20edit%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

result: object {id, bullet\_points, content\_r2\_key, 16 more }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

bullet\_points: object {impact, what\_happened, who\_affected }

</summary>

impact: string

<a href="#">Link to this property</a>

what\_happened: string

<a href="#">Link to this property</a>

who\_affected: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

content\_r2\_key: string

<a href="#">Link to this property</a>

feed\_display\_name: string

<a href="#">Link to this property</a>

feed\_id: string

formatuuid

<a href="#">Link to this property</a>

fetched\_at: string

<a href="#">Link to this property</a>

<details>

<summary>

indicator\_extraction\_status: "in\_progress"or "complete"or "failed"or "unknown"

Progress of the article’s indicator extraction and IOC contextualization run. complete and failed are terminal; unknown means no run has been recorded.

</summary>

One of the following:

"in\_progress"

<a href="#">Link to this property</a>

"complete"

<a href="#">Link to this property</a>

"failed"

<a href="#">Link to this property</a>

"unknown"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

link: string

<a href="#">Link to this property</a>

metadata: map\[unknown]

<a href="#">Link to this property</a>

published\_at: string

<a href="#">Link to this property</a>

read: boolean

<a href="#">Link to this property</a>

read\_at: string

<a href="#">Link to this property</a>

source\_count: number

<a href="#">Link to this property</a>

summary: string

Persisted enrichment summary. Null until enrichment produces a summary.

<a href="#">Link to this property</a>

summary\_r2\_key: string

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

skill\_version: optional string

<a href="#">Link to this property</a>

tag\_skill\_version: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20edit%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20edit%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Update Threat Signals article read status

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/v2/threat-signals/articles/$ARTICLE_ID \
    -X PATCH \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
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
  "result": {
    "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
    "bullet_points": {
      "impact": "impact",
      "what_happened": "what_happened",
      "who_affected": "who_affected"
    },
    "content_r2_key": "content_r2_key",
    "feed_display_name": "feed_display_name",
    "feed_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
    "fetched_at": "fetched_at",
    "indicator_extraction_status": "in_progress",
    "link": "link",
    "metadata": {
      "foo": "bar"
    },
    "published_at": "published_at",
    "read": true,
    "read_at": "read_at",
    "source_count": 0,
    "summary": "summary",
    "summary_r2_key": "summary_r2_key",
    "tags": [
      {
        "applied_by": "ai",
        "categoryId": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "uuid": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "value": "value"
      }
    ],
    "title": "title",
    "skill_version": "skill_version",
    "tag_skill_version": "tag_skill_version"
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
    "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
    "bullet_points": {
      "impact": "impact",
      "what_happened": "what_happened",
      "who_affected": "who_affected"
    },
    "content_r2_key": "content_r2_key",
    "feed_display_name": "feed_display_name",
    "feed_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
    "fetched_at": "fetched_at",
    "indicator_extraction_status": "in_progress",
    "link": "link",
    "metadata": {
      "foo": "bar"
    },
    "published_at": "published_at",
    "read": true,
    "read_at": "read_at",
    "source_count": 0,
    "summary": "summary",
    "summary_r2_key": "summary_r2_key",
    "tags": [
      {
        "applied_by": "ai",
        "categoryId": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "uuid": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
        "value": "value"
      }
    ],
    "title": "title",
    "skill_version": "skill_version",
    "tag_skill_version": "tag_skill_version"
  },
  "success": true
}
```