---
title: Get a key's value
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[KV](https://developers.cloudflare.com/api/resources/kv)

[Namespaces](https://developers.cloudflare.com/api/resources/kv/subresources/namespaces)

[Values](https://developers.cloudflare.com/api/resources/kv/subresources/namespaces/subresources/values)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Get a key's value

GET/accounts/{account\_id}/storage/kv/namespaces/{namespace\_id}/values/{key\_name}

Returns the value stored under the specified key in the Workers KV namespace as raw bytes. Use URL-encoding for special characters (for example, `:`, `!`, `%`) in the key name when constructing the request URL. If the key-value pair expires, the `expiration` response header contains its expiration time in seconds since the UNIX epoch.

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

`Workers KV Storage Write``Workers KV Storage Read`

##### P ath ParametersExpand Collapse

account\_id: string

ID of the Cloudflare account that owns the Workers KV namespaces.

maxLength32

[Link to this property](#)%20kv.namespaces.values%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

namespace\_id: string

ID of the Workers KV namespace.

maxLength32

[Link to this property](#)%20kv.namespaces.values%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20namespace_id%20%3E%20(schema)>)

key\_name: string

A key’s name. The name may be at most 512 bytes. All printable, non-whitespace characters are valid. Use percent-encoding to define key names as part of a URL.

maxLength512

[Link to this property](#)%20kv.namespaces.values%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20key_name%20%3E%20(schema)>)

### Get a key's value

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/storage/kv/namespaces/$NAMESPACE_ID/values/$KEY_NAME \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

##### Returns Examples