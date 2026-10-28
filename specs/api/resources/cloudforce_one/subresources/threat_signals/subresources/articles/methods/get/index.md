---
title: Get Threat Signals article
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

# Get Threat Signals article

GET/accounts/{account\_id}/cloudforce-one/v2/threat-signals/articles/{article\_id}

Retrieves a Threat Signals article with its summary, tags, indicator status and relevance to the account’s Priority Intelligence Requirements.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write``Cloudforce One Read`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

article\_id: string

Threat Signals article UUID

formatuuid

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20article_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

result: object {id, bullet\_points, content\_r2\_key, 18 more }

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

<details>

<summary>

relevance: object {band, pir\_id, pirs }

Beta. The article’s relevance to the account’s active Priority Intelligence Requirements. Null when the article has not been scored against them, including when the account has no active PIRs, or has not been scored against the requested pir\_id.

</summary>

<details>

<summary>

band: "low"or "medium"or "high"

Beta. How relevant the article is to a Priority Intelligence Requirement: high, medium, or low. Cloudflare may change the scores behind each band as relevance scoring is calibrated.

</summary>

One of the following:

"low"

<a href="#">Link to this property</a>

"medium"

<a href="#">Link to this property</a>

"high"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

pir\_id: string

Beta. The pir\_id requested from the article list, or otherwise the account’s most relevant active PIR for this article.

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

pirs: array of object {band, pir\_id }

Beta. Every active PIR the article was scored against, most relevant first. Draft and deleted PIRs are excluded.

</summary>

<details>

<summary>

band: "low"or "medium"or "high"

Beta. How relevant the article is to a Priority Intelligence Requirement: high, medium, or low. Cloudflare may change the scores behind each band as relevance scoring is calibrated.

</summary>

One of the following:

"low"

<a href="#">Link to this property</a>

"medium"

<a href="#">Link to this property</a>

"high"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

pir\_id: string

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

severity: "informational"or "low"or "medium"or 2 more

Beta. Intrinsic article severity band, from informational to critical, independent of any organisation or Priority Intelligence Requirement. Null when the account has no active Priority Intelligence Requirements, scoring has not completed, or a historic article has not entered an automatic rescore window.

</summary>

One of the following:

"informational"

<a href="#">Link to this property</a>

"low"

<a href="#">Link to this property</a>

"medium"

<a href="#">Link to this property</a>

"high"

<a href="#">Link to this property</a>

"critical"

<a href="#">Link to this property</a>

</details>

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

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20cloudforce_one.threat_signals.articles%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Get Threat Signals article

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/v2/threat-signals/articles/$ARTICLE_ID \
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
    "relevance": {
      "band": "low",
      "pir_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
      "pirs": [
        {
          "band": "low",
          "pir_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
        }
      ]
    },
    "severity": "informational",
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
    "relevance": {
      "band": "low",
      "pir_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
      "pirs": [
        {
          "band": "low",
          "pir_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
        }
      ]
    },
    "severity": "informational",
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