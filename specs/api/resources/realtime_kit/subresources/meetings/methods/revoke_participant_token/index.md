---
title: Revoke participant's authentication token
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Realtime Kit](https://developers.cloudflare.com/api/resources/realtime_kit)

[Meetings](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/meetings)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Revoke participant's authentication token

DELETE/accounts/{account\_id}/realtime/kit/{app\_id}/meetings/{meeting\_id}/participants/{participant\_id}/token

Revokes a previously issued participant authentication token without deleting the participant. Other tokens issued to the participant remain valid.

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

[Link to this property](#)%20realtime_kit.meetings%20%3E%20(method)%20revoke_participant_token%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

app\_id: string

The app identifier tag.

[Link to this property](#)%20realtime_kit.meetings%20%3E%20(method)%20revoke_participant_token%20%3E%20(params)%20default%20%3E%20(param)%20app_id%20%3E%20(schema)>)

meeting\_id: string

formatuuid

[Link to this property](#)%20realtime_kit.meetings%20%3E%20(method)%20revoke_participant_token%20%3E%20(params)%20default%20%3E%20(param)%20meeting_id%20%3E%20(schema)>)

participant\_id: string

[Link to this property](#)%20realtime_kit.meetings%20%3E%20(method)%20revoke_participant_token%20%3E%20(params)%20default%20%3E%20(param)%20participant_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

data: object {token }

Data returned by the operation

</summary>

token: string

The revoked participant authentication token.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.meetings%20%3E%20(model)%20meeting_revoke_participant_token_response%20%3E%20(schema)%20%3E%20(property)%20data>)

success: boolean

Success status of the operation

[Link to this property](#)%20realtime_kit.meetings%20%3E%20(model)%20meeting_revoke_participant_token_response%20%3E%20(schema)%20%3E%20(property)%20success>)

### Revoke participant's authentication token

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/realtime/kit/$APP_ID/meetings/$MEETING_ID/participants/$PARTICIPANT_ID/token \
    -X DELETE \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "data": {
    "token": "token"
  },
  "success": true
}
```

##### Returns Examples

200 example

```
{
  "data": {
    "token": "token"
  },
  "success": true
}
```