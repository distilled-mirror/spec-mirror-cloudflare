---
title: Update a policy
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

# Update a policy

PUT/accounts/{account\_id}/cws/policies/{policy\_id}

Replaces the policy’s configuration. Omit tags or use {} to clear them.

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

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20update%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

policy\_id: string

ID of the policy to update

formatuuid

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20update%20%3E%20(params)%20default%20%3E%20(param)%20policy_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

entrypoint: string

Non-function rule declared in rego\_source. Evaluation uses data.\<package\_path>..

maxLength255

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20entrypoint%20%3E%20(schema)>)

filter: string

Filter expression that determines whether this policy applies. Maximum 4096 UTF-8 bytes.

maxLength4096

minLength1

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20filter%20%3E%20(schema)>)

name: string

Name of the policy

maxLength100

minLength1

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20name%20%3E%20(schema)>)

rego\_source: string

Inline Rego source with a package beginning with “policy.” Maximum 16384 UTF-8 bytes.

maxLength16384

minLength1

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20rego_source%20%3E%20(schema)>)

description: optional string

Optional free-form description.

maxLength1024

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20description%20%3E%20(schema)>)

tags: optional map\[string]

Replacement tag set. Omit or use {} to clear. Keys are limited to 256 UTF-8 bytes and values to 1024 UTF-8 bytes.

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20tags%20%3E%20(schema)>)

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

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.cws.policies%20%3E%20(model)%20policy%20%3E%20(schema)">Policy</a> { id, created\_at, entrypoint, 7 more }

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

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Update a policy

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cws/policies/$POLICY_ID \
    -X PUT \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "entrypoint": "entrypoint",
          "filter": "x",
          "name": "x",
          "rego_source": "x"
        }'
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
  },
  "success": true
}
```