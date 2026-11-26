---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
title: Tenants
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy MarkdownView as Markdown**

# Tenants

#### TenantsAccount Types

#### TenantsAccounts

##### [List tenant accounts](https://developers.cloudflare.com/api/resources/tenants/subresources/accounts/methods/list)

GET/tenants/{tenant\_id}/accounts

##### ModelsExpand Collapse

<details>

<summary>

TenantAccount object { id, created\_on, name, 5 more }

</summary>

id: string

<a href="#">Link to this property</a>

created\_on: string

formatdate-time

<a href="#">Link to this property</a>

name: string

<a href="#">Link to this property</a>

<details>

<summary>

settings: object { abuse\_contact\_email, access\_approval\_expiry, api\_access\_enabled, 3 more }

</summary>

abuse\_contact\_email: string

<a href="#">Link to this property</a>

access\_approval\_expiry: string

formatdate-time

<a href="#">Link to this property</a>

api\_access\_enabled: boolean

<a href="#">Link to this property</a>

Deprecateddefault\_nameservers: string

Use <a href="https://developers.cloudflare.com/api/operations/dns-settings-for-an-account-list-dns-settings">DNS Settings</a> instead. Deprecated.

<a href="#">Link to this property</a>

enforce\_twofactor: boolean

<a href="#">Link to this property</a>

Deprecateduse\_account\_custom\_ns\_by\_default: boolean

Use <a href="https://developers.cloudflare.com/api/operations/dns-settings-for-an-account-list-dns-settings">DNS Settings</a> instead. Deprecated.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

type: "standard" or "enterprise"

</summary>

One of the following:

"standard"

<a href="#">Link to this property</a>

"enterprise"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

enterprise\_provisioning\_status: optional "pending" or "completed" or "rejected" or "cancelled"

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"completed"

<a href="#">Link to this property</a>

"rejected"

<a href="#">Link to this property</a>

"cancelled"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

provisioning\_mode: optional "assisted"

<a href="#">Link to this property</a>

tags: optional map\[string]

Account tags, present only when <code>include_tags=true</code> is requested.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20tenants.accounts%20%3E%20(model)%20tenant_account%20%3E%20(schema)>)

<details>

<summary>

AccountListResponse object { account\_pubname, account\_tag, account\_type, 2 more }

</summary>

account\_pubname: string

<a href="#">Link to this property</a>

account\_tag: string

<a href="#">Link to this property</a>

<details>

<summary>

account\_type: "standard" or "enterprise"

</summary>

One of the following:

"standard"

<a href="#">Link to this property</a>

"enterprise"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_on: string

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

settings: object { access\_approval\_expiry, api\_access\_enabled, enforce\_two\_factor, use\_account\_custom\_ns\_by\_default }

</summary>

access\_approval\_expiry: string

formatdate-time

<a href="#">Link to this property</a>

api\_access\_enabled: boolean

<a href="#">Link to this property</a>

enforce\_two\_factor: boolean

<a href="#">Link to this property</a>

use\_account\_custom\_ns\_by\_default: boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20tenants.accounts%20%3E%20(model)%20account_list_response%20%3E%20(schema)>)

#### TenantsEntitlements

#### TenantsMemberships