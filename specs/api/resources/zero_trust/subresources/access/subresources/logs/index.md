---
title: Logs
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Access](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Logs

#### LogsAccess Requests

##### [Get Access authentication logs](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/logs/subresources/access_requests/methods/list)

GET/accounts/{account\_id}/access/logs/access\_requests

##### ModelsExpand Collapse

<details>

<summary>

AccessRequestListResponse = array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.logs.scim%20%3E%20(model)%20access_request%20%3E%20(schema)">AccessRequest</a> { action, allowed, app\_domain, 6 more }

</summary>

action: optional string

The event that occurred, such as a login attempt.

<a href="#">Link to this property</a>

allowed: optional boolean

The result of the authentication event.

<a href="#">Link to this property</a>

app\_domain: optional string

The URL of the Access application.

<a href="#">Link to this property</a>

app\_uid: optional string

The unique identifier for the Access application.

<a href="#">Link to this property</a>

connection: optional string

The IdP used to authenticate.

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

ip\_address: optional string

The IP address of the authenticating user.

<a href="#">Link to this property</a>

ray\_id: optional string

The unique identifier for the request to Cloudflare.

maxLength16

<a href="#">Link to this property</a>

user\_email: optional string

The email address of the authenticating user.

formatemail

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.logs.access_requests%20%3E%20(model)%20access_request_list_response%20%3E%20(schema)>)

#### LogsJit Requests

##### [List Access JIT request logs](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/logs/subresources/jit_requests/methods/list)

GET/accounts/{account\_id}/access/logs/jit\_requests

##### [Get an Access JIT request log](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/logs/subresources/jit_requests/methods/get)

GET/accounts/{account\_id}/access/logs/jit\_requests/{knock\_request\_id}

##### ModelsExpand Collapse

<details>

<summary>

JitRequestListResponse object {app\_aud, app\_hostname, approvals\_received, 7 more }

</summary>

app\_aud: optional string

Audience of the Access application.

<a href="#">Link to this property</a>

app\_hostname: optional string

<a href="#">Link to this property</a>

approvals\_received: optional number

Number of unique actors who approved the request.

<a href="#">Link to this property</a>

approver\_emails: optional array of string

Unique actors who approved the request.

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

expires\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

knock\_request\_id: optional string

Unique identifier for the JIT request.

<a href="#">Link to this property</a>

purpose\_justification: optional string

<a href="#">Link to this property</a>

requester\_email: optional string

formatemail

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "PENDING"or "APPROVED"or "DENIED"or 2 more

JIT request status. <code>SPENT</code> is deprecated and interpreted as <code>APPROVED</code>.

</summary>

One of the following:

"PENDING"

<a href="#">Link to this property</a>

"APPROVED"

<a href="#">Link to this property</a>

"DENIED"

<a href="#">Link to this property</a>

"CANCELED"

<a href="#">Link to this property</a>

"SPENT"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.logs.jit_requests%20%3E%20(model)%20jit_request_list_response%20%3E%20(schema)>)

<details>

<summary>

JitRequestGetResponse object {app\_aud, app\_hostname, approvals\_received, 8 more }

</summary>

app\_aud: optional string

Audience of the Access application.

<a href="#">Link to this property</a>

app\_hostname: optional string

<a href="#">Link to this property</a>

approvals\_received: optional number

Number of unique actors who approved the request.

<a href="#">Link to this property</a>

approver\_emails: optional array of string

Unique actors who approved the request.

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

events: optional array of object {actor\_email, actor\_idp, actor\_uuid, 6 more }

</summary>

actor\_email: optional string

formatemail

<a href="#">Link to this property</a>

actor\_idp: optional string

<a href="#">Link to this property</a>

actor\_uuid: optional string

formatuuid

<a href="#">Link to this property</a>

decision\_outcome: optional string

<a href="#">Link to this property</a>

ray\_id: optional string

<a href="#">Link to this property</a>

session\_duration\_seconds: optional number

<a href="#">Link to this property</a>

success: optional boolean

<a href="#">Link to this property</a>

timestamp: optional string

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "CREATED"or "APPROVER\_DECISION"or "COMMITTED"or 3 more

</summary>

One of the following:

"CREATED"

<a href="#">Link to this property</a>

"APPROVER\_DECISION"

<a href="#">Link to this property</a>

"COMMITTED"

<a href="#">Link to this property</a>

"CANCELED"

<a href="#">Link to this property</a>

"LOGIN\_SUCCESS"

<a href="#">Link to this property</a>

"REDIRECT\_TO\_ACTIVE"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

expires\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

knock\_request\_id: optional string

Unique identifier for the JIT request.

<a href="#">Link to this property</a>

purpose\_justification: optional string

<a href="#">Link to this property</a>

requester\_email: optional string

formatemail

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "PENDING"or "APPROVED"or "DENIED"or 2 more

JIT request status. <code>SPENT</code> is deprecated and interpreted as <code>APPROVED</code>.

</summary>

One of the following:

"PENDING"

<a href="#">Link to this property</a>

"APPROVED"

<a href="#">Link to this property</a>

"DENIED"

<a href="#">Link to this property</a>

"CANCELED"

<a href="#">Link to this property</a>

"SPENT"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.logs.jit_requests%20%3E%20(model)%20jit_request_get_response%20%3E%20(schema)>)

#### LogsSCIM

##### ModelsExpand Collapse

<details>

<summary>

AccessRequest object {action, allowed, app\_domain, 6 more }

</summary>

action: optional string

The event that occurred, such as a login attempt.

<a href="#">Link to this property</a>

allowed: optional boolean

The result of the authentication event.

<a href="#">Link to this property</a>

app\_domain: optional string

The URL of the Access application.

<a href="#">Link to this property</a>

app\_uid: optional string

The unique identifier for the Access application.

<a href="#">Link to this property</a>

connection: optional string

The IdP used to authenticate.

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

ip\_address: optional string

The IP address of the authenticating user.

<a href="#">Link to this property</a>

ray\_id: optional string

The unique identifier for the request to Cloudflare.

maxLength16

<a href="#">Link to this property</a>

user\_email: optional string

The email address of the authenticating user.

formatemail

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.logs.scim%20%3E%20(model)%20access_request%20%3E%20(schema)>)

#### LogsSCIMUpdates

##### [List Access SCIM update logs](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/logs/subresources/scim/subresources/updates/methods/list)

GET/accounts/{account\_id}/access/logs/scim/updates

##### ModelsExpand Collapse

<details>

<summary>

UpdateListResponse object {cf\_resource\_id, error\_description, idp\_id, 8 more }

</summary>

cf\_resource\_id: optional string

The unique Cloudflare-generated Id of the SCIM resource.

<a href="#">Link to this property</a>

error\_description: optional string

The error message which is generated when the status of the SCIM request is ‘FAILURE’.

<a href="#">Link to this property</a>

idp\_id: optional string

The unique Id of the IdP that has SCIM enabled.

<a href="#">Link to this property</a>

idp\_resource\_id: optional string

The IdP-generated Id of the SCIM resource.

<a href="#">Link to this property</a>

logged\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

request\_body: optional string

The JSON-encoded string body of the SCIM request.

<a href="#">Link to this property</a>

request\_method: optional string

The request method of the SCIM request.

<a href="#">Link to this property</a>

resource\_group\_name: optional string

The display name of the SCIM Group resource if it exists.

<a href="#">Link to this property</a>

resource\_type: optional string

The resource type of the SCIM request.

<a href="#">Link to this property</a>

resource\_user\_email: optional string

The email address of the SCIM User resource if it exists.

formatemail

<a href="#">Link to this property</a>

status: optional string

The status of the SCIM request.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.logs.scim.updates%20%3E%20(model)%20update_list_response%20%3E%20(schema)>)