---
title: Delete logo query
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

# Delete logo query

DELETE/accounts/{account\_id}/cloudforce-one/v2/brand-protection/logo/queries/{query\_id}

Permanently deletes a saved logo query and all of its matches. If the query does not exist in this account, the request fails with error code 404.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Cloudforce One Write`

##### P ath ParametersExpand Collapse

account\_id: string

minLength1

[Link to this property](#)%20brand_protection.v2.logos%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

query\_id: string

ID of the logo query.

minLength1

[Link to this property](#)%20brand_protection.v2.logos%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20query_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

message: string

[Link to this property](#)%20brand_protection.v2.logos%20%3E%20(model)%20logo_delete_response%20%3E%20(schema)%20%3E%20(property)%20message>)

success: boolean

[Link to this property](#)%20brand_protection.v2.logos%20%3E%20(model)%20logo_delete_response%20%3E%20(schema)%20%3E%20(property)%20success>)

### Delete logo query

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cloudforce-one/v2/brand-protection/logo/queries/$QUERY_ID \
    -X DELETE \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "message": "message",
  "success": true
}
```

##### Returns Examples

200 example

```
{
  "message": "message",
  "success": true
}
```