---
title: Fetch livestream session details using livestream session ID
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Realtime Kit](https://developers.cloudflare.com/api/resources/realtime_kit)

[Livestreams](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/livestreams)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Fetch livestream session details using livestream session ID

GET/accounts/{account\_id}/realtime/kit/{app\_id}/livestreams/sessions/{livestream-session-id}

Returns livestream session details for the given livestream session ID. Retrieve the `livestream_session_id`using the `Fetch livestream session details using a session ID` API.

##### Security

API Token

The preferred authorization scheme for interacting with the Cloudflare API. [Create a token](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/).

**Example:**`Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY`

##### Accepted Permissions (at least one required)

`Realtime Admin``Realtime`

##### P ath ParametersExpand Collapse

account\_id: string

The account identifier tag.

maxLength32

[Link to this property](#)%20realtime_kit.livestreams%20%3E%20(method)%20get_livestream_session_details_for_session_id%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

app\_id: string

The app identifier tag.

[Link to this property](#)%20realtime_kit.livestreams%20%3E%20(method)%20get_livestream_session_details_for_session_id%20%3E%20(params)%20default%20%3E%20(param)%20app_id%20%3E%20(schema)>)

"livestream-session-id": string

[Link to this property](#)%20realtime_kit.livestreams%20%3E%20(method)%20get_livestream_session_details_for_session_id%20%3E%20(params)%20default%20%3E%20(param)%20livestream-session-id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

data: object {id, created\_at, err\_message, 7 more }

</summary>

id: string

ID of the livestream session.

formatuuid

<a href="#">Link to this property</a>

created\_at: string

Timestamp the livestream session was created at, in ISO format.

formatdate-time

<a href="#">Link to this property</a>

err\_message: string

Error message, if the livestream session failed.

<a href="#">Link to this property</a>

ingest\_seconds: number

The time duration for which the input was given or the meeting was streamed.

<a href="#">Link to this property</a>

invoked\_time: string

Timestamp the livestream session was invoked at, in ISO format.

formatdate-time

<a href="#">Link to this property</a>

livestream\_id: string

ID of the livestream.

formatuuid

<a href="#">Link to this property</a>

started\_time: string

Timestamp the livestream session started at, in ISO format.

formatdate-time

<a href="#">Link to this property</a>

stopped\_time: string

Timestamp the livestream session stopped at, in ISO format.

formatdate-time

<a href="#">Link to this property</a>

updated\_at: string

Timestamp the livestream session was last updated at, in ISO format.

formatdate-time

<a href="#">Link to this property</a>

viewer\_seconds: number

The total view time for which the viewers watched the stream.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.livestreams%20%3E%20(model)%20livestream_get_livestream_session_details_for_session_id_response%20%3E%20(schema)%20%3E%20(property)%20data>)

success: boolean

[Link to this property](#)%20realtime_kit.livestreams%20%3E%20(model)%20livestream_get_livestream_session_details_for_session_id_response%20%3E%20(schema)%20%3E%20(property)%20success>)

### Fetch livestream session details using livestream session ID

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/realtime/kit/$APP_ID/livestreams/sessions/$LIVESTREAM_SESSION_ID \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "data": {
    "created_at": "2023-07-15T07:08:40.742Z",
    "err_message": null,
    "id": "cf55a850-c3fd-46b5-b5d2-25b3b9aa1686",
    "ingest_seconds": 600,
    "invoked_time": "2023-07-15T07:08:26.634Z",
    "livestream_id": "b60ef3da-fbbb-441b-9168-8235b0035248",
    "started_time": "2023-07-15T07:08:39Z",
    "stopped_time": "2023-07-15T07:18:39Z",
    "updated_at": "2023-07-15T07:18:40.742Z",
    "viewer_seconds": 1200
  },
  "success": true
}
```

##### Returns Examples

200 example

```
{
  "data": {
    "created_at": "2023-07-15T07:08:40.742Z",
    "err_message": null,
    "id": "cf55a850-c3fd-46b5-b5d2-25b3b9aa1686",
    "ingest_seconds": 600,
    "invoked_time": "2023-07-15T07:08:26.634Z",
    "livestream_id": "b60ef3da-fbbb-441b-9168-8235b0035248",
    "started_time": "2023-07-15T07:08:39Z",
    "stopped_time": "2023-07-15T07:18:39Z",
    "updated_at": "2023-07-15T07:18:40.742Z",
    "viewer_seconds": 1200
  },
  "success": true
}
```