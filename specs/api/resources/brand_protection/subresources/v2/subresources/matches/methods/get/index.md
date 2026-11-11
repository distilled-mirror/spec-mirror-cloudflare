---
title: List domain matches
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Brand Protection](https://developers.cloudflare.com/api/resources/brand_protection)

[V2](https://developers.cloudflare.com/api/resources/brand_protection/subresources/v2)

[Matches](https://developers.cloudflare.com/api/resources/brand_protection/subresources/v2/subresources/matches)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List domain matches

GET/accounts/{account\_id}/cloudforce-one/v2/brand-protection/domain/matches

Lists domains that matched one or more saved domain queries, most recently matched first by default. When you pass several comma-separated `query_id` values, matches are deduplicated by domain and each match includes a `match_details` array with per-query dismissed state. Set `include_domain_id=true` to get the `domain_id` needed to dismiss or undismiss a match.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write``Cloudforce One Read`

##### P ath ParametersExpand Collapse

account\_id: string

minLength1

[Link to this property](#)%20brand_protection.v2.matches%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

query\_id: array of string

ID of a domain query, or a comma-separated list of domain query IDs. When you pass several IDs, matches are deduplicated by domain and each match includes a `match_details` array with per-query metadata and dismissed state.

[Link to this property](#)%20brand_protection.v2.matches%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20query_id%20%3E%20(schema)>)

domain\_search: optional string

Return only matches whose domain contains this text (case-insensitive).

[Link to this property](#)%20brand_protection.v2.matches%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20domain_search%20%3E%20(schema)>)

include\_dismissed: optional string

Set to `false` to exclude dismissed matches. Dismissed matches are included when this is omitted or `true`.

[Link to this property](#)%20brand_protection.v2.matches%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20include_dismissed%20%3E%20(schema)>)

include\_domain\_id: optional string

Set to `true` to include `domain_id` on each match. Required to dismiss or undismiss a match. Defaults to `false`.

[Link to this property](#)%20brand_protection.v2.matches%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20include_domain_id%20%3E%20(schema)>)

limit: optional string

Maximum number of matches to return. Defaults to 50.

[Link to this property](#)%20brand_protection.v2.matches%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20limit%20%3E%20(schema)>)

offset: optional string

Number of matches to skip, for pagination. Defaults to 0.

[Link to this property](#)%20brand_protection.v2.matches%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20offset%20%3E%20(schema)>)

<details>

<summary>

order: optional "asc"or "desc"

Sort direction: <code>asc</code> or <code>desc</code>. Defaults to <code>desc</code>. For single-query requests, <code>asc</code> applies only when <code>orderBy</code> is set.

</summary>

One of the following:

"asc"

<a href="#">Link to this property</a>

"desc"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20brand_protection.v2.matches%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20order%20%3E%20(schema)>)

<details>

<summary>

orderBy: optional "domain"or "first\_seen"or "registrar"

Field to sort by: <code>domain</code>, <code>first_seen</code>, or <code>registrar</code>. Defaults to <code>first_seen</code>.

</summary>

One of the following:

"domain"

<a href="#">Link to this property</a>

"first\_seen"

<a href="#">Link to this property</a>

"registrar"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20brand_protection.v2.matches%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20orderBy%20%3E%20(schema)>)

<details>

<summary>

quality: optional "high"or "low"

Filter matches by quality. Options: ‘high’ or ‘low’

</summary>

One of the following:

"high"

<a href="#">Link to this property</a>

"low"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20brand_protection.v2.matches%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20quality%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

matches: array of object {ai\_verdict, domain, edit\_distance, 11 more }

</summary>

<details>

<summary>

ai\_verdict: "confirmed"or "rejected"or "unavailable"or "not\_sent"

</summary>

One of the following:

"confirmed"

<a href="#">Link to this property</a>

"rejected"

<a href="#">Link to this property</a>

"unavailable"

<a href="#">Link to this property</a>

"not\_sent"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

domain: string

The matched domain name.

<a href="#">Link to this property</a>

edit\_distance: number

<a href="#">Link to this property</a>

first\_seen: string

When the domain was matched. For multi-query requests, the most recent match time across the requested queries.

<a href="#">Link to this property</a>

match\_category: string

<a href="#">Link to this property</a>

<details>

<summary>

public\_scans: object {submission\_id }

</summary>

submission\_id: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

quality: "high"or "low"

</summary>

One of the following:

"high"

<a href="#">Link to this property</a>

"low"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

registrar: string

Registrar of the matched domain, if known.

<a href="#">Link to this property</a>

scan\_status: string

<a href="#">Link to this property</a>

scan\_submission\_id: number

<a href="#">Link to this property</a>

source: string

<a href="#">Link to this property</a>

dismissed: optional boolean

Whether the match is dismissed. Only present for single-query requests. For multi-query requests, use the dismissed field in each match\_details entry.

<a href="#">Link to this property</a>

domain\_id: optional number

ID of the matched domain. Present only when <code>include_domain_id=true</code>. Use it with <code>query_id</code> to dismiss or undismiss the match.

<a href="#">Link to this property</a>

<details>

<summary>

match\_details: optional array of object {ai\_verdict, dismissed, edit\_distance, 5 more }

Per-match detail objects with query metadata and individual dismissed state. Only present when multiple query\_ids are requested.

</summary>

<details>

<summary>

ai\_verdict: "confirmed"or "rejected"or "unavailable"or "not\_sent"

</summary>

One of the following:

"confirmed"

<a href="#">Link to this property</a>

"rejected"

<a href="#">Link to this property</a>

"unavailable"

<a href="#">Link to this property</a>

"not\_sent"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

dismissed: boolean

Individual dismissed state for this specific match.

<a href="#">Link to this property</a>

edit\_distance: number

<a href="#">Link to this property</a>

match\_category: string

<a href="#">Link to this property</a>

match\_id: number

ID of the match. Accepted by the legacy <code>match_ids</code> format.

<a href="#">Link to this property</a>

<details>

<summary>

quality: "high"or "low"

</summary>

One of the following:

"high"

<a href="#">Link to this property</a>

"low"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

query\_id: number

ID of the domain query that produced this match.

<a href="#">Link to this property</a>

query\_tag: string

Tag associated with the query, if one exists.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20brand_protection.v2.matches%20%3E%20(model)%20match_get_response%20%3E%20(schema)%20%3E%20(property)%20matches>)

total: number

Number of matching domains available for pagination. For requests with several `query_id` values, matches are deduplicated from at most 5,000 query-domain rows, so `total` can be lower than the actual number of matches.

minimum0

[Link to this property](#)%20brand_protection.v2.matches%20%3E%20(model)%20match_get_response%20%3E%20(schema)%20%3E%20(property)%20total>)

### List domain matches

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/v2/brand-protection/domain/matches \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "matches": [
    {
      "ai_verdict": "confirmed",
      "domain": "domain",
      "edit_distance": 0,
      "first_seen": "first_seen",
      "match_category": "match_category",
      "public_scans": {
        "submission_id": "submission_id"
      },
      "quality": "high",
      "registrar": "registrar",
      "scan_status": "scan_status",
      "scan_submission_id": 0,
      "source": "source",
      "dismissed": true,
      "domain_id": 0,
      "match_details": [
        {
          "ai_verdict": "confirmed",
          "dismissed": true,
          "edit_distance": 0,
          "match_category": "match_category",
          "match_id": 0,
          "quality": "high",
          "query_id": 0,
          "query_tag": "query_tag"
        }
      ]
    }
  ],
  "total": 0
}
```

##### Returns Examples

200 example

```
{
  "matches": [
    {
      "ai_verdict": "confirmed",
      "domain": "domain",
      "edit_distance": 0,
      "first_seen": "first_seen",
      "match_category": "match_category",
      "public_scans": {
        "submission_id": "submission_id"
      },
      "quality": "high",
      "registrar": "registrar",
      "scan_status": "scan_status",
      "scan_submission_id": 0,
      "source": "source",
      "dismissed": true,
      "domain_id": 0,
      "match_details": [
        {
          "ai_verdict": "confirmed",
          "dismissed": true,
          "edit_distance": 0,
          "match_category": "match_category",
          "match_id": 0,
          "quality": "high",
          "query_id": 0,
          "query_tag": "query_tag"
        }
      ]
    }
  ],
  "total": 0
}
```