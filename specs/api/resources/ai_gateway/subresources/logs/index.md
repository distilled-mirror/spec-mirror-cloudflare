---
title: Logs
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[AI Gateway](https://developers.cloudflare.com/api/resources/ai_gateway)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Logs

##### [List Gateway Logs](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/logs/methods/list)

GET/accounts/{account\_id}/ai-gateway/gateways/{gateway\_id}/logs

##### [Get Gateway Log Detail](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/logs/methods/get)

GET/accounts/{account\_id}/ai-gateway/gateways/{gateway\_id}/logs/{id}

##### [Patch Gateway Log](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/logs/methods/edit)

PATCH/accounts/{account\_id}/ai-gateway/gateways/{gateway\_id}/logs/{id}

##### [Delete Gateway Logs](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/logs/methods/delete)

DELETE/accounts/{account\_id}/ai-gateway/gateways/{gateway\_id}/logs

##### [Get Gateway Log Request](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/logs/methods/request)

GET/accounts/{account\_id}/ai-gateway/gateways/{gateway\_id}/logs/{id}/request

##### [Get Gateway Log Response](https://developers.cloudflare.com/api/resources/ai_gateway/subresources/logs/methods/response)

GET/accounts/{account\_id}/ai-gateway/gateways/{gateway\_id}/logs/{id}/response

##### ModelsExpand Collapse

<details>

<summary>

LogListResponse object {id, cached, created\_at, 17 more }

</summary>

id: string

<a href="#">Link to this property</a>

cached: boolean

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

duration: number

<a href="#">Link to this property</a>

model: string

<a href="#">Link to this property</a>

path: string

<a href="#">Link to this property</a>

provider: string

<a href="#">Link to this property</a>

success: boolean

<a href="#">Link to this property</a>

tokens\_in: number

<a href="#">Link to this property</a>

tokens\_out: number

<a href="#">Link to this property</a>

collect\_log\_payload: optional boolean

Whether the request and response bodies were eligible to be stored. False when the request sent <code>cf-aig-collect-log-payload: false</code>, logging was off, or the gateway does not store bodies for the request. Null for logs written before this field existed.

<a href="#">Link to this property</a>

cost: optional number

<a href="#">Link to this property</a>

custom\_cost: optional boolean

<a href="#">Link to this property</a>

metadata: optional string

<a href="#">Link to this property</a>

model\_type: optional string

<a href="#">Link to this property</a>

request\_content\_type: optional string

<a href="#">Link to this property</a>

request\_type: optional string

<a href="#">Link to this property</a>

response\_content\_type: optional string

<a href="#">Link to this property</a>

status\_code: optional number

<a href="#">Link to this property</a>

step: optional number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.logs%20%3E%20(model)%20log_list_response%20%3E%20(schema)>)

<details>

<summary>

LogGetResponse object {id, cached, created\_at, 23 more }

</summary>

id: string

<a href="#">Link to this property</a>

cached: boolean

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

duration: number

<a href="#">Link to this property</a>

model: string

<a href="#">Link to this property</a>

path: string

<a href="#">Link to this property</a>

provider: string

<a href="#">Link to this property</a>

success: boolean

<a href="#">Link to this property</a>

tokens\_in: number

<a href="#">Link to this property</a>

tokens\_out: number

<a href="#">Link to this property</a>

collect\_log\_payload: optional boolean

Whether the request and response bodies were eligible to be stored. False when the request sent <code>cf-aig-collect-log-payload: false</code>, logging was off, or the gateway does not store bodies for the request. Null for logs written before this field existed.

<a href="#">Link to this property</a>

cost: optional number

<a href="#">Link to this property</a>

custom\_cost: optional boolean

<a href="#">Link to this property</a>

metadata: optional string

<a href="#">Link to this property</a>

model\_type: optional string

<a href="#">Link to this property</a>

request\_content\_type: optional string

<a href="#">Link to this property</a>

request\_head: optional string

<a href="#">Link to this property</a>

request\_head\_complete: optional boolean

<a href="#">Link to this property</a>

request\_size: optional number

<a href="#">Link to this property</a>

request\_type: optional string

<a href="#">Link to this property</a>

response\_content\_type: optional string

<a href="#">Link to this property</a>

response\_head: optional string

<a href="#">Link to this property</a>

response\_head\_complete: optional boolean

<a href="#">Link to this property</a>

response\_size: optional number

<a href="#">Link to this property</a>

status\_code: optional number

<a href="#">Link to this property</a>

step: optional number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.logs%20%3E%20(model)%20log_get_response%20%3E%20(schema)>)

LogEditResponse = unknown

[Link to this property](#)%20ai_gateway.logs%20%3E%20(model)%20log_edit_response%20%3E%20(schema)>)

<details>

<summary>

LogDeleteResponse object {success }

</summary>

success: boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20ai_gateway.logs%20%3E%20(model)%20log_delete_response%20%3E%20(schema)>)

LogRequestResponse = unknown

[Link to this property](#)%20ai_gateway.logs%20%3E%20(model)%20log_request_response%20%3E%20(schema)>)

LogResponseResponse = unknown

[Link to this property](#)%20ai_gateway.logs%20%3E%20(model)%20log_response_response%20%3E%20(schema)>)