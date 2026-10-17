---
title: List policies
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Cloud Workload Security](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws)

[Policies](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policies)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List policies

GET/accounts/{account\_id}/cws/policies

Returns a paginated list of policies in the account.

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

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

cursor: optional string

Pagination cursor from previous response

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20cursor%20%3E%20(schema)>)

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

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20direction%20%3E%20(schema)>)

name: optional string

Filter by policy name (case-insensitive substring match)

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20name%20%3E%20(schema)>)

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

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20order%20%3E%20(schema)>)

package\_path: optional string

Filter by package path (case-sensitive literal substring match)

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20package_path%20%3E%20(schema)>)

per\_page: optional number

Number of items per page (1-100, default 20)

formatint64

maximum100

minimum1

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20per_page%20%3E%20(schema)>)

policy\_set\_id: optional string

Filter to policies attached to (members of) this policy set

formatuuid

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20policy_set_id%20%3E%20(schema)>)

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

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.cws.policies%20%3E%20(model)%20policy%20%3E%20(schema)">Policy</a> { id, created\_at, entrypoint, 7 more }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

entrypoint: string

Non-function rule declared in rego\_source. Evaluation uses data.&lt;package\_path&gt;..

maxLength255

<a href="#">Link to this property</a>

filter: string

Filter expression that determines whether this policy applies. Maximum 4096 UTF-8 bytes.

maxLength4096

minLength1

<a href="#">Link to this property</a>

name: string

Human-readable name; unique per account

maxLength100

minLength1

<a href="#">Link to this property</a>

package\_path: string

Dotted path derived from rego\_source. Begins with policy. and is unique per account.

maxLength1024

<a href="#">Link to this property</a>

rego\_source: string

Inline Rego source with a package beginning with “policy.” Maximum 16384 UTF-8 bytes.

maxLength16384

minLength1

<a href="#">Link to this property</a>

tags: map\[string]

Tags attached to this policy

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

description: optional string

Optional free-form description.

maxLength1024

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

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

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

success: boolean

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List policies

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cws/policies \
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
      "created_at": "2019-12-27T18:11:19.117Z",
      "entrypoint": "entrypoint",
      "filter": "x",
      "name": "x",
      "package_path": "package_path",
      "rego_source": "x",
      "tags": {
        "foo": "string"
      },
      "updated_at": "2019-12-27T18:11:19.117Z",
      "description": "description"
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
      "created_at": "2019-12-27T18:11:19.117Z",
      "entrypoint": "entrypoint",
      "filter": "x",
      "name": "x",
      "package_path": "package_path",
      "rego_source": "x",
      "tags": {
        "foo": "string"
      },
      "updated_at": "2019-12-27T18:11:19.117Z",
      "description": "description"
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