---
title: Add a node to a tenant structure
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Cloud Workload Security](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws)

[Tenant Structures](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures)

[Nodes](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/subresources/nodes)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Add a node to a tenant structure

POST/accounts/{account\_id}/cws/tenant-structures/{structure\_id}/nodes

Adds a validated cloud-native node to the tenant hierarchy.

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

[Link to this property](#)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

structure\_id: string

ID of the parent tenant structure

formatuuid

[Link to this property](#)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20structure_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

native\_id: string

Cloud-native identifier of this node, unique within the structure; the parent-reference target. Shape depends on the structure’s application. Immutable after create.

maxLength255

minLength1

[Link to this property](#)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20native_id%20%3E%20(schema)>)

node\_kind: string

Position in the tree. Legal values depend on the structure’s application (aws: root/ou/account; cloudflare: org/account/zone). At most one root per structure. Immutable after create.

maxLength64

minLength1

[Link to this property](#)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20node_kind%20%3E%20(schema)>)

name: optional string

Display name (e.g. an OU or account name), mutable. Optional; empty by default.

maxLength100

[Link to this property](#)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20name%20%3E%20(schema)>)

parent: optional string

Native ID of this node’s parent. Required for non-root nodes and omitted for the root. The parent must be in the same structure and able to contain this node kind.

maxLength255

[Link to this property](#)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20parent%20%3E%20(schema)>)

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

[Link to this property](#)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(model)%20tenant_structure_node%20%3E%20(schema)">TenantStructureNode</a> { id, created\_at, native\_id, 4 more }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

native\_id: string

Cloud-native identifier of this node, unique within the structure; the parent-reference target. Shape depends on the structure’s application. Immutable after create.

maxLength255

minLength1

<a href="#">Link to this property</a>

node\_kind: string

Position in the tree. Legal values depend on the structure’s application (aws: root/ou/account; cloudflare: org/account/zone). At most one root per structure. Immutable after create.

maxLength64

minLength1

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

name: optional string

Display name (e.g. an OU or account name), mutable. Optional; empty by default.

maxLength100

<a href="#">Link to this property</a>

parent: optional string

Native ID of this node’s parent. Required for non-root nodes and omitted for the root. The parent must be in the same structure and able to contain this node kind.

maxLength255

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

[Link to this property](#)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Add a node to a tenant structure

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cws/tenant-structures/$STRUCTURE_ID/nodes \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "native_id": "x",
          "node_kind": "x"
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
    "native_id": "x",
    "node_kind": "x",
    "updated_at": "2019-12-27T18:11:19.117Z",
    "name": "name",
    "parent": "parent"
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
    "native_id": "x",
    "node_kind": "x",
    "updated_at": "2019-12-27T18:11:19.117Z",
    "name": "name",
    "parent": "parent"
  },
  "success": true
}
```