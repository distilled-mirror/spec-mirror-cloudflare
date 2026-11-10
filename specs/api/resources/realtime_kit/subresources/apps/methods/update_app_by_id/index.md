---
title: Update an app
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Realtime Kit](https://developers.cloudflare.com/api/resources/realtime_kit)

[Apps](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/apps)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Update an app

PATCH/accounts/{account\_id}/realtime/kit/apps/{app\_id}

Update the name of an app in your account.

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

`Realtime Admin``Realtime`

##### P ath ParametersExpand Collapse

account\_id: string

The account identifier tag.

maxLength32

[Link to this property](#)%20realtime_kit.apps%20%3E%20(method)%20update_app_by_id%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

app\_id: string

formatuuid

[Link to this property](#)%20realtime_kit.apps%20%3E%20(method)%20update_app_by_id%20%3E%20(params)%20default%20%3E%20(param)%20app_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

name: string

The app name. Leading and trailing whitespace is removed, and the name must contain at least one non-whitespace character.

maxLength150

[Link to this property](#)%20realtime_kit.apps%20%3E%20(method)%20update_app_by_id%20%3E%20(params)%200%20%3E%20(param)%20name%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

data: object {id, created\_at, name }

</summary>

id: optional string

formatuuid

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

name: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.apps%20%3E%20(model)%20app_update_app_by_id_response%20%3E%20(schema)%20%3E%20(property)%20data>)

success: true

[Link to this property](#)%20realtime_kit.apps%20%3E%20(model)%20app_update_app_by_id_response%20%3E%20(schema)%20%3E%20(property)%20success>)

### Update an app

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/realtime/kit/apps/$APP_ID \
    -X PATCH \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "name": "name"
        }'
```

200 example

```
{
  "data": {
    "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
    "created_at": "2019-12-27T18:11:19.117Z",
    "name": "name"
  },
  "success": true
}
```

##### Returns Examples

200 example

```
{
  "data": {
    "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
    "created_at": "2019-12-27T18:11:19.117Z",
    "name": "name"
  },
  "success": true
}
```