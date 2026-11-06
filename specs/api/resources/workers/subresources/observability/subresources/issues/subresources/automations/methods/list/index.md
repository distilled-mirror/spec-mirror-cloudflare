---
title: List issue automations
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Workers](https://developers.cloudflare.com/api/resources/workers)

[Observability](https://developers.cloudflare.com/api/resources/workers/subresources/observability)

[Issues](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/issues)

[Automations](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/issues/subresources/automations)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List issue automations

GET/accounts/{account\_id}/workers/observability/issues/automations

List account and service issue automations.

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

`Workers Observability Write``Workers Observability Read`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20workers.observability.issues.automations%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

service: optional string

maxLength128

minLength1

[Link to this property](#)%20workers.observability.issues.automations%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20service%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues.automations%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {message }

</summary>

message: "Successful request"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues.automations%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {automations }

</summary>

<details>

<summary>

automations: array of object {id, ansPolicyId, created, 12 more }

</summary>

id: string

<a href="#">Link to this property</a>

ansPolicyId: string

<a href="#">Link to this property</a>

created: number

<a href="#">Link to this property</a>

createdByUserId: string

<a href="#">Link to this property</a>

enabled: boolean

<a href="#">Link to this property</a>

inactivitySeconds: number

<a href="#">Link to this property</a>

name: string

<a href="#">Link to this property</a>

revision: number

<a href="#">Link to this property</a>

<details>

<summary>

scope: "account"or "service"

</summary>

One of the following:

"account"

<a href="#">Link to this property</a>

"service"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

service: string

<a href="#">Link to this property</a>

serviceType: string

<a href="#">Link to this property</a>

threshold: number

<a href="#">Link to this property</a>

<details>

<summary>

triggerType: "occurrence\_threshold"or "recurrence\_after\_inactivity"

</summary>

One of the following:

"occurrence\_threshold"

<a href="#">Link to this property</a>

"recurrence\_after\_inactivity"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated: number

<a href="#">Link to this property</a>

updatedByUserId: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues.automations%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

[Link to this property](#)%20workers.observability.issues.automations%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List issue automations

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/workers/observability/issues/automations \
    -H "X-Auth-Email: $CLOUDFLARE_EMAIL" \
    -H "X-Auth-Key: $CLOUDFLARE_API_KEY"
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
    "automations": [
      {
        "id": "id",
        "ansPolicyId": "ansPolicyId",
        "created": 0,
        "createdByUserId": "createdByUserId",
        "enabled": true,
        "inactivitySeconds": 0,
        "name": "name",
        "revision": 0,
        "scope": "account",
        "service": "service",
        "serviceType": "serviceType",
        "threshold": 0,
        "triggerType": "occurrence_threshold",
        "updated": 0,
        "updatedByUserId": "updatedByUserId"
      }
    ]
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
    "automations": [
      {
        "id": "id",
        "ansPolicyId": "ansPolicyId",
        "created": 0,
        "createdByUserId": "createdByUserId",
        "enabled": true,
        "inactivitySeconds": 0,
        "name": "name",
        "revision": 0,
        "scope": "account",
        "service": "service",
        "serviceType": "serviceType",
        "threshold": 0,
        "triggerType": "occurrence_threshold",
        "updated": 0,
        "updatedByUserId": "updatedByUserId"
      }
    ]
  },
  "success": true
}
```