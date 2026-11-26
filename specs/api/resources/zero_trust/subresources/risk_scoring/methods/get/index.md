---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Get risk event/score information for a specific user
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Risk Scoring](https://developers.cloudflare.com/api/resources/zero_trust/subresources/risk_scoring)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Get risk event/score information for a specific user

GET/accounts/{account\_id}/zt\_risk\_scoring/{user\_id}

Gets the risk level, the last reset time, and the risk events of one user. The server reads risk events from at most 180 days before the current time, and after the last reset of the user. Returns 404 when the request reaches a server outside of the configured region of the account.

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

[Link to this property](#)%20zero_trust.risk_scoring%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

user\_id: string

formatuuid

[Link to this property](#)%20zero_trust.risk_scoring%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20user_id%20%3E%20(schema)>)

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

[Link to this property](#)%20zero_trust.risk_scoring%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20direction%20%3E%20(schema)>)

<details>

<summary>

order\_by: optional "timestamp" or "risk\_level"

Field to sort the events by.

</summary>

One of the following:

"timestamp"

<a href="#">Link to this property</a>

"risk\_level"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.risk_scoring%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20order_by%20%3E%20(schema)>)

page: optional number

Page number, starting at 1.

minimum1

[Link to this property](#)%20zero_trust.risk_scoring%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20page%20%3E%20(schema)>)

per\_page: optional number

Number of results per page. The server uses 100 for a larger value.

maximum100

minimum1

[Link to this property](#)%20zero_trust.risk_scoring%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20per_page%20%3E%20(schema)>)

time\_zone: optional string

IANA time zone name. The server validates the value. The value does not change the response.

[Link to this property](#)%20zero_trust.risk_scoring%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20time_zone%20%3E%20(schema)>)

<details>

<summary>

timestamp: optional object { between }

</summary>

between: optional string

Time range as &lt;start\_seconds&gt;:&lt;end\_seconds&gt; in Unix epoch seconds. The start must be before the end.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.risk_scoring%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20timestamp%20%3E%20(schema)>)

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

[Link to this property](#)%20zero_trust.risk_scoring%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20zero_trust.risk_scoring%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: true

Whether the API call was successful.

[Link to this property](#)%20zero_trust.risk_scoring%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional object { email, events, last\_reset\_time, 2 more }

Risk level, last reset time, and risk events of one user.

</summary>

email: string

Email address of the user.

<a href="#">Link to this property</a>

<details>

<summary>

events: array of object { id, name, points, 3 more }

Risk events of the user on this page.

</summary>

id: string

ID of the behavior that caused the event.

<a href="#">Link to this property</a>

name: string

Name of the behavior that caused the event.

<a href="#">Link to this property</a>

points: number

Risk score points of a behavior.

maximum100

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

risk\_level: "info" or "low" or "medium" or "high"

Risk level of a behavior or an event.

</summary>

One of the following:

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

timestamp: string

Time of the event.

formatdate-time

<a href="#">Link to this property</a>

event\_details: optional map\[unknown]

Details of the event. The fields depend on the behavior. The server omits the field when the details are not valid JSON.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

last\_reset\_time: string

Time of the last risk score reset of the user. The value is null when the score was never reset.

formatdate-time

<a href="#">Link to this property</a>

name: string

Name of the user.

<a href="#">Link to this property</a>

<details>

<summary>

risk\_level: optional "info" or "low" or "medium" or "high"

Risk level of a behavior or an event.

</summary>

One of the following:

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

</details>

[Link to this property](#)%20zero_trust.risk_scoring%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

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

[Link to this property](#)%20zero_trust.risk_scoring%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

### Get risk event/score information for a specific user

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/zt_risk_scoring/$USER_ID \
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
    "email": "jdoe@example.com",
    "events": [
      {
        "id": "high_dlp",
        "name": "High number of DLP policies triggered",
        "points": 85,
        "risk_level": "info",
        "timestamp": "2026-04-08T13:48:01Z",
        "event_details": {
          "foo": "bar"
        }
      }
    ],
    "last_reset_time": "2019-12-27T18:11:19.117Z",
    "name": "John Doe",
    "risk_level": "info"
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
    "email": "jdoe@example.com",
    "events": [
      {
        "id": "high_dlp",
        "name": "High number of DLP policies triggered",
        "points": 85,
        "risk_level": "info",
        "timestamp": "2026-04-08T13:48:01Z",
        "event_details": {
          "foo": "bar"
        }
      }
    ],
    "last_reset_time": "2019-12-27T18:11:19.117Z",
    "name": "John Doe",
    "risk_level": "info"
  },
  "result_info": {
    "count": 25,
    "page": 1,
    "per_page": 25,
    "total_count": 2000
  }
}
```