---
title: Asset Schemas
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Casb](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb)

[Posture](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Asset Schemas

##### [List asset schemas](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/asset_schemas/methods/list)

GET/accounts/{account\_id}/data-security/posture/asset\_schemas

##### [Get asset schema by asset class](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/asset_schemas/methods/get)

GET/accounts/{account\_id}/data-security/posture/asset\_schemas/{asset\_class}

##### ModelsExpand Collapse

<details>

<summary>

AssetSchemaListResponse object {asset\_classes, vendor }

</summary>

<details>

<summary>

asset\_classes: array of object {asset\_class }

Asset classes belonging to this vendor, sorted by asset\_class.

</summary>

asset\_class: string

Asset class identifier (PascalCase), e.g. AnthropicUser.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

vendor: string

Canonical vendor enum value, e.g. GOOGLE\_WORKSPACE.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.asset_schemas%20%3E%20(model)%20asset_schema_list_response%20%3E%20(schema)>)

<details>

<summary>

AssetSchemaGetResponse object {asset\_class, schema }

</summary>

asset\_class: string

Asset class identifier (PascalCase), e.g. AnthropicApiKey.

<a href="#">Link to this property</a>

schema: map\[unknown]

Fields and related attributes a custom finding type may reference for this asset class, as a JSON Schema. Top-level properties are <code>asset</code> and, when related resources exist, <code>associated</code>.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.asset_schemas%20%3E%20(model)%20asset_schema_get_response%20%3E%20(schema)>)