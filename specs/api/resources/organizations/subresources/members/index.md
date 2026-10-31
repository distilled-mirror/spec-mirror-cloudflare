---
title: Members
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Organizations](https://developers.cloudflare.com/api/resources/organizations)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Members

##### [List organization members](https://developers.cloudflare.com/api/resources/organizations/subresources/members/methods/list)

GET/organizations/{organization\_id}/members

##### [Get organization member](https://developers.cloudflare.com/api/resources/organizations/subresources/members/methods/get)

GET/organizations/{organization\_id}/members/{member\_id}

##### [Create organization member](https://developers.cloudflare.com/api/resources/organizations/subresources/members/methods/create)

POST/organizations/{organization\_id}/members

##### [Delete organization member](https://developers.cloudflare.com/api/resources/organizations/subresources/members/methods/delete)

DELETE/organizations/{organization\_id}/members/{member\_id}

##### ModelsExpand Collapse

<details>

<summary>

OrganizationMember object {id, create\_time, meta, 4 more }

</summary>

id: string

Organization Member ID

<a href="#">Link to this property</a>

create\_time: string

formatdate-time

<a href="#">Link to this property</a>

meta: map\[unknown]

<a href="#">Link to this property</a>

<details>

<summary>

status: "active"or "pending"or "rejected"or "canceled"

</summary>

One of the following:

"active"

<a href="#">Link to this property</a>

"pending"

<a href="#">Link to this property</a>

"rejected"

<a href="#">Link to this property</a>

"canceled"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

update\_time: string

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

user: object {id, email, name, two\_factor\_authentication\_enabled }

</summary>

id: string

<a href="#">Link to this property</a>

email: string

<a href="#">Link to this property</a>

name: string

<a href="#">Link to this property</a>

two\_factor\_authentication\_enabled: boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

policies: optional array of object {roles, scopes, id }

Direct policies of the membership. Present only for DSR members enrolled in Organization Roles.

</summary>

<details>

<summary>

roles: array of object {id }

</summary>

id: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

scopes: array of object {key, subset\_of }

</summary>

key: string

An Organization (<code>com.cloudflare.api.tenant.unit.&lt;tag&gt;</code>) or Account (<code>com.cloudflare.api.account.&lt;tag&gt;</code>) key.

<a href="#">Link to this property</a>

subset\_of: optional array of unknown

The route Organization for Account scopes. Optional in requests and always returned for Account scopes.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

id: optional string

Omit to create a policy. An unchanged policy keeps its ID; a changed policy is replaced under a new ID.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20organizations.members%20%3E%20(model)%20organization_member%20%3E%20(schema)>)

<details>

<summary>

MemberDeleteResponse object {id }

</summary>

id: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20organizations.members%20%3E%20(model)%20member_delete_response%20%3E%20(schema)>)