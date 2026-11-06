---
title: Issues
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Workers](https://developers.cloudflare.com/api/resources/workers)

[Observability](https://developers.cloudflare.com/api/resources/workers/subresources/observability)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Issues

##### [List detected issues](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/issues/methods/list)

GET/accounts/{account\_id}/workers/observability/issues

##### [Get an issue](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/issues/methods/get)

GET/accounts/{account\_id}/workers/observability/issues/{issueId}

##### [Modify an issue](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/issues/methods/update)

PATCH/accounts/{account\_id}/workers/observability/issues/{issueId}

##### [Summarize detected issues](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/issues/methods/summary)

GET/accounts/{account\_id}/workers/observability/issues/summary

##### [Create an issue group](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/issues/methods/group)

POST/accounts/{account\_id}/workers/observability/issues/groups

##### [Dissolve an issue group](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/issues/methods/ungroup)

DELETE/accounts/{account\_id}/workers/observability/issues/groups/{groupId}

##### [Add issue group members](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/issues/methods/add)

POST/accounts/{account\_id}/workers/observability/issues/groups/{groupId}/members

##### [Remove an issue group member](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/issues/methods/remove)

DELETE/accounts/{account\_id}/workers/observability/issues/groups/{groupId}/members/{issueId}

##### [Notify about an issue](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/issues/methods/notify)

POST/accounts/{account\_id}/workers/observability/issues/{issueId}/notification-runs

##### [List issue occurrences](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/issues/methods/occurrences)

GET/accounts/{account\_id}/workers/observability/issues/{issueId}/occurrences

##### ModelsExpand Collapse

<details>

<summary>

IssueListResponse object {id, activity, count, 11 more }

</summary>

id: string

<a href="#">Link to this property</a>

<details>

<summary>

activity: array of object {id, created, inactivitySeconds, 14 more }

</summary>

id: string

<a href="#">Link to this property</a>

created: number

<a href="#">Link to this property</a>

inactivitySeconds: number

<a href="#">Link to this property</a>

<details>

<summary>

initiatedBy: "automatic"or "manual"

</summary>

One of the following:

"automatic"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

issueCount: number

<a href="#">Link to this property</a>

issueId: string

<a href="#">Link to this property</a>

lastError: string

<a href="#">Link to this property</a>

policyId: string

<a href="#">Link to this property</a>

<details>

<summary>

status: "pending"or "succeeded"or "failed"

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"succeeded"

<a href="#">Link to this property</a>

"failed"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

terminalAt: number

<a href="#">Link to this property</a>

threshold: number

<a href="#">Link to this property</a>

type: "notification"

<a href="#">Link to this property</a>

automationId: optional string

<a href="#">Link to this property</a>

automationName: optional string

<a href="#">Link to this property</a>

automationRevision: optional number

<a href="#">Link to this property</a>

<details>

<summary>

scope: optional "account"or "service"

</summary>

One of the following:

"account"

<a href="#">Link to this property</a>

"service"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

triggerType: optional "occurrence\_threshold"or "recurrence\_after\_inactivity"

</summary>

One of the following:

"occurrence\_threshold"

<a href="#">Link to this property</a>

"recurrence\_after\_inactivity"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

count: number

<a href="#">Link to this property</a>

created: number

<a href="#">Link to this property</a>

firstObserved: number

<a href="#">Link to this property</a>

lastObserved: number

<a href="#">Link to this property</a>

service: string

<a href="#">Link to this property</a>

<details>

<summary>

status: "active"or "resolved"or "ignored"

</summary>

One of the following:

"active"

<a href="#">Link to this property</a>

"resolved"

<a href="#">Link to this property</a>

"ignored"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

statusUpdated: number

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

updated: number

<a href="#">Link to this property</a>

fingerprint: optional string

<a href="#">Link to this property</a>

<details>

<summary>

members: optional array of object {fingerprint, issueId, title }

</summary>

fingerprint: string

<a href="#">Link to this property</a>

issueId: string

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

type: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues%20%3E%20(model)%20issue_list_response%20%3E%20(schema)>)

<details>

<summary>

IssueGetResponse object {issue }

</summary>

<details>

<summary>

issue: object {id, activity, count, 11 more }

</summary>

id: string

<a href="#">Link to this property</a>

<details>

<summary>

activity: array of object {id, created, inactivitySeconds, 14 more }

</summary>

id: string

<a href="#">Link to this property</a>

created: number

<a href="#">Link to this property</a>

inactivitySeconds: number

<a href="#">Link to this property</a>

<details>

<summary>

initiatedBy: "automatic"or "manual"

</summary>

One of the following:

"automatic"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

issueCount: number

<a href="#">Link to this property</a>

issueId: string

<a href="#">Link to this property</a>

lastError: string

<a href="#">Link to this property</a>

policyId: string

<a href="#">Link to this property</a>

<details>

<summary>

status: "pending"or "succeeded"or "failed"

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"succeeded"

<a href="#">Link to this property</a>

"failed"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

terminalAt: number

<a href="#">Link to this property</a>

threshold: number

<a href="#">Link to this property</a>

type: "notification"

<a href="#">Link to this property</a>

automationId: optional string

<a href="#">Link to this property</a>

automationName: optional string

<a href="#">Link to this property</a>

automationRevision: optional number

<a href="#">Link to this property</a>

<details>

<summary>

scope: optional "account"or "service"

</summary>

One of the following:

"account"

<a href="#">Link to this property</a>

"service"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

triggerType: optional "occurrence\_threshold"or "recurrence\_after\_inactivity"

</summary>

One of the following:

"occurrence\_threshold"

<a href="#">Link to this property</a>

"recurrence\_after\_inactivity"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

count: number

<a href="#">Link to this property</a>

created: number

<a href="#">Link to this property</a>

firstObserved: number

<a href="#">Link to this property</a>

lastObserved: number

<a href="#">Link to this property</a>

service: string

<a href="#">Link to this property</a>

<details>

<summary>

status: "active"or "resolved"or "ignored"

</summary>

One of the following:

"active"

<a href="#">Link to this property</a>

"resolved"

<a href="#">Link to this property</a>

"ignored"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

statusUpdated: number

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

updated: number

<a href="#">Link to this property</a>

fingerprint: optional string

<a href="#">Link to this property</a>

<details>

<summary>

members: optional array of object {fingerprint, issueId, title }

</summary>

fingerprint: string

<a href="#">Link to this property</a>

issueId: string

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

type: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues%20%3E%20(model)%20issue_get_response%20%3E%20(schema)>)

<details>

<summary>

IssueUpdateResponse object {id, count, created, 10 more }

</summary>

id: string

<a href="#">Link to this property</a>

count: number

<a href="#">Link to this property</a>

created: number

<a href="#">Link to this property</a>

firstObserved: number

<a href="#">Link to this property</a>

lastObserved: number

<a href="#">Link to this property</a>

service: string

<a href="#">Link to this property</a>

<details>

<summary>

status: "active"or "resolved"or "ignored"

</summary>

One of the following:

"active"

<a href="#">Link to this property</a>

"resolved"

<a href="#">Link to this property</a>

"ignored"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

statusUpdated: number

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

updated: number

<a href="#">Link to this property</a>

fingerprint: optional string

<a href="#">Link to this property</a>

<details>

<summary>

members: optional array of object {fingerprint, issueId, title }

</summary>

fingerprint: string

<a href="#">Link to this property</a>

issueId: string

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

type: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues%20%3E%20(model)%20issue_update_response%20%3E%20(schema)>)

<details>

<summary>

IssueSummaryResponse object {activeIssues, activeOccurrences, lastIssue, resolvedIssues }

</summary>

activeIssues: number

<a href="#">Link to this property</a>

activeOccurrences: number

<a href="#">Link to this property</a>

lastIssue: number

<a href="#">Link to this property</a>

resolvedIssues: number

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues%20%3E%20(model)%20issue_summary_response%20%3E%20(schema)>)

<details>

<summary>

IssueGroupResponse object {id, count, created, 10 more }

</summary>

id: string

<a href="#">Link to this property</a>

count: number

<a href="#">Link to this property</a>

created: number

<a href="#">Link to this property</a>

firstObserved: number

<a href="#">Link to this property</a>

lastObserved: number

<a href="#">Link to this property</a>

service: string

<a href="#">Link to this property</a>

<details>

<summary>

status: "active"or "resolved"or "ignored"

</summary>

One of the following:

"active"

<a href="#">Link to this property</a>

"resolved"

<a href="#">Link to this property</a>

"ignored"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

statusUpdated: number

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

updated: number

<a href="#">Link to this property</a>

fingerprint: optional string

<a href="#">Link to this property</a>

<details>

<summary>

members: optional array of object {fingerprint, issueId, title }

</summary>

fingerprint: string

<a href="#">Link to this property</a>

issueId: string

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

type: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues%20%3E%20(model)%20issue_group_response%20%3E%20(schema)>)

<details>

<summary>

IssueUngroupResponse object {deleted }

</summary>

deleted: true

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues%20%3E%20(model)%20issue_ungroup_response%20%3E%20(schema)>)

<details>

<summary>

IssueAddResponse object {id, count, created, 10 more }

</summary>

id: string

<a href="#">Link to this property</a>

count: number

<a href="#">Link to this property</a>

created: number

<a href="#">Link to this property</a>

firstObserved: number

<a href="#">Link to this property</a>

lastObserved: number

<a href="#">Link to this property</a>

service: string

<a href="#">Link to this property</a>

<details>

<summary>

status: "active"or "resolved"or "ignored"

</summary>

One of the following:

"active"

<a href="#">Link to this property</a>

"resolved"

<a href="#">Link to this property</a>

"ignored"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

statusUpdated: number

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

updated: number

<a href="#">Link to this property</a>

fingerprint: optional string

<a href="#">Link to this property</a>

<details>

<summary>

members: optional array of object {fingerprint, issueId, title }

</summary>

fingerprint: string

<a href="#">Link to this property</a>

issueId: string

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

type: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues%20%3E%20(model)%20issue_add_response%20%3E%20(schema)>)

<details>

<summary>

IssueRemoveResponse object {id, count, created, 10 more }

</summary>

id: string

<a href="#">Link to this property</a>

count: number

<a href="#">Link to this property</a>

created: number

<a href="#">Link to this property</a>

firstObserved: number

<a href="#">Link to this property</a>

lastObserved: number

<a href="#">Link to this property</a>

service: string

<a href="#">Link to this property</a>

<details>

<summary>

status: "active"or "resolved"or "ignored"

</summary>

One of the following:

"active"

<a href="#">Link to this property</a>

"resolved"

<a href="#">Link to this property</a>

"ignored"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

statusUpdated: number

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

updated: number

<a href="#">Link to this property</a>

fingerprint: optional string

<a href="#">Link to this property</a>

<details>

<summary>

members: optional array of object {fingerprint, issueId, title }

</summary>

fingerprint: string

<a href="#">Link to this property</a>

issueId: string

<a href="#">Link to this property</a>

title: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

type: optional string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues%20%3E%20(model)%20issue_remove_response%20%3E%20(schema)>)

<details>

<summary>

IssueNotifyResponse object {run }

</summary>

<details>

<summary>

run: object {id, created, inactivitySeconds, 13 more }

</summary>

id: string

<a href="#">Link to this property</a>

created: number

<a href="#">Link to this property</a>

inactivitySeconds: number

<a href="#">Link to this property</a>

<details>

<summary>

initiatedBy: "automatic"or "manual"

</summary>

One of the following:

"automatic"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

issueCount: number

<a href="#">Link to this property</a>

issueId: string

<a href="#">Link to this property</a>

lastError: string

<a href="#">Link to this property</a>

policyId: string

<a href="#">Link to this property</a>

<details>

<summary>

status: "pending"or "succeeded"or "failed"

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"succeeded"

<a href="#">Link to this property</a>

"failed"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

terminalAt: number

<a href="#">Link to this property</a>

threshold: number

<a href="#">Link to this property</a>

automationId: optional string

<a href="#">Link to this property</a>

automationName: optional string

<a href="#">Link to this property</a>

automationRevision: optional number

<a href="#">Link to this property</a>

<details>

<summary>

scope: optional "account"or "service"

</summary>

One of the following:

"account"

<a href="#">Link to this property</a>

"service"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

triggerType: optional "occurrence\_threshold"or "recurrence\_after\_inactivity"

</summary>

One of the following:

"occurrence\_threshold"

<a href="#">Link to this property</a>

"recurrence\_after\_inactivity"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues%20%3E%20(model)%20issue_notify_response%20%3E%20(schema)>)

<details>

<summary>

IssueOccurrencesResponse = array of object {id, error, invocation, 5 more }

</summary>

id: string

Unique occurrence ID.

<a href="#">Link to this property</a>

<details>

<summary>

error: object {handled, mechanism, message, 3 more }

</summary>

handled: boolean

<a href="#">Link to this property</a>

<details>

<summary>

mechanism: "structured-log"or "error-log"or "stack-log"or 3 more

</summary>

One of the following:

"structured-log"

<a href="#">Link to this property</a>

"error-log"

<a href="#">Link to this property</a>

"stack-log"

<a href="#">Link to this property</a>

"http-status"

<a href="#">Link to this property</a>

"exception"

<a href="#">Link to this property</a>

"outcome"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

name: string

<a href="#">Link to this property</a>

signature: string

<a href="#">Link to this property</a>

stack: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

invocation: object {id, traceId, type, 16 more }

</summary>

id: string

Worker invocation request ID.

<a href="#">Link to this property</a>

traceId: string

<a href="#">Link to this property</a>

type: string

<a href="#">Link to this property</a>

batchSize: optional number

<a href="#">Link to this property</a>

cron: optional string

<a href="#">Link to this property</a>

jsrpcMethod: optional string

<a href="#">Link to this property</a>

mailFrom: optional string

<a href="#">Link to this property</a>

method: optional string

<a href="#">Link to this property</a>

path: optional string

<a href="#">Link to this property</a>

queue: optional string

<a href="#">Link to this property</a>

rawSize: optional number

<a href="#">Link to this property</a>

rayId: optional string

<a href="#">Link to this property</a>

rcptTo: optional string

<a href="#">Link to this property</a>

scheduledTime: optional number

<a href="#">Link to this property</a>

spanId: optional string

<a href="#">Link to this property</a>

statusCode: optional number

minimum0

<a href="#">Link to this property</a>

url: optional string

Redacted request URL without query parameters.

<a href="#">Link to this property</a>

websocketCloseCode: optional number

<a href="#">Link to this property</a>

websocketEvent: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

timestamp: number

Occurrence timestamp as Unix epoch milliseconds.

<a href="#">Link to this property</a>

<details>

<summary>

trail: array of object {level, message, timestamp, type } or object {name, ongoing, spanId, 3 more }

</summary>

One of the following:

<details>

<summary>

object {level, message, timestamp, type }

</summary>

level: string

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

timestamp: number

<a href="#">Link to this property</a>

type: "log"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object {name, ongoing, spanId, 3 more }

</summary>

name: string

<a href="#">Link to this property</a>

ongoing: boolean

<a href="#">Link to this property</a>

spanId: string

<a href="#">Link to this property</a>

timestamp: number

<a href="#">Link to this property</a>

type: "span"

<a href="#">Link to this property</a>

parentSpanId: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

worker: object {executionModel, scriptName, scriptTags, 3 more }

</summary>

executionModel: string

<a href="#">Link to this property</a>

scriptName: string

<a href="#">Link to this property</a>

scriptTags: array of string

<a href="#">Link to this property</a>

dispatchNamespace: optional string

<a href="#">Link to this property</a>

entrypoint: optional string

<a href="#">Link to this property</a>

<details>

<summary>

scriptVersion: optional object {id, tag }

</summary>

id: string

<a href="#">Link to this property</a>

tag: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

context: optional object {account, session, user }

</summary>

account: optional string

<a href="#">Link to this property</a>

session: optional string

<a href="#">Link to this property</a>

user: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

request: optional object {headers }

</summary>

headers: map\[string]

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues%20%3E%20(model)%20issue_occurrences_response%20%3E%20(schema)>)

#### IssuesAutomations

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