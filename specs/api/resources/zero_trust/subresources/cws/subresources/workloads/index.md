---
title: Workloads
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Cloud Workload Security](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Workloads

##### [List workloads](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/workloads/methods/list)

GET/accounts/{account\_id}/cws/workloads

##### [Get a workload by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/workloads/methods/get)

GET/accounts/{account\_id}/cws/workloads/{workload\_id}

##### [Create a new workload](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/workloads/methods/create)

POST/accounts/{account\_id}/cws/workloads

##### [Update a workload](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/workloads/methods/update)

PUT/accounts/{account\_id}/cws/workloads/{workload\_id}

##### [Delete a workload](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/workloads/methods/delete)

DELETE/accounts/{account\_id}/cws/workloads/{workload\_id}

##### ModelsExpand Collapse

<details>

<summary>

Workload object {id, created\_at, filter, 4 more }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

filter: string

Filter expression selecting the requests this workload matches. Maximum 4096 UTF-8 bytes.

maxLength4096

minLength1

<a href="#">Link to this property</a>

name: string

Human-readable handle; unique per account.

maxLength100

minLength1

<a href="#">Link to this property</a>

tags: map\[string]

Tags attached to this workload

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

description: optional string

Optional free-form description.

maxLength1024

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.workloads%20%3E%20(model)%20workload%20%3E%20(schema)>)

<details>

<summary>

WorkloadDeleteResponse object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.workloads%20%3E%20(model)%20workload_delete_response%20%3E%20(schema)>)