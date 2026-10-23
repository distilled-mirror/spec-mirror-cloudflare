---
title: Read matches for logo queries by ID
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Brand Protection](https://developers.cloudflare.com/api/resources/brand_protection)

[Logo Matches](https://developers.cloudflare.com/api/resources/brand_protection/subresources/logo_matches)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Read matches for logo queries by ID

GET/accounts/{account\_id}/brand-protection/logo-matches

Return matches for logo queries based on ID.

##### Security

<details>

<summary>API Token</summary>



The preferred authorization scheme for interacting with the Cloudflare API. <a href="https://developers.cloudflare.com/fundamentals/api/get-started/create-token/">Create a token</a>.

**Example:**<code>Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY</code>

</details>

<details>

<summary>API Email + API Key</summary>



The previous authorization scheme for interacting with the Cloudflare API, used in conjunction with a Global API key.

**Example:**<code>X-Auth-Email: user@example.com</code>

The previous authorization scheme for interacting with the Cloudflare API. When possible, use API tokens instead of Global API keys.

**Example:**<code>X-Auth-Key: 144c9defac04969c7bfad8efaa8ea194</code>

</details>

##### Accepted Permissions (at least one required)

`Intel Write``Intel Read`

##### P ath ParametersExpand Collapse

account\_id: string

minLength1

[Link to this property](#)%20brand_protection.logo_matches%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

limit: optional string

[Link to this property](#)%20brand_protection.logo_matches%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20limit%20%3E%20(schema)>)

logo\_id: optional array of string

[Link to this property](#)%20brand_protection.logo_matches%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20logo_id%20%3E%20(schema)>)

offset: optional string

[Link to this property](#)%20brand_protection.logo_matches%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20offset%20%3E%20(schema)>)

##### ReturnsExpand Collapse

matches: optional array of map\[unknown]

[Link to this property](#)%20brand_protection.logo_matches%20%3E%20(model)%20logo_match_get_response%20%3E%20(schema)%20%3E%20(property)%20matches>)

total: optional number

[Link to this property](#)%20brand_protection.logo_matches%20%3E%20(model)%20logo_match_get_response%20%3E%20(schema)%20%3E%20(property)%20total>)

### Read matches for logo queries by ID

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/brand-protection/logo-matches \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "matches": [
    {
      "foo": {}
    }
  ],
  "total": 0
}
```

##### Returns Examples

200 example

```
{
  "matches": [
    {
      "foo": {}
    }
  ],
  "total": 0
}
```