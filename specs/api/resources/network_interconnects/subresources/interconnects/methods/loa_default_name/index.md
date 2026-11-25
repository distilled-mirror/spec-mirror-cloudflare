---
agent:
  instructions: "This site offers a search API that returns relevant content across the entire site. Use the search endpoint to find information instead of crawling individual pages."
  search: "https://developers.cloudflare.com/.well-known/search?q={query}"
title: Get the default customer name for LOA generation
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Network Interconnects](https://developers.cloudflare.com/api/resources/network_interconnects)

[Interconnects](https://developers.cloudflare.com/api/resources/network_interconnects/subresources/interconnects)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Get the default customer name for LOA generation

GET/accounts/{account\_id}/cni/interconnects/{icon}/loa/default

Retrieves the default customer name that will be used in the LOA if no name is provided to the `/accounts/{account_id}/cni/interconnects/{icon}/loa` endpoint.

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

`Magic WAN Write``Magic WAN Read``Magic Transit Read``Magic Transit Write`

##### P ath ParametersExpand Collapse

account\_id: string

Customer account tag

[Link to this property](#)%20network_interconnects.interconnects%20%3E%20(method)%20loa_default_name%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

icon: string

[Link to this property](#)%20network_interconnects.interconnects%20%3E%20(method)%20loa_default_name%20%3E%20(params)%20default%20%3E%20(param)%20icon%20%3E%20(schema)>)

##### ReturnsExpand Collapse

name: string

The default customer name for the interconnect

[Link to this property](#)%20network_interconnects.interconnects%20%3E%20(model)%20interconnect_loa_default_name_response%20%3E%20(schema)%20%3E%20(property)%20name>)

### Get the default customer name for LOA generation

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cni/interconnects/$ICON/loa/default \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "name": "name"
}
```

##### Returns Examples

200 example

```
{
  "name": "name"
}
```