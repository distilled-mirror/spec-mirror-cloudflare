---
title: Realtime Kit
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Realtime Kit

#### Realtime KitApps

##### [Fetch all apps](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/apps/methods/get)

GET/accounts/{account\_id}/realtime/kit/apps

##### [Create App](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/apps/methods/post)

POST/accounts/{account\_id}/realtime/kit/apps

##### ModelsExpand Collapse

<details>

<summary>

AppGetResponse object {data, paging, success }

</summary>

<details>

<summary>

data: optional array of object {id, created\_at, name }

</summary>

id: optional string

formatuuid

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

name: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

paging: optional object {end\_offset, start\_offset, total\_count }

</summary>

end\_offset: optional number

<a href="#">Link to this property</a>

start\_offset: optional number

<a href="#">Link to this property</a>

total\_count: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

success: optional boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.apps%20%3E%20(model)%20app_get_response%20%3E%20(schema)>)

<details>

<summary>

AppPostResponse object {data, success }

</summary>

<details>

<summary>

data: optional object {app }

</summary>

<details>

<summary>

app: optional object {id, created\_at, name }

</summary>

id: optional string

formatuuid

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

name: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

success: optional boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.apps%20%3E%20(model)%20app_post_response%20%3E%20(schema)>)

#### Realtime KitMeetings

##### [Fetch all meetings for an App](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/meetings/methods/get)

GET/accounts/{account\_id}/realtime/kit/{app\_id}/meetings

##### [Create a meeting](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/meetings/methods/create)

POST/accounts/{account\_id}/realtime/kit/{app\_id}/meetings

##### [Fetch a meeting for an App](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/meetings/methods/get_meeting_by_id)

GET/accounts/{account\_id}/realtime/kit/{app\_id}/meetings/{meeting\_id}

##### [Update a meeting](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/meetings/methods/update_meeting_by_id)

PATCH/accounts/{account\_id}/realtime/kit/{app\_id}/meetings/{meeting\_id}

##### [Replace a meeting](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/meetings/methods/replace_meeting_by_id)

PUT/accounts/{account\_id}/realtime/kit/{app\_id}/meetings/{meeting\_id}

##### [Fetch all participants of a meeting](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/meetings/methods/get_meeting_participants)

GET/accounts/{account\_id}/realtime/kit/{app\_id}/meetings/{meeting\_id}/participants

##### [Add a participant](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/meetings/methods/add_participant)

POST/accounts/{account\_id}/realtime/kit/{app\_id}/meetings/{meeting\_id}/participants

##### [Fetch a participant's detail](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/meetings/methods/get_meeting_participant)

GET/accounts/{account\_id}/realtime/kit/{app\_id}/meetings/{meeting\_id}/participants/{participant\_id}

##### [Edit a participant's detail](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/meetings/methods/edit_participant)

PATCH/accounts/{account\_id}/realtime/kit/{app\_id}/meetings/{meeting\_id}/participants/{participant\_id}

##### [Delete a participant](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/meetings/methods/delete_meeting_participant)

DELETE/accounts/{account\_id}/realtime/kit/{app\_id}/meetings/{meeting\_id}/participants/{participant\_id}

##### [Refresh participant's authentication token](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/meetings/methods/refresh_participant_token)

POST/accounts/{account\_id}/realtime/kit/{app\_id}/meetings/{meeting\_id}/participants/{participant\_id}/token

##### ModelsExpand Collapse

<details>

<summary>

MeetingGetResponse object {data, paging, success }

</summary>

<details>

<summary>

data: array of object {id, created\_at, updated\_at, 9 more }

</summary>

id: string

ID of the meeting.

formatuuid

<a href="#">Link to this property</a>

created\_at: string

Timestamp the object was created at. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

updated\_at: string

Timestamp the object was updated at. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

live\_stream\_on\_start: optional boolean

Specifies if the meeting should start getting livestreamed on start.

<a href="#">Link to this property</a>

persist\_chat: optional boolean

Specifies if Chat within a meeting should persist for a week.

<a href="#">Link to this property</a>

record\_on\_start: optional boolean

Specifies if the meeting should start getting recorded as soon as someone joins the meeting.

<a href="#">Link to this property</a>

<details>

<summary>

recording\_config: optional object {audio\_config, file\_name\_prefix, live\_streaming\_config, 4 more }

Recording Configurations to be used for this meeting. This level of configs takes higher preference over App level configs on the RealtimeKit developer portal.

</summary>

<details>

<summary>

audio\_config: optional object {channel, codec, export\_file }

Object containing configuration regarding the audio that is being recorded.

</summary>

<details>

<summary>

channel: optional "mono"or "stereo"

Audio signal pathway within an audio file that carries a specific sound source.

</summary>

One of the following:

"mono"

<a href="#">Link to this property</a>

"stereo"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

codec: optional "MP3"or "AAC"

Codec using which the recording will be encoded. If VP8/VP9 is selected for videoConfig, changing audioConfig is not allowed. In this case, the codec in the audioConfig is automatically set to vorbis.

</summary>

One of the following:

"MP3"

<a href="#">Link to this property</a>

"AAC"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

export\_file: optional boolean

Controls whether to export audio file seperately

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

file\_name\_prefix: optional string

Adds a prefix to the beginning of the file name of the recording.

<a href="#">Link to this property</a>

<details>

<summary>

live\_streaming\_config: optional object {rtmp\_url }

</summary>

rtmp\_url: optional string

RTMP URL to stream to

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

max\_seconds: optional number

Specifies the maximum duration for recording in seconds, ranging from a minimum of 60 seconds to a maximum of 24 hours.

maximum86400

minimum60

<a href="#">Link to this property</a>

<details>

<summary>

realtimekit\_bucket\_config: optional object {enabled }

</summary>

enabled: boolean

Controls whether recordings are uploaded to RealtimeKit’s bucket. If set to false, <code>download_url</code>, <code>audio_download_url</code>, <code>download_url_expiry</code> won’t be generated for a recording.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

storage\_config: optional object {access\_key, auth\_method, bucket, 9 more } or object {access\_key, region, auth\_method, 9 more } or object {private\_key, access\_key, auth\_method, 9 more } or object {password, access\_key, auth\_method, 9 more }

</summary>

One of the following:

<details>

<summary>

object {access\_key, auth\_method, bucket, 9 more }

</summary>

access\_key: optional string

Access key of the storage medium. Access key is not required for the <code>gcs</code> storage media type.

Note that this field is not readable by clients, only writeable.

<a href="#">Link to this property</a>

<details>

<summary>

auth\_method: optional "KEY"or "PASSWORD"

Authentication method used for “sftp” type storage medium

</summary>

One of the following:

"KEY"

<a href="#">Link to this property</a>

"PASSWORD"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

password: optional string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

private\_key: optional string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

region: optional string

Region of the storage medium.

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

type: optional "gcs"

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object {access\_key, region, auth\_method, 9 more }

</summary>

access\_key: unknown

minLength1

<a href="#">Link to this property</a>

region: unknown

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

auth\_method: optional "KEY"or "PASSWORD"

Authentication method used for “sftp” type storage medium

</summary>

One of the following:

"KEY"

<a href="#">Link to this property</a>

"PASSWORD"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

password: optional string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

private\_key: optional string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "aws"or "azure"or "digitalocean"

</summary>

One of the following:

"aws"

<a href="#">Link to this property</a>

"azure"

<a href="#">Link to this property</a>

"digitalocean"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object {private\_key, access\_key, auth\_method, 9 more }

</summary>

private\_key: string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

access\_key: optional string

Access key of the storage medium. Access key is not required for the <code>gcs</code> storage media type.

Note that this field is not readable by clients, only writeable.

<a href="#">Link to this property</a>

auth\_method: optional "KEY"

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

password: optional string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

region: optional string

Region of the storage medium.

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "aws"or "azure"or "digitalocean"or 2 more

Type of storage media.

</summary>

One of the following:

"aws"

<a href="#">Link to this property</a>

"azure"

<a href="#">Link to this property</a>

"digitalocean"

<a href="#">Link to this property</a>

"gcs"

<a href="#">Link to this property</a>

"sftp"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object {password, access\_key, auth\_method, 9 more }

</summary>

password: string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

access\_key: optional string

Access key of the storage medium. Access key is not required for the <code>gcs</code> storage media type.

Note that this field is not readable by clients, only writeable.

<a href="#">Link to this property</a>

auth\_method: optional "PASSWORD"

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

private\_key: optional string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

region: optional string

Region of the storage medium.

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "aws"or "azure"or "digitalocean"or 2 more

Type of storage media.

</summary>

One of the following:

"aws"

<a href="#">Link to this property</a>

"azure"

<a href="#">Link to this property</a>

"digitalocean"

<a href="#">Link to this property</a>

"gcs"

<a href="#">Link to this property</a>

"sftp"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video\_config: optional object {codec, export\_file, height, 2 more }

</summary>

<details>

<summary>

codec: optional "H264"or "VP8"or "VP9"

Codec using which the recording will be encoded.

</summary>

One of the following:

"H264"

<a href="#">Link to this property</a>

"VP8"

<a href="#">Link to this property</a>

"VP9"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

export\_file: optional boolean

Controls whether to export video file seperately

<a href="#">Link to this property</a>

height: optional number

Height of the recording video in pixels

maximum1920

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

watermark: optional object {position, size, url }

Watermark to be added to the recording

</summary>

<details>

<summary>

position: optional "left top"or "right top"or "left bottom"or "right bottom"

Position of the watermark

</summary>

One of the following:

"left top"

<a href="#">Link to this property</a>

"right top"

<a href="#">Link to this property</a>

"left bottom"

<a href="#">Link to this property</a>

"right bottom"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

size: optional object {height, width }

Size of the watermark

</summary>

height: optional number

Height of the watermark in px

minimum1

<a href="#">Link to this property</a>

width: optional number

Width of the watermark in px

minimum1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

url: optional string

URL of the watermark image

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

width: optional number

Width of the recording video in pixels

maximum1920

minimum1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

session\_keep\_alive\_time\_in\_secs: optional number

Time in seconds, for which a session remains active, after the last participant has left the meeting.

maximum600

minimum60

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "ACTIVE"or "INACTIVE"

Whether the meeting is <code>ACTIVE</code> or <code>INACTIVE</code>. Users will not be able to join an <code>INACTIVE</code> meeting.

</summary>

One of the following:

"ACTIVE"

<a href="#">Link to this property</a>

"INACTIVE"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

summarize\_on\_end: optional boolean

Automatically generate summary of meetings using transcripts. Requires Transcriptions to be enabled, and can be retrieved via Webhooks or summary API.

<a href="#">Link to this property</a>

title: optional string

Title of the meeting.

<a href="#">Link to this property</a>

transcribe\_on\_end: optional boolean

Automatically generate transcripts when the meeting ends.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

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

<a href="#">Link to this property</a>

success: boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.meetings%20%3E%20(model)%20meeting_get_response%20%3E%20(schema)>)

<details>

<summary>

MeetingCreateResponse object {success, data }

</summary>

success: boolean

Success status of the operation

<a href="#">Link to this property</a>

<details>

<summary>

data: optional object {id, created\_at, updated\_at, 10 more }

Data returned by the operation

</summary>

id: string

ID of the meeting.

formatuuid

<a href="#">Link to this property</a>

created\_at: string

Timestamp the object was created at. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

updated\_at: string

Timestamp the object was updated at. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

ai\_config: optional object {summarization, transcription }

The AI Config allows you to customize the behavior of meeting transcriptions and summaries

</summary>

<details>

<summary>

summarization: optional object {summary\_type, text\_format, word\_limit }

Summary Config

</summary>

<details>

<summary>

summary\_type: optional "general"or "team\_meeting"or "sales\_call"or 6 more

Defines the style of the summary, such as general, team meeting, or sales call.

</summary>

One of the following:

"general"

<a href="#">Link to this property</a>

"team\_meeting"

<a href="#">Link to this property</a>

"sales\_call"

<a href="#">Link to this property</a>

"client\_check\_in"

<a href="#">Link to this property</a>

"interview"

<a href="#">Link to this property</a>

"daily\_standup"

<a href="#">Link to this property</a>

"one\_on\_one\_meeting"

<a href="#">Link to this property</a>

"lecture"

<a href="#">Link to this property</a>

"code\_review"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

text\_format: optional "plain\_text"or "markdown"

Determines the text format of the summary, such as plain text or markdown.

</summary>

One of the following:

"plain\_text"

<a href="#">Link to this property</a>

"markdown"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

word\_limit: optional number

Sets the maximum number of words in the meeting summary.

maximum1000

minimum150

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

transcription: optional object {keywords, language, profanity\_filter }

Transcription Configurations

</summary>

keywords: optional array of string

Adds specific terms to improve accurate detection during transcription.

<a href="#">Link to this property</a>

<details>

<summary>

language: optional "en-US"or "en-IN"or "de"or 7 more

Specifies the language code for transcription to ensure accurate results.

</summary>

One of the following:

"en-US"

<a href="#">Link to this property</a>

"en-IN"

<a href="#">Link to this property</a>

"de"

<a href="#">Link to this property</a>

"hi"

<a href="#">Link to this property</a>

"sv"

<a href="#">Link to this property</a>

"ru"

<a href="#">Link to this property</a>

"pl"

<a href="#">Link to this property</a>

"el"

<a href="#">Link to this property</a>

"fr"

<a href="#">Link to this property</a>

"nl"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

profanity\_filter: optional boolean

Control the inclusion of offensive language in transcriptions.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

live\_stream\_on\_start: optional boolean

Specifies if the meeting should start getting livestreamed on start.

<a href="#">Link to this property</a>

persist\_chat: optional boolean

Specifies if Chat within a meeting should persist for a week.

<a href="#">Link to this property</a>

record\_on\_start: optional boolean

Specifies if the meeting should start getting recorded as soon as someone joins the meeting.

<a href="#">Link to this property</a>

<details>

<summary>

recording\_config: optional object {audio\_config, file\_name\_prefix, live\_streaming\_config, 4 more }

Recording Configurations to be used for this meeting. This level of configs takes higher preference over App level configs on the RealtimeKit developer portal.

</summary>

<details>

<summary>

audio\_config: optional object {channel, codec, export\_file }

Object containing configuration regarding the audio that is being recorded.

</summary>

<details>

<summary>

channel: optional "mono"or "stereo"

Audio signal pathway within an audio file that carries a specific sound source.

</summary>

One of the following:

"mono"

<a href="#">Link to this property</a>

"stereo"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

codec: optional "MP3"or "AAC"

Codec using which the recording will be encoded. If VP8/VP9 is selected for videoConfig, changing audioConfig is not allowed. In this case, the codec in the audioConfig is automatically set to vorbis.

</summary>

One of the following:

"MP3"

<a href="#">Link to this property</a>

"AAC"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

export\_file: optional boolean

Controls whether to export audio file seperately

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

file\_name\_prefix: optional string

Adds a prefix to the beginning of the file name of the recording.

<a href="#">Link to this property</a>

<details>

<summary>

live\_streaming\_config: optional object {rtmp\_url }

</summary>

rtmp\_url: optional string

RTMP URL to stream to

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

max\_seconds: optional number

Specifies the maximum duration for recording in seconds, ranging from a minimum of 60 seconds to a maximum of 24 hours.

maximum86400

minimum60

<a href="#">Link to this property</a>

<details>

<summary>

realtimekit\_bucket\_config: optional object {enabled }

</summary>

enabled: boolean

Controls whether recordings are uploaded to RealtimeKit’s bucket. If set to false, <code>download_url</code>, <code>audio_download_url</code>, <code>download_url_expiry</code> won’t be generated for a recording.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

storage\_config: optional object {access\_key, auth\_method, bucket, 9 more } or object {access\_key, region, auth\_method, 9 more } or object {private\_key, access\_key, auth\_method, 9 more } or object {password, access\_key, auth\_method, 9 more }

</summary>

One of the following:

<details>

<summary>

object {access\_key, auth\_method, bucket, 9 more }

</summary>

access\_key: optional string

Access key of the storage medium. Access key is not required for the <code>gcs</code> storage media type.

Note that this field is not readable by clients, only writeable.

<a href="#">Link to this property</a>

<details>

<summary>

auth\_method: optional "KEY"or "PASSWORD"

Authentication method used for “sftp” type storage medium

</summary>

One of the following:

"KEY"

<a href="#">Link to this property</a>

"PASSWORD"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

password: optional string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

private\_key: optional string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

region: optional string

Region of the storage medium.

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

type: optional "gcs"

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object {access\_key, region, auth\_method, 9 more }

</summary>

access\_key: unknown

minLength1

<a href="#">Link to this property</a>

region: unknown

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

auth\_method: optional "KEY"or "PASSWORD"

Authentication method used for “sftp” type storage medium

</summary>

One of the following:

"KEY"

<a href="#">Link to this property</a>

"PASSWORD"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

password: optional string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

private\_key: optional string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "aws"or "azure"or "digitalocean"

</summary>

One of the following:

"aws"

<a href="#">Link to this property</a>

"azure"

<a href="#">Link to this property</a>

"digitalocean"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object {private\_key, access\_key, auth\_method, 9 more }

</summary>

private\_key: string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

access\_key: optional string

Access key of the storage medium. Access key is not required for the <code>gcs</code> storage media type.

Note that this field is not readable by clients, only writeable.

<a href="#">Link to this property</a>

auth\_method: optional "KEY"

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

password: optional string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

region: optional string

Region of the storage medium.

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "aws"or "azure"or "digitalocean"or 2 more

Type of storage media.

</summary>

One of the following:

"aws"

<a href="#">Link to this property</a>

"azure"

<a href="#">Link to this property</a>

"digitalocean"

<a href="#">Link to this property</a>

"gcs"

<a href="#">Link to this property</a>

"sftp"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object {password, access\_key, auth\_method, 9 more }

</summary>

password: string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

access\_key: optional string

Access key of the storage medium. Access key is not required for the <code>gcs</code> storage media type.

Note that this field is not readable by clients, only writeable.

<a href="#">Link to this property</a>

auth\_method: optional "PASSWORD"

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

private\_key: optional string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

region: optional string

Region of the storage medium.

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "aws"or "azure"or "digitalocean"or 2 more

Type of storage media.

</summary>

One of the following:

"aws"

<a href="#">Link to this property</a>

"azure"

<a href="#">Link to this property</a>

"digitalocean"

<a href="#">Link to this property</a>

"gcs"

<a href="#">Link to this property</a>

"sftp"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video\_config: optional object {codec, export\_file, height, 2 more }

</summary>

<details>

<summary>

codec: optional "H264"or "VP8"or "VP9"

Codec using which the recording will be encoded.

</summary>

One of the following:

"H264"

<a href="#">Link to this property</a>

"VP8"

<a href="#">Link to this property</a>

"VP9"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

export\_file: optional boolean

Controls whether to export video file seperately

<a href="#">Link to this property</a>

height: optional number

Height of the recording video in pixels

maximum1920

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

watermark: optional object {position, size, url }

Watermark to be added to the recording

</summary>

<details>

<summary>

position: optional "left top"or "right top"or "left bottom"or "right bottom"

Position of the watermark

</summary>

One of the following:

"left top"

<a href="#">Link to this property</a>

"right top"

<a href="#">Link to this property</a>

"left bottom"

<a href="#">Link to this property</a>

"right bottom"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

size: optional object {height, width }

Size of the watermark

</summary>

height: optional number

Height of the watermark in px

minimum1

<a href="#">Link to this property</a>

width: optional number

Width of the watermark in px

minimum1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

url: optional string

URL of the watermark image

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

width: optional number

Width of the recording video in pixels

maximum1920

minimum1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

session\_keep\_alive\_time\_in\_secs: optional number

Time in seconds, for which a session remains active, after the last participant has left the meeting.

maximum600

minimum60

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "ACTIVE"or "INACTIVE"

Whether the meeting is <code>ACTIVE</code> or <code>INACTIVE</code>. Users will not be able to join an <code>INACTIVE</code> meeting.

</summary>

One of the following:

"ACTIVE"

<a href="#">Link to this property</a>

"INACTIVE"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

summarize\_on\_end: optional boolean

Automatically generate summary of meetings using transcripts. Requires Transcriptions to be enabled, and can be retrieved via Webhooks or summary API.

<a href="#">Link to this property</a>

title: optional string

Title of the meeting.

<a href="#">Link to this property</a>

transcribe\_on\_end: optional boolean

Automatically generate transcripts when the meeting ends.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.meetings%20%3E%20(model)%20meeting_create_response%20%3E%20(schema)>)

<details>

<summary>

MeetingGetMeetingByIDResponse object {success, data }

</summary>

success: boolean

Success status of the operation

<a href="#">Link to this property</a>

<details>

<summary>

data: optional object {id, created\_at, updated\_at, 10 more }

Data returned by the operation

</summary>

id: string

ID of the meeting.

formatuuid

<a href="#">Link to this property</a>

created\_at: string

Timestamp the object was created at. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

updated\_at: string

Timestamp the object was updated at. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

ai\_config: optional object {summarization, transcription }

The AI Config allows you to customize the behavior of meeting transcriptions and summaries

</summary>

<details>

<summary>

summarization: optional object {summary\_type, text\_format, word\_limit }

Summary Config

</summary>

<details>

<summary>

summary\_type: optional "general"or "team\_meeting"or "sales\_call"or 6 more

Defines the style of the summary, such as general, team meeting, or sales call.

</summary>

One of the following:

"general"

<a href="#">Link to this property</a>

"team\_meeting"

<a href="#">Link to this property</a>

"sales\_call"

<a href="#">Link to this property</a>

"client\_check\_in"

<a href="#">Link to this property</a>

"interview"

<a href="#">Link to this property</a>

"daily\_standup"

<a href="#">Link to this property</a>

"one\_on\_one\_meeting"

<a href="#">Link to this property</a>

"lecture"

<a href="#">Link to this property</a>

"code\_review"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

text\_format: optional "plain\_text"or "markdown"

Determines the text format of the summary, such as plain text or markdown.

</summary>

One of the following:

"plain\_text"

<a href="#">Link to this property</a>

"markdown"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

word\_limit: optional number

Sets the maximum number of words in the meeting summary.

maximum1000

minimum150

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

transcription: optional object {keywords, language, profanity\_filter }

Transcription Configurations

</summary>

keywords: optional array of string

Adds specific terms to improve accurate detection during transcription.

<a href="#">Link to this property</a>

<details>

<summary>

language: optional "en-US"or "en-IN"or "de"or 7 more

Specifies the language code for transcription to ensure accurate results.

</summary>

One of the following:

"en-US"

<a href="#">Link to this property</a>

"en-IN"

<a href="#">Link to this property</a>

"de"

<a href="#">Link to this property</a>

"hi"

<a href="#">Link to this property</a>

"sv"

<a href="#">Link to this property</a>

"ru"

<a href="#">Link to this property</a>

"pl"

<a href="#">Link to this property</a>

"el"

<a href="#">Link to this property</a>

"fr"

<a href="#">Link to this property</a>

"nl"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

profanity\_filter: optional boolean

Control the inclusion of offensive language in transcriptions.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

live\_stream\_on\_start: optional boolean

Specifies if the meeting should start getting livestreamed on start.

<a href="#">Link to this property</a>

persist\_chat: optional boolean

Specifies if Chat within a meeting should persist for a week.

<a href="#">Link to this property</a>

record\_on\_start: optional boolean

Specifies if the meeting should start getting recorded as soon as someone joins the meeting.

<a href="#">Link to this property</a>

<details>

<summary>

recording\_config: optional object {audio\_config, file\_name\_prefix, live\_streaming\_config, 4 more }

Recording Configurations to be used for this meeting. This level of configs takes higher preference over App level configs on the RealtimeKit developer portal.

</summary>

<details>

<summary>

audio\_config: optional object {channel, codec, export\_file }

Object containing configuration regarding the audio that is being recorded.

</summary>

<details>

<summary>

channel: optional "mono"or "stereo"

Audio signal pathway within an audio file that carries a specific sound source.

</summary>

One of the following:

"mono"

<a href="#">Link to this property</a>

"stereo"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

codec: optional "MP3"or "AAC"

Codec using which the recording will be encoded. If VP8/VP9 is selected for videoConfig, changing audioConfig is not allowed. In this case, the codec in the audioConfig is automatically set to vorbis.

</summary>

One of the following:

"MP3"

<a href="#">Link to this property</a>

"AAC"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

export\_file: optional boolean

Controls whether to export audio file seperately

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

file\_name\_prefix: optional string

Adds a prefix to the beginning of the file name of the recording.

<a href="#">Link to this property</a>

<details>

<summary>

live\_streaming\_config: optional object {rtmp\_url }

</summary>

rtmp\_url: optional string

RTMP URL to stream to

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

max\_seconds: optional number

Specifies the maximum duration for recording in seconds, ranging from a minimum of 60 seconds to a maximum of 24 hours.

maximum86400

minimum60

<a href="#">Link to this property</a>

<details>

<summary>

realtimekit\_bucket\_config: optional object {enabled }

</summary>

enabled: boolean

Controls whether recordings are uploaded to RealtimeKit’s bucket. If set to false, <code>download_url</code>, <code>audio_download_url</code>, <code>download_url_expiry</code> won’t be generated for a recording.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

storage\_config: optional object {access\_key, auth\_method, bucket, 9 more } or object {access\_key, region, auth\_method, 9 more } or object {private\_key, access\_key, auth\_method, 9 more } or object {password, access\_key, auth\_method, 9 more }

</summary>

One of the following:

<details>

<summary>

object {access\_key, auth\_method, bucket, 9 more }

</summary>

access\_key: optional string

Access key of the storage medium. Access key is not required for the <code>gcs</code> storage media type.

Note that this field is not readable by clients, only writeable.

<a href="#">Link to this property</a>

<details>

<summary>

auth\_method: optional "KEY"or "PASSWORD"

Authentication method used for “sftp” type storage medium

</summary>

One of the following:

"KEY"

<a href="#">Link to this property</a>

"PASSWORD"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

password: optional string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

private\_key: optional string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

region: optional string

Region of the storage medium.

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

type: optional "gcs"

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object {access\_key, region, auth\_method, 9 more }

</summary>

access\_key: unknown

minLength1

<a href="#">Link to this property</a>

region: unknown

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

auth\_method: optional "KEY"or "PASSWORD"

Authentication method used for “sftp” type storage medium

</summary>

One of the following:

"KEY"

<a href="#">Link to this property</a>

"PASSWORD"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

password: optional string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

private\_key: optional string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "aws"or "azure"or "digitalocean"

</summary>

One of the following:

"aws"

<a href="#">Link to this property</a>

"azure"

<a href="#">Link to this property</a>

"digitalocean"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object {private\_key, access\_key, auth\_method, 9 more }

</summary>

private\_key: string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

access\_key: optional string

Access key of the storage medium. Access key is not required for the <code>gcs</code> storage media type.

Note that this field is not readable by clients, only writeable.

<a href="#">Link to this property</a>

auth\_method: optional "KEY"

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

password: optional string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

region: optional string

Region of the storage medium.

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "aws"or "azure"or "digitalocean"or 2 more

Type of storage media.

</summary>

One of the following:

"aws"

<a href="#">Link to this property</a>

"azure"

<a href="#">Link to this property</a>

"digitalocean"

<a href="#">Link to this property</a>

"gcs"

<a href="#">Link to this property</a>

"sftp"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object {password, access\_key, auth\_method, 9 more }

</summary>

password: string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

access\_key: optional string

Access key of the storage medium. Access key is not required for the <code>gcs</code> storage media type.

Note that this field is not readable by clients, only writeable.

<a href="#">Link to this property</a>

auth\_method: optional "PASSWORD"

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

private\_key: optional string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

region: optional string

Region of the storage medium.

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "aws"or "azure"or "digitalocean"or 2 more

Type of storage media.

</summary>

One of the following:

"aws"

<a href="#">Link to this property</a>

"azure"

<a href="#">Link to this property</a>

"digitalocean"

<a href="#">Link to this property</a>

"gcs"

<a href="#">Link to this property</a>

"sftp"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video\_config: optional object {codec, export\_file, height, 2 more }

</summary>

<details>

<summary>

codec: optional "H264"or "VP8"or "VP9"

Codec using which the recording will be encoded.

</summary>

One of the following:

"H264"

<a href="#">Link to this property</a>

"VP8"

<a href="#">Link to this property</a>

"VP9"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

export\_file: optional boolean

Controls whether to export video file seperately

<a href="#">Link to this property</a>

height: optional number

Height of the recording video in pixels

maximum1920

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

watermark: optional object {position, size, url }

Watermark to be added to the recording

</summary>

<details>

<summary>

position: optional "left top"or "right top"or "left bottom"or "right bottom"

Position of the watermark

</summary>

One of the following:

"left top"

<a href="#">Link to this property</a>

"right top"

<a href="#">Link to this property</a>

"left bottom"

<a href="#">Link to this property</a>

"right bottom"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

size: optional object {height, width }

Size of the watermark

</summary>

height: optional number

Height of the watermark in px

minimum1

<a href="#">Link to this property</a>

width: optional number

Width of the watermark in px

minimum1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

url: optional string

URL of the watermark image

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

width: optional number

Width of the recording video in pixels

maximum1920

minimum1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

session\_keep\_alive\_time\_in\_secs: optional number

Time in seconds, for which a session remains active, after the last participant has left the meeting.

maximum600

minimum60

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "ACTIVE"or "INACTIVE"

Whether the meeting is <code>ACTIVE</code> or <code>INACTIVE</code>. Users will not be able to join an <code>INACTIVE</code> meeting.

</summary>

One of the following:

"ACTIVE"

<a href="#">Link to this property</a>

"INACTIVE"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

summarize\_on\_end: optional boolean

Automatically generate summary of meetings using transcripts. Requires Transcriptions to be enabled, and can be retrieved via Webhooks or summary API.

<a href="#">Link to this property</a>

title: optional string

Title of the meeting.

<a href="#">Link to this property</a>

transcribe\_on\_end: optional boolean

Automatically generate transcripts when the meeting ends.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.meetings%20%3E%20(model)%20meeting_get_meeting_by_id_response%20%3E%20(schema)>)

<details>

<summary>

MeetingUpdateMeetingByIDResponse object {success, data }

</summary>

success: boolean

Success status of the operation

<a href="#">Link to this property</a>

<details>

<summary>

data: optional object {id, created\_at, updated\_at, 10 more }

Data returned by the operation

</summary>

id: string

ID of the meeting.

formatuuid

<a href="#">Link to this property</a>

created\_at: string

Timestamp the object was created at. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

updated\_at: string

Timestamp the object was updated at. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

ai\_config: optional object {summarization, transcription }

The AI Config allows you to customize the behavior of meeting transcriptions and summaries

</summary>

<details>

<summary>

summarization: optional object {summary\_type, text\_format, word\_limit }

Summary Config

</summary>

<details>

<summary>

summary\_type: optional "general"or "team\_meeting"or "sales\_call"or 6 more

Defines the style of the summary, such as general, team meeting, or sales call.

</summary>

One of the following:

"general"

<a href="#">Link to this property</a>

"team\_meeting"

<a href="#">Link to this property</a>

"sales\_call"

<a href="#">Link to this property</a>

"client\_check\_in"

<a href="#">Link to this property</a>

"interview"

<a href="#">Link to this property</a>

"daily\_standup"

<a href="#">Link to this property</a>

"one\_on\_one\_meeting"

<a href="#">Link to this property</a>

"lecture"

<a href="#">Link to this property</a>

"code\_review"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

text\_format: optional "plain\_text"or "markdown"

Determines the text format of the summary, such as plain text or markdown.

</summary>

One of the following:

"plain\_text"

<a href="#">Link to this property</a>

"markdown"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

word\_limit: optional number

Sets the maximum number of words in the meeting summary.

maximum1000

minimum150

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

transcription: optional object {keywords, language, profanity\_filter }

Transcription Configurations

</summary>

keywords: optional array of string

Adds specific terms to improve accurate detection during transcription.

<a href="#">Link to this property</a>

<details>

<summary>

language: optional "en-US"or "en-IN"or "de"or 7 more

Specifies the language code for transcription to ensure accurate results.

</summary>

One of the following:

"en-US"

<a href="#">Link to this property</a>

"en-IN"

<a href="#">Link to this property</a>

"de"

<a href="#">Link to this property</a>

"hi"

<a href="#">Link to this property</a>

"sv"

<a href="#">Link to this property</a>

"ru"

<a href="#">Link to this property</a>

"pl"

<a href="#">Link to this property</a>

"el"

<a href="#">Link to this property</a>

"fr"

<a href="#">Link to this property</a>

"nl"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

profanity\_filter: optional boolean

Control the inclusion of offensive language in transcriptions.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

live\_stream\_on\_start: optional boolean

Specifies if the meeting should start getting livestreamed on start.

<a href="#">Link to this property</a>

persist\_chat: optional boolean

Specifies if Chat within a meeting should persist for a week.

<a href="#">Link to this property</a>

record\_on\_start: optional boolean

Specifies if the meeting should start getting recorded as soon as someone joins the meeting.

<a href="#">Link to this property</a>

<details>

<summary>

recording\_config: optional object {audio\_config, file\_name\_prefix, live\_streaming\_config, 4 more }

Recording Configurations to be used for this meeting. This level of configs takes higher preference over App level configs on the RealtimeKit developer portal.

</summary>

<details>

<summary>

audio\_config: optional object {channel, codec, export\_file }

Object containing configuration regarding the audio that is being recorded.

</summary>

<details>

<summary>

channel: optional "mono"or "stereo"

Audio signal pathway within an audio file that carries a specific sound source.

</summary>

One of the following:

"mono"

<a href="#">Link to this property</a>

"stereo"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

codec: optional "MP3"or "AAC"

Codec using which the recording will be encoded. If VP8/VP9 is selected for videoConfig, changing audioConfig is not allowed. In this case, the codec in the audioConfig is automatically set to vorbis.

</summary>

One of the following:

"MP3"

<a href="#">Link to this property</a>

"AAC"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

export\_file: optional boolean

Controls whether to export audio file seperately

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

file\_name\_prefix: optional string

Adds a prefix to the beginning of the file name of the recording.

<a href="#">Link to this property</a>

<details>

<summary>

live\_streaming\_config: optional object {rtmp\_url }

</summary>

rtmp\_url: optional string

RTMP URL to stream to

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

max\_seconds: optional number

Specifies the maximum duration for recording in seconds, ranging from a minimum of 60 seconds to a maximum of 24 hours.

maximum86400

minimum60

<a href="#">Link to this property</a>

<details>

<summary>

realtimekit\_bucket\_config: optional object {enabled }

</summary>

enabled: boolean

Controls whether recordings are uploaded to RealtimeKit’s bucket. If set to false, <code>download_url</code>, <code>audio_download_url</code>, <code>download_url_expiry</code> won’t be generated for a recording.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

storage\_config: optional object {access\_key, auth\_method, bucket, 9 more } or object {access\_key, region, auth\_method, 9 more } or object {private\_key, access\_key, auth\_method, 9 more } or object {password, access\_key, auth\_method, 9 more }

</summary>

One of the following:

<details>

<summary>

object {access\_key, auth\_method, bucket, 9 more }

</summary>

access\_key: optional string

Access key of the storage medium. Access key is not required for the <code>gcs</code> storage media type.

Note that this field is not readable by clients, only writeable.

<a href="#">Link to this property</a>

<details>

<summary>

auth\_method: optional "KEY"or "PASSWORD"

Authentication method used for “sftp” type storage medium

</summary>

One of the following:

"KEY"

<a href="#">Link to this property</a>

"PASSWORD"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

password: optional string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

private\_key: optional string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

region: optional string

Region of the storage medium.

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

type: optional "gcs"

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object {access\_key, region, auth\_method, 9 more }

</summary>

access\_key: unknown

minLength1

<a href="#">Link to this property</a>

region: unknown

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

auth\_method: optional "KEY"or "PASSWORD"

Authentication method used for “sftp” type storage medium

</summary>

One of the following:

"KEY"

<a href="#">Link to this property</a>

"PASSWORD"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

password: optional string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

private\_key: optional string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "aws"or "azure"or "digitalocean"

</summary>

One of the following:

"aws"

<a href="#">Link to this property</a>

"azure"

<a href="#">Link to this property</a>

"digitalocean"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object {private\_key, access\_key, auth\_method, 9 more }

</summary>

private\_key: string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

access\_key: optional string

Access key of the storage medium. Access key is not required for the <code>gcs</code> storage media type.

Note that this field is not readable by clients, only writeable.

<a href="#">Link to this property</a>

auth\_method: optional "KEY"

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

password: optional string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

region: optional string

Region of the storage medium.

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "aws"or "azure"or "digitalocean"or 2 more

Type of storage media.

</summary>

One of the following:

"aws"

<a href="#">Link to this property</a>

"azure"

<a href="#">Link to this property</a>

"digitalocean"

<a href="#">Link to this property</a>

"gcs"

<a href="#">Link to this property</a>

"sftp"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object {password, access\_key, auth\_method, 9 more }

</summary>

password: string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

access\_key: optional string

Access key of the storage medium. Access key is not required for the <code>gcs</code> storage media type.

Note that this field is not readable by clients, only writeable.

<a href="#">Link to this property</a>

auth\_method: optional "PASSWORD"

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

private\_key: optional string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

region: optional string

Region of the storage medium.

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "aws"or "azure"or "digitalocean"or 2 more

Type of storage media.

</summary>

One of the following:

"aws"

<a href="#">Link to this property</a>

"azure"

<a href="#">Link to this property</a>

"digitalocean"

<a href="#">Link to this property</a>

"gcs"

<a href="#">Link to this property</a>

"sftp"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video\_config: optional object {codec, export\_file, height, 2 more }

</summary>

<details>

<summary>

codec: optional "H264"or "VP8"or "VP9"

Codec using which the recording will be encoded.

</summary>

One of the following:

"H264"

<a href="#">Link to this property</a>

"VP8"

<a href="#">Link to this property</a>

"VP9"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

export\_file: optional boolean

Controls whether to export video file seperately

<a href="#">Link to this property</a>

height: optional number

Height of the recording video in pixels

maximum1920

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

watermark: optional object {position, size, url }

Watermark to be added to the recording

</summary>

<details>

<summary>

position: optional "left top"or "right top"or "left bottom"or "right bottom"

Position of the watermark

</summary>

One of the following:

"left top"

<a href="#">Link to this property</a>

"right top"

<a href="#">Link to this property</a>

"left bottom"

<a href="#">Link to this property</a>

"right bottom"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

size: optional object {height, width }

Size of the watermark

</summary>

height: optional number

Height of the watermark in px

minimum1

<a href="#">Link to this property</a>

width: optional number

Width of the watermark in px

minimum1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

url: optional string

URL of the watermark image

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

width: optional number

Width of the recording video in pixels

maximum1920

minimum1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

session\_keep\_alive\_time\_in\_secs: optional number

Time in seconds, for which a session remains active, after the last participant has left the meeting.

maximum600

minimum60

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "ACTIVE"or "INACTIVE"

Whether the meeting is <code>ACTIVE</code> or <code>INACTIVE</code>. Users will not be able to join an <code>INACTIVE</code> meeting.

</summary>

One of the following:

"ACTIVE"

<a href="#">Link to this property</a>

"INACTIVE"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

summarize\_on\_end: optional boolean

Automatically generate summary of meetings using transcripts. Requires Transcriptions to be enabled, and can be retrieved via Webhooks or summary API.

<a href="#">Link to this property</a>

title: optional string

Title of the meeting.

<a href="#">Link to this property</a>

transcribe\_on\_end: optional boolean

Automatically generate transcripts when the meeting ends.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.meetings%20%3E%20(model)%20meeting_update_meeting_by_id_response%20%3E%20(schema)>)

<details>

<summary>

MeetingReplaceMeetingByIDResponse object {success, data }

</summary>

success: boolean

Success status of the operation

<a href="#">Link to this property</a>

<details>

<summary>

data: optional object {id, created\_at, updated\_at, 10 more }

Data returned by the operation

</summary>

id: string

ID of the meeting.

formatuuid

<a href="#">Link to this property</a>

created\_at: string

Timestamp the object was created at. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

updated\_at: string

Timestamp the object was updated at. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

ai\_config: optional object {summarization, transcription }

The AI Config allows you to customize the behavior of meeting transcriptions and summaries

</summary>

<details>

<summary>

summarization: optional object {summary\_type, text\_format, word\_limit }

Summary Config

</summary>

<details>

<summary>

summary\_type: optional "general"or "team\_meeting"or "sales\_call"or 6 more

Defines the style of the summary, such as general, team meeting, or sales call.

</summary>

One of the following:

"general"

<a href="#">Link to this property</a>

"team\_meeting"

<a href="#">Link to this property</a>

"sales\_call"

<a href="#">Link to this property</a>

"client\_check\_in"

<a href="#">Link to this property</a>

"interview"

<a href="#">Link to this property</a>

"daily\_standup"

<a href="#">Link to this property</a>

"one\_on\_one\_meeting"

<a href="#">Link to this property</a>

"lecture"

<a href="#">Link to this property</a>

"code\_review"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

text\_format: optional "plain\_text"or "markdown"

Determines the text format of the summary, such as plain text or markdown.

</summary>

One of the following:

"plain\_text"

<a href="#">Link to this property</a>

"markdown"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

word\_limit: optional number

Sets the maximum number of words in the meeting summary.

maximum1000

minimum150

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

transcription: optional object {keywords, language, profanity\_filter }

Transcription Configurations

</summary>

keywords: optional array of string

Adds specific terms to improve accurate detection during transcription.

<a href="#">Link to this property</a>

<details>

<summary>

language: optional "en-US"or "en-IN"or "de"or 7 more

Specifies the language code for transcription to ensure accurate results.

</summary>

One of the following:

"en-US"

<a href="#">Link to this property</a>

"en-IN"

<a href="#">Link to this property</a>

"de"

<a href="#">Link to this property</a>

"hi"

<a href="#">Link to this property</a>

"sv"

<a href="#">Link to this property</a>

"ru"

<a href="#">Link to this property</a>

"pl"

<a href="#">Link to this property</a>

"el"

<a href="#">Link to this property</a>

"fr"

<a href="#">Link to this property</a>

"nl"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

profanity\_filter: optional boolean

Control the inclusion of offensive language in transcriptions.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

live\_stream\_on\_start: optional boolean

Specifies if the meeting should start getting livestreamed on start.

<a href="#">Link to this property</a>

persist\_chat: optional boolean

Specifies if Chat within a meeting should persist for a week.

<a href="#">Link to this property</a>

record\_on\_start: optional boolean

Specifies if the meeting should start getting recorded as soon as someone joins the meeting.

<a href="#">Link to this property</a>

<details>

<summary>

recording\_config: optional object {audio\_config, file\_name\_prefix, live\_streaming\_config, 4 more }

Recording Configurations to be used for this meeting. This level of configs takes higher preference over App level configs on the RealtimeKit developer portal.

</summary>

<details>

<summary>

audio\_config: optional object {channel, codec, export\_file }

Object containing configuration regarding the audio that is being recorded.

</summary>

<details>

<summary>

channel: optional "mono"or "stereo"

Audio signal pathway within an audio file that carries a specific sound source.

</summary>

One of the following:

"mono"

<a href="#">Link to this property</a>

"stereo"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

codec: optional "MP3"or "AAC"

Codec using which the recording will be encoded. If VP8/VP9 is selected for videoConfig, changing audioConfig is not allowed. In this case, the codec in the audioConfig is automatically set to vorbis.

</summary>

One of the following:

"MP3"

<a href="#">Link to this property</a>

"AAC"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

export\_file: optional boolean

Controls whether to export audio file seperately

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

file\_name\_prefix: optional string

Adds a prefix to the beginning of the file name of the recording.

<a href="#">Link to this property</a>

<details>

<summary>

live\_streaming\_config: optional object {rtmp\_url }

</summary>

rtmp\_url: optional string

RTMP URL to stream to

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

max\_seconds: optional number

Specifies the maximum duration for recording in seconds, ranging from a minimum of 60 seconds to a maximum of 24 hours.

maximum86400

minimum60

<a href="#">Link to this property</a>

<details>

<summary>

realtimekit\_bucket\_config: optional object {enabled }

</summary>

enabled: boolean

Controls whether recordings are uploaded to RealtimeKit’s bucket. If set to false, <code>download_url</code>, <code>audio_download_url</code>, <code>download_url_expiry</code> won’t be generated for a recording.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

storage\_config: optional object {access\_key, auth\_method, bucket, 9 more } or object {access\_key, region, auth\_method, 9 more } or object {private\_key, access\_key, auth\_method, 9 more } or object {password, access\_key, auth\_method, 9 more }

</summary>

One of the following:

<details>

<summary>

object {access\_key, auth\_method, bucket, 9 more }

</summary>

access\_key: optional string

Access key of the storage medium. Access key is not required for the <code>gcs</code> storage media type.

Note that this field is not readable by clients, only writeable.

<a href="#">Link to this property</a>

<details>

<summary>

auth\_method: optional "KEY"or "PASSWORD"

Authentication method used for “sftp” type storage medium

</summary>

One of the following:

"KEY"

<a href="#">Link to this property</a>

"PASSWORD"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

password: optional string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

private\_key: optional string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

region: optional string

Region of the storage medium.

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

type: optional "gcs"

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object {access\_key, region, auth\_method, 9 more }

</summary>

access\_key: unknown

minLength1

<a href="#">Link to this property</a>

region: unknown

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

auth\_method: optional "KEY"or "PASSWORD"

Authentication method used for “sftp” type storage medium

</summary>

One of the following:

"KEY"

<a href="#">Link to this property</a>

"PASSWORD"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

password: optional string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

private\_key: optional string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "aws"or "azure"or "digitalocean"

</summary>

One of the following:

"aws"

<a href="#">Link to this property</a>

"azure"

<a href="#">Link to this property</a>

"digitalocean"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object {private\_key, access\_key, auth\_method, 9 more }

</summary>

private\_key: string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

access\_key: optional string

Access key of the storage medium. Access key is not required for the <code>gcs</code> storage media type.

Note that this field is not readable by clients, only writeable.

<a href="#">Link to this property</a>

auth\_method: optional "KEY"

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

password: optional string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

region: optional string

Region of the storage medium.

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "aws"or "azure"or "digitalocean"or 2 more

Type of storage media.

</summary>

One of the following:

"aws"

<a href="#">Link to this property</a>

"azure"

<a href="#">Link to this property</a>

"digitalocean"

<a href="#">Link to this property</a>

"gcs"

<a href="#">Link to this property</a>

"sftp"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object {password, access\_key, auth\_method, 9 more }

</summary>

password: string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

access\_key: optional string

Access key of the storage medium. Access key is not required for the <code>gcs</code> storage media type.

Note that this field is not readable by clients, only writeable.

<a href="#">Link to this property</a>

auth\_method: optional "PASSWORD"

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

private\_key: optional string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

region: optional string

Region of the storage medium.

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "aws"or "azure"or "digitalocean"or 2 more

Type of storage media.

</summary>

One of the following:

"aws"

<a href="#">Link to this property</a>

"azure"

<a href="#">Link to this property</a>

"digitalocean"

<a href="#">Link to this property</a>

"gcs"

<a href="#">Link to this property</a>

"sftp"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video\_config: optional object {codec, export\_file, height, 2 more }

</summary>

<details>

<summary>

codec: optional "H264"or "VP8"or "VP9"

Codec using which the recording will be encoded.

</summary>

One of the following:

"H264"

<a href="#">Link to this property</a>

"VP8"

<a href="#">Link to this property</a>

"VP9"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

export\_file: optional boolean

Controls whether to export video file seperately

<a href="#">Link to this property</a>

height: optional number

Height of the recording video in pixels

maximum1920

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

watermark: optional object {position, size, url }

Watermark to be added to the recording

</summary>

<details>

<summary>

position: optional "left top"or "right top"or "left bottom"or "right bottom"

Position of the watermark

</summary>

One of the following:

"left top"

<a href="#">Link to this property</a>

"right top"

<a href="#">Link to this property</a>

"left bottom"

<a href="#">Link to this property</a>

"right bottom"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

size: optional object {height, width }

Size of the watermark

</summary>

height: optional number

Height of the watermark in px

minimum1

<a href="#">Link to this property</a>

width: optional number

Width of the watermark in px

minimum1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

url: optional string

URL of the watermark image

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

width: optional number

Width of the recording video in pixels

maximum1920

minimum1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

session\_keep\_alive\_time\_in\_secs: optional number

Time in seconds, for which a session remains active, after the last participant has left the meeting.

maximum600

minimum60

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "ACTIVE"or "INACTIVE"

Whether the meeting is <code>ACTIVE</code> or <code>INACTIVE</code>. Users will not be able to join an <code>INACTIVE</code> meeting.

</summary>

One of the following:

"ACTIVE"

<a href="#">Link to this property</a>

"INACTIVE"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

summarize\_on\_end: optional boolean

Automatically generate summary of meetings using transcripts. Requires Transcriptions to be enabled, and can be retrieved via Webhooks or summary API.

<a href="#">Link to this property</a>

title: optional string

Title of the meeting.

<a href="#">Link to this property</a>

transcribe\_on\_end: optional boolean

Automatically generate transcripts when the meeting ends.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.meetings%20%3E%20(model)%20meeting_replace_meeting_by_id_response%20%3E%20(schema)>)

<details>

<summary>

MeetingGetMeetingParticipantsResponse object {data, paging, success }

</summary>

<details>

<summary>

data: array of object {id, created\_at, custom\_participant\_id, 4 more }

</summary>

id: string

ID of the participant.

formatuuid

<a href="#">Link to this property</a>

created\_at: string

When this object was created. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

custom\_participant\_id: string

A unique participant ID generated by the client.

<a href="#">Link to this property</a>

preset\_name: string

Preset applied to the participant.

<a href="#">Link to this property</a>

updated\_at: string

When this object was updated. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

name: optional string

Name of the participant.

<a href="#">Link to this property</a>

picture: optional string

URL to a picture of the participant.

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

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

<a href="#">Link to this property</a>

success: boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.meetings%20%3E%20(model)%20meeting_get_meeting_participants_response%20%3E%20(schema)>)

<details>

<summary>

MeetingAddParticipantResponse object {success, data }

</summary>

success: boolean

Success status of the operation

<a href="#">Link to this property</a>

<details>

<summary>

data: optional object {id, token, created\_at, 5 more }

Represents a participant.

</summary>

id: string

ID of the participant.

formatuuid

<a href="#">Link to this property</a>

token: string

The participant’s auth token that can be used for joining a meeting from the client side.

<a href="#">Link to this property</a>

created\_at: string

When this object was created. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

custom\_participant\_id: string

A unique participant ID generated by the client.

<a href="#">Link to this property</a>

preset\_name: string

Preset applied to the participant.

<a href="#">Link to this property</a>

updated\_at: string

When this object was updated. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

name: optional string

Name of the participant.

<a href="#">Link to this property</a>

picture: optional string

URL to a picture of the participant.

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.meetings%20%3E%20(model)%20meeting_add_participant_response%20%3E%20(schema)>)

<details>

<summary>

MeetingGetMeetingParticipantResponse object {data, success }

</summary>

<details>

<summary>

data: object {id, created\_at, custom\_participant\_id, 4 more }

Data returned by the operation

</summary>

id: string

ID of the participant.

formatuuid

<a href="#">Link to this property</a>

created\_at: string

When this object was created. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

custom\_participant\_id: string

A unique participant ID generated by the client.

<a href="#">Link to this property</a>

preset\_name: string

Preset applied to the participant.

<a href="#">Link to this property</a>

updated\_at: string

When this object was updated. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

name: optional string

Name of the participant.

<a href="#">Link to this property</a>

picture: optional string

URL to a picture of the participant.

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

success: boolean

Success status of the operation

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.meetings%20%3E%20(model)%20meeting_get_meeting_participant_response%20%3E%20(schema)>)

<details>

<summary>

MeetingEditParticipantResponse object {success, data }

</summary>

success: boolean

Success status of the operation

<a href="#">Link to this property</a>

<details>

<summary>

data: optional object {id, token, created\_at, 5 more }

Represents a participant.

</summary>

id: string

ID of the participant.

formatuuid

<a href="#">Link to this property</a>

token: string

The participant’s auth token that can be used for joining a meeting from the client side.

<a href="#">Link to this property</a>

created\_at: string

When this object was created. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

custom\_participant\_id: string

A unique participant ID generated by the client.

<a href="#">Link to this property</a>

preset\_name: string

Preset applied to the participant.

<a href="#">Link to this property</a>

updated\_at: string

When this object was updated. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

name: optional string

Name of the participant.

<a href="#">Link to this property</a>

picture: optional string

URL to a picture of the participant.

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.meetings%20%3E%20(model)%20meeting_edit_participant_response%20%3E%20(schema)>)

<details>

<summary>

MeetingDeleteMeetingParticipantResponse object {success, data }

</summary>

success: boolean

Success status of the operation

<a href="#">Link to this property</a>

<details>

<summary>

data: optional object {created\_at, custom\_participant\_id, preset\_id, updated\_at }

Data returned by the operation

</summary>

created\_at: string

Timestamp this object was created at. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

custom\_participant\_id: string

A unique participant ID generated by the client.

<a href="#">Link to this property</a>

preset\_id: string

ID of the preset applied to this participant.

formatuuid

<a href="#">Link to this property</a>

updated\_at: string

Timestamp this object was updated at. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.meetings%20%3E%20(model)%20meeting_delete_meeting_participant_response%20%3E%20(schema)>)

<details>

<summary>

MeetingRefreshParticipantTokenResponse object {data, success }

</summary>

<details>

<summary>

data: object {token }

Data returned by the operation

</summary>

token: string

Regenerated participant’s authentication token.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

success: boolean

Success status of the operation

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.meetings%20%3E%20(model)%20meeting_refresh_participant_token_response%20%3E%20(schema)>)

#### Realtime KitPresets

##### [Fetch all presets](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/presets/methods/get)

GET/accounts/{account\_id}/realtime/kit/{app\_id}/presets

##### [Create a preset](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/presets/methods/create)

POST/accounts/{account\_id}/realtime/kit/{app\_id}/presets

##### [Fetch details of a preset](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/presets/methods/get_preset_by_id)

GET/accounts/{account\_id}/realtime/kit/{app\_id}/presets/{preset\_id}

##### [Delete a preset](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/presets/methods/delete)

DELETE/accounts/{account\_id}/realtime/kit/{app\_id}/presets/{preset\_id}

##### [Update a preset](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/presets/methods/update)

PATCH/accounts/{account\_id}/realtime/kit/{app\_id}/presets/{preset\_id}

##### [Replace a preset](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/presets/methods/replace_preset_by_id)

PUT/accounts/{account\_id}/realtime/kit/{app\_id}/presets/{preset\_id}

##### ModelsExpand Collapse

<details>

<summary>

PresetGetResponse object {data, paging, success }

</summary>

<details>

<summary>

data: array of object {id, created\_at, name, updated\_at }

</summary>

id: optional string

ID of the preset

formatuuid

<a href="#">Link to this property</a>

created\_at: optional string

Timestamp this preset was created at

formatdate-time

<a href="#">Link to this property</a>

name: optional string

Name of the preset

<a href="#">Link to this property</a>

updated\_at: optional string

Timestamp this preset was last updated

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

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

<a href="#">Link to this property</a>

success: boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.presets%20%3E%20(model)%20preset_get_response%20%3E%20(schema)>)

<details>

<summary>

PresetCreateResponse object {data, success }

</summary>

<details>

<summary>

data: object {id, config, created\_at, 4 more }

Data returned by the operation

</summary>

id: string

ID of the preset

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

config: object {max\_screenshare\_count, max\_video\_streams, media, 2 more }

</summary>

max\_screenshare\_count: number

Maximum number of screen shares that can be active at a given time

<a href="#">Link to this property</a>

<details>

<summary>

max\_video\_streams: object {desktop, mobile }

Maximum number of streams that are visible on a device

</summary>

desktop: number

Maximum number of video streams visible on desktop devices

<a href="#">Link to this property</a>

mobile: number

Maximum number of streams visible on mobile devices

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

media: object {screenshare, video, audio }

Media configuration options. eg: Video quality

</summary>

<details>

<summary>

screenshare: object {frame\_rate, quality }

Configuration options for participant screen shares

</summary>

frame\_rate: number

Frame rate of screen share

<a href="#">Link to this property</a>

<details>

<summary>

quality: "hd"or "vga"or "qvga"or 2 more

Quality of screen share

</summary>

One of the following:

"hd"

<a href="#">Link to this property</a>

"vga"

<a href="#">Link to this property</a>

"qvga"

<a href="#">Link to this property</a>

"fhd"

<a href="#">Link to this property</a>

"uhd"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video: object {frame\_rate, quality, simulcast }

Configuration options for participant videos

</summary>

frame\_rate: number

Frame rate of participants’ video

maximum30

<a href="#">Link to this property</a>

<details>

<summary>

quality: "hd"or "vga"or "qvga"or 2 more

Video quality of participants

</summary>

One of the following:

"hd"

<a href="#">Link to this property</a>

"vga"

<a href="#">Link to this property</a>

"qvga"

<a href="#">Link to this property</a>

"fhd"

<a href="#">Link to this property</a>

"uhd"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

simulcast: optional boolean

Enable simulcast for participant videos.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

audio: optional object {enable\_high\_bitrate, enable\_stereo }

Control options for Audio quality.

</summary>

enable\_high\_bitrate: optional boolean

Enable High Quality Audio for your meetings

<a href="#">Link to this property</a>

enable\_stereo: optional boolean

Enable Stereo for your meetings

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

view\_type: "GROUP\_CALL"or "WEBINAR"or "AUDIO\_ROOM"or "LIVESTREAM"

Type of the meeting

</summary>

One of the following:

"GROUP\_CALL"

<a href="#">Link to this property</a>

"WEBINAR"

<a href="#">Link to this property</a>

"AUDIO\_ROOM"

<a href="#">Link to this property</a>

"LIVESTREAM"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

livestream\_viewer\_qualities: optional array of number

Livestream viewer quality levels.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: string

Timestamp this preset was created at

formatdate-time

<a href="#">Link to this property</a>

name: string

Name of the preset

<a href="#">Link to this property</a>

<details>

<summary>

permissions: object {accept\_waiting\_requests, can\_accept\_production\_requests, can\_change\_participant\_permissions, 23 more }

</summary>

accept\_waiting\_requests: boolean

Whether this participant can accept waiting requests

<a href="#">Link to this property</a>

can\_accept\_production\_requests: boolean

<a href="#">Link to this property</a>

can\_change\_participant\_permissions: boolean

<a href="#">Link to this property</a>

can\_edit\_display\_name: boolean

<a href="#">Link to this property</a>

can\_livestream: boolean

<a href="#">Link to this property</a>

can\_record: boolean

<a href="#">Link to this property</a>

can\_spotlight: boolean

<a href="#">Link to this property</a>

<details>

<summary>

chat: object {private, public }

</summary>

<details>

<summary>

private: object {can\_receive, can\_send, files, text }

</summary>

can\_receive: boolean

<a href="#">Link to this property</a>

can\_send: boolean

<a href="#">Link to this property</a>

files: boolean

<a href="#">Link to this property</a>

text: boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

public: object {can\_send, files, text }

</summary>

can\_send: boolean

Can send messages in general

<a href="#">Link to this property</a>

files: boolean

Can send file messages

<a href="#">Link to this property</a>

text: boolean

Can send text messages

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

connected\_meetings: object {can\_alter\_connected\_meetings, can\_switch\_connected\_meetings, can\_switch\_to\_parent\_meeting }

</summary>

can\_alter\_connected\_meetings: boolean

<a href="#">Link to this property</a>

can\_switch\_connected\_meetings: boolean

<a href="#">Link to this property</a>

can\_switch\_to\_parent\_meeting: boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

disable\_participant\_audio: boolean

<a href="#">Link to this property</a>

disable\_participant\_screensharing: boolean

<a href="#">Link to this property</a>

disable\_participant\_video: boolean

<a href="#">Link to this property</a>

hidden\_participant: boolean

Whether this participant is visible to others or not

<a href="#">Link to this property</a>

kick\_participant: boolean

<a href="#">Link to this property</a>

<details>

<summary>

media: object {audio, screenshare, video }

Media permissions

</summary>

<details>

<summary>

audio: object {can\_produce }

Audio permissions

</summary>

<details>

<summary>

can\_produce: "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

Can produce audio

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

screenshare: object {can\_produce }

Screenshare permissions

</summary>

<details>

<summary>

can\_produce: "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

Can produce screen share video

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video: object {can\_produce }

Video permissions

</summary>

<details>

<summary>

can\_produce: "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

Can produce video

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

pin\_participant: boolean

<a href="#">Link to this property</a>

<details>

<summary>

plugins: object {can\_close, can\_edit\_config, can\_start, config }

Plugin permissions

</summary>

can\_close: boolean

Can close plugins that are already open

<a href="#">Link to this property</a>

can\_edit\_config: boolean

Can edit plugin config

<a href="#">Link to this property</a>

can\_start: boolean

Can start plugins

<a href="#">Link to this property</a>

<details>

<summary>

config: map\[object {access\_control, handles\_view\_only } ]

Plugin configuration keyed by plugin UUID.

</summary>

<details>

<summary>

access\_control: optional "FULL\_ACCESS"or "VIEW\_ONLY"

</summary>

One of the following:

"FULL\_ACCESS"

<a href="#">Link to this property</a>

"VIEW\_ONLY"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

handles\_view\_only: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

polls: object {can\_create, can\_view, can\_vote }

Poll permissions

</summary>

can\_create: boolean

Can create polls

<a href="#">Link to this property</a>

can\_view: boolean

Can view polls

<a href="#">Link to this property</a>

can\_vote: boolean

Can vote on polls

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

recorder\_type: "RECORDER"or "LIVESTREAMER"or "NONE"

Type of the recording peer

</summary>

One of the following:

"RECORDER"

<a href="#">Link to this property</a>

"LIVESTREAMER"

<a href="#">Link to this property</a>

"NONE"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

show\_participant\_list: boolean

<a href="#">Link to this property</a>

<details>

<summary>

waiting\_room\_type: "SKIP"or "ON\_PRIVILEGED\_USER\_ENTRY"or "SKIP\_ON\_ACCEPT"

Waiting room type

</summary>

One of the following:

"SKIP"

<a href="#">Link to this property</a>

"ON\_PRIVILEGED\_USER\_ENTRY"

<a href="#">Link to this property</a>

"SKIP\_ON\_ACCEPT"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

accept\_stage\_requests: optional boolean

<a href="#">Link to this property</a>

is\_recorder: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

stage\_access: optional "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

stage\_enabled: optional boolean

<a href="#">Link to this property</a>

transcription\_enabled: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ui: object {design\_tokens }

</summary>

<details>

<summary>

design\_tokens: object {border\_radius, border\_width, colors, 5 more }

</summary>

<details>

<summary>

border\_radius: "sharp"or "rounded"or "extra-rounded"or "circular"

</summary>

One of the following:

"sharp"

<a href="#">Link to this property</a>

"rounded"

<a href="#">Link to this property</a>

"extra-rounded"

<a href="#">Link to this property</a>

"circular"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

border\_width: "none"or "thin"or "fat"

</summary>

One of the following:

"none"

<a href="#">Link to this property</a>

"thin"

<a href="#">Link to this property</a>

"fat"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

colors: object {background, brand, danger, 5 more }

</summary>

<details>

<summary>

background: object {"1000", "600", "700", 2 more }

</summary>

"1000": string

<a href="#">Link to this property</a>

"600": string

<a href="#">Link to this property</a>

"700": string

<a href="#">Link to this property</a>

"800": string

<a href="#">Link to this property</a>

"900": string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

brand: object {"300", "400", "500", 2 more }

</summary>

"300": string

<a href="#">Link to this property</a>

"400": string

<a href="#">Link to this property</a>

"500": string

<a href="#">Link to this property</a>

"600": string

<a href="#">Link to this property</a>

"700": string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

danger: string

<a href="#">Link to this property</a>

success: string

<a href="#">Link to this property</a>

text: string

<a href="#">Link to this property</a>

text\_on\_brand: string

<a href="#">Link to this property</a>

video\_bg: string

<a href="#">Link to this property</a>

warning: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

spacing\_base: number

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

theme: "darkest"or "dark"or "light"

</summary>

One of the following:

"darkest"

<a href="#">Link to this property</a>

"dark"

<a href="#">Link to this property</a>

"light"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

font\_family: optional string

<a href="#">Link to this property</a>

google\_font: optional string

<a href="#">Link to this property</a>

logo: optional string

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

Timestamp this preset was last updated

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

success: boolean

Success status of the operation

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.presets%20%3E%20(model)%20preset_create_response%20%3E%20(schema)>)

<details>

<summary>

PresetGetPresetByIDResponse object {data, success }

</summary>

<details>

<summary>

data: object {id, config, created\_at, 4 more }

Data returned by the operation

</summary>

id: string

ID of the preset

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

config: object {max\_screenshare\_count, max\_video\_streams, media, 2 more }

</summary>

max\_screenshare\_count: number

Maximum number of screen shares that can be active at a given time

<a href="#">Link to this property</a>

<details>

<summary>

max\_video\_streams: object {desktop, mobile }

Maximum number of streams that are visible on a device

</summary>

desktop: number

Maximum number of video streams visible on desktop devices

<a href="#">Link to this property</a>

mobile: number

Maximum number of streams visible on mobile devices

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

media: object {screenshare, video, audio }

Media configuration options. eg: Video quality

</summary>

<details>

<summary>

screenshare: object {frame\_rate, quality }

Configuration options for participant screen shares

</summary>

frame\_rate: number

Frame rate of screen share

<a href="#">Link to this property</a>

<details>

<summary>

quality: "hd"or "vga"or "qvga"or 2 more

Quality of screen share

</summary>

One of the following:

"hd"

<a href="#">Link to this property</a>

"vga"

<a href="#">Link to this property</a>

"qvga"

<a href="#">Link to this property</a>

"fhd"

<a href="#">Link to this property</a>

"uhd"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video: object {frame\_rate, quality, simulcast }

Configuration options for participant videos

</summary>

frame\_rate: number

Frame rate of participants’ video

maximum30

<a href="#">Link to this property</a>

<details>

<summary>

quality: "hd"or "vga"or "qvga"or 2 more

Video quality of participants

</summary>

One of the following:

"hd"

<a href="#">Link to this property</a>

"vga"

<a href="#">Link to this property</a>

"qvga"

<a href="#">Link to this property</a>

"fhd"

<a href="#">Link to this property</a>

"uhd"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

simulcast: optional boolean

Enable simulcast for participant videos.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

audio: optional object {enable\_high\_bitrate, enable\_stereo }

Control options for Audio quality.

</summary>

enable\_high\_bitrate: optional boolean

Enable High Quality Audio for your meetings

<a href="#">Link to this property</a>

enable\_stereo: optional boolean

Enable Stereo for your meetings

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

view\_type: "GROUP\_CALL"or "WEBINAR"or "AUDIO\_ROOM"or "LIVESTREAM"

Type of the meeting

</summary>

One of the following:

"GROUP\_CALL"

<a href="#">Link to this property</a>

"WEBINAR"

<a href="#">Link to this property</a>

"AUDIO\_ROOM"

<a href="#">Link to this property</a>

"LIVESTREAM"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

livestream\_viewer\_qualities: optional array of number

Livestream viewer quality levels.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: string

Timestamp this preset was created at

formatdate-time

<a href="#">Link to this property</a>

name: string

Name of the preset

<a href="#">Link to this property</a>

<details>

<summary>

permissions: object {accept\_waiting\_requests, can\_accept\_production\_requests, can\_change\_participant\_permissions, 23 more }

</summary>

accept\_waiting\_requests: boolean

Whether this participant can accept waiting requests

<a href="#">Link to this property</a>

can\_accept\_production\_requests: boolean

<a href="#">Link to this property</a>

can\_change\_participant\_permissions: boolean

<a href="#">Link to this property</a>

can\_edit\_display\_name: boolean

<a href="#">Link to this property</a>

can\_livestream: boolean

<a href="#">Link to this property</a>

can\_record: boolean

<a href="#">Link to this property</a>

can\_spotlight: boolean

<a href="#">Link to this property</a>

<details>

<summary>

chat: object {private, public }

</summary>

<details>

<summary>

private: object {can\_receive, can\_send, files, text }

</summary>

can\_receive: boolean

<a href="#">Link to this property</a>

can\_send: boolean

<a href="#">Link to this property</a>

files: boolean

<a href="#">Link to this property</a>

text: boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

public: object {can\_send, files, text }

</summary>

can\_send: boolean

Can send messages in general

<a href="#">Link to this property</a>

files: boolean

Can send file messages

<a href="#">Link to this property</a>

text: boolean

Can send text messages

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

connected\_meetings: object {can\_alter\_connected\_meetings, can\_switch\_connected\_meetings, can\_switch\_to\_parent\_meeting }

</summary>

can\_alter\_connected\_meetings: boolean

<a href="#">Link to this property</a>

can\_switch\_connected\_meetings: boolean

<a href="#">Link to this property</a>

can\_switch\_to\_parent\_meeting: boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

disable\_participant\_audio: boolean

<a href="#">Link to this property</a>

disable\_participant\_screensharing: boolean

<a href="#">Link to this property</a>

disable\_participant\_video: boolean

<a href="#">Link to this property</a>

hidden\_participant: boolean

Whether this participant is visible to others or not

<a href="#">Link to this property</a>

kick\_participant: boolean

<a href="#">Link to this property</a>

<details>

<summary>

media: object {audio, screenshare, video }

Media permissions

</summary>

<details>

<summary>

audio: object {can\_produce }

Audio permissions

</summary>

<details>

<summary>

can\_produce: "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

Can produce audio

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

screenshare: object {can\_produce }

Screenshare permissions

</summary>

<details>

<summary>

can\_produce: "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

Can produce screen share video

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video: object {can\_produce }

Video permissions

</summary>

<details>

<summary>

can\_produce: "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

Can produce video

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

pin\_participant: boolean

<a href="#">Link to this property</a>

<details>

<summary>

plugins: object {can\_close, can\_edit\_config, can\_start, config }

Plugin permissions

</summary>

can\_close: boolean

Can close plugins that are already open

<a href="#">Link to this property</a>

can\_edit\_config: boolean

Can edit plugin config

<a href="#">Link to this property</a>

can\_start: boolean

Can start plugins

<a href="#">Link to this property</a>

<details>

<summary>

config: map\[object {access\_control, handles\_view\_only } ]

Plugin configuration keyed by plugin UUID.

</summary>

<details>

<summary>

access\_control: optional "FULL\_ACCESS"or "VIEW\_ONLY"

</summary>

One of the following:

"FULL\_ACCESS"

<a href="#">Link to this property</a>

"VIEW\_ONLY"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

handles\_view\_only: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

polls: object {can\_create, can\_view, can\_vote }

Poll permissions

</summary>

can\_create: boolean

Can create polls

<a href="#">Link to this property</a>

can\_view: boolean

Can view polls

<a href="#">Link to this property</a>

can\_vote: boolean

Can vote on polls

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

recorder\_type: "RECORDER"or "LIVESTREAMER"or "NONE"

Type of the recording peer

</summary>

One of the following:

"RECORDER"

<a href="#">Link to this property</a>

"LIVESTREAMER"

<a href="#">Link to this property</a>

"NONE"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

show\_participant\_list: boolean

<a href="#">Link to this property</a>

<details>

<summary>

waiting\_room\_type: "SKIP"or "ON\_PRIVILEGED\_USER\_ENTRY"or "SKIP\_ON\_ACCEPT"

Waiting room type

</summary>

One of the following:

"SKIP"

<a href="#">Link to this property</a>

"ON\_PRIVILEGED\_USER\_ENTRY"

<a href="#">Link to this property</a>

"SKIP\_ON\_ACCEPT"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

accept\_stage\_requests: optional boolean

<a href="#">Link to this property</a>

is\_recorder: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

stage\_access: optional "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

stage\_enabled: optional boolean

<a href="#">Link to this property</a>

transcription\_enabled: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ui: object {design\_tokens }

</summary>

<details>

<summary>

design\_tokens: object {border\_radius, border\_width, colors, 5 more }

</summary>

<details>

<summary>

border\_radius: "sharp"or "rounded"or "extra-rounded"or "circular"

</summary>

One of the following:

"sharp"

<a href="#">Link to this property</a>

"rounded"

<a href="#">Link to this property</a>

"extra-rounded"

<a href="#">Link to this property</a>

"circular"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

border\_width: "none"or "thin"or "fat"

</summary>

One of the following:

"none"

<a href="#">Link to this property</a>

"thin"

<a href="#">Link to this property</a>

"fat"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

colors: object {background, brand, danger, 5 more }

</summary>

<details>

<summary>

background: object {"1000", "600", "700", 2 more }

</summary>

"1000": string

<a href="#">Link to this property</a>

"600": string

<a href="#">Link to this property</a>

"700": string

<a href="#">Link to this property</a>

"800": string

<a href="#">Link to this property</a>

"900": string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

brand: object {"300", "400", "500", 2 more }

</summary>

"300": string

<a href="#">Link to this property</a>

"400": string

<a href="#">Link to this property</a>

"500": string

<a href="#">Link to this property</a>

"600": string

<a href="#">Link to this property</a>

"700": string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

danger: string

<a href="#">Link to this property</a>

success: string

<a href="#">Link to this property</a>

text: string

<a href="#">Link to this property</a>

text\_on\_brand: string

<a href="#">Link to this property</a>

video\_bg: string

<a href="#">Link to this property</a>

warning: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

spacing\_base: number

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

theme: "darkest"or "dark"or "light"

</summary>

One of the following:

"darkest"

<a href="#">Link to this property</a>

"dark"

<a href="#">Link to this property</a>

"light"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

font\_family: optional string

<a href="#">Link to this property</a>

google\_font: optional string

<a href="#">Link to this property</a>

logo: optional string

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

Timestamp this preset was last updated

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

success: boolean

Success status of the operation

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.presets%20%3E%20(model)%20preset_get_preset_by_id_response%20%3E%20(schema)>)

<details>

<summary>

PresetDeleteResponse object {data, success }

</summary>

<details>

<summary>

data: object {id, config, created\_at, 4 more }

Data returned by the operation

</summary>

id: string

ID of the preset

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

config: object {max\_screenshare\_count, max\_video\_streams, media, 2 more }

</summary>

max\_screenshare\_count: number

Maximum number of screen shares that can be active at a given time

<a href="#">Link to this property</a>

<details>

<summary>

max\_video\_streams: object {desktop, mobile }

Maximum number of streams that are visible on a device

</summary>

desktop: number

Maximum number of video streams visible on desktop devices

<a href="#">Link to this property</a>

mobile: number

Maximum number of streams visible on mobile devices

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

media: object {screenshare, video, audio }

Media configuration options. eg: Video quality

</summary>

<details>

<summary>

screenshare: object {frame\_rate, quality }

Configuration options for participant screen shares

</summary>

frame\_rate: number

Frame rate of screen share

<a href="#">Link to this property</a>

<details>

<summary>

quality: "hd"or "vga"or "qvga"or 2 more

Quality of screen share

</summary>

One of the following:

"hd"

<a href="#">Link to this property</a>

"vga"

<a href="#">Link to this property</a>

"qvga"

<a href="#">Link to this property</a>

"fhd"

<a href="#">Link to this property</a>

"uhd"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video: object {frame\_rate, quality, simulcast }

Configuration options for participant videos

</summary>

frame\_rate: number

Frame rate of participants’ video

maximum30

<a href="#">Link to this property</a>

<details>

<summary>

quality: "hd"or "vga"or "qvga"or 2 more

Video quality of participants

</summary>

One of the following:

"hd"

<a href="#">Link to this property</a>

"vga"

<a href="#">Link to this property</a>

"qvga"

<a href="#">Link to this property</a>

"fhd"

<a href="#">Link to this property</a>

"uhd"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

simulcast: optional boolean

Enable simulcast for participant videos.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

audio: optional object {enable\_high\_bitrate, enable\_stereo }

Control options for Audio quality.

</summary>

enable\_high\_bitrate: optional boolean

Enable High Quality Audio for your meetings

<a href="#">Link to this property</a>

enable\_stereo: optional boolean

Enable Stereo for your meetings

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

view\_type: "GROUP\_CALL"or "WEBINAR"or "AUDIO\_ROOM"or "LIVESTREAM"

Type of the meeting

</summary>

One of the following:

"GROUP\_CALL"

<a href="#">Link to this property</a>

"WEBINAR"

<a href="#">Link to this property</a>

"AUDIO\_ROOM"

<a href="#">Link to this property</a>

"LIVESTREAM"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

livestream\_viewer\_qualities: optional array of number

Livestream viewer quality levels.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: string

Timestamp this preset was created at

formatdate-time

<a href="#">Link to this property</a>

name: string

Name of the preset

<a href="#">Link to this property</a>

<details>

<summary>

permissions: object {accept\_waiting\_requests, can\_accept\_production\_requests, can\_change\_participant\_permissions, 23 more }

</summary>

accept\_waiting\_requests: boolean

Whether this participant can accept waiting requests

<a href="#">Link to this property</a>

can\_accept\_production\_requests: boolean

<a href="#">Link to this property</a>

can\_change\_participant\_permissions: boolean

<a href="#">Link to this property</a>

can\_edit\_display\_name: boolean

<a href="#">Link to this property</a>

can\_livestream: boolean

<a href="#">Link to this property</a>

can\_record: boolean

<a href="#">Link to this property</a>

can\_spotlight: boolean

<a href="#">Link to this property</a>

<details>

<summary>

chat: object {private, public }

</summary>

<details>

<summary>

private: object {can\_receive, can\_send, files, text }

</summary>

can\_receive: boolean

<a href="#">Link to this property</a>

can\_send: boolean

<a href="#">Link to this property</a>

files: boolean

<a href="#">Link to this property</a>

text: boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

public: object {can\_send, files, text }

</summary>

can\_send: boolean

Can send messages in general

<a href="#">Link to this property</a>

files: boolean

Can send file messages

<a href="#">Link to this property</a>

text: boolean

Can send text messages

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

connected\_meetings: object {can\_alter\_connected\_meetings, can\_switch\_connected\_meetings, can\_switch\_to\_parent\_meeting }

</summary>

can\_alter\_connected\_meetings: boolean

<a href="#">Link to this property</a>

can\_switch\_connected\_meetings: boolean

<a href="#">Link to this property</a>

can\_switch\_to\_parent\_meeting: boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

disable\_participant\_audio: boolean

<a href="#">Link to this property</a>

disable\_participant\_screensharing: boolean

<a href="#">Link to this property</a>

disable\_participant\_video: boolean

<a href="#">Link to this property</a>

hidden\_participant: boolean

Whether this participant is visible to others or not

<a href="#">Link to this property</a>

kick\_participant: boolean

<a href="#">Link to this property</a>

<details>

<summary>

media: object {audio, screenshare, video }

Media permissions

</summary>

<details>

<summary>

audio: object {can\_produce }

Audio permissions

</summary>

<details>

<summary>

can\_produce: "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

Can produce audio

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

screenshare: object {can\_produce }

Screenshare permissions

</summary>

<details>

<summary>

can\_produce: "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

Can produce screen share video

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video: object {can\_produce }

Video permissions

</summary>

<details>

<summary>

can\_produce: "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

Can produce video

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

pin\_participant: boolean

<a href="#">Link to this property</a>

<details>

<summary>

plugins: object {can\_close, can\_edit\_config, can\_start, config }

Plugin permissions

</summary>

can\_close: boolean

Can close plugins that are already open

<a href="#">Link to this property</a>

can\_edit\_config: boolean

Can edit plugin config

<a href="#">Link to this property</a>

can\_start: boolean

Can start plugins

<a href="#">Link to this property</a>

<details>

<summary>

config: map\[object {access\_control, handles\_view\_only } ]

Plugin configuration keyed by plugin UUID.

</summary>

<details>

<summary>

access\_control: optional "FULL\_ACCESS"or "VIEW\_ONLY"

</summary>

One of the following:

"FULL\_ACCESS"

<a href="#">Link to this property</a>

"VIEW\_ONLY"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

handles\_view\_only: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

polls: object {can\_create, can\_view, can\_vote }

Poll permissions

</summary>

can\_create: boolean

Can create polls

<a href="#">Link to this property</a>

can\_view: boolean

Can view polls

<a href="#">Link to this property</a>

can\_vote: boolean

Can vote on polls

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

recorder\_type: "RECORDER"or "LIVESTREAMER"or "NONE"

Type of the recording peer

</summary>

One of the following:

"RECORDER"

<a href="#">Link to this property</a>

"LIVESTREAMER"

<a href="#">Link to this property</a>

"NONE"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

show\_participant\_list: boolean

<a href="#">Link to this property</a>

<details>

<summary>

waiting\_room\_type: "SKIP"or "ON\_PRIVILEGED\_USER\_ENTRY"or "SKIP\_ON\_ACCEPT"

Waiting room type

</summary>

One of the following:

"SKIP"

<a href="#">Link to this property</a>

"ON\_PRIVILEGED\_USER\_ENTRY"

<a href="#">Link to this property</a>

"SKIP\_ON\_ACCEPT"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

accept\_stage\_requests: optional boolean

<a href="#">Link to this property</a>

is\_recorder: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

stage\_access: optional "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

stage\_enabled: optional boolean

<a href="#">Link to this property</a>

transcription\_enabled: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ui: object {design\_tokens }

</summary>

<details>

<summary>

design\_tokens: object {border\_radius, border\_width, colors, 5 more }

</summary>

<details>

<summary>

border\_radius: "sharp"or "rounded"or "extra-rounded"or "circular"

</summary>

One of the following:

"sharp"

<a href="#">Link to this property</a>

"rounded"

<a href="#">Link to this property</a>

"extra-rounded"

<a href="#">Link to this property</a>

"circular"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

border\_width: "none"or "thin"or "fat"

</summary>

One of the following:

"none"

<a href="#">Link to this property</a>

"thin"

<a href="#">Link to this property</a>

"fat"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

colors: object {background, brand, danger, 5 more }

</summary>

<details>

<summary>

background: object {"1000", "600", "700", 2 more }

</summary>

"1000": string

<a href="#">Link to this property</a>

"600": string

<a href="#">Link to this property</a>

"700": string

<a href="#">Link to this property</a>

"800": string

<a href="#">Link to this property</a>

"900": string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

brand: object {"300", "400", "500", 2 more }

</summary>

"300": string

<a href="#">Link to this property</a>

"400": string

<a href="#">Link to this property</a>

"500": string

<a href="#">Link to this property</a>

"600": string

<a href="#">Link to this property</a>

"700": string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

danger: string

<a href="#">Link to this property</a>

success: string

<a href="#">Link to this property</a>

text: string

<a href="#">Link to this property</a>

text\_on\_brand: string

<a href="#">Link to this property</a>

video\_bg: string

<a href="#">Link to this property</a>

warning: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

spacing\_base: number

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

theme: "darkest"or "dark"or "light"

</summary>

One of the following:

"darkest"

<a href="#">Link to this property</a>

"dark"

<a href="#">Link to this property</a>

"light"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

font\_family: optional string

<a href="#">Link to this property</a>

google\_font: optional string

<a href="#">Link to this property</a>

logo: optional string

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

Timestamp this preset was last updated

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

success: boolean

Success status of the operation

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.presets%20%3E%20(model)%20preset_delete_response%20%3E%20(schema)>)

<details>

<summary>

PresetUpdateResponse object {data, success }

</summary>

<details>

<summary>

data: object {id, config, created\_at, 4 more }

Data returned by the operation

</summary>

id: string

ID of the preset

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

config: object {max\_screenshare\_count, max\_video\_streams, media, 2 more }

</summary>

max\_screenshare\_count: number

Maximum number of screen shares that can be active at a given time

<a href="#">Link to this property</a>

<details>

<summary>

max\_video\_streams: object {desktop, mobile }

Maximum number of streams that are visible on a device

</summary>

desktop: number

Maximum number of video streams visible on desktop devices

<a href="#">Link to this property</a>

mobile: number

Maximum number of streams visible on mobile devices

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

media: object {screenshare, video, audio }

Media configuration options. eg: Video quality

</summary>

<details>

<summary>

screenshare: object {frame\_rate, quality }

Configuration options for participant screen shares

</summary>

frame\_rate: number

Frame rate of screen share

<a href="#">Link to this property</a>

<details>

<summary>

quality: "hd"or "vga"or "qvga"or 2 more

Quality of screen share

</summary>

One of the following:

"hd"

<a href="#">Link to this property</a>

"vga"

<a href="#">Link to this property</a>

"qvga"

<a href="#">Link to this property</a>

"fhd"

<a href="#">Link to this property</a>

"uhd"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video: object {frame\_rate, quality, simulcast }

Configuration options for participant videos

</summary>

frame\_rate: number

Frame rate of participants’ video

maximum30

<a href="#">Link to this property</a>

<details>

<summary>

quality: "hd"or "vga"or "qvga"or 2 more

Video quality of participants

</summary>

One of the following:

"hd"

<a href="#">Link to this property</a>

"vga"

<a href="#">Link to this property</a>

"qvga"

<a href="#">Link to this property</a>

"fhd"

<a href="#">Link to this property</a>

"uhd"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

simulcast: optional boolean

Enable simulcast for participant videos.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

audio: optional object {enable\_high\_bitrate, enable\_stereo }

Control options for Audio quality.

</summary>

enable\_high\_bitrate: optional boolean

Enable High Quality Audio for your meetings

<a href="#">Link to this property</a>

enable\_stereo: optional boolean

Enable Stereo for your meetings

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

view\_type: "GROUP\_CALL"or "WEBINAR"or "AUDIO\_ROOM"or "LIVESTREAM"

Type of the meeting

</summary>

One of the following:

"GROUP\_CALL"

<a href="#">Link to this property</a>

"WEBINAR"

<a href="#">Link to this property</a>

"AUDIO\_ROOM"

<a href="#">Link to this property</a>

"LIVESTREAM"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

livestream\_viewer\_qualities: optional array of number

Livestream viewer quality levels.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: string

Timestamp this preset was created at

formatdate-time

<a href="#">Link to this property</a>

name: string

Name of the preset

<a href="#">Link to this property</a>

<details>

<summary>

permissions: object {accept\_waiting\_requests, can\_accept\_production\_requests, can\_change\_participant\_permissions, 23 more }

</summary>

accept\_waiting\_requests: boolean

Whether this participant can accept waiting requests

<a href="#">Link to this property</a>

can\_accept\_production\_requests: boolean

<a href="#">Link to this property</a>

can\_change\_participant\_permissions: boolean

<a href="#">Link to this property</a>

can\_edit\_display\_name: boolean

<a href="#">Link to this property</a>

can\_livestream: boolean

<a href="#">Link to this property</a>

can\_record: boolean

<a href="#">Link to this property</a>

can\_spotlight: boolean

<a href="#">Link to this property</a>

<details>

<summary>

chat: object {private, public }

</summary>

<details>

<summary>

private: object {can\_receive, can\_send, files, text }

</summary>

can\_receive: boolean

<a href="#">Link to this property</a>

can\_send: boolean

<a href="#">Link to this property</a>

files: boolean

<a href="#">Link to this property</a>

text: boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

public: object {can\_send, files, text }

</summary>

can\_send: boolean

Can send messages in general

<a href="#">Link to this property</a>

files: boolean

Can send file messages

<a href="#">Link to this property</a>

text: boolean

Can send text messages

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

connected\_meetings: object {can\_alter\_connected\_meetings, can\_switch\_connected\_meetings, can\_switch\_to\_parent\_meeting }

</summary>

can\_alter\_connected\_meetings: boolean

<a href="#">Link to this property</a>

can\_switch\_connected\_meetings: boolean

<a href="#">Link to this property</a>

can\_switch\_to\_parent\_meeting: boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

disable\_participant\_audio: boolean

<a href="#">Link to this property</a>

disable\_participant\_screensharing: boolean

<a href="#">Link to this property</a>

disable\_participant\_video: boolean

<a href="#">Link to this property</a>

hidden\_participant: boolean

Whether this participant is visible to others or not

<a href="#">Link to this property</a>

kick\_participant: boolean

<a href="#">Link to this property</a>

<details>

<summary>

media: object {audio, screenshare, video }

Media permissions

</summary>

<details>

<summary>

audio: object {can\_produce }

Audio permissions

</summary>

<details>

<summary>

can\_produce: "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

Can produce audio

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

screenshare: object {can\_produce }

Screenshare permissions

</summary>

<details>

<summary>

can\_produce: "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

Can produce screen share video

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video: object {can\_produce }

Video permissions

</summary>

<details>

<summary>

can\_produce: "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

Can produce video

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

pin\_participant: boolean

<a href="#">Link to this property</a>

<details>

<summary>

plugins: object {can\_close, can\_edit\_config, can\_start, config }

Plugin permissions

</summary>

can\_close: boolean

Can close plugins that are already open

<a href="#">Link to this property</a>

can\_edit\_config: boolean

Can edit plugin config

<a href="#">Link to this property</a>

can\_start: boolean

Can start plugins

<a href="#">Link to this property</a>

<details>

<summary>

config: map\[object {access\_control, handles\_view\_only } ]

Plugin configuration keyed by plugin UUID.

</summary>

<details>

<summary>

access\_control: optional "FULL\_ACCESS"or "VIEW\_ONLY"

</summary>

One of the following:

"FULL\_ACCESS"

<a href="#">Link to this property</a>

"VIEW\_ONLY"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

handles\_view\_only: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

polls: object {can\_create, can\_view, can\_vote }

Poll permissions

</summary>

can\_create: boolean

Can create polls

<a href="#">Link to this property</a>

can\_view: boolean

Can view polls

<a href="#">Link to this property</a>

can\_vote: boolean

Can vote on polls

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

recorder\_type: "RECORDER"or "LIVESTREAMER"or "NONE"

Type of the recording peer

</summary>

One of the following:

"RECORDER"

<a href="#">Link to this property</a>

"LIVESTREAMER"

<a href="#">Link to this property</a>

"NONE"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

show\_participant\_list: boolean

<a href="#">Link to this property</a>

<details>

<summary>

waiting\_room\_type: "SKIP"or "ON\_PRIVILEGED\_USER\_ENTRY"or "SKIP\_ON\_ACCEPT"

Waiting room type

</summary>

One of the following:

"SKIP"

<a href="#">Link to this property</a>

"ON\_PRIVILEGED\_USER\_ENTRY"

<a href="#">Link to this property</a>

"SKIP\_ON\_ACCEPT"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

accept\_stage\_requests: optional boolean

<a href="#">Link to this property</a>

is\_recorder: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

stage\_access: optional "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

stage\_enabled: optional boolean

<a href="#">Link to this property</a>

transcription\_enabled: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ui: object {design\_tokens }

</summary>

<details>

<summary>

design\_tokens: object {border\_radius, border\_width, colors, 5 more }

</summary>

<details>

<summary>

border\_radius: "sharp"or "rounded"or "extra-rounded"or "circular"

</summary>

One of the following:

"sharp"

<a href="#">Link to this property</a>

"rounded"

<a href="#">Link to this property</a>

"extra-rounded"

<a href="#">Link to this property</a>

"circular"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

border\_width: "none"or "thin"or "fat"

</summary>

One of the following:

"none"

<a href="#">Link to this property</a>

"thin"

<a href="#">Link to this property</a>

"fat"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

colors: object {background, brand, danger, 5 more }

</summary>

<details>

<summary>

background: object {"1000", "600", "700", 2 more }

</summary>

"1000": string

<a href="#">Link to this property</a>

"600": string

<a href="#">Link to this property</a>

"700": string

<a href="#">Link to this property</a>

"800": string

<a href="#">Link to this property</a>

"900": string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

brand: object {"300", "400", "500", 2 more }

</summary>

"300": string

<a href="#">Link to this property</a>

"400": string

<a href="#">Link to this property</a>

"500": string

<a href="#">Link to this property</a>

"600": string

<a href="#">Link to this property</a>

"700": string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

danger: string

<a href="#">Link to this property</a>

success: string

<a href="#">Link to this property</a>

text: string

<a href="#">Link to this property</a>

text\_on\_brand: string

<a href="#">Link to this property</a>

video\_bg: string

<a href="#">Link to this property</a>

warning: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

spacing\_base: number

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

theme: "darkest"or "dark"or "light"

</summary>

One of the following:

"darkest"

<a href="#">Link to this property</a>

"dark"

<a href="#">Link to this property</a>

"light"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

font\_family: optional string

<a href="#">Link to this property</a>

google\_font: optional string

<a href="#">Link to this property</a>

logo: optional string

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

Timestamp this preset was last updated

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

success: boolean

Success status of the operation

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.presets%20%3E%20(model)%20preset_update_response%20%3E%20(schema)>)

<details>

<summary>

PresetReplacePresetByIDResponse object {data, success }

</summary>

<details>

<summary>

data: object {id, config, created\_at, 4 more }

Data returned by the operation

</summary>

id: string

ID of the preset

formatuuid

<a href="#">Link to this property</a>

<details>

<summary>

config: object {max\_screenshare\_count, max\_video\_streams, media, 2 more }

</summary>

max\_screenshare\_count: number

Maximum number of screen shares that can be active at a given time

<a href="#">Link to this property</a>

<details>

<summary>

max\_video\_streams: object {desktop, mobile }

Maximum number of streams that are visible on a device

</summary>

desktop: number

Maximum number of video streams visible on desktop devices

<a href="#">Link to this property</a>

mobile: number

Maximum number of streams visible on mobile devices

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

media: object {screenshare, video, audio }

Media configuration options. eg: Video quality

</summary>

<details>

<summary>

screenshare: object {frame\_rate, quality }

Configuration options for participant screen shares

</summary>

frame\_rate: number

Frame rate of screen share

<a href="#">Link to this property</a>

<details>

<summary>

quality: "hd"or "vga"or "qvga"or 2 more

Quality of screen share

</summary>

One of the following:

"hd"

<a href="#">Link to this property</a>

"vga"

<a href="#">Link to this property</a>

"qvga"

<a href="#">Link to this property</a>

"fhd"

<a href="#">Link to this property</a>

"uhd"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video: object {frame\_rate, quality, simulcast }

Configuration options for participant videos

</summary>

frame\_rate: number

Frame rate of participants’ video

maximum30

<a href="#">Link to this property</a>

<details>

<summary>

quality: "hd"or "vga"or "qvga"or 2 more

Video quality of participants

</summary>

One of the following:

"hd"

<a href="#">Link to this property</a>

"vga"

<a href="#">Link to this property</a>

"qvga"

<a href="#">Link to this property</a>

"fhd"

<a href="#">Link to this property</a>

"uhd"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

simulcast: optional boolean

Enable simulcast for participant videos.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

audio: optional object {enable\_high\_bitrate, enable\_stereo }

Control options for Audio quality.

</summary>

enable\_high\_bitrate: optional boolean

Enable High Quality Audio for your meetings

<a href="#">Link to this property</a>

enable\_stereo: optional boolean

Enable Stereo for your meetings

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

view\_type: "GROUP\_CALL"or "WEBINAR"or "AUDIO\_ROOM"or "LIVESTREAM"

Type of the meeting

</summary>

One of the following:

"GROUP\_CALL"

<a href="#">Link to this property</a>

"WEBINAR"

<a href="#">Link to this property</a>

"AUDIO\_ROOM"

<a href="#">Link to this property</a>

"LIVESTREAM"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

livestream\_viewer\_qualities: optional array of number

Livestream viewer quality levels.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: string

Timestamp this preset was created at

formatdate-time

<a href="#">Link to this property</a>

name: string

Name of the preset

<a href="#">Link to this property</a>

<details>

<summary>

permissions: object {accept\_waiting\_requests, can\_accept\_production\_requests, can\_change\_participant\_permissions, 23 more }

</summary>

accept\_waiting\_requests: boolean

Whether this participant can accept waiting requests

<a href="#">Link to this property</a>

can\_accept\_production\_requests: boolean

<a href="#">Link to this property</a>

can\_change\_participant\_permissions: boolean

<a href="#">Link to this property</a>

can\_edit\_display\_name: boolean

<a href="#">Link to this property</a>

can\_livestream: boolean

<a href="#">Link to this property</a>

can\_record: boolean

<a href="#">Link to this property</a>

can\_spotlight: boolean

<a href="#">Link to this property</a>

<details>

<summary>

chat: object {private, public }

</summary>

<details>

<summary>

private: object {can\_receive, can\_send, files, text }

</summary>

can\_receive: boolean

<a href="#">Link to this property</a>

can\_send: boolean

<a href="#">Link to this property</a>

files: boolean

<a href="#">Link to this property</a>

text: boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

public: object {can\_send, files, text }

</summary>

can\_send: boolean

Can send messages in general

<a href="#">Link to this property</a>

files: boolean

Can send file messages

<a href="#">Link to this property</a>

text: boolean

Can send text messages

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

connected\_meetings: object {can\_alter\_connected\_meetings, can\_switch\_connected\_meetings, can\_switch\_to\_parent\_meeting }

</summary>

can\_alter\_connected\_meetings: boolean

<a href="#">Link to this property</a>

can\_switch\_connected\_meetings: boolean

<a href="#">Link to this property</a>

can\_switch\_to\_parent\_meeting: boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

disable\_participant\_audio: boolean

<a href="#">Link to this property</a>

disable\_participant\_screensharing: boolean

<a href="#">Link to this property</a>

disable\_participant\_video: boolean

<a href="#">Link to this property</a>

hidden\_participant: boolean

Whether this participant is visible to others or not

<a href="#">Link to this property</a>

kick\_participant: boolean

<a href="#">Link to this property</a>

<details>

<summary>

media: object {audio, screenshare, video }

Media permissions

</summary>

<details>

<summary>

audio: object {can\_produce }

Audio permissions

</summary>

<details>

<summary>

can\_produce: "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

Can produce audio

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

screenshare: object {can\_produce }

Screenshare permissions

</summary>

<details>

<summary>

can\_produce: "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

Can produce screen share video

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video: object {can\_produce }

Video permissions

</summary>

<details>

<summary>

can\_produce: "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

Can produce video

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

pin\_participant: boolean

<a href="#">Link to this property</a>

<details>

<summary>

plugins: object {can\_close, can\_edit\_config, can\_start, config }

Plugin permissions

</summary>

can\_close: boolean

Can close plugins that are already open

<a href="#">Link to this property</a>

can\_edit\_config: boolean

Can edit plugin config

<a href="#">Link to this property</a>

can\_start: boolean

Can start plugins

<a href="#">Link to this property</a>

<details>

<summary>

config: map\[object {access\_control, handles\_view\_only } ]

Plugin configuration keyed by plugin UUID.

</summary>

<details>

<summary>

access\_control: optional "FULL\_ACCESS"or "VIEW\_ONLY"

</summary>

One of the following:

"FULL\_ACCESS"

<a href="#">Link to this property</a>

"VIEW\_ONLY"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

handles\_view\_only: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

polls: object {can\_create, can\_view, can\_vote }

Poll permissions

</summary>

can\_create: boolean

Can create polls

<a href="#">Link to this property</a>

can\_view: boolean

Can view polls

<a href="#">Link to this property</a>

can\_vote: boolean

Can vote on polls

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

recorder\_type: "RECORDER"or "LIVESTREAMER"or "NONE"

Type of the recording peer

</summary>

One of the following:

"RECORDER"

<a href="#">Link to this property</a>

"LIVESTREAMER"

<a href="#">Link to this property</a>

"NONE"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

show\_participant\_list: boolean

<a href="#">Link to this property</a>

<details>

<summary>

waiting\_room\_type: "SKIP"or "ON\_PRIVILEGED\_USER\_ENTRY"or "SKIP\_ON\_ACCEPT"

Waiting room type

</summary>

One of the following:

"SKIP"

<a href="#">Link to this property</a>

"ON\_PRIVILEGED\_USER\_ENTRY"

<a href="#">Link to this property</a>

"SKIP\_ON\_ACCEPT"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

accept\_stage\_requests: optional boolean

<a href="#">Link to this property</a>

is\_recorder: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

stage\_access: optional "ALLOWED"or "NOT\_ALLOWED"or "CAN\_REQUEST"

</summary>

One of the following:

"ALLOWED"

<a href="#">Link to this property</a>

"NOT\_ALLOWED"

<a href="#">Link to this property</a>

"CAN\_REQUEST"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

stage\_enabled: optional boolean

<a href="#">Link to this property</a>

transcription\_enabled: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ui: object {design\_tokens }

</summary>

<details>

<summary>

design\_tokens: object {border\_radius, border\_width, colors, 5 more }

</summary>

<details>

<summary>

border\_radius: "sharp"or "rounded"or "extra-rounded"or "circular"

</summary>

One of the following:

"sharp"

<a href="#">Link to this property</a>

"rounded"

<a href="#">Link to this property</a>

"extra-rounded"

<a href="#">Link to this property</a>

"circular"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

border\_width: "none"or "thin"or "fat"

</summary>

One of the following:

"none"

<a href="#">Link to this property</a>

"thin"

<a href="#">Link to this property</a>

"fat"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

colors: object {background, brand, danger, 5 more }

</summary>

<details>

<summary>

background: object {"1000", "600", "700", 2 more }

</summary>

"1000": string

<a href="#">Link to this property</a>

"600": string

<a href="#">Link to this property</a>

"700": string

<a href="#">Link to this property</a>

"800": string

<a href="#">Link to this property</a>

"900": string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

brand: object {"300", "400", "500", 2 more }

</summary>

"300": string

<a href="#">Link to this property</a>

"400": string

<a href="#">Link to this property</a>

"500": string

<a href="#">Link to this property</a>

"600": string

<a href="#">Link to this property</a>

"700": string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

danger: string

<a href="#">Link to this property</a>

success: string

<a href="#">Link to this property</a>

text: string

<a href="#">Link to this property</a>

text\_on\_brand: string

<a href="#">Link to this property</a>

video\_bg: string

<a href="#">Link to this property</a>

warning: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

spacing\_base: number

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

theme: "darkest"or "dark"or "light"

</summary>

One of the following:

"darkest"

<a href="#">Link to this property</a>

"dark"

<a href="#">Link to this property</a>

"light"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

font\_family: optional string

<a href="#">Link to this property</a>

google\_font: optional string

<a href="#">Link to this property</a>

logo: optional string

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

Timestamp this preset was last updated

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

success: boolean

Success status of the operation

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.presets%20%3E%20(model)%20preset_replace_preset_by_id_response%20%3E%20(schema)>)

#### Realtime KitSessions

##### [Fetch all sessions of an App](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/sessions/methods/get_sessions)

GET/accounts/{account\_id}/realtime/kit/{app\_id}/sessions

##### [Fetch details of a session](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/sessions/methods/get_session_details)

GET/accounts/{account\_id}/realtime/kit/{app\_id}/sessions/{session\_id}

##### [Fetch participants list of a session](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/sessions/methods/get_session_participants)

GET/accounts/{account\_id}/realtime/kit/{app\_id}/sessions/{session\_id}/participants

##### [Fetch details of a participant](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/sessions/methods/get_session_participant_details)

GET/accounts/{account\_id}/realtime/kit/{app\_id}/sessions/{session\_id}/participants/{participant\_id}

##### [Fetch all chat messages of a session](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/sessions/methods/get_session_chat)

GET/accounts/{account\_id}/realtime/kit/{app\_id}/sessions/{session\_id}/chat

##### [Fetch the complete transcript for a session](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/sessions/methods/get_session_transcripts)

GET/accounts/{account\_id}/realtime/kit/{app\_id}/sessions/{session\_id}/transcript

##### [Fetch summary of transcripts for a session](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/sessions/methods/get_session_summary)

GET/accounts/{account\_id}/realtime/kit/{app\_id}/sessions/{session\_id}/summary

##### [Generate summary of Transcripts for the session](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/sessions/methods/generate_summary_of_transcripts)

POST/accounts/{account\_id}/realtime/kit/{app\_id}/sessions/{session\_id}/summary

##### [Fetch details of peer](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/sessions/methods/get_participant_data_from_peer_id)

GET/accounts/{account\_id}/realtime/kit/{app\_id}/sessions/peer-report/{peer\_id}

##### ModelsExpand Collapse

<details>

<summary>

SessionGetSessionsResponse object {data, paging, success }

</summary>

<details>

<summary>

data: optional object {sessions }

</summary>

<details>

<summary>

sessions: optional array of object {id, associated\_id, created\_at, 11 more }

</summary>

id: string

ID of the session

<a href="#">Link to this property</a>

associated\_id: string

ID of the meeting this session is associated with. In the case of V2 meetings, it is always a UUID. In V1 meetings, it is a room name of the form <code>abcdef-ghijkl</code>

<a href="#">Link to this property</a>

created\_at: string

timestamp when session created

<a href="#">Link to this property</a>

live\_participants: number

number of participants currently in the session

<a href="#">Link to this property</a>

max\_concurrent\_participants: number

number of maximum participants that were in the session

<a href="#">Link to this property</a>

meeting\_display\_name: string

Title of the meeting this session belongs to

<a href="#">Link to this property</a>

minutes\_consumed: number

number of minutes consumed since the session started

<a href="#">Link to this property</a>

organization\_id: string

App id that hosted this session

<a href="#">Link to this property</a>

started\_at: string

timestamp when session started

<a href="#">Link to this property</a>

<details>

<summary>

status: "LIVE"or "ENDED"

current status of session

</summary>

One of the following:

"LIVE"

<a href="#">Link to this property</a>

"ENDED"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

type: "meeting"or "livestream"or "participant"

type of session

</summary>

One of the following:

"meeting"

<a href="#">Link to this property</a>

"livestream"

<a href="#">Link to this property</a>

"participant"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

timestamp when session was last updated

<a href="#">Link to this property</a>

breakout\_rooms: optional array of unknown

<a href="#">Link to this property</a>

ended\_at: optional string

timestamp when session ended

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

paging: optional object {end\_offset, start\_offset, total\_count }

</summary>

end\_offset: optional number

<a href="#">Link to this property</a>

start\_offset: optional number

<a href="#">Link to this property</a>

total\_count: optional number

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

success: optional boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.sessions%20%3E%20(model)%20session_get_sessions_response%20%3E%20(schema)>)

<details>

<summary>

SessionGetSessionDetailsResponse object {data, success }

</summary>

<details>

<summary>

data: optional object {id, associated\_id, created\_at, 11 more }

</summary>

id: string

ID of the session

<a href="#">Link to this property</a>

associated\_id: string

ID of the meeting this session is associated with. In the case of V2 meetings, it is always a UUID. In V1 meetings, it is a room name of the form <code>abcdef-ghijkl</code>

<a href="#">Link to this property</a>

created\_at: string

timestamp when session created

<a href="#">Link to this property</a>

live\_participants: number

number of participants currently in the session

<a href="#">Link to this property</a>

max\_concurrent\_participants: number

number of maximum participants that were in the session

<a href="#">Link to this property</a>

meeting\_display\_name: string

Title of the meeting this session belongs to

<a href="#">Link to this property</a>

minutes\_consumed: number

number of minutes consumed since the session started

<a href="#">Link to this property</a>

organization\_id: string

App id that hosted this session

<a href="#">Link to this property</a>

started\_at: string

timestamp when session started

<a href="#">Link to this property</a>

<details>

<summary>

status: "LIVE"or "ENDED"

current status of session

</summary>

One of the following:

"LIVE"

<a href="#">Link to this property</a>

"ENDED"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

type: "meeting"or "livestream"or "participant"

type of session

</summary>

One of the following:

"meeting"

<a href="#">Link to this property</a>

"livestream"

<a href="#">Link to this property</a>

"participant"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

timestamp when session was last updated

<a href="#">Link to this property</a>

breakout\_rooms: optional array of unknown

<a href="#">Link to this property</a>

ended\_at: optional string

timestamp when session ended

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

success: optional boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.sessions%20%3E%20(model)%20session_get_session_details_response%20%3E%20(schema)>)

<details>

<summary>

SessionGetSessionParticipantsResponse object {data, success }

</summary>

<details>

<summary>

data: optional object {participants }

</summary>

<details>

<summary>

participants: optional array of object {id, created\_at, custom\_participant\_id, 8 more }

</summary>

id: optional string

Participant ID. This maps to the corresponding peerId.

<a href="#">Link to this property</a>

created\_at: optional string

timestamp when this participant was created.

<a href="#">Link to this property</a>

custom\_participant\_id: optional string

ID passed by client to create this participant.

<a href="#">Link to this property</a>

display\_name: optional string

Display name of participant when joining the session.

<a href="#">Link to this property</a>

duration: optional number

number of minutes for which the participant was in the session.

<a href="#">Link to this property</a>

joined\_at: optional string

timestamp at which participant joined the session.

<a href="#">Link to this property</a>

left\_at: optional string

timestamp at which participant left the session.

<a href="#">Link to this property</a>

<details>

<summary>

peer\_events: optional array of object {id, created\_at, event\_name, 7 more }

Connection lifecycle events for the participant’s peer. Only included when <code>include_peer_events</code> is true.

</summary>

id: optional string

ID of the peer event.

<a href="#">Link to this property</a>

created\_at: optional string

Timestamp when this peer event was created.

<a href="#">Link to this property</a>

<details>

<summary>

event\_name: optional "PEER\_CREATED"or "PEER\_JOINING"or "PEER\_LEAVING"

Name of the peer event.

</summary>

One of the following:

"PEER\_CREATED"

<a href="#">Link to this property</a>

"PEER\_JOINING"

<a href="#">Link to this property</a>

"PEER\_LEAVING"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

minutes\_consumed: optional number

Minutes consumed attributed to this event.

<a href="#">Link to this property</a>

participant\_id: optional string

ID of the participant this event belongs to.

<a href="#">Link to this property</a>

peer\_id: optional string

Peer ID this event belongs to.

<a href="#">Link to this property</a>

<details>

<summary>

preset\_view\_type: optional "GROUP\_CALL"or "WEBINAR"or "AUDIO\_ROOM"or 2 more

View type of the preset associated with the peer.

</summary>

One of the following:

"GROUP\_CALL"

<a href="#">Link to this property</a>

"WEBINAR"

<a href="#">Link to this property</a>

"AUDIO\_ROOM"

<a href="#">Link to this property</a>

"LIVESTREAM"

<a href="#">Link to this property</a>

"CHAT"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

session\_id: optional string

ID of the session this event belongs to.

<a href="#">Link to this property</a>

socket\_session\_id: optional string

ID of the socket session associated with this event.

<a href="#">Link to this property</a>

updated\_at: optional string

Timestamp when this peer event was last updated.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

preset\_name: optional string

Name of the preset associated with the participant.

<a href="#">Link to this property</a>

updated\_at: optional string

timestamp when this participant’s data was last updated.

<a href="#">Link to this property</a>

user\_id: optional string

User id for this participant.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

success: optional boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.sessions%20%3E%20(model)%20session_get_session_participants_response%20%3E%20(schema)>)

<details>

<summary>

SessionGetSessionParticipantDetailsResponse object {data, success }

</summary>

<details>

<summary>

data: optional object {participant }

</summary>

<details>

<summary>

participant: optional object {id, created\_at, custom\_participant\_id, 8 more }

</summary>

id: optional string

Participant ID. This maps to the corresponding peerId.

<a href="#">Link to this property</a>

created\_at: optional string

timestamp when this participant was created.

<a href="#">Link to this property</a>

custom\_participant\_id: optional string

ID passed by client to create this participant.

<a href="#">Link to this property</a>

display\_name: optional string

Display name of participant when joining the session.

<a href="#">Link to this property</a>

duration: optional number

number of minutes for which the participant was in the session.

<a href="#">Link to this property</a>

joined\_at: optional string

timestamp at which participant joined the session.

<a href="#">Link to this property</a>

left\_at: optional string

timestamp at which participant left the session.

<a href="#">Link to this property</a>

<details>

<summary>

peer\_events: optional array of object {id, created\_at, event\_name, 7 more }

Connection lifecycle events for the participant’s peer. Only included when <code>include_peer_events</code> is true.

</summary>

id: optional string

ID of the peer event.

<a href="#">Link to this property</a>

created\_at: optional string

Timestamp when this peer event was created.

<a href="#">Link to this property</a>

<details>

<summary>

event\_name: optional "PEER\_CREATED"or "PEER\_JOINING"or "PEER\_LEAVING"

Name of the peer event.

</summary>

One of the following:

"PEER\_CREATED"

<a href="#">Link to this property</a>

"PEER\_JOINING"

<a href="#">Link to this property</a>

"PEER\_LEAVING"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

minutes\_consumed: optional number

Minutes consumed attributed to this event.

<a href="#">Link to this property</a>

participant\_id: optional string

ID of the participant this event belongs to.

<a href="#">Link to this property</a>

peer\_id: optional string

Peer ID this event belongs to.

<a href="#">Link to this property</a>

<details>

<summary>

preset\_view\_type: optional "GROUP\_CALL"or "WEBINAR"or "AUDIO\_ROOM"or 2 more

View type of the preset associated with the peer.

</summary>

One of the following:

"GROUP\_CALL"

<a href="#">Link to this property</a>

"WEBINAR"

<a href="#">Link to this property</a>

"AUDIO\_ROOM"

<a href="#">Link to this property</a>

"LIVESTREAM"

<a href="#">Link to this property</a>

"CHAT"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

session\_id: optional string

ID of the session this event belongs to.

<a href="#">Link to this property</a>

socket\_session\_id: optional string

ID of the socket session associated with this event.

<a href="#">Link to this property</a>

updated\_at: optional string

Timestamp when this peer event was last updated.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

preset\_name: optional string

Name of the preset associated with the participant.

<a href="#">Link to this property</a>

updated\_at: optional string

timestamp when this participant’s data was last updated.

<a href="#">Link to this property</a>

user\_id: optional string

User id for this participant.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

success: optional boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.sessions%20%3E%20(model)%20session_get_session_participant_details_response%20%3E%20(schema)>)

<details>

<summary>

SessionGetSessionChatResponse object {data, success }

</summary>

<details>

<summary>

data: optional object {chat\_download\_url, chat\_download\_url\_expiry }

</summary>

chat\_download\_url: string

URL where the chat logs can be downloaded

<a href="#">Link to this property</a>

chat\_download\_url\_expiry: string

Time when the download URL will expire

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

success: optional boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.sessions%20%3E%20(model)%20session_get_session_chat_response%20%3E%20(schema)>)

<details>

<summary>

SessionGetSessionTranscriptsResponse object {data, success }

</summary>

<details>

<summary>

data: optional object {sessionId, transcript\_download\_url, transcript\_download\_url\_expiry }

</summary>

sessionId: string

<a href="#">Link to this property</a>

transcript\_download\_url: string

URL where the transcript can be downloaded

<a href="#">Link to this property</a>

transcript\_download\_url\_expiry: string

Time when the download URL will expire

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

success: optional boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.sessions%20%3E%20(model)%20session_get_session_transcripts_response%20%3E%20(schema)>)

<details>

<summary>

SessionGetSessionSummaryResponse object {data, success }

</summary>

<details>

<summary>

data: optional object {sessionId, summaryDownloadUrl, summaryDownloadUrlExpiry }

</summary>

sessionId: string

<a href="#">Link to this property</a>

summaryDownloadUrl: string

URL where the summary of transcripts can be downloaded

<a href="#">Link to this property</a>

summaryDownloadUrlExpiry: string

Time of Expiry before when you need to download the csv file.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

success: optional boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.sessions%20%3E%20(model)%20session_get_session_summary_response%20%3E%20(schema)>)

<details>

<summary>

SessionGenerateSummaryOfTranscriptsResponse object {data, success }

</summary>

<details>

<summary>

data: optional object {session\_id, status }

</summary>

session\_id: optional string

formatuuid

<a href="#">Link to this property</a>

status: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

success: optional boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.sessions%20%3E%20(model)%20session_generate_summary_of_transcripts_response%20%3E%20(schema)>)

<details>

<summary>

SessionGetParticipantDataFromPeerIDResponse object {data, success }

</summary>

<details>

<summary>

data: optional object {participant }

</summary>

<details>

<summary>

participant: optional object {id, created\_at, custom\_participant\_id, 10 more }

</summary>

id: optional string

ID of the participant.

formatuuid

<a href="#">Link to this property</a>

created\_at: optional string

timestamp when this participant was created.

<a href="#">Link to this property</a>

custom\_participant\_id: optional string

ID passed by client to create this participant.

<a href="#">Link to this property</a>

display\_name: optional string

Display name of participant when joining the session.

<a href="#">Link to this property</a>

duration: optional number

number of minutes for which the participant was in the session.

<a href="#">Link to this property</a>

joined\_at: optional string

timestamp at which participant joined the session.

<a href="#">Link to this property</a>

left\_at: optional string

timestamp at which participant left the session.

<a href="#">Link to this property</a>

<details>

<summary>

peer\_events: optional array of object {id, created\_at, event\_name, 7 more }

Connection lifecycle events for the participant’s peer.

</summary>

id: optional string

ID of the peer event.

<a href="#">Link to this property</a>

created\_at: optional string

Timestamp when this peer event was created.

<a href="#">Link to this property</a>

<details>

<summary>

event\_name: optional "PEER\_CREATED"or "PEER\_JOINING"or "PEER\_LEAVING"

Name of the peer event.

</summary>

One of the following:

"PEER\_CREATED"

<a href="#">Link to this property</a>

"PEER\_JOINING"

<a href="#">Link to this property</a>

"PEER\_LEAVING"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

minutes\_consumed: optional number

Minutes consumed attributed to this event.

<a href="#">Link to this property</a>

participant\_id: optional string

ID of the participant this event belongs to.

<a href="#">Link to this property</a>

peer\_id: optional string

Peer ID this event belongs to.

<a href="#">Link to this property</a>

<details>

<summary>

preset\_view\_type: optional "GROUP\_CALL"or "WEBINAR"or "AUDIO\_ROOM"or 2 more

View type of the preset associated with the peer.

</summary>

One of the following:

"GROUP\_CALL"

<a href="#">Link to this property</a>

"WEBINAR"

<a href="#">Link to this property</a>

"AUDIO\_ROOM"

<a href="#">Link to this property</a>

"LIVESTREAM"

<a href="#">Link to this property</a>

"CHAT"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

session\_id: optional string

ID of the session this event belongs to.

<a href="#">Link to this property</a>

socket\_session\_id: optional string

ID of the socket session associated with this event.

<a href="#">Link to this property</a>

updated\_at: optional string

Timestamp when this peer event was last updated.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

peer\_report: optional object {metadata, quality }

Peer call statistics report.

</summary>

<details>

<summary>

metadata: optional object {audio\_devices\_updates, browser\_metadata, candidate\_pairs, 12 more }

Connection and device metadata for the participant.

</summary>

<details>

<summary>

audio\_devices\_updates: optional array of object {added, removed, timestamp }

</summary>

<details>

<summary>

added: optional array of object {device\_id, kind, label }

Devices that became available.

</summary>

device\_id: optional string

ID of the device.

<a href="#">Link to this property</a>

kind: optional string

Kind of device, for example audioinput or videoinput.

<a href="#">Link to this property</a>

label: optional string

Human-readable label of the device.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

removed: optional array of object {device\_id, kind, label }

Devices that became unavailable.

</summary>

device\_id: optional string

ID of the device.

<a href="#">Link to this property</a>

kind: optional string

Kind of device, for example audioinput or videoinput.

<a href="#">Link to this property</a>

label: optional string

Human-readable label of the device.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

timestamp: optional string

Timestamp of the device update.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

browser\_metadata: optional object {browser, browser\_version, engine, 2 more }

</summary>

browser: optional string

<a href="#">Link to this property</a>

browser\_version: optional string

<a href="#">Link to this property</a>

engine: optional string

<a href="#">Link to this property</a>

user\_agent: optional string

<a href="#">Link to this property</a>

webgl\_support: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

candidate\_pairs: optional object {consuming\_transport, producing\_transport }

</summary>

<details>

<summary>

consuming\_transport: optional array of object {available\_incoming\_bitrate, available\_outgoing\_bitrate, bytes\_discarded\_on\_send, 25 more }

</summary>

available\_incoming\_bitrate: optional number

<a href="#">Link to this property</a>

available\_outgoing\_bitrate: optional number

<a href="#">Link to this property</a>

bytes\_discarded\_on\_send: optional number

<a href="#">Link to this property</a>

bytes\_received: optional number

<a href="#">Link to this property</a>

bytes\_sent: optional number

<a href="#">Link to this property</a>

current\_round\_trip\_time: optional number

<a href="#">Link to this property</a>

last\_packet\_received\_timestamp: optional number

Epoch milliseconds when the last packet was received.

<a href="#">Link to this property</a>

last\_packet\_sent\_timestamp: optional number

Epoch milliseconds when the last packet was sent.

<a href="#">Link to this property</a>

local\_candidate\_address: optional string

<a href="#">Link to this property</a>

local\_candidate\_id: optional string

<a href="#">Link to this property</a>

local\_candidate\_network\_type: optional string

<a href="#">Link to this property</a>

local\_candidate\_port: optional number

<a href="#">Link to this property</a>

local\_candidate\_protocol: optional string

<a href="#">Link to this property</a>

local\_candidate\_related\_address: optional string

<a href="#">Link to this property</a>

local\_candidate\_related\_port: optional number

<a href="#">Link to this property</a>

local\_candidate\_type: optional string

<a href="#">Link to this property</a>

local\_candidate\_url: optional string

<a href="#">Link to this property</a>

nominated: optional boolean

<a href="#">Link to this property</a>

packets\_discarded\_on\_send: optional number

<a href="#">Link to this property</a>

packets\_received: optional number

<a href="#">Link to this property</a>

packets\_sent: optional number

<a href="#">Link to this property</a>

remote\_candidate\_address: optional string

<a href="#">Link to this property</a>

remote\_candidate\_id: optional string

<a href="#">Link to this property</a>

remote\_candidate\_port: optional number

<a href="#">Link to this property</a>

remote\_candidate\_protocol: optional string

<a href="#">Link to this property</a>

remote\_candidate\_type: optional string

<a href="#">Link to this property</a>

remote\_candidate\_url: optional string

<a href="#">Link to this property</a>

total\_round\_trip\_time: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

producing\_transport: optional array of object {available\_incoming\_bitrate, available\_outgoing\_bitrate, bytes\_discarded\_on\_send, 25 more }

</summary>

available\_incoming\_bitrate: optional number

<a href="#">Link to this property</a>

available\_outgoing\_bitrate: optional number

<a href="#">Link to this property</a>

bytes\_discarded\_on\_send: optional number

<a href="#">Link to this property</a>

bytes\_received: optional number

<a href="#">Link to this property</a>

bytes\_sent: optional number

<a href="#">Link to this property</a>

current\_round\_trip\_time: optional number

<a href="#">Link to this property</a>

last\_packet\_received\_timestamp: optional number

Epoch milliseconds when the last packet was received.

<a href="#">Link to this property</a>

last\_packet\_sent\_timestamp: optional number

Epoch milliseconds when the last packet was sent.

<a href="#">Link to this property</a>

local\_candidate\_address: optional string

<a href="#">Link to this property</a>

local\_candidate\_id: optional string

<a href="#">Link to this property</a>

local\_candidate\_network\_type: optional string

<a href="#">Link to this property</a>

local\_candidate\_port: optional number

<a href="#">Link to this property</a>

local\_candidate\_protocol: optional string

<a href="#">Link to this property</a>

local\_candidate\_related\_address: optional string

<a href="#">Link to this property</a>

local\_candidate\_related\_port: optional number

<a href="#">Link to this property</a>

local\_candidate\_type: optional string

<a href="#">Link to this property</a>

local\_candidate\_url: optional string

<a href="#">Link to this property</a>

nominated: optional boolean

<a href="#">Link to this property</a>

packets\_discarded\_on\_send: optional number

<a href="#">Link to this property</a>

packets\_received: optional number

<a href="#">Link to this property</a>

packets\_sent: optional number

<a href="#">Link to this property</a>

remote\_candidate\_address: optional string

<a href="#">Link to this property</a>

remote\_candidate\_id: optional string

<a href="#">Link to this property</a>

remote\_candidate\_port: optional number

<a href="#">Link to this property</a>

remote\_candidate\_protocol: optional string

<a href="#">Link to this property</a>

remote\_candidate\_type: optional string

<a href="#">Link to this property</a>

remote\_candidate\_url: optional string

<a href="#">Link to this property</a>

total\_round\_trip\_time: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

device\_info: optional object {cpus, is\_mobile, os, os\_version }

</summary>

cpus: optional number

<a href="#">Link to this property</a>

is\_mobile: optional boolean

<a href="#">Link to this property</a>

os: optional string

<a href="#">Link to this property</a>

os\_version: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

events: optional array of object {metadata, name, timestamp }

</summary>

<details>

<summary>

metadata: optional map\[stringor numberor boolean]

Event-specific metadata. Keys vary per event; values are primitive scalars (string, number, boolean, or null).

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: optional string

Name of the event.

<a href="#">Link to this property</a>

timestamp: optional string

Timestamp when the event occurred.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ip\_information: optional object {asn, city, country, 4 more }

</summary>

<details>

<summary>

asn: optional object {asn, domain, name, 2 more }

</summary>

asn: optional string

<a href="#">Link to this property</a>

domain: optional string

<a href="#">Link to this property</a>

name: optional string

<a href="#">Link to this property</a>

route: optional string

<a href="#">Link to this property</a>

type: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

city: optional string

<a href="#">Link to this property</a>

country: optional string

<a href="#">Link to this property</a>

ipv4: optional string

<a href="#">Link to this property</a>

org: optional string

<a href="#">Link to this property</a>

region: optional string

<a href="#">Link to this property</a>

timezone: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

native\_metadata: optional object {audio\_encoder, video\_encoder }

</summary>

audio\_encoder: optional string

<a href="#">Link to this property</a>

video\_encoder: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

pc\_metadata: optional array of object {effective\_network\_type, reflexive\_connectivity, relay\_connectivity, 3 more }

</summary>

effective\_network\_type: optional string

<a href="#">Link to this property</a>

reflexive\_connectivity: optional boolean

<a href="#">Link to this property</a>

relay\_connectivity: optional boolean

<a href="#">Link to this property</a>

sdp: optional array of string

<a href="#">Link to this property</a>

timestamp: optional string

<a href="#">Link to this property</a>

turn\_connectivity: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

room\_view\_type: optional string

<a href="#">Link to this property</a>

sdk\_name: optional string

<a href="#">Link to this property</a>

sdk\_type: optional string

<a href="#">Link to this property</a>

sdk\_version: optional string

<a href="#">Link to this property</a>

<details>

<summary>

selected\_device\_updates: optional array of object {device, timestamp }

</summary>

<details>

<summary>

device: optional object {device\_id, kind, label }

A media device (camera, microphone, or speaker).

</summary>

device\_id: optional string

ID of the device.

<a href="#">Link to this property</a>

kind: optional string

Kind of device, for example audioinput or videoinput.

<a href="#">Link to this property</a>

label: optional string

Human-readable label of the device.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

timestamp: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

speaker\_devices\_updates: optional array of object {added, removed, timestamp }

</summary>

<details>

<summary>

added: optional array of object {device\_id, kind, label }

Devices that became available.

</summary>

device\_id: optional string

ID of the device.

<a href="#">Link to this property</a>

kind: optional string

Kind of device, for example audioinput or videoinput.

<a href="#">Link to this property</a>

label: optional string

Human-readable label of the device.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

removed: optional array of object {device\_id, kind, label }

Devices that became unavailable.

</summary>

device\_id: optional string

ID of the device.

<a href="#">Link to this property</a>

kind: optional string

Kind of device, for example audioinput or videoinput.

<a href="#">Link to this property</a>

label: optional string

Human-readable label of the device.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

timestamp: optional string

Timestamp of the device update.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video\_devices\_updates: optional array of object {added, removed, timestamp }

</summary>

<details>

<summary>

added: optional array of object {device\_id, kind, label }

Devices that became available.

</summary>

device\_id: optional string

ID of the device.

<a href="#">Link to this property</a>

kind: optional string

Kind of device, for example audioinput or videoinput.

<a href="#">Link to this property</a>

label: optional string

Human-readable label of the device.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

removed: optional array of object {device\_id, kind, label }

Devices that became unavailable.

</summary>

device\_id: optional string

ID of the device.

<a href="#">Link to this property</a>

kind: optional string

Kind of device, for example audioinput or videoinput.

<a href="#">Link to this property</a>

label: optional string

Human-readable label of the device.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

timestamp: optional string

Timestamp of the device update.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

quality: optional object {audio\_consumer, audio\_consumer\_cumulative, audio\_producer, 13 more }

Media quality statistics for the participant.

</summary>

<details>

<summary>

audio\_consumer: optional array of object {bytes\_received, concealment\_events, consumer\_id, 11 more }

</summary>

bytes\_received: optional number

<a href="#">Link to this property</a>

concealment\_events: optional number

<a href="#">Link to this property</a>

consumer\_id: optional string

<a href="#">Link to this property</a>

jitter: optional number

<a href="#">Link to this property</a>

jitter\_buffer\_delay: optional number

<a href="#">Link to this property</a>

jitter\_buffer\_emitted\_count: optional number

<a href="#">Link to this property</a>

mid: optional string

<a href="#">Link to this property</a>

mos\_quality: optional number

<a href="#">Link to this property</a>

packets\_lost: optional number

<a href="#">Link to this property</a>

packets\_received: optional number

<a href="#">Link to this property</a>

peer\_id: optional string

<a href="#">Link to this property</a>

producer\_id: optional string

<a href="#">Link to this property</a>

ssrc: optional number

<a href="#">Link to this property</a>

timestamp: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

audio\_consumer\_cumulative: optional object {jitter\_buffer\_delay, packet\_loss, quality\_mos }

Aggregated inbound (consumer) audio statistics for the session.

</summary>

<details>

<summary>

jitter\_buffer\_delay: optional object {"100ms\_or\_greater\_event\_fraction", "250ms\_or\_greater\_event\_fraction", "500ms\_or\_greater\_event\_fraction", avg }

Cumulative latency distribution (milliseconds-based thresholds).

</summary>

"100ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"250ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"500ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

avg: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

packet\_loss: optional object {"10\_or\_greater\_event\_fraction", "25\_or\_greater\_event\_fraction", "5\_or\_greater\_event\_fraction", 2 more }

Cumulative packet loss distribution.

</summary>

"10\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"25\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"5\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"50\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

avg: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

quality\_mos: optional object {avg, p50, p75, p90 }

Distribution summary with average and percentiles.

</summary>

avg: optional number

<a href="#">Link to this property</a>

p50: optional number

<a href="#">Link to this property</a>

p75: optional number

<a href="#">Link to this property</a>

p90: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

audio\_producer: optional array of object {bytes\_sent, jitter, mid, 7 more }

</summary>

bytes\_sent: optional number

<a href="#">Link to this property</a>

jitter: optional number

<a href="#">Link to this property</a>

mid: optional string

<a href="#">Link to this property</a>

mos\_quality: optional number

<a href="#">Link to this property</a>

packets\_lost: optional number

<a href="#">Link to this property</a>

packets\_sent: optional number

<a href="#">Link to this property</a>

producer\_id: optional string

<a href="#">Link to this property</a>

rtt: optional number

<a href="#">Link to this property</a>

ssrc: optional number

<a href="#">Link to this property</a>

timestamp: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

audio\_producer\_cumulative: optional object {packet\_loss, quality\_mos, rtt }

Aggregated outbound (producer) audio statistics for the session.

</summary>

<details>

<summary>

packet\_loss: optional object {"10\_or\_greater\_event\_fraction", "25\_or\_greater\_event\_fraction", "5\_or\_greater\_event\_fraction", 2 more }

Cumulative packet loss distribution.

</summary>

"10\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"25\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"5\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"50\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

avg: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

quality\_mos: optional object {avg, p50, p75, p90 }

Distribution summary with average and percentiles.

</summary>

avg: optional number

<a href="#">Link to this property</a>

p50: optional number

<a href="#">Link to this property</a>

p75: optional number

<a href="#">Link to this property</a>

p90: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

rtt: optional object {"100ms\_or\_greater\_event\_fraction", "250ms\_or\_greater\_event\_fraction", "500ms\_or\_greater\_event\_fraction", avg }

Cumulative latency distribution (milliseconds-based thresholds).

</summary>

"100ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"250ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"500ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

avg: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

screenshare\_audio\_consumer: optional array of object {bytes\_received, concealment\_events, consumer\_id, 11 more }

</summary>

bytes\_received: optional number

<a href="#">Link to this property</a>

concealment\_events: optional number

<a href="#">Link to this property</a>

consumer\_id: optional string

<a href="#">Link to this property</a>

jitter: optional number

<a href="#">Link to this property</a>

jitter\_buffer\_delay: optional number

<a href="#">Link to this property</a>

jitter\_buffer\_emitted\_count: optional number

<a href="#">Link to this property</a>

mid: optional string

<a href="#">Link to this property</a>

mos\_quality: optional number

<a href="#">Link to this property</a>

packets\_lost: optional number

<a href="#">Link to this property</a>

packets\_received: optional number

<a href="#">Link to this property</a>

peer\_id: optional string

<a href="#">Link to this property</a>

producer\_id: optional string

<a href="#">Link to this property</a>

ssrc: optional number

<a href="#">Link to this property</a>

timestamp: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

screenshare\_audio\_consumer\_cumulative: optional object {jitter\_buffer\_delay, packet\_loss, quality\_mos }

Aggregated inbound (consumer) audio statistics for the session.

</summary>

<details>

<summary>

jitter\_buffer\_delay: optional object {"100ms\_or\_greater\_event\_fraction", "250ms\_or\_greater\_event\_fraction", "500ms\_or\_greater\_event\_fraction", avg }

Cumulative latency distribution (milliseconds-based thresholds).

</summary>

"100ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"250ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"500ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

avg: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

packet\_loss: optional object {"10\_or\_greater\_event\_fraction", "25\_or\_greater\_event\_fraction", "5\_or\_greater\_event\_fraction", 2 more }

Cumulative packet loss distribution.

</summary>

"10\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"25\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"5\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"50\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

avg: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

quality\_mos: optional object {avg, p50, p75, p90 }

Distribution summary with average and percentiles.

</summary>

avg: optional number

<a href="#">Link to this property</a>

p50: optional number

<a href="#">Link to this property</a>

p75: optional number

<a href="#">Link to this property</a>

p90: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

screenshare\_audio\_producer: optional array of object {bytes\_sent, jitter, mid, 7 more }

</summary>

bytes\_sent: optional number

<a href="#">Link to this property</a>

jitter: optional number

<a href="#">Link to this property</a>

mid: optional string

<a href="#">Link to this property</a>

mos\_quality: optional number

<a href="#">Link to this property</a>

packets\_lost: optional number

<a href="#">Link to this property</a>

packets\_sent: optional number

<a href="#">Link to this property</a>

producer\_id: optional string

<a href="#">Link to this property</a>

rtt: optional number

<a href="#">Link to this property</a>

ssrc: optional number

<a href="#">Link to this property</a>

timestamp: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

screenshare\_audio\_producer\_cumulative: optional object {packet\_loss, quality\_mos, rtt }

Aggregated outbound (producer) audio statistics for the session.

</summary>

<details>

<summary>

packet\_loss: optional object {"10\_or\_greater\_event\_fraction", "25\_or\_greater\_event\_fraction", "5\_or\_greater\_event\_fraction", 2 more }

Cumulative packet loss distribution.

</summary>

"10\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"25\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"5\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"50\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

avg: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

quality\_mos: optional object {avg, p50, p75, p90 }

Distribution summary with average and percentiles.

</summary>

avg: optional number

<a href="#">Link to this property</a>

p50: optional number

<a href="#">Link to this property</a>

p75: optional number

<a href="#">Link to this property</a>

p90: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

rtt: optional object {"100ms\_or\_greater\_event\_fraction", "250ms\_or\_greater\_event\_fraction", "500ms\_or\_greater\_event\_fraction", avg }

Cumulative latency distribution (milliseconds-based thresholds).

</summary>

"100ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"250ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"500ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

avg: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

screenshare\_video\_consumer: optional array of object {bytes\_received, consumer\_id, fir\_count, 17 more }

</summary>

bytes\_received: optional number

<a href="#">Link to this property</a>

consumer\_id: optional string

<a href="#">Link to this property</a>

fir\_count: optional number

<a href="#">Link to this property</a>

frame\_height: optional number

<a href="#">Link to this property</a>

frame\_width: optional number

<a href="#">Link to this property</a>

frames\_decoded: optional number

<a href="#">Link to this property</a>

frames\_dropped: optional number

<a href="#">Link to this property</a>

frames\_per\_second: optional number

<a href="#">Link to this property</a>

jitter: optional number

<a href="#">Link to this property</a>

jitter\_buffer\_delay: optional number

<a href="#">Link to this property</a>

jitter\_buffer\_emitted\_count: optional number

<a href="#">Link to this property</a>

key\_frames\_decoded: optional number

<a href="#">Link to this property</a>

mid: optional string

<a href="#">Link to this property</a>

mos\_quality: optional number

<a href="#">Link to this property</a>

packets\_lost: optional number

<a href="#">Link to this property</a>

packets\_received: optional number

<a href="#">Link to this property</a>

peer\_id: optional string

<a href="#">Link to this property</a>

producer\_id: optional string

<a href="#">Link to this property</a>

ssrc: optional number

<a href="#">Link to this property</a>

timestamp: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

screenshare\_video\_consumer\_cumulative: optional object {frame\_per\_second, frame\_width, issues, 4 more }

Aggregated inbound (consumer) video statistics for the session.

</summary>

<details>

<summary>

frame\_per\_second: optional object {avg, p50, p75, p90 }

Distribution summary with average and percentiles.

</summary>

avg: optional number

<a href="#">Link to this property</a>

p50: optional number

<a href="#">Link to this property</a>

p75: optional number

<a href="#">Link to this property</a>

p90: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

frame\_width: optional object {avg, p50, p75, p90 }

Distribution summary with average and percentiles.

</summary>

avg: optional number

<a href="#">Link to this property</a>

p50: optional number

<a href="#">Link to this property</a>

p75: optional number

<a href="#">Link to this property</a>

p90: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

issues: optional object {lag\_fraction, no\_video\_fraction, poor\_resolution\_fraction }

</summary>

lag\_fraction: optional number

<a href="#">Link to this property</a>

no\_video\_fraction: optional number

<a href="#">Link to this property</a>

poor\_resolution\_fraction: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

jitter\_buffer\_delay: optional object {"100ms\_or\_greater\_event\_fraction", "250ms\_or\_greater\_event\_fraction", "500ms\_or\_greater\_event\_fraction", avg }

Cumulative latency distribution (milliseconds-based thresholds).

</summary>

"100ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"250ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"500ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

avg: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

key\_frames\_decoded\_fraction: optional number

<a href="#">Link to this property</a>

<details>

<summary>

packet\_loss: optional object {"10\_or\_greater\_event\_fraction", "25\_or\_greater\_event\_fraction", "5\_or\_greater\_event\_fraction", 2 more }

Cumulative packet loss distribution.

</summary>

"10\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"25\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"5\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"50\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

avg: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

quality\_mos: optional object {avg, p50, p75, p90 }

Distribution summary with average and percentiles.

</summary>

avg: optional number

<a href="#">Link to this property</a>

p50: optional number

<a href="#">Link to this property</a>

p75: optional number

<a href="#">Link to this property</a>

p90: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

screenshare\_video\_producer: optional array of object {bytes\_sent, fir\_count, frame\_height, 17 more }

</summary>

bytes\_sent: optional number

<a href="#">Link to this property</a>

fir\_count: optional number

<a href="#">Link to this property</a>

frame\_height: optional number

<a href="#">Link to this property</a>

frame\_width: optional number

<a href="#">Link to this property</a>

frames\_encoded: optional number

<a href="#">Link to this property</a>

frames\_per\_second: optional number

<a href="#">Link to this property</a>

jitter: optional number

<a href="#">Link to this property</a>

key\_frames\_encoded: optional number

<a href="#">Link to this property</a>

mid: optional string

<a href="#">Link to this property</a>

mos\_quality: optional number

<a href="#">Link to this property</a>

packets\_lost: optional number

<a href="#">Link to this property</a>

packets\_sent: optional number

<a href="#">Link to this property</a>

pli\_count: optional number

<a href="#">Link to this property</a>

producer\_id: optional string

<a href="#">Link to this property</a>

<details>

<summary>

quality\_limitation\_durations: optional object {bandwidth, cpu, none, other }

</summary>

bandwidth: optional number

<a href="#">Link to this property</a>

cpu: optional number

<a href="#">Link to this property</a>

none: optional number

<a href="#">Link to this property</a>

other: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

quality\_limitation\_reason: optional "cpu"or "bandwidth"or "none"or "other"

</summary>

One of the following:

"cpu"

<a href="#">Link to this property</a>

"bandwidth"

<a href="#">Link to this property</a>

"none"

<a href="#">Link to this property</a>

"other"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

quality\_limitation\_resolution\_changes: optional number

<a href="#">Link to this property</a>

rtt: optional number

<a href="#">Link to this property</a>

ssrc: optional number

<a href="#">Link to this property</a>

timestamp: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

screenshare\_video\_producer\_cumulative: optional object {frame\_per\_second, frame\_width, high\_negative\_feedback\_fraction, 5 more }

Aggregated outbound (producer) video statistics for the session.

</summary>

<details>

<summary>

frame\_per\_second: optional object {avg, p50, p75, p90 }

Distribution summary with average and percentiles.

</summary>

avg: optional number

<a href="#">Link to this property</a>

p50: optional number

<a href="#">Link to this property</a>

p75: optional number

<a href="#">Link to this property</a>

p90: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

frame\_width: optional object {avg, p50, p75, p90 }

Distribution summary with average and percentiles.

</summary>

avg: optional number

<a href="#">Link to this property</a>

p50: optional number

<a href="#">Link to this property</a>

p75: optional number

<a href="#">Link to this property</a>

p90: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

high\_negative\_feedback\_fraction: optional number

<a href="#">Link to this property</a>

<details>

<summary>

issues: optional object {bandwidth\_quality\_limitation\_fraction, cpu\_quality\_limitation\_fraction, no\_video\_fraction, 2 more }

</summary>

bandwidth\_quality\_limitation\_fraction: optional number

<a href="#">Link to this property</a>

cpu\_quality\_limitation\_fraction: optional number

<a href="#">Link to this property</a>

no\_video\_fraction: optional number

<a href="#">Link to this property</a>

poor\_resolution\_fraction: optional number

<a href="#">Link to this property</a>

quality\_limitation\_fraction: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

key\_frames\_encoded\_fraction: optional number

<a href="#">Link to this property</a>

<details>

<summary>

packet\_loss: optional object {"10\_or\_greater\_event\_fraction", "25\_or\_greater\_event\_fraction", "5\_or\_greater\_event\_fraction", 2 more }

Cumulative packet loss distribution.

</summary>

"10\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"25\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"5\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"50\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

avg: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

quality\_mos: optional object {avg, p50, p75, p90 }

Distribution summary with average and percentiles.

</summary>

avg: optional number

<a href="#">Link to this property</a>

p50: optional number

<a href="#">Link to this property</a>

p75: optional number

<a href="#">Link to this property</a>

p90: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

rtt: optional object {"100ms\_or\_greater\_event\_fraction", "250ms\_or\_greater\_event\_fraction", "500ms\_or\_greater\_event\_fraction", avg }

Cumulative latency distribution (milliseconds-based thresholds).

</summary>

"100ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"250ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"500ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

avg: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video\_consumer: optional array of object {bytes\_received, consumer\_id, fir\_count, 17 more }

</summary>

bytes\_received: optional number

<a href="#">Link to this property</a>

consumer\_id: optional string

<a href="#">Link to this property</a>

fir\_count: optional number

<a href="#">Link to this property</a>

frame\_height: optional number

<a href="#">Link to this property</a>

frame\_width: optional number

<a href="#">Link to this property</a>

frames\_decoded: optional number

<a href="#">Link to this property</a>

frames\_dropped: optional number

<a href="#">Link to this property</a>

frames\_per\_second: optional number

<a href="#">Link to this property</a>

jitter: optional number

<a href="#">Link to this property</a>

jitter\_buffer\_delay: optional number

<a href="#">Link to this property</a>

jitter\_buffer\_emitted\_count: optional number

<a href="#">Link to this property</a>

key\_frames\_decoded: optional number

<a href="#">Link to this property</a>

mid: optional string

<a href="#">Link to this property</a>

mos\_quality: optional number

<a href="#">Link to this property</a>

packets\_lost: optional number

<a href="#">Link to this property</a>

packets\_received: optional number

<a href="#">Link to this property</a>

peer\_id: optional string

<a href="#">Link to this property</a>

producer\_id: optional string

<a href="#">Link to this property</a>

ssrc: optional number

<a href="#">Link to this property</a>

timestamp: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video\_consumer\_cumulative: optional object {frame\_per\_second, frame\_width, issues, 4 more }

Aggregated inbound (consumer) video statistics for the session.

</summary>

<details>

<summary>

frame\_per\_second: optional object {avg, p50, p75, p90 }

Distribution summary with average and percentiles.

</summary>

avg: optional number

<a href="#">Link to this property</a>

p50: optional number

<a href="#">Link to this property</a>

p75: optional number

<a href="#">Link to this property</a>

p90: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

frame\_width: optional object {avg, p50, p75, p90 }

Distribution summary with average and percentiles.

</summary>

avg: optional number

<a href="#">Link to this property</a>

p50: optional number

<a href="#">Link to this property</a>

p75: optional number

<a href="#">Link to this property</a>

p90: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

issues: optional object {lag\_fraction, no\_video\_fraction, poor\_resolution\_fraction }

</summary>

lag\_fraction: optional number

<a href="#">Link to this property</a>

no\_video\_fraction: optional number

<a href="#">Link to this property</a>

poor\_resolution\_fraction: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

jitter\_buffer\_delay: optional object {"100ms\_or\_greater\_event\_fraction", "250ms\_or\_greater\_event\_fraction", "500ms\_or\_greater\_event\_fraction", avg }

Cumulative latency distribution (milliseconds-based thresholds).

</summary>

"100ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"250ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"500ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

avg: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

key\_frames\_decoded\_fraction: optional number

<a href="#">Link to this property</a>

<details>

<summary>

packet\_loss: optional object {"10\_or\_greater\_event\_fraction", "25\_or\_greater\_event\_fraction", "5\_or\_greater\_event\_fraction", 2 more }

Cumulative packet loss distribution.

</summary>

"10\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"25\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"5\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"50\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

avg: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

quality\_mos: optional object {avg, p50, p75, p90 }

Distribution summary with average and percentiles.

</summary>

avg: optional number

<a href="#">Link to this property</a>

p50: optional number

<a href="#">Link to this property</a>

p75: optional number

<a href="#">Link to this property</a>

p90: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video\_producer: optional array of object {bytes\_sent, fir\_count, frame\_height, 17 more }

</summary>

bytes\_sent: optional number

<a href="#">Link to this property</a>

fir\_count: optional number

<a href="#">Link to this property</a>

frame\_height: optional number

<a href="#">Link to this property</a>

frame\_width: optional number

<a href="#">Link to this property</a>

frames\_encoded: optional number

<a href="#">Link to this property</a>

frames\_per\_second: optional number

<a href="#">Link to this property</a>

jitter: optional number

<a href="#">Link to this property</a>

key\_frames\_encoded: optional number

<a href="#">Link to this property</a>

mid: optional string

<a href="#">Link to this property</a>

mos\_quality: optional number

<a href="#">Link to this property</a>

packets\_lost: optional number

<a href="#">Link to this property</a>

packets\_sent: optional number

<a href="#">Link to this property</a>

pli\_count: optional number

<a href="#">Link to this property</a>

producer\_id: optional string

<a href="#">Link to this property</a>

<details>

<summary>

quality\_limitation\_durations: optional object {bandwidth, cpu, none, other }

</summary>

bandwidth: optional number

<a href="#">Link to this property</a>

cpu: optional number

<a href="#">Link to this property</a>

none: optional number

<a href="#">Link to this property</a>

other: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

quality\_limitation\_reason: optional "cpu"or "bandwidth"or "none"or "other"

</summary>

One of the following:

"cpu"

<a href="#">Link to this property</a>

"bandwidth"

<a href="#">Link to this property</a>

"none"

<a href="#">Link to this property</a>

"other"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

quality\_limitation\_resolution\_changes: optional number

<a href="#">Link to this property</a>

rtt: optional number

<a href="#">Link to this property</a>

ssrc: optional number

<a href="#">Link to this property</a>

timestamp: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

video\_producer\_cumulative: optional object {frame\_per\_second, frame\_width, high\_negative\_feedback\_fraction, 5 more }

Aggregated outbound (producer) video statistics for the session.

</summary>

<details>

<summary>

frame\_per\_second: optional object {avg, p50, p75, p90 }

Distribution summary with average and percentiles.

</summary>

avg: optional number

<a href="#">Link to this property</a>

p50: optional number

<a href="#">Link to this property</a>

p75: optional number

<a href="#">Link to this property</a>

p90: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

frame\_width: optional object {avg, p50, p75, p90 }

Distribution summary with average and percentiles.

</summary>

avg: optional number

<a href="#">Link to this property</a>

p50: optional number

<a href="#">Link to this property</a>

p75: optional number

<a href="#">Link to this property</a>

p90: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

high\_negative\_feedback\_fraction: optional number

<a href="#">Link to this property</a>

<details>

<summary>

issues: optional object {bandwidth\_quality\_limitation\_fraction, cpu\_quality\_limitation\_fraction, no\_video\_fraction, 2 more }

</summary>

bandwidth\_quality\_limitation\_fraction: optional number

<a href="#">Link to this property</a>

cpu\_quality\_limitation\_fraction: optional number

<a href="#">Link to this property</a>

no\_video\_fraction: optional number

<a href="#">Link to this property</a>

poor\_resolution\_fraction: optional number

<a href="#">Link to this property</a>

quality\_limitation\_fraction: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

key\_frames\_encoded\_fraction: optional number

<a href="#">Link to this property</a>

<details>

<summary>

packet\_loss: optional object {"10\_or\_greater\_event\_fraction", "25\_or\_greater\_event\_fraction", "5\_or\_greater\_event\_fraction", 2 more }

Cumulative packet loss distribution.

</summary>

"10\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"25\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"5\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"50\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

avg: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

quality\_mos: optional object {avg, p50, p75, p90 }

Distribution summary with average and percentiles.

</summary>

avg: optional number

<a href="#">Link to this property</a>

p50: optional number

<a href="#">Link to this property</a>

p75: optional number

<a href="#">Link to this property</a>

p90: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

rtt: optional object {"100ms\_or\_greater\_event\_fraction", "250ms\_or\_greater\_event\_fraction", "500ms\_or\_greater\_event\_fraction", avg }

Cumulative latency distribution (milliseconds-based thresholds).

</summary>

"100ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"250ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

"500ms\_or\_greater\_event\_fraction": optional number

<a href="#">Link to this property</a>

avg: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

role: optional string

Name of the preset associated with the participant.

<a href="#">Link to this property</a>

session\_id: optional string

formatuuid

<a href="#">Link to this property</a>

updated\_at: optional string

timestamp when this participant’s data was last updated.

<a href="#">Link to this property</a>

user\_id: optional string

User id for this participant.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

success: optional boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.sessions%20%3E%20(model)%20session_get_participant_data_from_peer_id_response%20%3E%20(schema)>)

#### Realtime KitRecordings

##### [Fetch all recordings for an App](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/recordings/methods/get_recordings)

GET/accounts/{account\_id}/realtime/kit/{app\_id}/recordings

##### [Start recording a meeting](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/recordings/methods/start_recordings)

POST/accounts/{account\_id}/realtime/kit/{app\_id}/recordings

##### [Fetch active recording](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/recordings/methods/get_active_recordings)

GET/accounts/{account\_id}/realtime/kit/{app\_id}/recordings/active-recording/{meeting\_id}

##### [Fetch details of a recording](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/recordings/methods/get_one_recording)

GET/accounts/{account\_id}/realtime/kit/{app\_id}/recordings/{recording\_id}

##### [Pause/Resume/Stop recording](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/recordings/methods/pause_resume_stop_recording)

PUT/accounts/{account\_id}/realtime/kit/{app\_id}/recordings/{recording\_id}

##### [Start recording participant audio tracks](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/recordings/methods/start_track_recording)

POST/accounts/{account\_id}/realtime/kit/{app\_id}/recordings/track

##### ModelsExpand Collapse

<details>

<summary>

RecordingGetRecordingsResponse object {data, paging, success }

</summary>

<details>

<summary>

data: array of object {id, audio\_download\_url, download\_url, 11 more }

</summary>

id: string

ID of the recording

formatuuid

<a href="#">Link to this property</a>

audio\_download\_url: string

If the audio\_config is passed, the URL for downloading the audio recording is returned.

formaturi

<a href="#">Link to this property</a>

download\_url: string

URL where the recording can be downloaded.

formaturi

<a href="#">Link to this property</a>

download\_url\_expiry: string

Timestamp when the download URL expires.

formatdate-time

<a href="#">Link to this property</a>

file\_size: number

File size of the recording, in bytes.

<a href="#">Link to this property</a>

invoked\_time: string

Timestamp when this recording was invoked.

formatdate-time

<a href="#">Link to this property</a>

output\_file\_name: string

File name of the recording.

<a href="#">Link to this property</a>

session\_id: string

ID of the meeting session this recording is for.

formatuuid

<a href="#">Link to this property</a>

started\_time: string

Timestamp when this recording actually started after being invoked. Usually a few seconds after <code>invoked_time</code>.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

status: "INVOKED"or "RECORDING"or "UPLOADING"or 3 more

Current status of the recording.

</summary>

One of the following:

"INVOKED"

<a href="#">Link to this property</a>

"RECORDING"

<a href="#">Link to this property</a>

"UPLOADING"

<a href="#">Link to this property</a>

"UPLOADED"

<a href="#">Link to this property</a>

"ERRORED"

<a href="#">Link to this property</a>

"PAUSED"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

stopped\_time: string

Timestamp when this recording was stopped. Optional; is present only when the recording has actually been stopped.

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

meeting: optional object {id, created\_at, updated\_at, 9 more }

</summary>

id: string

ID of the meeting.

formatuuid

<a href="#">Link to this property</a>

created\_at: string

Timestamp the object was created at. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

updated\_at: string

Timestamp the object was updated at. The time is returned in ISO format.

formatdate-time

<a href="#">Link to this property</a>

live\_stream\_on\_start: optional boolean

Specifies if the meeting should start getting livestreamed on start.

<a href="#">Link to this property</a>

persist\_chat: optional boolean

Specifies if Chat within a meeting should persist for a week.

<a href="#">Link to this property</a>

record\_on\_start: optional boolean

Specifies if the meeting should start getting recorded as soon as someone joins the meeting.

<a href="#">Link to this property</a>

<details>

<summary>

recording\_config: optional object {audio\_config, file\_name\_prefix, live\_streaming\_config, 4 more }

Recording Configurations to be used for this meeting. This level of configs takes higher preference over App level configs on the RealtimeKit developer portal.

</summary>

<details>

<summary>

audio\_config: optional object {channel, codec, export\_file }

Object containing configuration regarding the audio that is being recorded.

</summary>

<details>

<summary>

channel: optional "mono"or "stereo"

Audio signal pathway within an audio file that carries a specific sound source.

</summary>

One of the following:

"mono"

<a href="#">Link to this property</a>

"stereo"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

codec: optional "MP3"or "AAC"

Codec using which the recording will be encoded. If VP8/VP9 is selected for videoConfig, changing audioConfig is not allowed. In this case, the codec in the audioConfig is automatically set to vorbis.

</summary>

One of the following:

"MP3"

<a href="#">Link to this property</a>

"AAC"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

export\_file: optional boolean

Controls whether to export audio file seperately

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

file\_name\_prefix: optional string

Adds a prefix to the beginning of the file name of the recording.

<a href="#">Link to this property</a>

<details>

<summary>

live\_streaming\_config: optional object {rtmp\_url }

</summary>

rtmp\_url: optional string

RTMP URL to stream to

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

max\_seconds: optional number

Specifies the maximum duration for recording in seconds, ranging from a minimum of 60 seconds to a maximum of 24 hours.

maximum86400

minimum60

<a href="#">Link to this property</a>

<details>

<summary>

realtimekit\_bucket\_config: optional object {enabled }

</summary>

enabled: boolean

Controls whether recordings are uploaded to RealtimeKit’s bucket. If set to false, <code>download_url</code>, <code>audio_download_url</code>, <code>download_url_expiry</code> won’t be generated for a recording.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

storage\_config: optional object {access\_key, auth\_method, bucket, 9 more } or object {access\_key, region, auth\_method, 9 more } or object {private\_key, access\_key, auth\_method, 9 more } or object {password, access\_key, auth\_method, 9 more }

</summary>

One of the following:

<details>

<summary>

object {access\_key, auth\_method, bucket, 9 more }

</summary>

access\_key: optional string

Access key of the storage medium. Access key is not required for the <code>gcs</code> storage media type.

Note that this field is not readable by clients, only writeable.

<a href="#">Link to this property</a>

<details>

<summary>

auth\_method: optional "KEY"or "PASSWORD"

Authentication method used for “sftp” type storage medium

</summary>

One of the following:

"KEY"

<a href="#">Link to this property</a>

"PASSWORD"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

password: optional string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

path: optional string

Path relative to the bucket root at which the recording will be placed.

<a href="#">Link to this property</a>

port: optional number

SSH destination server port for SFTP type storage medium

<a href="#">Link to this property</a>

private\_key: optional string

Private key used to login to destination SSH server for SFTP type storage medium, when auth\_method used is “KEY”

<a href="#">Link to this property</a>

region: optional string

Region of the storage medium.

<a href="#">Link to this property</a>

secret: optional string

Secret key of the storage medium. Similar to <code>access_key</code>, it is only writeable by clients, not readable.

<a href="#">Link to this property</a>

type: optional "gcs"

<a href="#">Link to this property</a>

username: optional string

SSH destination server username for SFTP type storage medium

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object {access\_key, region, auth\_method, 9 more }

</summary>

access\_key: unknown

minLength1

<a href="#">Link to this property</a>

region: unknown

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

auth\_method: optional "KEY"or "PASSWORD"

Authentication method used for “sftp” type storage medium

</summary>

One of the following:

"KEY"

<a href="#">Link to this property</a>

"PASSWORD"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

bucket: optional string

Name of the storage medium’s bucket.

<a href="#">Link to this property</a>

host: optional string

SSH destination server host for SFTP type storage medium

<a href="#">Link to this property</a>

password: optional string

SSH destination server password for SFTP type storage medium when auth\_method is “PASSWORD”. If auth\_method is “KEY”, this specifies the password for the ssh private key.

<a href="#">Link to this property</a>

</details>

</details>

</details>

</details>

</details>

</details>

<!-- Cloudflare Markdown for Agents: incomplete conversion; source HTML truncated at the conversion size limit -->
