---
title: Policy Sets
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Cloud Workload Security](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Policy Sets

##### [List policy sets](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policy_sets/methods/list)

GET/accounts/{account\_id}/cws/policy-sets

##### [Get a policy set by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policy_sets/methods/get)

GET/accounts/{account\_id}/cws/policy-sets/{policy\_set\_id}

##### [Create a new policy set](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policy_sets/methods/create)

POST/accounts/{account\_id}/cws/policy-sets

##### [Update a policy set](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policy_sets/methods/update)

PUT/accounts/{account\_id}/cws/policy-sets/{policy\_set\_id}

##### [Delete a policy set](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/policy_sets/methods/delete)

DELETE/accounts/{account\_id}/cws/policy-sets/{policy\_set\_id}

##### ModelsExpand Collapse

<details>

<summary>

PolicySet object {id, created\_at, exclude\_workload\_ids, 6 more }

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

[Link to this property](#)%20zero_trust.cws.policy_sets%20%3E%20(model)%20policy_set%20%3E%20(schema)>)

<details>

<summary>

PolicySetDeleteResponse object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.policy_sets%20%3E%20(model)%20policy_set_delete_response%20%3E%20(schema)>)