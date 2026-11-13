---
title: Account Regions
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Account Regions

##### [List available regions](https://developers.cloudflare.com/api/resources/zero_trust/subresources/regions/methods/list)

GET/accounts/{account\_id}/zerotrust/regions

##### [Get active region](https://developers.cloudflare.com/api/resources/zero_trust/subresources/regions/methods/get)

GET/accounts/{account\_id}/zerotrust/region

##### [Select region](https://developers.cloudflare.com/api/resources/zero_trust/subresources/regions/methods/update)

PUT/accounts/{account\_id}/zerotrust/region

##### [Clear active region](https://developers.cloudflare.com/api/resources/zero_trust/subresources/regions/methods/delete)

DELETE/accounts/{account\_id}/zerotrust/region

##### ModelsExpand Collapse

<details>

<summary>

AccountRegion object {region\_key }

</summary>

region\_key: string

The key of a Data Localization Suite region.

minLength1

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.regions%20%3E%20(model)%20account_region%20%3E%20(schema)>)

<details>

<summary>

ActiveAccountRegion object {region\_key }

</summary>

region\_key: string

The key of the account’s active Data Localization Suite region, or <code>null</code> if the account has not selected a region.

minLength1

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.regions%20%3E%20(model)%20active_account_region%20%3E%20(schema)>)