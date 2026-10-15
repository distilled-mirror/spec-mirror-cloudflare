---
title: Delete a user population user
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Access](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access)

[User Populations](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/user_populations)

[Users](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/user_populations/subresources/users)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Delete a user population user

DELETE/accounts/{account\_id}/access/user\_populations/{user\_population\_id}/users/{user\_id}

Deletes a SCIM user from a user population.

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

account\_id: string

Identifier.

maxLength32

[Link to this property](#)%20zero_trust.access.user_populations.users%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

user\_population\_id: string

UUID.

maxLength36

[Link to this property](#)%20zero_trust.access.user_populations.users%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20user_population_id%20%3E%20(schema)>)

user\_id: string

The SCIM user identifier.

[Link to this property](#)%20zero_trust.access.user_populations.users%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20user_id%20%3E%20(schema)>)

### Delete a user population user

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/access/user_populations/$USER_POPULATION_ID/users/$USER_ID \
    -X DELETE \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

##### Returns Examples