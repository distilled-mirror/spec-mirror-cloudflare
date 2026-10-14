---
title: Tenant Structures
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Cloud Workload Security](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Tenant Structures

##### [List tenant structures for an account](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/methods/list)

GET/accounts/{account\_id}/cws/tenant-structures

##### [Get a tenant structure by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/methods/get)

GET/accounts/{account\_id}/cws/tenant-structures/{structure\_id}

##### [Create a tenant structure](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/methods/create)

POST/accounts/{account\_id}/cws/tenant-structures

##### [Update a tenant structure](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/methods/update)

PUT/accounts/{account\_id}/cws/tenant-structures/{structure\_id}

##### [Delete a tenant structure](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/tenant_structures/methods/delete)

DELETE/accounts/{account\_id}/cws/tenant-structures/{structure\_id}

##### ModelsExpand Collapse

<details>

<summary>

TenantStructure object {id, application, created\_at, 3 more }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

application: "aws"or "cloudflare"

Platform this structure models. Immutable after creation; determines valid node kinds and identifier formats.

</summary>

One of the following:

"aws"

<a href="#">Link to this property</a>

"cloudflare"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

name: string

Human-readable name; unique per account

maxLength100

minLength1

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

import\_path: optional string

Optional unique Rego mount path in the form tenant... The application segment must match application; omitted when unmounted.

maxLength255

minLength1

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.tenant_structures%20%3E%20(model)%20tenant_structure%20%3E%20(schema)>)

<details>

<summary>

TenantStructureDeleteResponse object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.tenant_structures%20%3E%20(model)%20tenant_structure_delete_response%20%3E%20(schema)>)

#### Tenant StructuresNodes

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