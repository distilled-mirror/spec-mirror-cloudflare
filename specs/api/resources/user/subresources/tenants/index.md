---
title: Tenants
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[User](https://developers.cloudflare.com/api/resources/user)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Tenants

##### [List user tenants](https://developers.cloudflare.com/api/resources/user/subresources/tenants/methods/list)

GET/user/tenants

##### ModelsExpand Collapse

<details>

<summary>

TenantListResponse object {cdate, customer\_id, edate, 10 more }

</summary>

cdate: string

formatdate-time

<a href="#">Link to this property</a>

customer\_id: string

<a href="#">Link to this property</a>

edate: string

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

tenant\_contacts: object {email, website }

</summary>

email: optional string

<a href="#">Link to this property</a>

website: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

tenant\_labels: array of string

<a href="#">Link to this property</a>

<details>

<summary>

tenant\_metadata: object {billing\_account\_type, configuration\_account, created\_by, 4 more }

</summary>

billing\_account\_type: optional string

<a href="#">Link to this property</a>

configuration\_account: optional string

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

<details>

<summary>

dns: optional object {ns\_pool }

</summary>

<details>

<summary>

ns\_pool: object {primary, secondary }

</summary>

primary: string

<a href="#">Link to this property</a>

secondary: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

flags: optional map\[string]

<a href="#">Link to this property</a>

<details>

<summary>

innate\_account\_entitlements: optional array of object {allocation, feature }

</summary>

<details>

<summary>

allocation: object {type, value }

</summary>

type: string

<a href="#">Link to this property</a>

<details>

<summary>

value: booleanor numberor stringor 2 more

</summary>

One of the following:

boolean

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

string

<a href="#">Link to this property</a>

map\[unknown]

<a href="#">Link to this property</a>

array of unknown

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

feature: object {key }

</summary>

key: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

tenant\_entitlements: optional array of object {allocation, feature }

</summary>

<details>

<summary>

allocation: object {type, value }

</summary>

type: string

<a href="#">Link to this property</a>

<details>

<summary>

value: booleanor numberor stringor 2 more

</summary>

One of the following:

boolean

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

string

<a href="#">Link to this property</a>

map\[unknown]

<a href="#">Link to this property</a>

array of unknown

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

feature: object {key }

</summary>

key: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

tenant\_name: string

<a href="#">Link to this property</a>

<details>

<summary>

tenant\_network: object {choices }

</summary>

choices: optional map\[unknown]

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

tenant\_status: string

<a href="#">Link to this property</a>

tenant\_tag: string

<a href="#">Link to this property</a>

tenant\_type: string

<a href="#">Link to this property</a>

<details>

<summary>

tenant\_units: array of object {unit\_memberships, unit\_metadata, unit\_name, 2 more }

</summary>

<details>

<summary>

unit\_memberships: array of object {member\_metadata, member\_status, member\_tag }

</summary>

member\_metadata: unknown

<a href="#">Link to this property</a>

member\_status: string

<a href="#">Link to this property</a>

member\_tag: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

unit\_metadata: unknown

<a href="#">Link to this property</a>

unit\_name: string

<a href="#">Link to this property</a>

unit\_status: string

<a href="#">Link to this property</a>

unit\_tag: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ui\_flags: object {show\_orgs\_ui, show\_tenants\_ui }

Which top-level dashboard experiences to render for this tenant; both may be true.

</summary>

show\_orgs\_ui: boolean

Render the Organizations experience for this tenant.

<a href="#">Link to this property</a>

show\_tenants\_ui: boolean

Render the legacy Tenants experience for this tenant.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20user.tenants%20%3E%20(model)%20tenant_list_response%20%3E%20(schema)>)