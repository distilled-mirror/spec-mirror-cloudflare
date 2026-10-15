---
title: Delete a SCIM Group resource
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Identity Providers](https://developers.cloudflare.com/api/resources/zero_trust/subresources/identity_providers)

[SCIM](https://developers.cloudflare.com/api/resources/zero_trust/subresources/identity_providers/subresources/scim)

[Groups](https://developers.cloudflare.com/api/resources/zero_trust/subresources/identity_providers/subresources/scim/subresources/groups)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Delete a SCIM Group resource

DELETE/accounts/{account\_id}/access/identity\_providers/{identity\_provider\_id}/scim/groups/{group\_id}

Deletes a SCIM Group resource from the identity provider’s SCIM population.

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

`Access: Organizations, Identity Providers, and Groups Write`

##### P ath ParametersExpand Collapse

account\_id: string

Identifier.

maxLength32

[Link to this property](#)%20zero_trust.identity_providers.scim.groups%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

identity\_provider\_id: string

UUID.

maxLength36

[Link to this property](#)%20zero_trust.identity_providers.scim.groups%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20identity_provider_id%20%3E%20(schema)>)

group\_id: string

Identifier.

maxLength32

[Link to this property](#)%20zero_trust.identity_providers.scim.groups%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20group_id%20%3E%20(schema)>)

### Delete a SCIM Group resource

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/access/identity_providers/$IDENTITY_PROVIDER_ID/scim/groups/$GROUP_ID \
    -X DELETE \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

##### Returns Examples