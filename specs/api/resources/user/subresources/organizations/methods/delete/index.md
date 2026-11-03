---
title: Leave Organization
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[User](https://developers.cloudflare.com/api/resources/user)

[Organizations](https://developers.cloudflare.com/api/resources/user/subresources/organizations)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Leave Organization

Deprecated

DELETE/user/organizations/{organization\_id}

Removes association to an organization.

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

##### P ath ParametersExpand Collapse

organization\_id: string

Identifier

maxLength32

minLength32

[Link to this property](#)%20user.organizations%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20organization_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

id: optional string

Identifier

maxLength32

minLength32

[Link to this property](#)%20user.organizations%20%3E%20(model)%20organization_delete_response%20%3E%20(schema)%20%3E%20(property)%20id>)

### Leave Organization

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/user/organizations/$ORGANIZATION_ID \
    -X DELETE \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "id": "023e105f4ecef8ad9ca31a8372d0c353"
}
```

##### Returns Examples

200 example

```
{
  "id": "023e105f4ecef8ad9ca31a8372d0c353"
}
```