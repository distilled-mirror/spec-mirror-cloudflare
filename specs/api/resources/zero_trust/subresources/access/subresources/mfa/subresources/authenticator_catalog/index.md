---
title: Authenticator Catalog
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Access](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access)

[Mfa](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/mfa)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Authenticator Catalog

##### [List authenticator device AAGUIDs](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/mfa/subresources/authenticator_catalog/methods/list)

GET/accounts/{account\_id}/access/authenticator\_device\_aaguids

##### ModelsExpand Collapse

<details>

<summary>

AuthenticatorCatalogListResponse object {aaguid, name }

A FIDO2 authenticator device AAGUID entry

</summary>

aaguid: string

The Authenticator Attestation GUID (AAGUID) uniquely identifying a FIDO2 authenticator model

formatuuid

<a href="#">Link to this property</a>

name: string

The human-readable name of the FIDO2 authenticator

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.mfa.authenticator_catalog%20%3E%20(model)%20authenticator_catalog_list_response%20%3E%20(schema)>)