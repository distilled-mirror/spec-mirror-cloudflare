---
title: Modify an issue
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Workers](https://developers.cloudflare.com/api/resources/workers)

[Observability](https://developers.cloudflare.com/api/resources/workers/subresources/observability)

[Issues](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/issues)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Modify an issue

PATCH/accounts/{account\_id}/workers/observability/issues/{issueId}

Modify an issue status or group title.

##### Security

<details>

<summary>API Email + API Key</summary>



The previous authorization scheme for interacting with the Cloudflare API, used in conjunction with a Global API key.

**Example:**<code>X-Auth-Email: user@example.com</code>

The previous authorization scheme for interacting with the Cloudflare API. When possible, use API tokens instead of Global API keys.

**Example:**<code>X-Auth-Key: 144c9defac04969c7bfad8efaa8ea194</code>

</details>

<details>

<summary>API Token</summary>



The preferred authorization scheme for interacting with the Cloudflare API. <a href="https://developers.cloudflare.com/fundamentals/api/get-started/create-token/">Create a token</a>.

**Example:**<code>Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY</code>

</details>

<details>

<summary>User Service Key</summary>



Used when interacting with the Origin CA certificates API. <a href="https://developers.cloudflare.com/fundamentals/api/get-started/ca-keys/#viewchange-your-origin-ca-keys">View/change your key</a>.

**Example:**<code>X-Auth-User-Service-Key: v1.0-144c9defac04969c7bfad8ef-631a41d003a32d25fe878081ef365c49503f7fada600da935e2851a1c7326084b85cbf6429c4b859de8475731dc92a9c329631e6d59e6c73da7b198497172b4cefe071d90d0f5d2719</code>

</details>

##### Accepted Permissions (at least one required)

`Workers Observability Write`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20workers.observability.issues%20%3E%20(method)%20update%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

issueId: string

minLength1

[Link to this property](#)%20workers.observability.issues%20%3E%20(method)%20update%20%3E%20(params)%20default%20%3E%20(param)%20issueId%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

<details>

<summary>

status: optional "active"or "resolved"or "ignored"

</summary>

One of the following:

"active"

<a href="#">Link to this property</a>

"resolved"

<a href="#">Link to this property</a>

"ignored"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20status%20%3E%20(schema)>)

title: optional string

maxLength128

minLength1

[Link to this property](#)%20workers.observability.issues%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20title%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {message }

</summary>

message: "Successful request"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {id, count, created, 10 more }

</summary>

id: string

<a href="#">Link to this property</a>

count: number

<a href="#">Link to this property</a>

created: number

<a href="#">Link to this property</a>

firstObserved: number

<a href="#">Link to this property</a>

lastObserved: number

<a href="#">Link to this property</a>

service: string

<a href="#">Link to this property</a>

<details>

<summary>

status: "active"or "resolved"or "ignored"

</summary>

One of the following:

"active"

<a href="#">Link to this property</a>

"resolved"

<a href="#">Link to this property</a>

"ignored"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

statusUpdated: number

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

updated: number

<a href="#">Link to this property</a>

fingerprint: optional string

<a href="#">Link to this property</a>

<details>

<summary>

members: optional array of object {fingerprint, issueId, title }

</summary>

fingerprint: string

<a href="#">Link to this property</a>

issueId: string

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

type: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20workers.observability.issues%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Modify an issue

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/workers/observability/issues/$ISSUE_ID \
    -X PATCH \
    -H 'Content-Type: application/json' \
    -H "X-Auth-Email: $CLOUDFLARE_EMAIL" \
    -H "X-Auth-Key: $CLOUDFLARE_API_KEY" \
    -d '{}'
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
      "message": "Successful request"
    }
  ],
  "result": {
    "id": "id",
    "count": 0,
    "created": 0,
    "firstObserved": 0,
    "lastObserved": 0,
    "service": "service",
    "status": "active",
    "statusUpdated": 0,
    "title": "title",
    "updated": 0,
    "fingerprint": "fingerprint",
    "members": [
      {
        "fingerprint": "fingerprint",
        "issueId": "issueId",
        "title": "title"
      }
    ],
    "type": "type"
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
      "message": "Successful request"
    }
  ],
  "result": {
    "id": "id",
    "count": 0,
    "created": 0,
    "firstObserved": 0,
    "lastObserved": 0,
    "service": "service",
    "status": "active",
    "statusUpdated": 0,
    "title": "title",
    "updated": 0,
    "fingerprint": "fingerprint",
    "members": [
      {
        "fingerprint": "fingerprint",
        "issueId": "issueId",
        "title": "title"
      }
    ],
    "type": "type"
  },
  "success": true
}
```