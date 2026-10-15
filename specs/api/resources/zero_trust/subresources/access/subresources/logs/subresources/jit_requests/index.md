---
title: Jit Requests
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Access](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access)

[Logs](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/logs)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Jit Requests

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