---
title: Automations
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Workers](https://developers.cloudflare.com/api/resources/workers)

[Observability](https://developers.cloudflare.com/api/resources/workers/subresources/observability)

[Issues](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/issues)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Automations

##### [List issue automations](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/issues/subresources/automations/methods/list)

GET/accounts/{account\_id}/workers/observability/issues/automations

##### [Get an issue automation](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/issues/subresources/automations/methods/get)

GET/accounts/{account\_id}/workers/observability/issues/automations/{automationId}

##### [Create an issue automation](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/issues/subresources/automations/methods/create)

POST/accounts/{account\_id}/workers/observability/issues/automations

##### [Update an issue automation](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/issues/subresources/automations/methods/update)

PUT/accounts/{account\_id}/workers/observability/issues/automations/{automationId}

##### [Delete an issue automation](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/issues/subresources/automations/methods/delete)

DELETE/accounts/{account\_id}/workers/observability/issues/automations/{automationId}

##### ModelsExpand Collapse

<details>

<summary>

AutomationListResponse object {automations }

</summary>

<details>

<summary>

automations: array of object {id, ansPolicyId, created, 12 more }

</summary>

id: string

<a href="#">Link to this property</a>

ansPolicyId: string

<a href="#">Link to this property</a>

created: number

<a href="#">Link to this property</a>

createdByUserId: string

<a href="#">Link to this property</a>

enabled: boolean

<a href="#">Link to this property</a>

inactivitySeconds: number

<a href="#">Link to this property</a>

name: string

<a href="#">Link to this property</a>

revision: number

<a href="#">Link to this property</a>

<details>

<summary>

scope: "account"or "service"

</summary>

One of the following:

"account"

<a href="#">Link to this property</a>

"service"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

service: string

<a href="#">Link to this property</a>

serviceType: string

<a href="#">Link to this property</a>

threshold: number

<a href="#">Link to this property</a>

<details>

<summary>

triggerType: "occurrence\_threshold"or "recurrence\_after\_inactivity"

</summary>

One of the following:

"occurrence\_threshold"

<a href="#">Link to this property</a>

"recurrence\_after\_inactivity"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated: number

<a href="#">Link to this property</a>

updatedByUserId: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues.automations%20%3E%20(model)%20automation_list_response%20%3E%20(schema)>)

<details>

<summary>

AutomationGetResponse object {automation }

</summary>

<details>

<summary>

automation: object {id, ansPolicyId, created, 12 more }

</summary>

id: string

<a href="#">Link to this property</a>

ansPolicyId: string

<a href="#">Link to this property</a>

created: number

<a href="#">Link to this property</a>

createdByUserId: string

<a href="#">Link to this property</a>

enabled: boolean

<a href="#">Link to this property</a>

inactivitySeconds: number

<a href="#">Link to this property</a>

name: string

<a href="#">Link to this property</a>

revision: number

<a href="#">Link to this property</a>

<details>

<summary>

scope: "account"or "service"

</summary>

One of the following:

"account"

<a href="#">Link to this property</a>

"service"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

service: string

<a href="#">Link to this property</a>

serviceType: string

<a href="#">Link to this property</a>

threshold: number

<a href="#">Link to this property</a>

<details>

<summary>

triggerType: "occurrence\_threshold"or "recurrence\_after\_inactivity"

</summary>

One of the following:

"occurrence\_threshold"

<a href="#">Link to this property</a>

"recurrence\_after\_inactivity"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated: number

<a href="#">Link to this property</a>

updatedByUserId: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues.automations%20%3E%20(model)%20automation_get_response%20%3E%20(schema)>)

<details>

<summary>

AutomationCreateResponse object {automation }

</summary>

<details>

<summary>

automation: object {id, ansPolicyId, created, 12 more }

</summary>

id: string

<a href="#">Link to this property</a>

ansPolicyId: string

<a href="#">Link to this property</a>

created: number

<a href="#">Link to this property</a>

createdByUserId: string

<a href="#">Link to this property</a>

enabled: boolean

<a href="#">Link to this property</a>

inactivitySeconds: number

<a href="#">Link to this property</a>

name: string

<a href="#">Link to this property</a>

revision: number

<a href="#">Link to this property</a>

<details>

<summary>

scope: "account"or "service"

</summary>

One of the following:

"account"

<a href="#">Link to this property</a>

"service"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

service: string

<a href="#">Link to this property</a>

serviceType: string

<a href="#">Link to this property</a>

threshold: number

<a href="#">Link to this property</a>

<details>

<summary>

triggerType: "occurrence\_threshold"or "recurrence\_after\_inactivity"

</summary>

One of the following:

"occurrence\_threshold"

<a href="#">Link to this property</a>

"recurrence\_after\_inactivity"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated: number

<a href="#">Link to this property</a>

updatedByUserId: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues.automations%20%3E%20(model)%20automation_create_response%20%3E%20(schema)>)

<details>

<summary>

AutomationUpdateResponse object {automation }

</summary>

<details>

<summary>

automation: object {id, ansPolicyId, created, 12 more }

</summary>

id: string

<a href="#">Link to this property</a>

ansPolicyId: string

<a href="#">Link to this property</a>

created: number

<a href="#">Link to this property</a>

createdByUserId: string

<a href="#">Link to this property</a>

enabled: boolean

<a href="#">Link to this property</a>

inactivitySeconds: number

<a href="#">Link to this property</a>

name: string

<a href="#">Link to this property</a>

revision: number

<a href="#">Link to this property</a>

<details>

<summary>

scope: "account"or "service"

</summary>

One of the following:

"account"

<a href="#">Link to this property</a>

"service"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

service: string

<a href="#">Link to this property</a>

serviceType: string

<a href="#">Link to this property</a>

threshold: number

<a href="#">Link to this property</a>

<details>

<summary>

triggerType: "occurrence\_threshold"or "recurrence\_after\_inactivity"

</summary>

One of the following:

"occurrence\_threshold"

<a href="#">Link to this property</a>

"recurrence\_after\_inactivity"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated: number

<a href="#">Link to this property</a>

updatedByUserId: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues.automations%20%3E%20(model)%20automation_update_response%20%3E%20(schema)>)

<details>

<summary>

AutomationDeleteResponse object {automation }

</summary>

<details>

<summary>

automation: object {id, ansPolicyId, created, 12 more }

</summary>

id: string

<a href="#">Link to this property</a>

ansPolicyId: string

<a href="#">Link to this property</a>

created: number

<a href="#">Link to this property</a>

createdByUserId: string

<a href="#">Link to this property</a>

enabled: boolean

<a href="#">Link to this property</a>

inactivitySeconds: number

<a href="#">Link to this property</a>

name: string

<a href="#">Link to this property</a>

revision: number

<a href="#">Link to this property</a>

<details>

<summary>

scope: "account"or "service"

</summary>

One of the following:

"account"

<a href="#">Link to this property</a>

"service"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

service: string

<a href="#">Link to this property</a>

serviceType: string

<a href="#">Link to this property</a>

threshold: number

<a href="#">Link to this property</a>

<details>

<summary>

triggerType: "occurrence\_threshold"or "recurrence\_after\_inactivity"

</summary>

One of the following:

"occurrence\_threshold"

<a href="#">Link to this property</a>

"recurrence\_after\_inactivity"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated: number

<a href="#">Link to this property</a>

updatedByUserId: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues.automations%20%3E%20(model)%20automation_delete_response%20%3E%20(schema)>)