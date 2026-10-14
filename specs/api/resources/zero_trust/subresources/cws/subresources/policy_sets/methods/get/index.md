---
title: Get a policy set by ID
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Cloud Workload Security](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws)

[Policy Sets](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policy_sets)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Get a policy set by ID

GET/accounts/{account\_id}/cws/policy-sets/{policy\_set\_id}

Returns the policy set with the specified ID.

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

Cloudflare account ID (32-character hexadecimal string)

maxLength32

minLength32

[Link to this property](#)%20zero_trust.cws.policy_sets%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

policy\_set\_id: string

ID of the policy set to retrieve

formatuuid

[Link to this property](#)%20zero_trust.cws.policy_sets%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20policy_set_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {code, message, source }

</summary>

code: number

formatint64

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.policy_sets%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {code, message, source }

</summary>

code: number

formatint64

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.policy_sets%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.cws.policy_sets%20%3E%20(model)%20policy_set%20%3E%20(schema)">PolicySet</a> { id, created\_at, exclude\_workload\_ids, 6 more }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

exclude\_workload\_ids: array of string

IDs of workloads that exclude matching requests. Exclusions take precedence.

<a href="#">Link to this property</a>

include\_workload\_ids: array of string

IDs of workloads that include matching requests. Empty includes all requests before exclusions.

<a href="#">Link to this property</a>

name: string

Human-readable name; unique per account

maxLength100

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

policies: array of object {enforce, policy\_id }

Member policies and their per-membership enforcement mode

</summary>

enforce: boolean

Whether this policy should enforce when it matches. False keeps the policy attached for non-enforcing evaluation.

<a href="#">Link to this property</a>

policy\_id: string

ID of the member policy

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

tags: map\[string]

Tags attached to this policy set

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

description: optional string

Optional free-form description.

maxLength1024

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.policy_sets%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

[Link to this property](#)%20zero_trust.cws.policy_sets%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Get a policy set by ID

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cws/policy-sets/$POLICY_SET_ID \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "errors": [
    {
      "code": 0,
      "message": "message",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    {
      "code": 0,
      "message": "message",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "result": {
    "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
    "created_at": "2019-12-27T18:11:19.117Z",
    "exclude_workload_ids": [
      "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
    ],
    "include_workload_ids": [
      "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
    ],
    "name": "x",
    "policies": [
      {
        "enforce": true,
        "policy_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
      }
    ],
    "tags": {
      "foo": "string"
    },
    "updated_at": "2019-12-27T18:11:19.117Z",
    "description": "description"
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
      "code": 0,
      "message": "message",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    {
      "code": 0,
      "message": "message",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "result": {
    "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
    "created_at": "2019-12-27T18:11:19.117Z",
    "exclude_workload_ids": [
      "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
    ],
    "include_workload_ids": [
      "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
    ],
    "name": "x",
    "policies": [
      {
        "enforce": true,
        "policy_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
      }
    ],
    "tags": {
      "foo": "string"
    },
    "updated_at": "2019-12-27T18:11:19.117Z",
    "description": "description"
  },
  "success": true
}
```