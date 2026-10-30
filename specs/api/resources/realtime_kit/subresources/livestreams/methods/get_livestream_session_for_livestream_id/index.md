---
title: Fetch livestream details using livestream ID
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Realtime Kit](https://developers.cloudflare.com/api/resources/realtime_kit)

[Livestreams](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/livestreams)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Fetch livestream details using livestream ID

GET/accounts/{account\_id}/realtime/kit/{app\_id}/livestreams/{livestream\_id}

Returns details of a livestream with sessions for the given livestream ID. Retreive the livestream ID using the `Start livestreaming a meeting` API.

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

[Link to this property](#)%20realtime_kit.livestreams%20%3E%20(method)%20get_livestream_session_for_livestream_id%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

app\_id: string

The app identifier tag.

[Link to this property](#)%20realtime_kit.livestreams%20%3E%20(method)%20get_livestream_session_for_livestream_id%20%3E%20(params)%20default%20%3E%20(param)%20app_id%20%3E%20(schema)>)

livestream\_id: string

[Link to this property](#)%20realtime_kit.livestreams%20%3E%20(method)%20get_livestream_session_for_livestream_id%20%3E%20(params)%20default%20%3E%20(param)%20livestream_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

page\_no: optional number

The page number from which you want your page search results to be displayed.

[Link to this property](#)%20realtime_kit.livestreams%20%3E%20(method)%20get_livestream_session_for_livestream_id%20%3E%20(params)%20default%20%3E%20(param)%20page_no%20%3E%20(schema)>)

per\_page: optional number

Number of results per page.

[Link to this property](#)%20realtime_kit.livestreams%20%3E%20(method)%20get_livestream_session_for_livestream_id%20%3E%20(params)%20default%20%3E%20(param)%20per_page%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

data: object {livestream, sessions }

</summary>

<details>

<summary>

livestream: object {id, created\_at, disabled, 9 more }

</summary>

id: string

ID of the livestream.

formatuuid

<a href="#">Link to this property</a>

created\_at: string

Timestamp the livestream was created at, in ISO format.

formatdate-time

<a href="#">Link to this property</a>

disabled: boolean

Specifies if the livestream is disabled.

<a href="#">Link to this property</a>

external\_id: string

ID of the underlying Cloudflare Stream live input.

<a href="#">Link to this property</a>

ingest\_server: string

The server URL to which the RTMP encoder sends the video and audio data.

<a href="#">Link to this property</a>

manual\_ingest: boolean

Specifies if the livestream is ingested manually by an RTMP encoder.

<a href="#">Link to this property</a>

meeting\_id: string

ID of the meeting being livestreamed, if any.

<a href="#">Link to this property</a>

name: string

Name of the livestream.

<a href="#">Link to this property</a>

playback\_url: string

The web address that viewers can use to watch the livestream.

<a href="#">Link to this property</a>

<details>

<summary>

status: "LIVE"or "IDLE"or "ERRORED"or 2 more

Status of the livestream.

</summary>

One of the following:

"LIVE"

<a href="#">Link to this property</a>

"IDLE"

<a href="#">Link to this property</a>

"ERRORED"

<a href="#">Link to this property</a>

"INVOKED"

<a href="#">Link to this property</a>

"METRICS\_READY"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

stream\_key: string

Unique key for accessing each livestream. Empty if the livestream is disabled.

<a href="#">Link to this property</a>

updated\_at: string

Timestamp the livestream was last updated at, in ISO format.

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

sessions: array of object {id, created\_at, err\_message, 7 more }

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

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.livestreams%20%3E%20(model)%20livestream_get_livestream_session_for_livestream_id_response%20%3E%20(schema)%20%3E%20(property)%20data>)

<details>

<summary>

paging: object {end\_offset, start\_offset, total\_count }

</summary>

end\_offset: number

<a href="#">Link to this property</a>

start\_offset: number

<a href="#">Link to this property</a>

total\_count: number

minimum0

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.livestreams%20%3E%20(model)%20livestream_get_livestream_session_for_livestream_id_response%20%3E%20(schema)%20%3E%20(property)%20paging>)

success: boolean

[Link to this property](#)%20realtime_kit.livestreams%20%3E%20(model)%20livestream_get_livestream_session_for_livestream_id_response%20%3E%20(schema)%20%3E%20(property)%20success>)

### Fetch livestream details using livestream ID

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/realtime/kit/$APP_ID/livestreams/$LIVESTREAM_ID \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "data": {
    "livestream": {
      "created_at": "2023-07-15T07:08:26.634Z",
      "disabled": false,
      "external_id": "7de6a3fec0f9c05bf1df140950d3a237",
      "id": "b60ef3da-fbbb-441b-9168-8235b0035248",
      "ingest_server": "rtmps://live.cloudflare.com:443/live/",
      "manual_ingest": false,
      "meeting_id": "bbb87945-df1c-49d9-8159-262a7ae6cfde",
      "name": "test",
      "playback_url": "https://customer-s8oj0c1n5ek8ah1e.cloudflarestream.com/7de6a3fec0f9c05bf1df140950d3a237/manifest/video.m3u8",
      "status": "LIVE",
      "stream_key": "f26566285faca6fbe2e79a73a66rsrrsrrsr3cde23a2bb7dbc6c2c1761b98f4e4",
      "updated_at": "2023-07-15T07:08:40.726Z"
    },
    "sessions": [
      {
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
      }
    ]
  },
  "paging": {
    "end_offset": 1,
    "start_offset": 1,
    "total_count": 1
  },
  "success": true
}
```

##### Returns Examples

200 example

```
{
  "data": {
    "livestream": {
      "created_at": "2023-07-15T07:08:26.634Z",
      "disabled": false,
      "external_id": "7de6a3fec0f9c05bf1df140950d3a237",
      "id": "b60ef3da-fbbb-441b-9168-8235b0035248",
      "ingest_server": "rtmps://live.cloudflare.com:443/live/",
      "manual_ingest": false,
      "meeting_id": "bbb87945-df1c-49d9-8159-262a7ae6cfde",
      "name": "test",
      "playback_url": "https://customer-s8oj0c1n5ek8ah1e.cloudflarestream.com/7de6a3fec0f9c05bf1df140950d3a237/manifest/video.m3u8",
      "status": "LIVE",
      "stream_key": "f26566285faca6fbe2e79a73a66rsrrsrrsr3cde23a2bb7dbc6c2c1761b98f4e4",
      "updated_at": "2023-07-15T07:08:40.726Z"
    },
    "sessions": [
      {
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
      }
    ]
  },
  "paging": {
    "end_offset": 1,
    "start_offset": 1,
    "total_count": 1
  },
  "success": true
}
```