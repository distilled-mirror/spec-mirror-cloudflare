---
title: Create new saved string queries
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Brand Protection](https://developers.cloudflare.com/api/resources/brand_protection)

[Queries](https://developers.cloudflare.com/api/resources/brand_protection/subresources/queries)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Create new saved string queries

POST/accounts/{account\_id}/brand-protection/queries

Return a success message after creating new saved string queries.

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

`Intel Write`

##### P ath ParametersExpand Collapse

account\_id: string

minLength1

[Link to this property](#)%20brand_protection.queries%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

id: optional string

[Link to this property](#)%20brand_protection.queries%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20id%20%3E%20(schema)>)

scan: optional boolean

[Link to this property](#)%20brand_protection.queries%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20scan%20%3E%20(schema)>)

tag: optional string

[Link to this property](#)%20brand_protection.queries%20%3E%20(method)%20create%20%3E%20(params)%20default%20%3E%20(param)%20tag%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

max\_time: optional string

formatdate-time

[Link to this property](#)%20brand_protection.queries%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20max_time%20%3E%20(schema)>)

min\_time: optional string

formatdate-time

[Link to this property](#)%20brand_protection.queries%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20min_time%20%3E%20(schema)>)

scan: optional boolean

[Link to this property](#)%20brand_protection.queries%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20scan%20%3E%20(schema)>)

<details>

<summary>

string\_matches: optional array of object {pattern, max\_edit\_distance }

</summary>

pattern: string

<a href="#">Link to this property</a>

max\_edit\_distance: optional number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20brand_protection.queries%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20string_matches%20%3E%20(schema)>)

tag: optional string

[Link to this property](#)%20brand_protection.queries%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20tag%20%3E%20(schema)>)

### Create new saved string queries

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/brand-protection/queries \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{}'
```

##### Returns Examples