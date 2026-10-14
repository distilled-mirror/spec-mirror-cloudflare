---
title: Domain ACLs
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Cloud Workload Security](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Domain ACLs

##### [List domain ACLs](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/domain_acls/methods/list)

GET/accounts/{account\_id}/cws/domain-acls

##### [Get a domain ACL by ID](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/domain_acls/methods/get)

GET/accounts/{account\_id}/cws/domain-acls/{domain\_acl\_id}

##### [Create a new domain ACL](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/domain_acls/methods/create)

POST/accounts/{account\_id}/cws/domain-acls

##### [Update a domain ACL and replace its entries](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/domain_acls/methods/update)

PUT/accounts/{account\_id}/cws/domain-acls/{domain\_acl\_id}

##### [Delete a domain ACL](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/domain_acls/methods/delete)

DELETE/accounts/{account\_id}/cws/domain-acls/{domain\_acl\_id}

##### ModelsExpand Collapse

<details>

<summary>

DomainACL object {id, created\_at, default\_action, 3 more }

</summary>

id: string

Server-assigned UUID

formatuuid

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

default\_action: "ALLOW"or "BLOCK"

Action applied when no entry matches the request domain

</summary>

One of the following:

"ALLOW"

<a href="#">Link to this property</a>

"BLOCK"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

entries: array of object {action, domain }

Per-domain action overrides. Each domain appears at most once.

</summary>

<details>

<summary>

action: "ALLOW"or "BLOCK"

Per-domain decision overriding the parent ACL’s default\_action

</summary>

One of the following:

"ALLOW"

<a href="#">Link to this property</a>

"BLOCK"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

domain: string

Hostname or domain pattern, capped at 255 UTF-8 bytes

maxLength255

minLength1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

Human-readable name; unique per account

maxLength100

minLength1

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.domain_acls%20%3E%20(model)%20domain_acl%20%3E%20(schema)>)

<details>

<summary>

DomainACLDeleteResponse object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.domain_acls%20%3E%20(model)%20domain_acl_delete_response%20%3E%20(schema)>)