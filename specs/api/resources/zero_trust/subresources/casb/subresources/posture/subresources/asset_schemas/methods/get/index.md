---
title: Get asset schema by asset class
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Casb](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb)

[Posture](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture)

[Asset Schemas](https://developers.cloudflare.com/api/resources/zero_trust/subresources/casb/subresources/posture/subresources/asset_schemas)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Get asset schema by asset class

GET/accounts/{account\_id}/data-security/posture/asset\_schemas/{asset\_class}

Returns the fields and related attributes a custom finding type may reference for the given asset class (JSON Schema). Used by the custom finding types builder.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Zero Trust Read``Zero Trust Write`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20zero_trust.casb.posture.asset_schemas%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

asset\_class: string

[Link to this property](#)%20zero_trust.casb.posture.asset_schemas%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20asset_class%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {code, message, documentation\_url, source }

</summary>

code: number

Error or message code.

minimum1000

<a href="#">Link to this property</a>

message: string

Human-readable message.

<a href="#">Link to this property</a>

documentation\_url: optional string

Link to relevant documentation.

formaturi

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: optional string

JSON pointer to the source of the error.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.asset_schemas%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {code, message, documentation\_url, source }

</summary>

code: number

Error or message code.

minimum1000

<a href="#">Link to this property</a>

message: string

Human-readable message.

<a href="#">Link to this property</a>

documentation\_url: optional string

Link to relevant documentation.

formaturi

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: optional string

JSON pointer to the source of the error.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.casb.posture.asset_schemas%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: boolean

Whether the API call was successful.

[Link to this property](#)%20zero_trust.casb.posture.asset_schemas%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional object {asset\_class, origin, schema, 4 more }

</summary>

asset\_class: string

Asset class identifier (PascalCase), e.g. AnthropicApiKey.

<a href="#">Link to this property</a>

<details>

<summary>

origin: "system"or "cloudflare"or "custom"

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

[Link to this property](#)%20zero_trust.casb.posture.asset_schemas%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

### Get asset schema by asset class

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/data-security/posture/asset_schemas/$ASSET_CLASS \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "errors": [
    {
      "code": 1000,
      "message": "Request processed successfully",
      "documentation_url": "https://developers.cloudflare.com/api/operations/list-findings",
      "source": {
        "pointer": "/data/attributes/name"
      }
    }
  ],
  "messages": [
    {
      "code": 1000,
      "message": "Request processed successfully",
      "documentation_url": "https://developers.cloudflare.com/api/operations/list-findings",
      "source": {
        "pointer": "/data/attributes/name"
      }
    }
  ],
  "success": true,
  "result": {
    "asset_class": "AnthropicApiKey",
    "origin": "system",
    "schema": {
      "type": "bar",
      "properties": "bar",
      "$schema": "bar",
      "required": "bar",
      "title": "bar"
    },
    "id": "3f1c2d6e-8b4a-4f7e-9c1d-2a5b6c7d8e9f",
    "content_schema": {
      "properties": "bar",
      "required": "bar",
      "type": "bar"
    },
    "display_name": "Custom file",
    "version": 3
  }
}
```

##### Returns Examples

200 example

```
{
  "errors": [
    {
      "code": 1000,
      "message": "Request processed successfully",
      "documentation_url": "https://developers.cloudflare.com/api/operations/list-findings",
      "source": {
        "pointer": "/data/attributes/name"
      }
    }
  ],
  "messages": [
    {
      "code": 1000,
      "message": "Request processed successfully",
      "documentation_url": "https://developers.cloudflare.com/api/operations/list-findings",
      "source": {
        "pointer": "/data/attributes/name"
      }
    }
  ],
  "success": true,
  "result": {
    "asset_class": "AnthropicApiKey",
    "origin": "system",
    "schema": {
      "type": "bar",
      "properties": "bar",
      "$schema": "bar",
      "required": "bar",
      "title": "bar"
    },
    "id": "3f1c2d6e-8b4a-4f7e-9c1d-2a5b6c7d8e9f",
    "content_schema": {
      "properties": "bar",
      "required": "bar",
      "type": "bar"
    },
    "display_name": "Custom file",
    "version": 3
  }
}
```