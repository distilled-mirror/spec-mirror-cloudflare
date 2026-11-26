---
agent:
  instructions: "Use this search API to find relevant content across this site with keywords or natural-language queries, instead of crawling individual pages. Results are returned in Markdown."
  endpoint: "https://developers.cloudflare.com/.well-known/search?q={query}"
  method: "GET"
  documentation: "https://developers.cloudflare.com/ai-search/how-to/search-for-agents/"
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

**Copy MarkdownView as Markdown**

# Asset Schemas

##### [List asset schemas](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/asset_schemas/methods/list)

GET/accounts/{account\_id}/data-security/posture/asset\_schemas

##### [Get asset schema by asset class](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/asset_schemas/methods/get)

GET/accounts/{account\_id}/data-security/posture/asset\_schemas/{asset\_class}

##### ModelsExpand Collapse

<details>

<summary>

AssetSchemaListResponse object { asset\_classes, vendor }

</summary>

<details>

<summary>

asset\_classes: array of object { asset\_class, origin, id, 2 more }

Asset classes belonging to this vendor, sorted by asset\_class.

</summary>

asset\_class: string

Asset class identifier (PascalCase), e.g. AnthropicUser.

<a href="#">Link to this property</a>

<details>

<summary>

origin: "system" or "cloudflare" or "custom"

Who defines the asset class: <code>system</code> for built-in asset classes, <code>cloudflare</code> for asset types provided by Cloudflare, and <code>custom</code> for the account’s own asset types.

</summary>

One of the following:

"system"

<a href="#">Link to this property</a>

"cloudflare"

<a href="#">Link to this property</a>

"custom"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

id: optional string

Unique identifier. Present for <code>cloudflare</code> and <code>custom</code> asset types.

formatuuid

<a href="#">Link to this property</a>

display\_name: optional string

Human-readable name. Present for <code>cloudflare</code> and <code>custom</code> asset types.

<a href="#">Link to this property</a>

version: optional number

Current version. Present for <code>cloudflare</code> and <code>custom</code> asset types.

formatint64

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

AssetSchemaGetResponse object { asset\_class, origin, schema, 4 more }

</summary>

asset\_class: string

Asset class identifier (PascalCase), e.g. AnthropicApiKey.

<a href="#">Link to this property</a>

<details>

<summary>

origin: "system" or "cloudflare" or "custom"

Who defines the asset class: <code>system</code> for built-in asset classes, <code>cloudflare</code> for asset types provided by Cloudflare, and <code>custom</code> for the account’s own asset types.

</summary>

One of the following:

"system"

<a href="#">Link to this property</a>

"cloudflare"

<a href="#">Link to this property</a>

"custom"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

schema: map\[unknown]

Fields and related attributes a custom finding type may reference for this asset class, as a JSON Schema. Top-level properties are <code>asset</code> and, when related resources exist, <code>associated</code>.

<a href="#">Link to this property</a>

id: optional string

Unique identifier. Present for <code>cloudflare</code> and <code>custom</code> asset types.

formatuuid

<a href="#">Link to this property</a>

content\_schema: optional map\[unknown]

JSON Schema subset describing the content of each asset of this type. The top level is an <code>object</code> with <code>properties</code> and an optional <code>required</code> list. Property names must be 1 to 32 letters, digits or underscores. A property may be nullable by listing <code>null</code> alongside its type.

<a href="#">Link to this property</a>

display\_name: optional string

Human-readable name. Present for <code>cloudflare</code> and <code>custom</code> asset types.

<a href="#">Link to this property</a>

version: optional number

Current version. Present for <code>cloudflare</code> and <code>custom</code> asset types.

formatint64

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.asset_schemas%20%3E%20(model)%20asset_schema_get_response%20%3E%20(schema)>)