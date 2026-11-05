---
title: List logo queries
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Brand Protection](https://developers.cloudflare.com/api/resources/brand_protection)

[V2](https://developers.cloudflare.com/api/resources/brand_protection/subresources/v2)

[Logos](https://developers.cloudflare.com/api/resources/brand_protection/subresources/v2/subresources/logos)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List logo queries

GET/accounts/{account\_id}/cloudforce-one/v2/brand-protection/logo/queries

Lists the account’s saved logo queries. Set `id` to return a single query object instead of an array. Set `download=true` to include each logo image as base64 data.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write``Cloudforce One Read`

##### P ath ParametersExpand Collapse

account\_id: string

minLength1

[Link to this property](#)%20brand_protection.v2.logos%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

id: optional string

ID of a logo query. When set, `result` is that single query object instead of an array.

[Link to this property](#)%20brand_protection.v2.logos%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20id%20%3E%20(schema)>)

download: optional string

Set to `true` to include each logo image as base64 data in `image_data`, with its MIME type in `content_type`.

[Link to this property](#)%20brand_protection.v2.logos%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20download%20%3E%20(schema)>)

##### ReturnsExpand Collapse

id: number

ID of the logo query.

[Link to this property](#)%20brand_protection.v2.logos%20%3E%20(model)%20logo_get_response%20%3E%20(schema)%20%3E%20(items)%20%3E%20(property)%20id>)

r2\_path: string

[Link to this property](#)%20brand_protection.v2.logos%20%3E%20(model)%20logo_get_response%20%3E%20(schema)%20%3E%20(items)%20%3E%20(property)%20r2_path>)

similarity\_threshold: number

Minimum similarity score (0-1) required for a visual match.

[Link to this property](#)%20brand_protection.v2.logos%20%3E%20(model)%20logo_get_response%20%3E%20(schema)%20%3E%20(items)%20%3E%20(property)%20similarity_threshold>)

tag: string

Name of the logo query.

[Link to this property](#)%20brand_protection.v2.logos%20%3E%20(model)%20logo_get_response%20%3E%20(schema)%20%3E%20(items)%20%3E%20(property)%20tag>)

uploaded\_at: string

When the logo was uploaded.

[Link to this property](#)%20brand_protection.v2.logos%20%3E%20(model)%20logo_get_response%20%3E%20(schema)%20%3E%20(items)%20%3E%20(property)%20uploaded_at>)

content\_type: optional string

MIME type of the image (only present when download=true)

[Link to this property](#)%20brand_protection.v2.logos%20%3E%20(model)%20logo_get_response%20%3E%20(schema)%20%3E%20(items)%20%3E%20(property)%20content_type>)

image\_data: optional string

Base64-encoded image data (only present when download=true)

[Link to this property](#)%20brand_protection.v2.logos%20%3E%20(model)%20logo_get_response%20%3E%20(schema)%20%3E%20(items)%20%3E%20(property)%20image_data>)

### List logo queries

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/v2/brand-protection/logo/queries \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
[
  {
    "id": 0,
    "r2_path": "r2_path",
    "similarity_threshold": 0,
    "tag": "tag",
    "uploaded_at": "uploaded_at",
    "content_type": "content_type",
    "image_data": "image_data"
  }
]
```

##### Returns Examples

200 example

```
[
  {
    "id": 0,
    "r2_path": "r2_path",
    "similarity_threshold": 0,
    "tag": "tag",
    "uploaded_at": "uploaded_at",
    "content_type": "content_type",
    "image_data": "image_data"
  }
]
```