---
title: Apps
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Realtime Kit](https://developers.cloudflare.com/api/resources/realtime_kit)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Apps

##### [Fetch all apps](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/apps/methods/get)

GET/accounts/{account\_id}/realtime/kit/apps

##### [Fetch app details](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/apps/methods/get_app_by_id)

GET/accounts/{account\_id}/realtime/kit/apps/{app\_id}

##### [Update an app](https://developers.cloudflare.com/api/resources/realtime_kit/subresources/apps/methods/update_app_by_id)

PATCH/accounts/{account\_id}/realtime/kit/apps/{app\_id}

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

AppGetAppByIDResponse object {data, success }

</summary>

<details>

<summary>

data: optional object {id, created\_at, name }

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

success: optional boolean

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.apps%20%3E%20(model)%20app_get_app_by_id_response%20%3E%20(schema)>)

<details>

<summary>

AppUpdateAppByIDResponse object {data, success }

</summary>

<details>

<summary>

data: object {id, cf\_account\_tag, created\_at, 2 more }

</summary>

id: optional string

formatuuid

<a href="#">Link to this property</a>

cf\_account\_tag: optional string

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

is\_org\_on\_kv: optional boolean

<a href="#">Link to this property</a>

name: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

success: true

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20realtime_kit.apps%20%3E%20(model)%20app_update_app_by_id_response%20%3E%20(schema)>)

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