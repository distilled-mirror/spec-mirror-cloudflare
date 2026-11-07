---
title: Trust Settings
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Organizations](https://developers.cloudflare.com/api/resources/zero_trust/subresources/organizations)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Trust Settings

##### [Get Zero Trust organization trust settings](https://developers.cloudflare.com/api/resources/zero_trust/subresources/organizations/subresources/trust_settings/methods/get)

GET/accounts/{account\_id}/access/organizations/trust\_settings

##### [Replace Zero Trust organization trust settings](https://developers.cloudflare.com/api/resources/zero_trust/subresources/organizations/subresources/trust_settings/methods/replace)

PUT/accounts/{account\_id}/access/organizations/trust\_settings

##### [Update Zero Trust organization trust settings](https://developers.cloudflare.com/api/resources/zero_trust/subresources/organizations/subresources/trust_settings/methods/update)

PATCH/accounts/{account\_id}/access/organizations/trust\_settings

##### [Delete Zero Trust organization trust settings](https://developers.cloudflare.com/api/resources/zero_trust/subresources/organizations/subresources/trust_settings/methods/delete)

DELETE/accounts/{account\_id}/access/organizations/trust\_settings

##### ModelsExpand Collapse

<details>

<summary>

TrustSettingGetResponse object {grant\_trust\_to\_all\_accounts\_in\_org, trusting\_accounts }

</summary>

grant\_trust\_to\_all\_accounts\_in\_org: boolean

Whether all accounts in the organization are trusted to use this account’s cross-account Access resources.

<a href="#">Link to this property</a>

trusting\_accounts: optional array of string

Explicit account IDs trusted to use this account’s cross-account Access resources. At most 100 unique valid account IDs are accepted. Omitted from responses when empty.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.organizations.trust_settings%20%3E%20(model)%20trust_setting_get_response%20%3E%20(schema)>)

<details>

<summary>

TrustSettingReplaceResponse object {grant\_trust\_to\_all\_accounts\_in\_org, trusting\_accounts }

</summary>

grant\_trust\_to\_all\_accounts\_in\_org: boolean

Whether all accounts in the organization are trusted to use this account’s cross-account Access resources.

<a href="#">Link to this property</a>

trusting\_accounts: optional array of string

Explicit account IDs trusted to use this account’s cross-account Access resources. At most 100 unique valid account IDs are accepted. Omitted from responses when empty.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.organizations.trust_settings%20%3E%20(model)%20trust_setting_replace_response%20%3E%20(schema)>)

<details>

<summary>

TrustSettingUpdateResponse object {grant\_trust\_to\_all\_accounts\_in\_org, trusting\_accounts }

</summary>

grant\_trust\_to\_all\_accounts\_in\_org: boolean

Whether all accounts in the organization are trusted to use this account’s cross-account Access resources.

<a href="#">Link to this property</a>

trusting\_accounts: optional array of string

Explicit account IDs trusted to use this account’s cross-account Access resources. At most 100 unique valid account IDs are accepted. Omitted from responses when empty.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.organizations.trust_settings%20%3E%20(model)%20trust_setting_update_response%20%3E%20(schema)>)

<details>

<summary>

TrustSettingDeleteResponse object {grant\_trust\_to\_all\_accounts\_in\_org, trusting\_accounts }

</summary>

grant\_trust\_to\_all\_accounts\_in\_org: boolean

Whether all accounts in the organization are trusted to use this account’s cross-account Access resources.

<a href="#">Link to this property</a>

trusting\_accounts: optional array of string

Explicit account IDs trusted to use this account’s cross-account Access resources. At most 100 unique valid account IDs are accepted. Omitted from responses when empty.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.organizations.trust_settings%20%3E%20(model)%20trust_setting_delete_response%20%3E%20(schema)>)