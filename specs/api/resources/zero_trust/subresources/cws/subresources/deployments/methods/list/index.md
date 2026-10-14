---
title: List deployments
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Cloud Workload Security](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws)

[Deployments](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/deployments)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List deployments

GET/accounts/{account\_id}/cws/deployments

Returns a paginated list of deployments in the account.

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

[Link to this property](#)%20zero_trust.cws.deployments%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

cursor: optional string

Pagination cursor from previous response

[Link to this property](#)%20zero_trust.cws.deployments%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20cursor%20%3E%20(schema)>)

<details>

<summary>

direction: optional "asc"or "desc"

Sort direction (default: asc)

</summary>

One of the following:

"asc"

<a href="#">Link to this property</a>

"desc"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.deployments%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20direction%20%3E%20(schema)>)

name: optional string

Filter by deployment name (case-insensitive substring match)

[Link to this property](#)%20zero_trust.cws.deployments%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20name%20%3E%20(schema)>)

<details>

<summary>

order: optional "name"or "created\_at"or "updated\_at"

Field to order results by (default: created\_at)

</summary>

One of the following:

"name"

<a href="#">Link to this property</a>

"created\_at"

<a href="#">Link to this property</a>

"updated\_at"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.deployments%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20order%20%3E%20(schema)>)

per\_page: optional number

Number of items per page (1-100, default 20)

formatint64

maximum100

minimum1

[Link to this property](#)%20zero_trust.cws.deployments%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20per_page%20%3E%20(schema)>)

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

[Link to this property](#)%20zero_trust.cws.deployments%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20zero_trust.cws.deployments%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.cws.deployments%20%3E%20(model)%20deployment%20%3E%20(schema)">Deployment</a> { id, basic\_auth\_credential\_ids, created\_at, 9 more }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

basic\_auth\_credential\_ids: array of string

IDs of basic-auth credentials attached to this deployment

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

default\_mode: "ALLOW"or "BLOCK"

Default traffic decision when no policy set matches

</summary>

One of the following:

"ALLOW"

<a href="#">Link to this property</a>

"BLOCK"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

Human-readable name; unique per account

maxLength100

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

on\_error\_action: "BLOCK"or "SKIP"

Action applied when an enforcing policy has a runtime Rego error

</summary>

One of the following:

"BLOCK"

<a href="#">Link to this property</a>

"SKIP"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

policy\_set\_ids: array of string

IDs of policy sets attached to this deployment

<a href="#">Link to this property</a>

rego\_raise\_error: boolean

Whether OPA builtin failures are raised as runtime evaluation errors

<a href="#">Link to this property</a>

tags: map\[string]

Tags attached to this deployment

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

description: optional string

Optional free-form description.

maxLength1024

<a href="#">Link to this property</a>

domain\_acl\_id: optional string

ID of the attached domain ACL. Omitted when none.

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.deployments%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

<details>

<summary>

result\_info: object {count, per\_page, total\_count, cursor }

</summary>

count: number

formatint64

<a href="#">Link to this property</a>

per\_page: number

formatint64

<a href="#">Link to this property</a>

total\_count: number

formatint64

<a href="#">Link to this property</a>

cursor: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.deployments%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

success: boolean

[Link to this property](#)%20zero_trust.cws.deployments%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List deployments

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cws/deployments \
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
  "result": [
    {
      "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
      "basic_auth_credential_ids": [
        "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
      ],
      "created_at": "2019-12-27T18:11:19.117Z",
      "default_mode": "ALLOW",
      "name": "x",
      "on_error_action": "BLOCK",
      "policy_set_ids": [
        "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
      ],
      "rego_raise_error": true,
      "tags": {
        "foo": "string"
      },
      "updated_at": "2019-12-27T18:11:19.117Z",
      "description": "description",
      "domain_acl_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
    }
  ],
  "result_info": {
    "count": 0,
    "per_page": 0,
    "total_count": 0,
    "cursor": "cursor"
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
  "result": [
    {
      "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
      "basic_auth_credential_ids": [
        "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
      ],
      "created_at": "2019-12-27T18:11:19.117Z",
      "default_mode": "ALLOW",
      "name": "x",
      "on_error_action": "BLOCK",
      "policy_set_ids": [
        "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
      ],
      "rego_raise_error": true,
      "tags": {
        "foo": "string"
      },
      "updated_at": "2019-12-27T18:11:19.117Z",
      "description": "description",
      "domain_acl_id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
    }
  ],
  "result_info": {
    "count": 0,
    "per_page": 0,
    "total_count": 0,
    "cursor": "cursor"
  },
  "success": true
}
```