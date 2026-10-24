---
title: Queries
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Cloudforce One](https://developers.cloudflare.com/api/resources/cloudforce_one)

[Threat Events](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_events)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Queries

##### [List saved event queries](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_events/subresources/queries/methods/list)

GET/accounts/{account\_id}/cloudforce-one/events/queries

##### [Create a saved event query](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_events/subresources/queries/methods/create)

POST/accounts/{account\_id}/cloudforce-one/events/queries/create

##### [Get a saved event query](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_events/subresources/queries/methods/get)

GET/accounts/{account\_id}/cloudforce-one/events/queries/{query\_id}

##### [Update a saved event query](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_events/subresources/queries/methods/edit)

PATCH/accounts/{account\_id}/cloudforce-one/events/queries/{query\_id}

##### [Delete a saved event query](https://developers.cloudflare.com/api/resources/cloudforce_one/subresources/threat_events/subresources/queries/methods/delete)

DELETE/accounts/{account\_id}/cloudforce-one/events/queries/{query\_id}

##### ModelsExpand Collapse

<details>

<summary>

QueryListResponse = array of object {id, account\_id, alert\_enabled, 10 more }

</summary>

id: number

Unique identifier for the saved query

<a href="#">Link to this property</a>

account\_id: number

Account ID

<a href="#">Link to this property</a>

Deprecatedalert\_enabled: boolean

Deprecated: saved-query alerting and rules were removed. Always false.

<a href="#">Link to this property</a>

Deprecatedalert\_rollup\_enabled: boolean

Deprecated: saved-query alerting and rules were removed. Always false.

<a href="#">Link to this property</a>

created\_at: string

Creation timestamp

<a href="#">Link to this property</a>

name: string

Name of the saved query

<a href="#">Link to this property</a>

query\_json: string

JSON string containing the query parameters

<a href="#">Link to this property</a>

Deprecatedrule\_enabled: boolean

Deprecated: saved-query alerting and rules were removed. Always false.

<a href="#">Link to this property</a>

updated\_at: string

Last update timestamp

<a href="#">Link to this property</a>

user\_email: string

Email of the user who created the query

<a href="#">Link to this property</a>

Deprecatedcustom\_threat\_feed\_id: optional number

Deprecated: saved-query alerting and rules were removed. Always null.

<a href="#">Link to this property</a>

Deprecatedrule\_list\_id: optional string

Deprecated: saved-query alerting and rules were removed. Always null.

<a href="#">Link to this property</a>

Deprecatedrule\_scope: optional string

Deprecated: saved-query alerting and rules were removed. Always null.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_events.queries%20%3E%20(model)%20query_list_response%20%3E%20(schema)>)

<details>

<summary>

QueryCreateResponse object {id, account\_id, alert\_enabled, 10 more }

</summary>

id: number

Unique identifier for the saved query

<a href="#">Link to this property</a>

account\_id: number

Account ID

<a href="#">Link to this property</a>

Deprecatedalert\_enabled: boolean

Deprecated: saved-query alerting and rules were removed. Always false.

<a href="#">Link to this property</a>

Deprecatedalert\_rollup\_enabled: boolean

Deprecated: saved-query alerting and rules were removed. Always false.

<a href="#">Link to this property</a>

created\_at: string

Creation timestamp

<a href="#">Link to this property</a>

name: string

Name of the saved query

<a href="#">Link to this property</a>

query\_json: string

JSON string containing the query parameters

<a href="#">Link to this property</a>

Deprecatedrule\_enabled: boolean

Deprecated: saved-query alerting and rules were removed. Always false.

<a href="#">Link to this property</a>

updated\_at: string

Last update timestamp

<a href="#">Link to this property</a>

user\_email: string

Email of the user who created the query

<a href="#">Link to this property</a>

Deprecatedcustom\_threat\_feed\_id: optional number

Deprecated: saved-query alerting and rules were removed. Always null.

<a href="#">Link to this property</a>

Deprecatedrule\_list\_id: optional string

Deprecated: saved-query alerting and rules were removed. Always null.

<a href="#">Link to this property</a>

Deprecatedrule\_scope: optional string

Deprecated: saved-query alerting and rules were removed. Always null.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_events.queries%20%3E%20(model)%20query_create_response%20%3E%20(schema)>)

<details>

<summary>

QueryGetResponse object {id, account\_id, alert\_enabled, 10 more }

</summary>

id: number

Unique identifier for the saved query

<a href="#">Link to this property</a>

account\_id: number

Account ID

<a href="#">Link to this property</a>

Deprecatedalert\_enabled: boolean

Deprecated: saved-query alerting and rules were removed. Always false.

<a href="#">Link to this property</a>

Deprecatedalert\_rollup\_enabled: boolean

Deprecated: saved-query alerting and rules were removed. Always false.

<a href="#">Link to this property</a>

created\_at: string

Creation timestamp

<a href="#">Link to this property</a>

name: string

Name of the saved query

<a href="#">Link to this property</a>

query\_json: string

JSON string containing the query parameters

<a href="#">Link to this property</a>

Deprecatedrule\_enabled: boolean

Deprecated: saved-query alerting and rules were removed. Always false.

<a href="#">Link to this property</a>

updated\_at: string

Last update timestamp

<a href="#">Link to this property</a>

user\_email: string

Email of the user who created the query

<a href="#">Link to this property</a>

Deprecatedcustom\_threat\_feed\_id: optional number

Deprecated: saved-query alerting and rules were removed. Always null.

<a href="#">Link to this property</a>

Deprecatedrule\_list\_id: optional string

Deprecated: saved-query alerting and rules were removed. Always null.

<a href="#">Link to this property</a>

Deprecatedrule\_scope: optional string

Deprecated: saved-query alerting and rules were removed. Always null.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_events.queries%20%3E%20(model)%20query_get_response%20%3E%20(schema)>)

<details>

<summary>

QueryEditResponse object {id, account\_id, alert\_enabled, 10 more }

</summary>

id: number

Unique identifier for the saved query

<a href="#">Link to this property</a>

account\_id: number

Account ID

<a href="#">Link to this property</a>

Deprecatedalert\_enabled: boolean

Deprecated: saved-query alerting and rules were removed. Always false.

<a href="#">Link to this property</a>

Deprecatedalert\_rollup\_enabled: boolean

Deprecated: saved-query alerting and rules were removed. Always false.

<a href="#">Link to this property</a>

created\_at: string

Creation timestamp

<a href="#">Link to this property</a>

name: string

Name of the saved query

<a href="#">Link to this property</a>

query\_json: string

JSON string containing the query parameters

<a href="#">Link to this property</a>

Deprecatedrule\_enabled: boolean

Deprecated: saved-query alerting and rules were removed. Always false.

<a href="#">Link to this property</a>

updated\_at: string

Last update timestamp

<a href="#">Link to this property</a>

user\_email: string

Email of the user who created the query

<a href="#">Link to this property</a>

Deprecatedcustom\_threat\_feed\_id: optional number

Deprecated: saved-query alerting and rules were removed. Always null.

<a href="#">Link to this property</a>

Deprecatedrule\_list\_id: optional string

Deprecated: saved-query alerting and rules were removed. Always null.

<a href="#">Link to this property</a>

Deprecatedrule\_scope: optional string

Deprecated: saved-query alerting and rules were removed. Always null.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20cloudforce_one.threat_events.queries%20%3E%20(model)%20query_edit_response%20%3E%20(schema)>)