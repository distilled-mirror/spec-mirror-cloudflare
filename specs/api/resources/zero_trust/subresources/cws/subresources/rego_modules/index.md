---
title: Rego Modules
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Cloud Workload Security](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Rego Modules

##### [List Rego modules](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/rego_modules/methods/list)

GET/accounts/{account\_id}/cws/rego-modules

##### [Get a Rego module by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/rego_modules/methods/get)

GET/accounts/{account\_id}/cws/rego-modules/{rego\_module\_id}

##### [Create a new Rego module](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/rego_modules/methods/create)

POST/accounts/{account\_id}/cws/rego-modules

##### [Update a Rego module](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/rego_modules/methods/update)

PUT/accounts/{account\_id}/cws/rego-modules/{rego\_module\_id}

##### [Delete a Rego module](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/rego_modules/methods/delete)

DELETE/accounts/{account\_id}/cws/rego-modules/{rego\_module\_id}

##### ModelsExpand Collapse

<details>

<summary>

RegoModule object {id, created\_at, name, 3 more }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

name: string

Human-readable name; unique per account

maxLength100

minLength1

<a href="#">Link to this property</a>

package\_path: string

Dotted path derived from rego\_source. Begins with lib. and is unique per account.

maxLength1024

<a href="#">Link to this property</a>

rego\_source: string

Library Rego source with a package beginning with “lib.” Maximum 16384 UTF-8 bytes.

maxLength16384

minLength1

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.rego_modules%20%3E%20(model)%20rego_module%20%3E%20(schema)>)

<details>

<summary>

RegoModuleDeleteResponse object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.rego_modules%20%3E%20(model)%20rego_module_delete_response%20%3E%20(schema)>)