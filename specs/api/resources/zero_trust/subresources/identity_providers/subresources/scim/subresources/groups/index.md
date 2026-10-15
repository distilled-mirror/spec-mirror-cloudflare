---
title: Groups
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Identity Providers](https://developers.cloudflare.com/api/resources/zero_trust/subresources/identity_providers)

[SCIM](https://developers.cloudflare.com/api/resources/zero_trust/subresources/identity_providers/subresources/scim)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Groups

##### [List SCIM Group resources](https://developers.cloudflare.com/api/resources/zero_trust/subresources/identity_providers/subresources/scim/subresources/groups/methods/list)

GET/accounts/{account\_id}/access/identity\_providers/{identity\_provider\_id}/scim/groups

##### [Get a SCIM Group resource](https://developers.cloudflare.com/api/resources/zero_trust/subresources/identity_providers/subresources/scim/subresources/groups/methods/get)

GET/accounts/{account\_id}/access/identity\_providers/{identity\_provider\_id}/scim/groups/{group\_id}

##### [Delete a SCIM Group resource](https://developers.cloudflare.com/api/resources/zero_trust/subresources/identity_providers/subresources/scim/subresources/groups/methods/delete)

DELETE/accounts/{account\_id}/access/identity\_providers/{identity\_provider\_id}/scim/groups/{group\_id}

##### ModelsExpand Collapse

<details>

<summary>

GroupGetResponse object {id, displayName, externalId, 3 more }

</summary>

id: optional string

The unique Cloudflare-generated Id of the SCIM resource.

<a href="#">Link to this property</a>

displayName: optional string

The display name of the SCIM Group resource.

<a href="#">Link to this property</a>

externalId: optional string

The IdP-generated Id of the SCIM resource.

<a href="#">Link to this property</a>

<details>

<summary>

members: optional array of object {value, "$ref", display, type }

The direct members of the SCIM Group resource.

</summary>

value: string

The unique Cloudflare-generated Id of the member resource.

<a href="#">Link to this property</a>

"$ref": optional string

The URI of the member resource.

formaturi

<a href="#">Link to this property</a>

display: optional string

The display name of the member resource.

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "User"or "Group"

The SCIM resource type of the member.

</summary>

One of the following:

"User"

<a href="#">Link to this property</a>

"Group"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

meta: optional object {created, lastModified }

The metadata of the SCIM resource.

</summary>

created: optional string

The timestamp of when the SCIM resource was created.

formatdate-time

<a href="#">Link to this property</a>

lastModified: optional string

The timestamp of when the SCIM resource was last modified.

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

schemas: optional array of string

The list of URIs which indicate the attributes contained within a SCIM resource.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.identity_providers.scim.groups%20%3E%20(model)%20group_get_response%20%3E%20(schema)>)