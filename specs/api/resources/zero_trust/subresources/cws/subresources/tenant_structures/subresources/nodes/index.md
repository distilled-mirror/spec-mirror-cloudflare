---
title: Nodes
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Cloud Workload Security](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws)

[Tenant Structures](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Nodes

##### [List nodes for a tenant structure](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/subresources/nodes/methods/list)

GET/accounts/{account\_id}/cws/tenant-structures/{structure\_id}/nodes

##### [Get a tenant node by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/subresources/nodes/methods/get)

GET/accounts/{account\_id}/cws/tenant-structures/{structure\_id}/nodes/{node\_id}

##### [Add a node to a tenant structure](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/subresources/nodes/methods/create)

POST/accounts/{account\_id}/cws/tenant-structures/{structure\_id}/nodes

##### [Update a tenant node](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/subresources/nodes/methods/update)

PUT/accounts/{account\_id}/cws/tenant-structures/{structure\_id}/nodes/{node\_id}

##### [Delete a tenant node](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/subresources/nodes/methods/delete)

DELETE/accounts/{account\_id}/cws/tenant-structures/{structure\_id}/nodes/{node\_id}

##### [Apply a batch of tenant node mutations](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/subresources/nodes/methods/batch)

POST/accounts/{account\_id}/cws/tenant-structures/{structure\_id}/nodes/batch

##### ModelsExpand Collapse

<details>

<summary>

TenantStructureNode object {id, created\_at, native\_id, 4 more }

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

[Link to this property](#)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(model)%20tenant_structure_node%20%3E%20(schema)>)

<details>

<summary>

NodeDeleteResponse object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(model)%20node_delete_response%20%3E%20(schema)>)

<details>

<summary>

NodeBatchResponse object {created, deleted, updated }

</summary>

<details>

<summary>

created: array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(model)%20tenant_structure_node%20%3E%20(schema)">TenantStructureNode</a> { id, created\_at, native\_id, 4 more }

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

<a href="#">Link to this property</a>

<details>

<summary>

deleted: array of object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated: array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(model)%20tenant_structure_node%20%3E%20(schema)">TenantStructureNode</a> { id, created\_at, native\_id, 4 more }

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

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.tenant_structures.nodes%20%3E%20(model)%20node_batch_response%20%3E%20(schema)>)