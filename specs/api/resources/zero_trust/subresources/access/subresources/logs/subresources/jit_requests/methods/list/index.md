---
title: List Access JIT request logs
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Access](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access)

[Logs](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/logs)

[Jit Requests](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/logs/subresources/jit_requests)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List Access JIT request logs

GET/accounts/{account\_id}/access/logs/jit\_requests

Lists account-wide Access JIT request logs reconstructed from request lifecycle events.

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

##### P ath ParametersExpand Collapse

account\_id: string

Identifier.

maxLength32

[Link to this property](#)%20zero_trust.access.logs.jit_requests%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

page: optional number

Page number of results.

[Link to this property](#)%20zero_trust.access.logs.jit_requests%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20page%20%3E%20(schema)>)

per\_page: optional number

Number of results per page.

maximum1000

[Link to this property](#)%20zero_trust.access.logs.jit_requests%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20per_page%20%3E%20(schema)>)

search: optional string

Case-insensitive search over request ID, requester email, application audience, and application hostname.

[Link to this property](#)%20zero_trust.access.logs.jit_requests%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20search%20%3E%20(schema)>)

since: optional string

The earliest request timestamp to query. Defaults to 366 days before the current time.

formatdate-time

[Link to this property](#)%20zero_trust.access.logs.jit_requests%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20since%20%3E%20(schema)>)

<details>

<summary>

status: optional "PENDING"or "APPROVED"or "DENIED"or 2 more

JIT request status. <code>SPENT</code> is deprecated and interpreted as <code>APPROVED</code>.

</summary>

One of the following:

"PENDING"

<a href="#">Link to this property</a>

"APPROVED"

<a href="#">Link to this property</a>

"DENIED"

<a href="#">Link to this property</a>

"CANCELED"

<a href="#">Link to this property</a>

"SPENT"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.logs.jit_requests%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20status%20%3E%20(schema)>)

until: optional string

The latest request timestamp to query. Defaults to the current time.

formatdate-time

[Link to this property](#)%20zero_trust.access.logs.jit_requests%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20until%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {code, message, documentation\_url, source }

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

source: optional object {pointer }

</summary>

pointer: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.logs.jit_requests%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {code, message, documentation\_url, source }

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

source: optional object {pointer }

</summary>

pointer: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.logs.jit_requests%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: true

Whether the API call was successful.

[Link to this property](#)%20zero_trust.access.logs.jit_requests%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional array of object {app\_aud, app\_hostname, approvals\_received, 7 more }

</summary>

app\_aud: optional string

Audience of the Access application.

<a href="#">Link to this property</a>

app\_hostname: optional string

<a href="#">Link to this property</a>

approvals\_received: optional number

Number of unique actors who approved the request.

<a href="#">Link to this property</a>

approver\_emails: optional array of string

Unique actors who approved the request.

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

expires\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

knock\_request\_id: optional string

Unique identifier for the JIT request.

<a href="#">Link to this property</a>

purpose\_justification: optional string

<a href="#">Link to this property</a>

requester\_email: optional string

formatemail

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "PENDING"or "APPROVED"or "DENIED"or 2 more

JIT request status. <code>SPENT</code> is deprecated and interpreted as <code>APPROVED</code>.

</summary>

One of the following:

"PENDING"

<a href="#">Link to this property</a>

"APPROVED"

<a href="#">Link to this property</a>

"DENIED"

<a href="#">Link to this property</a>

"CANCELED"

<a href="#">Link to this property</a>

"SPENT"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.logs.jit_requests%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

<details>

<summary>

result\_info: optional object {count, page, per\_page, 2 more }

</summary>

count: optional number

Total number of results for the requested service.

<a href="#">Link to this property</a>

page: optional number

Current page within paginated list of results.

<a href="#">Link to this property</a>

per\_page: optional number

Number of results per page of results.

<a href="#">Link to this property</a>

total\_count: optional number

Total results available without any search parameters.

<a href="#">Link to this property</a>

total\_pages: optional number

The number of total pages in the entire result set.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.logs.jit_requests%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

### List Access JIT request logs

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/access/logs/jit_requests \
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
  "result": [
    {
      "app_aud": "app_aud",
      "app_hostname": "app_hostname",
      "approvals_received": 0,
      "approver_emails": [
        "dev@stainless.com"
      ],
      "created_at": "2014-01-01T05:20:00.12345Z",
      "expires_at": "2014-01-01T05:20:00.12345Z",
      "knock_request_id": "knock_request_id",
      "purpose_justification": "purpose_justification",
      "requester_email": "dev@stainless.com",
      "status": "PENDING"
    }
  ],
  "result_info": {
    "count": 1,
    "page": 1,
    "per_page": 20,
    "total_count": 2000,
    "total_pages": 100
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
  "result": [
    {
      "app_aud": "app_aud",
      "app_hostname": "app_hostname",
      "approvals_received": 0,
      "approver_emails": [
        "dev@stainless.com"
      ],
      "created_at": "2014-01-01T05:20:00.12345Z",
      "expires_at": "2014-01-01T05:20:00.12345Z",
      "knock_request_id": "knock_request_id",
      "purpose_justification": "purpose_justification",
      "requester_email": "dev@stainless.com",
      "status": "PENDING"
    }
  ],
  "result_info": {
    "count": 1,
    "page": 1,
    "per_page": 20,
    "total_count": 2000,
    "total_pages": 100
  }
}
```