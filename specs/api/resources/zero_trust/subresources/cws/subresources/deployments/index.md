---
title: Deployments
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Cloud Workload Security](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Deployments

##### [List deployments](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/deployments/methods/list)

GET/accounts/{account\_id}/cws/deployments

##### [Get a deployment by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/deployments/methods/get)

GET/accounts/{account\_id}/cws/deployments/{deployment\_id}

##### [Create a new deployment](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/deployments/methods/create)

POST/accounts/{account\_id}/cws/deployments

##### [Update a deployment](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/deployments/methods/update)

PUT/accounts/{account\_id}/cws/deployments/{deployment\_id}

##### [Delete a deployment](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/deployments/methods/delete)

DELETE/accounts/{account\_id}/cws/deployments/{deployment\_id}

##### ModelsExpand Collapse

<details>

<summary>

Deployment object {id, basic\_auth\_credential\_ids, created\_at, 9 more }

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

[Link to this property](#)%20zero_trust.cws.deployments%20%3E%20(model)%20deployment%20%3E%20(schema)>)

<details>

<summary>

DeploymentDeleteResponse object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.deployments%20%3E%20(model)%20deployment_delete_response%20%3E%20(schema)>)