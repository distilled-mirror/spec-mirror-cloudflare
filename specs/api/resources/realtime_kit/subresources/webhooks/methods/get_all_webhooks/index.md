---
title: Fetch all supported webhook events
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Realtime Kit](https://developers.cloudflare.com/api/resources/realtime_kit)

[Webhooks](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/webhooks)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Fetch all supported webhook events

GET/accounts/{account\_id}/realtime/kit/{app\_id}/webhooks/all

Returns the list of webhook event names supported by RealtimeKit.

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

[Link to this property](#)%20realtime_kit.webhooks%20%3E%20(method)%20get_all_webhooks%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

app\_id: string

The app identifier tag.

[Link to this property](#)%20realtime_kit.webhooks%20%3E%20(method)%20get_all_webhooks%20%3E%20(params)%20default%20%3E%20(param)%20app_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

data: array of "meeting.started"or "meeting.ended"or "meeting.participantJoined"or 6 more

</summary>

One of the following:

"meeting.started"

<a href="#">Link to this property</a>

"meeting.ended"

<a href="#">Link to this property</a>

"meeting.participantJoined"

<a href="#">Link to this property</a>

"meeting.participantLeft"

<a href="#">Link to this property</a>

"meeting.chatSynced"

<a href="#">Link to this property</a>

"recording.statusUpdate"

<a href="#">Link to this property</a>

"livestreaming.statusUpdate"

<a href="#">Link to this property</a>

"meeting.transcript"

<a href="#">Link to this property</a>

"meeting.summary"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.webhooks%20%3E%20(model)%20webhook_get_all_webhooks_response%20%3E%20(schema)%20%3E%20(property)%20data>)

success: boolean

[Link to this property](#)%20realtime_kit.webhooks%20%3E%20(model)%20webhook_get_all_webhooks_response%20%3E%20(schema)%20%3E%20(property)%20success>)

### Fetch all supported webhook events

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/realtime/kit/$APP_ID/webhooks/all \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "data": [
    "meeting.started"
  ],
  "success": true
}
```

##### Returns Examples

200 example

```
{
  "data": [
    "meeting.started"
  ],
  "success": true
}
```