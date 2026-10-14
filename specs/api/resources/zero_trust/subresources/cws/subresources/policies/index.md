---
title: Policies
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Cloud Workload Security](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Policies

##### [List policies](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policies/methods/list)

GET/accounts/{account\_id}/cws/policies

##### [Get a policy by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policies/methods/get)

GET/accounts/{account\_id}/cws/policies/{policy\_id}

##### [Create a new policy](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policies/methods/create)

POST/accounts/{account\_id}/cws/policies

##### [Update a policy](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policies/methods/update)

PUT/accounts/{account\_id}/cws/policies/{policy\_id}

##### [Delete a policy](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policies/methods/delete)

DELETE/accounts/{account\_id}/cws/policies/{policy\_id}

##### ModelsExpand Collapse

<details>

<summary>

Policy object {id, created\_at, entrypoint, 7 more }

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

Optional filter expression that determines whether this policy applies. Null means the policy applies to every request. Maximum 4096 UTF-8 bytes.

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

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(model)%20policy%20%3E%20(schema)>)

<details>

<summary>

PolicyDeleteResponse object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.policies%20%3E%20(model)%20policy_delete_response%20%3E%20(schema)>)