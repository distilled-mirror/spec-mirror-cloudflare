---
title: Kick all participants
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Realtime Kit](https://developers.cloudflare.com/api/resources/realtime_kit)

[Active Session](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/active-session)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Kick all participants

POST/accounts/{account\_id}/realtime/kit/{app\_id}/meetings/{meeting\_id}/active-session/kick-all

Kicks all participants from an active session for the given meeting ID and ends the session. Participants in connected breakout rooms are kicked as well.

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

[Link to this property](#)%20realtime_kit.active-session%20%3E%20(method)%20kick_all_participants%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

app\_id: string

The app identifier tag.

[Link to this property](#)%20realtime_kit.active-session%20%3E%20(method)%20kick_all_participants%20%3E%20(params)%20default%20%3E%20(param)%20app_id%20%3E%20(schema)>)

meeting\_id: string

[Link to this property](#)%20realtime_kit.active-session%20%3E%20(method)%20kick_all_participants%20%3E%20(params)%20default%20%3E%20(param)%20meeting_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

data: optional object { action, kicked\_participants\_count }

</summary>

action: optional "kick-all"

<a href="#">Link to this property</a>

kicked\_participants\_count: optional number

Number of connections (peers) that were in the session when it was ended.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.active-session%20%3E%20(model)%20active_session_kick_all_participants_response%20%3E%20(schema)%20%3E%20(property)%20data>)

success: optional boolean

[Link to this property](#)%20realtime_kit.active-session%20%3E%20(model)%20active_session_kick_all_participants_response%20%3E%20(schema)%20%3E%20(property)%20success>)

### Kick all participants

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/realtime/kit/$APP_ID/meetings/$MEETING_ID/active-session/kick-all \
    -X POST \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

400 example

401 example

404 example

404 example

500 example

```
{
  "data": {
    "action": "kick-all",
    "kicked_participants_count": 3
  },
  "success": true
}
```

```
{
  "error": {
    "code": 400,
    "details": [
      {
        "code": "invalid_format",
        "field": "meeting_id",
        "location": "path",
        "message": "Invalid GUID"
      }
    ],
    "message": "Request validation failed"
  },
  "success": false
}
```

```
{
  "error": {
    "code": 401,
    "message": "app not found"
  },
  "success": false
}
```

```
{
  "error": {
    "code": 404,
    "message": "No active session found for meeting id: 6bf2b8be-04dd-4191-b602-1128921a306b"
  },
  "success": false
}
```

```
{
  "error": {
    "code": 404,
    "message": "Meeting 6bf2b8be-04dd-4191-b602-1128921a306b not found for organization 4f6c1a8e-2b39-4f6b-9c2d-7a1e5b3c9d10"
  },
  "success": false
}
```

```
{
  "error": {
    "code": 500,
    "message": "Internal Server Error"
  },
  "success": false
}
```

##### Returns Examples

200 example

400 example

401 example

404 example

404 example

500 example

```
{
  "data": {
    "action": "kick-all",
    "kicked_participants_count": 3
  },
  "success": true
}
```

```
{
  "error": {
    "code": 400,
    "details": [
      {
        "code": "invalid_format",
        "field": "meeting_id",
        "location": "path",
        "message": "Invalid GUID"
      }
    ],
    "message": "Request validation failed"
  },
  "success": false
}
```

```
{
  "error": {
    "code": 401,
    "message": "app not found"
  },
  "success": false
}
```

```
{
  "error": {
    "code": 404,
    "message": "No active session found for meeting id: 6bf2b8be-04dd-4191-b602-1128921a306b"
  },
  "success": false
}
```

```
{
  "error": {
    "code": 404,
    "message": "Meeting 6bf2b8be-04dd-4191-b602-1128921a306b not found for organization 4f6c1a8e-2b39-4f6b-9c2d-7a1e5b3c9d10"
  },
  "success": false
}
```

```
{
  "error": {
    "code": 500,
    "message": "Internal Server Error"
  },
  "success": false
}
```