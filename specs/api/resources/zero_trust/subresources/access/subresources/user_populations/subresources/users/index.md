---
title: Users
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Access](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access)

[User Populations](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/user_populations)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Users

##### [List users in a user population](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/user_populations/subresources/users/methods/list)

GET/accounts/{account\_id}/access/user\_populations/{user\_population\_id}/users

##### [Create a user population user](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/user_populations/subresources/users/methods/create)

POST/accounts/{account\_id}/access/user\_populations/{user\_population\_id}/users

##### [Get a user population user](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/user_populations/subresources/users/methods/get)

GET/accounts/{account\_id}/access/user\_populations/{user\_population\_id}/users/{user\_id}

##### [Update a user population user](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/user_populations/subresources/users/methods/update)

PATCH/accounts/{account\_id}/access/user\_populations/{user\_population\_id}/users/{user\_id}

##### [Replace a user population user](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/user_populations/subresources/users/methods/replace)

PUT/accounts/{account\_id}/access/user\_populations/{user\_population\_id}/users/{user\_id}

##### [Delete a user population user](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/user_populations/subresources/users/methods/delete)

DELETE/accounts/{account\_id}/access/user\_populations/{user\_population\_id}/users/{user\_id}

##### ModelsExpand Collapse

<details>

<summary>

UserListResponse object {itemsPerPage, Resources, schemas, 2 more }

</summary>

itemsPerPage: number

<a href="#">Link to this property</a>

<details>

<summary>

Resources: array of object {id, active, displayName, 6 more }

</summary>

id: optional string

<a href="#">Link to this property</a>

active: optional boolean

<a href="#">Link to this property</a>

displayName: optional string

<a href="#">Link to this property</a>

<details>

<summary>

emails: optional array of object {primary, type, value }

</summary>

primary: optional boolean

<a href="#">Link to this property</a>

type: optional string

<a href="#">Link to this property</a>

value: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

externalId: optional string

<a href="#">Link to this property</a>

<details>

<summary>

meta: optional object {created, lastModified, location, 2 more }

</summary>

created: optional string

formatdate-time

<a href="#">Link to this property</a>

lastModified: optional string

formatdate-time

<a href="#">Link to this property</a>

location: optional string

formaturi

<a href="#">Link to this property</a>

resourceType: optional string

<a href="#">Link to this property</a>

version: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

name: optional object {familyName, formatted, givenName, 3 more }

</summary>

familyName: optional string

<a href="#">Link to this property</a>

formatted: optional string

<a href="#">Link to this property</a>

givenName: optional string

<a href="#">Link to this property</a>

honorificPrefix: optional string

<a href="#">Link to this property</a>

honorificSuffix: optional string

<a href="#">Link to this property</a>

middleName: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

schemas: optional array of string

The SCIM schemas that apply to this resource.

<a href="#">Link to this property</a>

userName: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

schemas: array of string

<a href="#">Link to this property</a>

startIndex: number

<a href="#">Link to this property</a>

totalResults: number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.user_populations.users%20%3E%20(model)%20user_list_response%20%3E%20(schema)>)

<details>

<summary>

UserCreateResponse object {id, active, displayName, 6 more }

A SCIM User resource. Additional SCIM extension attributes are supported.

</summary>

id: optional string

<a href="#">Link to this property</a>

active: optional boolean

<a href="#">Link to this property</a>

displayName: optional string

<a href="#">Link to this property</a>

<details>

<summary>

emails: optional array of object {primary, type, value }

</summary>

primary: optional boolean

<a href="#">Link to this property</a>

type: optional string

<a href="#">Link to this property</a>

value: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

externalId: optional string

<a href="#">Link to this property</a>

<details>

<summary>

meta: optional object {created, lastModified, location, 2 more }

</summary>

created: optional string

formatdate-time

<a href="#">Link to this property</a>

lastModified: optional string

formatdate-time

<a href="#">Link to this property</a>

location: optional string

formaturi

<a href="#">Link to this property</a>

resourceType: optional string

<a href="#">Link to this property</a>

version: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

name: optional object {familyName, formatted, givenName, 3 more }

</summary>

familyName: optional string

<a href="#">Link to this property</a>

formatted: optional string

<a href="#">Link to this property</a>

givenName: optional string

<a href="#">Link to this property</a>

honorificPrefix: optional string

<a href="#">Link to this property</a>

honorificSuffix: optional string

<a href="#">Link to this property</a>

middleName: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

schemas: optional array of string

The SCIM schemas that apply to this resource.

<a href="#">Link to this property</a>

userName: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.user_populations.users%20%3E%20(model)%20user_create_response%20%3E%20(schema)>)

<details>

<summary>

UserGetResponse object {id, active, displayName, 6 more }

A SCIM User resource. Additional SCIM extension attributes are supported.

</summary>

id: optional string

<a href="#">Link to this property</a>

active: optional boolean

<a href="#">Link to this property</a>

displayName: optional string

<a href="#">Link to this property</a>

<details>

<summary>

emails: optional array of object {primary, type, value }

</summary>

primary: optional boolean

<a href="#">Link to this property</a>

type: optional string

<a href="#">Link to this property</a>

value: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

externalId: optional string

<a href="#">Link to this property</a>

<details>

<summary>

meta: optional object {created, lastModified, location, 2 more }

</summary>

created: optional string

formatdate-time

<a href="#">Link to this property</a>

lastModified: optional string

formatdate-time

<a href="#">Link to this property</a>

location: optional string

formaturi

<a href="#">Link to this property</a>

resourceType: optional string

<a href="#">Link to this property</a>

version: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

name: optional object {familyName, formatted, givenName, 3 more }

</summary>

familyName: optional string

<a href="#">Link to this property</a>

formatted: optional string

<a href="#">Link to this property</a>

givenName: optional string

<a href="#">Link to this property</a>

honorificPrefix: optional string

<a href="#">Link to this property</a>

honorificSuffix: optional string

<a href="#">Link to this property</a>

middleName: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

schemas: optional array of string

The SCIM schemas that apply to this resource.

<a href="#">Link to this property</a>

userName: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.user_populations.users%20%3E%20(model)%20user_get_response%20%3E%20(schema)>)

<details>

<summary>

UserUpdateResponse object {id, active, displayName, 6 more }

A SCIM User resource. Additional SCIM extension attributes are supported.

</summary>

id: optional string

<a href="#">Link to this property</a>

active: optional boolean

<a href="#">Link to this property</a>

displayName: optional string

<a href="#">Link to this property</a>

<details>

<summary>

emails: optional array of object {primary, type, value }

</summary>

primary: optional boolean

<a href="#">Link to this property</a>

type: optional string

<a href="#">Link to this property</a>

value: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

externalId: optional string

<a href="#">Link to this property</a>

<details>

<summary>

meta: optional object {created, lastModified, location, 2 more }

</summary>

created: optional string

formatdate-time

<a href="#">Link to this property</a>

lastModified: optional string

formatdate-time

<a href="#">Link to this property</a>

location: optional string

formaturi

<a href="#">Link to this property</a>

resourceType: optional string

<a href="#">Link to this property</a>

version: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

name: optional object {familyName, formatted, givenName, 3 more }

</summary>

familyName: optional string

<a href="#">Link to this property</a>

formatted: optional string

<a href="#">Link to this property</a>

givenName: optional string

<a href="#">Link to this property</a>

honorificPrefix: optional string

<a href="#">Link to this property</a>

honorificSuffix: optional string

<a href="#">Link to this property</a>

middleName: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

schemas: optional array of string

The SCIM schemas that apply to this resource.

<a href="#">Link to this property</a>

userName: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.user_populations.users%20%3E%20(model)%20user_update_response%20%3E%20(schema)>)

<details>

<summary>

UserReplaceResponse object {id, active, displayName, 6 more }

A SCIM User resource. Additional SCIM extension attributes are supported.

</summary>

id: optional string

<a href="#">Link to this property</a>

active: optional boolean

<a href="#">Link to this property</a>

displayName: optional string

<a href="#">Link to this property</a>

<details>

<summary>

emails: optional array of object {primary, type, value }

</summary>

primary: optional boolean

<a href="#">Link to this property</a>

type: optional string

<a href="#">Link to this property</a>

value: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

externalId: optional string

<a href="#">Link to this property</a>

<details>

<summary>

meta: optional object {created, lastModified, location, 2 more }

</summary>

created: optional string

formatdate-time

<a href="#">Link to this property</a>

lastModified: optional string

formatdate-time

<a href="#">Link to this property</a>

location: optional string

formaturi

<a href="#">Link to this property</a>

resourceType: optional string

<a href="#">Link to this property</a>

version: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

name: optional object {familyName, formatted, givenName, 3 more }

</summary>

familyName: optional string

<a href="#">Link to this property</a>

formatted: optional string

<a href="#">Link to this property</a>

givenName: optional string

<a href="#">Link to this property</a>

honorificPrefix: optional string

<a href="#">Link to this property</a>

honorificSuffix: optional string

<a href="#">Link to this property</a>

middleName: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

schemas: optional array of string

The SCIM schemas that apply to this resource.

<a href="#">Link to this property</a>

userName: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.user_populations.users%20%3E%20(model)%20user_replace_response%20%3E%20(schema)>)