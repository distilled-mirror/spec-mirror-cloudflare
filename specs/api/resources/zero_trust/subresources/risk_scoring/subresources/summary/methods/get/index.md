---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Get risk score info for all users in the account
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Risk Scoring](https://developers.cloudflare.com/api/resources/zero_trust/subresources/risk_scoring)

[Summary](https://developers.cloudflare.com/api/resources/zero_trust/subresources/risk_scoring/subresources/summary)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Get risk score info for all users in the account

GET/accounts/{account\_id}/zt\_risk\_scoring/summary

Gets the users in an account that have risk events, with the highest risk level, the event count, and the time of the last event for each user. The server reads risk events from at most 180 days before the current time, and after the last reset of each user. Returns 404 when the request reaches a server outside of the configured region of the account.

##### Security

<details>

<summary>API Token</summary>



The preferred authorization scheme for interacting with the Cloudflare API. <a href="https://developers.cloudflare.com/fundamentals/api/get-started/create-token/">Create a token</a>.

**Example:**<code>Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY</code>

</details>

<details>

<summary>API Email + API Key</summary>



The previous authorization scheme for interacting with the Cloudflare API, used in conjunction with a Global API key.

**Example:**<code>X-Auth-Email: user@example.com</code>

The previous authorization scheme for interacting with the Cloudflare API. When possible, use API tokens instead of Global API keys.

**Example:**<code>X-Auth-Key: 144c9defac04969c7bfad8efaa8ea194</code>

</details>

##### Accepted Permissions (at least one required)

`Zero Trust: PII Read`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20zero_trust.risk_scoring.summary%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

<details>

<summary>

direction: optional "asc" or "desc"

Sort direction.

</summary>

One of the following:

"asc"

<a href="#">Link to this property</a>

"desc"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.risk_scoring.summary%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20direction%20%3E%20(schema)>)

<details>

<summary>

order\_by: optional "last\_event" or "event\_count" or "max\_risk\_level"

Field to sort the users by.

</summary>

One of the following:

"last\_event"

<a href="#">Link to this property</a>

"event\_count"

<a href="#">Link to this property</a>

"max\_risk\_level"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.risk_scoring.summary%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20order_by%20%3E%20(schema)>)

page: optional number

Page number, starting at 1.

minimum1

[Link to this property](#)%20zero_trust.risk_scoring.summary%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20page%20%3E%20(schema)>)

per\_page: optional number

Number of results per page. The server uses 100 for a larger value.

maximum100

minimum1

[Link to this property](#)%20zero_trust.risk_scoring.summary%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20per_page%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object { code, message, documentation\_url, source }

</summary>

code: number

minimum1000

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

documentation\_url: optional string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object { pointer }

</summary>

pointer: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.risk_scoring.summary%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object { code, message, documentation\_url, source }

</summary>

code: number

minimum1000

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

documentation\_url: optional string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object { pointer }

</summary>

pointer: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.risk_scoring.summary%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: true

Whether the API call was successful.

[Link to this property](#)%20zero_trust.risk_scoring.summary%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional object { users }

Risk summary of the users in an account.

</summary>

<details>

<summary>

users: array of object { email, event\_count, last\_event, 3 more }

Users on this page, with their risk summary.

</summary>

email: string

Email address of the user.

<a href="#">Link to this property</a>

event\_count: number

Number of risk events of the user.

minimum0

<a href="#">Link to this property</a>

last\_event: string

Time of the most recent risk event of the user.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

max\_risk\_level: "unset" or "info" or "low" or 2 more

Highest risk level. The value is unset when no event maps to a configured behavior.

</summary>

One of the following:

"unset"

<a href="#">Link to this property</a>

"info"

<a href="#">Link to this property</a>

"low"

<a href="#">Link to this property</a>

"medium"

<a href="#">Link to this property</a>

"high"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

Name of the user.

<a href="#">Link to this property</a>

user\_id: string

User ID (UUID v4).

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.risk_scoring.summary%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

<details>

<summary>

result\_info: optional object { count, page, per\_page, total\_count }

Pagination information. The server always returns every field.

</summary>

count: number

Number of results on this page.

<a href="#">Link to this property</a>

page: number

Current page within the paginated list of results.

<a href="#">Link to this property</a>

per\_page: number

Number of results per page.

<a href="#">Link to this property</a>

total\_count: number

Total number of results that match the request.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.risk_scoring.summary%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

### Get risk score info for all users in the account

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/zt_risk_scoring/summary \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "errors": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "success": true,
  "result": {
    "users": [
      {
        "email": "email",
        "event_count": 0,
        "last_event": "2019-12-27T18:11:19.117Z",
        "max_risk_level": "unset",
        "name": "name",
        "user_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
      }
    ]
  },
  "result_info": {
    "count": 25,
    "page": 1,
    "per_page": 25,
    "total_count": 2000
  }
}
```

##### Returns Examples

200 example

```
{
  "errors": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "success": true,
  "result": {
    "users": [
      {
        "email": "email",
        "event_count": 0,
        "last_event": "2019-12-27T18:11:19.117Z",
        "max_risk_level": "unset",
        "name": "name",
        "user_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
      }
    ]
  },
  "result_info": {
    "count": 25,
    "page": 1,
    "per_page": 25,
    "total_count": 2000
  }
}
```