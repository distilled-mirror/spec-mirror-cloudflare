---
title: Tokens
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[User](https://developers.cloudflare.com/api/resources/user)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Tokens

##### [List Tokens](https://developers.cloudflare.com/api/resources/user/subresources/tokens/methods/list)

GET/user/tokens

##### [Token Details](https://developers.cloudflare.com/api/resources/user/subresources/tokens/methods/get)

GET/user/tokens/{token\_id}

##### [Create Token](https://developers.cloudflare.com/api/resources/user/subresources/tokens/methods/create)

POST/user/tokens

##### [Update Token](https://developers.cloudflare.com/api/resources/user/subresources/tokens/methods/update)

PUT/user/tokens/{token\_id}

##### [Delete Token](https://developers.cloudflare.com/api/resources/user/subresources/tokens/methods/delete)

DELETE/user/tokens/{token\_id}

##### [Verify Token](https://developers.cloudflare.com/api/resources/user/subresources/tokens/methods/verify)

GET/user/tokens/verify

##### ModelsExpand Collapse

<details>

<summary>

TokenCreateResponse object {id, condition, creator\_email\_at\_creation, 11 more }

</summary>

id: optional string

Token identifier tag.

maxLength32

<a href="#">Link to this property</a>

<details>

<summary>

condition: optional object {request\_ip }

</summary>

<details>

<summary>

request\_ip: optional object {in, not\_in }

Client IP restrictions.

</summary>

in: optional array of <a href="https://developers.cloudflare.com/api/resources/$shared#(resource)%20%24shared%20%3E%20(model)%20token_condition_cidr_list%20%3E%20(schema)">TokenConditionCIDRList</a>

List of IPv4/IPv6 CIDR addresses.

<a href="#">Link to this property</a>

not\_in: optional array of <a href="https://developers.cloudflare.com/api/resources/$shared#(resource)%20%24shared%20%3E%20(model)%20token_condition_cidr_list%20%3E%20(schema)">TokenConditionCIDRList</a>

List of IPv4/IPv6 CIDR addresses.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

creator\_email\_at\_creation: optional string

The email address of the user who created the token at the time of creation. Only present for Account Owned API Tokens when a creator email was available.

maxLength90

<a href="#">Link to this property</a>

expires\_on: optional string

The expiration time on or after which the JWT MUST NOT be accepted for processing.

formatdate-time

<a href="#">Link to this property</a>

issued\_on: optional string

The time on which the token was created.

formatdate-time

<a href="#">Link to this property</a>

last\_used\_on: optional string

Last time the token was used.

formatdate-time

<a href="#">Link to this property</a>

modified\_on: optional string

Last time the token was modified.

formatdate-time

<a href="#">Link to this property</a>

name: optional string

Token name.

maxLength120

<a href="#">Link to this property</a>

not\_before: optional string

The time before which the token MUST NOT be accepted for processing.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

policies: optional array of <a href="https://developers.cloudflare.com/api/resources/$shared#(resource)%20%24shared%20%3E%20(model)%20token_policy%20%3E%20(schema)">TokenPolicy</a> { id, effect, permission\_groups, resources }

List of access policies assigned to the token.

</summary>

id: string

Policy identifier.

<a href="#">Link to this property</a>

<details>

<summary>

effect: "allow"or "deny"

Allow or deny operations against the resources.

</summary>

One of the following:

"allow"

<a href="#">Link to this property</a>

"deny"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

permission\_groups: array of object {id, meta, name }

A set of permission groups that are specified to the policy.

</summary>

id: string

Identifier of the permission group.

<a href="#">Link to this property</a>

<details>

<summary>

meta: optional object {category, deprecated, description, 5 more }

Attributes associated to the permission group.

</summary>

category: optional string

A category used to group permission groups.

<a href="#">Link to this property</a>

deprecated: optional string

Indicates whether the permission group is deprecated.

<a href="#">Link to this property</a>

description: optional string

Additional information about the permission group.

<a href="#">Link to this property</a>

editable: optional string

Indicates whether the permission group can be edited.

<a href="#">Link to this property</a>

eol\_at: optional string

The planned end-of-life date and time, when provided.

formatdate-time

<a href="#">Link to this property</a>

label: optional string

A label identifying the permission group.

<a href="#">Link to this property</a>

scopes: optional string

The scope associated with the permission group.

<a href="#">Link to this property</a>

visibility: optional string

Indicates the permission group’s availability or visibility.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: optional string

Name of the permission group.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

resources: map\[string]or map\[map\[string]]

A list of resource names that the policy applies to.

</summary>

One of the following:

IAMResourcesTypeObjectString = map\[string]

Map of simple string resource permissions

<a href="#">Link to this property</a>

IAMResourcesTypeObjectNested = map\[map\[string]]

Map of nested resource permissions

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

provisioner\_id: optional string

The identifier of the service that provisioned the token. For an OAuth-provisioned token, this is the OAuth client identifier. Present when <code>provisioner_type</code> is present and null when the identifier is unavailable.

<a href="#">Link to this property</a>

provisioner\_type: optional string

The type of service that provisioned the token. Only present for provisioned Account Owned API Tokens.

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "active"or "disabled"or "expired"

Status of the token.

</summary>

One of the following:

"active"

<a href="#">Link to this property</a>

"disabled"

<a href="#">Link to this property</a>

"expired"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

value: optional <a href="https://developers.cloudflare.com/api/resources/$shared#(resource)%20%24shared%20%3E%20(model)%20token_value%20%3E%20(schema)">TokenValue</a>

The token value.

maxLength80

minLength40

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20user.tokens%20%3E%20(model)%20token_create_response%20%3E%20(schema)>)

<details>

<summary>

TokenDeleteResponse object {id }

</summary>

id: string

Identifier

maxLength32

minLength32

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20user.tokens%20%3E%20(model)%20token_delete_response%20%3E%20(schema)>)

<details>

<summary>

TokenVerifyResponse object {id, status, expires\_on, not\_before }

</summary>

id: string

Token identifier tag.

maxLength32

<a href="#">Link to this property</a>

<details>

<summary>

status: "active"or "disabled"or "expired"

Status of the token.

</summary>

One of the following:

"active"

<a href="#">Link to this property</a>

"disabled"

<a href="#">Link to this property</a>

"expired"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

expires\_on: optional string

The expiration time on or after which the JWT MUST NOT be accepted for processing.

formatdate-time

<a href="#">Link to this property</a>

not\_before: optional string

The time before which the token MUST NOT be accepted for processing.

formatdate-time

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20user.tokens%20%3E%20(model)%20token_verify_response%20%3E%20(schema)>)

#### TokensPermission Groups

##### [List Token Permission Groups](https://developers.cloudflare.com/api/resources/user/subresources/tokens/subresources/permission_groups/methods/list)

GET/user/tokens/permission\_groups

##### ModelsExpand Collapse

<details>

<summary>

PermissionGroupListResponse object {id, category, is\_selectable, 2 more }

</summary>

id: optional string

Public ID.

<a href="#">Link to this property</a>

<details>

<summary>

category: optional "developer\_platform"or "ai\_and\_machine\_learning"or "dns\_and\_zones"or 10 more

Product category that this permission group belongs to.

</summary>

One of the following:

"developer\_platform"

<a href="#">Link to this property</a>

"ai\_and\_machine\_learning"

<a href="#">Link to this property</a>

"dns\_and\_zones"

<a href="#">Link to this property</a>

"app\_security"

<a href="#">Link to this property</a>

"rules\_and\_configuration"

<a href="#">Link to this property</a>

"cloudflare\_one\_and\_zero\_trust"

<a href="#">Link to this property</a>

"analytics\_and\_logs"

<a href="#">Link to this property</a>

"network\_services"

<a href="#">Link to this property</a>

"media"

<a href="#">Link to this property</a>

"email\_and\_messaging"

<a href="#">Link to this property</a>

"cache\_and\_performance"

<a href="#">Link to this property</a>

"account\_and\_billing"

<a href="#">Link to this property</a>

"other"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

is\_selectable: optional boolean

Whether the caller can select this permission group when creating a token.

<a href="#">Link to this property</a>

name: optional string

Permission Group Name

<a href="#">Link to this property</a>

<details>

<summary>

scopes: optional array of "com.cloudflare.api.account"or "com.cloudflare.api.account.zone"or "com.cloudflare.api.user"or "com.cloudflare.edge.r2.bucket"

Resources to which the Permission Group is scoped

</summary>

One of the following:

"com.cloudflare.api.account"

<a href="#">Link to this property</a>

"com.cloudflare.api.account.zone"

<a href="#">Link to this property</a>

"com.cloudflare.api.user"

<a href="#">Link to this property</a>

"com.cloudflare.edge.r2.bucket"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20user.tokens.permission_groups%20%3E%20(model)%20permission_group_list_response%20%3E%20(schema)>)

#### TokensValue

##### [Roll Token](https://developers.cloudflare.com/api/resources/user/subresources/tokens/subresources/value/methods/update)

PUT/user/tokens/{token\_id}/value