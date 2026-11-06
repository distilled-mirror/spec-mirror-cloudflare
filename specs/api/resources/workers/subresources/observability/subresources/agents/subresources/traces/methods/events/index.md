---
title: List Agent Trace events
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Workers](https://developers.cloudflare.com/api/resources/workers)

[Observability](https://developers.cloudflare.com/api/resources/workers/subresources/observability)

[Agents](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/agents)

[Traces](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/agents/subresources/traces)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List Agent Trace events

GET/accounts/{account\_id}/workers/observability/agents/traces/{traceId}/events

Returns a page of authorized canonical otel events for a Trace containing named Agent activity, using the existing events-query flow. Searches the full 7-day retention unless from or to narrow it. Events are ordered by event timestamp and ID, newest first. Continue with result\_info.cursors.after; one page is not a complete span tree.

##### Security

<details>

<summary>API Email + API Key</summary>



The previous authorization scheme for interacting with the Cloudflare API, used in conjunction with a Global API key.

**Example:**<code>X-Auth-Email: user@example.com</code>

The previous authorization scheme for interacting with the Cloudflare API. When possible, use API tokens instead of Global API keys.

**Example:**<code>X-Auth-Key: 144c9defac04969c7bfad8efaa8ea194</code>

</details>

<details>

<summary>API Token</summary>



The preferred authorization scheme for interacting with the Cloudflare API. <a href="https://developers.cloudflare.com/fundamentals/api/get-started/create-token/">Create a token</a>.

**Example:**<code>Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY</code>

</details>

<details>

<summary>User Service Key</summary>



Used when interacting with the Origin CA certificates API. <a href="https://developers.cloudflare.com/fundamentals/api/get-started/ca-keys/#viewchange-your-origin-ca-keys">View/change your key</a>.

**Example:**<code>X-Auth-User-Service-Key: v1.0-144c9defac04969c7bfad8ef-631a41d003a32d25fe878081ef365c49503f7fada600da935e2851a1c7326084b85cbf6429c4b859de8475731dc92a9c329631e6d59e6c73da7b198497172b4cefe071d90d0f5d2719</code>

</details>

##### Accepted Permissions (at least one required)

`Workers Observability Write``Workers Observability Read`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20events%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

traceId: string

Trace ID: 32 hexadecimal characters, matched case-insensitively.

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20events%20%3E%20(params)%20default%20%3E%20(param)%20traceId%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

cursor: optional string

Opaque cursor from result\_info.cursors.after in the previous response. Send it with the same filters; its window replaces from and to.

maxLength4096

minLength1

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20events%20%3E%20(params)%20default%20%3E%20(param)%20cursor%20%3E%20(schema)>)

from: optional number

Optional. Narrows the search, which by default covers the full 7-day retention, so any retained Trace ID can be fetched without a window. Start as Unix epoch milliseconds; the effective value is in result\_info.from.

minimum0

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20events%20%3E%20(params)%20default%20%3E%20(param)%20from%20%3E%20(schema)>)

per\_page: optional number

Maximum items to return per page. Defaults to 100.

maximum500

minimum1

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20events%20%3E%20(params)%20default%20%3E%20(param)%20per_page%20%3E%20(schema)>)

to: optional number

Optional. Narrows the search; end as Unix epoch milliseconds. Defaults to now.

minimum0

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20events%20%3E%20(params)%20default%20%3E%20(param)%20to%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20events%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {message }

</summary>

message: "Successful request"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20events%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: array of object {"$metadata", dataset, source, 3 more }

</summary>

<details>

<summary>

"$metadata": object {id, account, cloudService, 35 more }

Structured metadata extracted from the event. These fields are indexed and available for filtering and aggregation.

</summary>

id: string

Unique event ID. Use as the cursor value for offset-based pagination.

<a href="#">Link to this property</a>

account: optional string

Cloudflare account identifier.

<a href="#">Link to this property</a>

cloudService: optional string

Cloudflare product that generated this event (e.g. workers, pages).

<a href="#">Link to this property</a>

coldStart: optional number

exclusiveMinimum

minimum0

<a href="#">Link to this property</a>

cost: optional number

Estimated cost units for this invocation.

exclusiveMinimum

minimum0

<a href="#">Link to this property</a>

duration: optional number

Span duration in milliseconds.

exclusiveMinimum

minimum0

<a href="#">Link to this property</a>

endTime: optional number

Span end time as a Unix epoch in milliseconds.

minimum0

<a href="#">Link to this property</a>

endTimeNs: optional string

Span end time as a Unix epoch in nanoseconds.

<a href="#">Link to this property</a>

error: optional string

Error message, present when the log represents an error.

<a href="#">Link to this property</a>

errorTemplate: optional string

Templatized version of the error message used for grouping similar errors.

<a href="#">Link to this property</a>

eventSize: optional number

Size of the stored telemetry event in bytes.

minimum0

<a href="#">Link to this property</a>

fingerprint: optional string

Content-based fingerprint used to group similar events.

<a href="#">Link to this property</a>

level: optional string

Log level (e.g. log, debug, info, warn, error).

<a href="#">Link to this property</a>

message: optional string

Log message text.

<a href="#">Link to this property</a>

messageTemplate: optional string

Templatized version of the log message used for grouping similar messages.

<a href="#">Link to this property</a>

metricName: optional string

Metric name when the event represents a metric data point.

<a href="#">Link to this property</a>

origin: optional string

Origin of the event (e.g. fetch, scheduled, queue).

<a href="#">Link to this property</a>

parentSpanId: optional string

Span ID of the parent span in the trace hierarchy.

<a href="#">Link to this property</a>

provider: optional string

Infrastructure provider identifier.

<a href="#">Link to this property</a>

rayId: optional string

Cloudflare Ray ID from the <code>cf-ray</code> header of the request that triggered the invocation.

<a href="#">Link to this property</a>

region: optional string

Cloudflare data center / region that handled the request.

<a href="#">Link to this property</a>

requestId: optional string

Cloudflare request ID that ties all logs from a single invocation together.

<a href="#">Link to this property</a>

service: optional string

Worker script name that produced this event.

<a href="#">Link to this property</a>

spanId: optional string

Span ID for this individual unit of work within a trace.

<a href="#">Link to this property</a>

spanName: optional string

Human-readable name for this span.

<a href="#">Link to this property</a>

<details>

<summary>

spanStatus: optional "unset"or "ok"or "error"

OpenTelemetry span status. Present only on spans. <code>unset</code> when the span did not set a status, including spans recorded before status was captured.

</summary>

One of the following:

"unset"

<a href="#">Link to this property</a>

"ok"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

spanStatusMessage: optional string

OpenTelemetry span status message. Present only on spans when the status is <code>error</code> and a message was set.

<a href="#">Link to this property</a>

stackId: optional string

Stack / deployment identifier.

<a href="#">Link to this property</a>

startTime: optional number

Span start time as a Unix epoch in milliseconds.

minimum0

<a href="#">Link to this property</a>

startTimeNs: optional string

Span start time as a Unix epoch in nanoseconds.

<a href="#">Link to this property</a>

statusCode: optional number

HTTP response status code returned by the Worker.

exclusiveMinimum

minimum0

<a href="#">Link to this property</a>

timestampNs: optional string

Event time as a Unix epoch in nanoseconds.

<a href="#">Link to this property</a>

traceDuration: optional number

Total duration of the entire trace in milliseconds.

exclusiveMinimum

minimum0

<a href="#">Link to this property</a>

traceId: optional string

Distributed trace ID linking spans across services.

<a href="#">Link to this property</a>

transactionName: optional string

Logical transaction name for this request.

<a href="#">Link to this property</a>

trigger: optional string

What triggered the invocation (e.g. GET /users, POST /orders, queue message).

<a href="#">Link to this property</a>

type: optional string

Event type classifier (e.g. cf-worker-event, cf-worker-log).

<a href="#">Link to this property</a>

url: optional string

Request URL that triggered the Worker invocation.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

dataset: string

The dataset this event belongs to (e.g. cloudflare-workers).

<a href="#">Link to this property</a>

<details>

<summary>

source: stringor map\[unknown]

Raw log payload. May be a string or a structured object depending on how the log was emitted.

</summary>

One of the following:

string

<a href="#">Link to this property</a>

map\[unknown]

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

timestamp: number

Event timestamp as a Unix epoch in milliseconds.

minimum0

<a href="#">Link to this property</a>

"$containers": optional map\[unknown]

Cloudflare Containers event information that enriches your logs for identifying and debugging issues.

<a href="#">Link to this property</a>

<details>

<summary>

"$workers": optional object {eventType, scriptName, durableObjectId, 11 more } or object {cpuTimeMs, eventType, outcome, 15 more }

Cloudflare Workers event information that enriches your logs for identifying and debugging issues.

</summary>

One of the following:

<details>

<summary>

object {eventType, scriptName, durableObjectId, 11 more }

</summary>

<details>

<summary>

eventType: "fetch"or "scheduled"or "alarm"or 9 more

</summary>

One of the following:

"fetch"

<a href="#">Link to this property</a>

"scheduled"

<a href="#">Link to this property</a>

"alarm"

<a href="#">Link to this property</a>

"cron"

<a href="#">Link to this property</a>

"queue"

<a href="#">Link to this property</a>

"email"

<a href="#">Link to this property</a>

"tail"

<a href="#">Link to this property</a>

"rpc"

<a href="#">Link to this property</a>

"jsrpc"

<a href="#">Link to this property</a>

"websocket"

<a href="#">Link to this property</a>

"workflow"

<a href="#">Link to this property</a>

"unknown"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

scriptName: string

<a href="#">Link to this property</a>

durableObjectId: optional string

<a href="#">Link to this property</a>

entrypoint: optional string

<a href="#">Link to this property</a>

event: optional map\[unknown]

<a href="#">Link to this property</a>

<details>

<summary>

executionModel: optional "durableObject"or "stateless"

</summary>

One of the following:

"durableObject"

<a href="#">Link to this property</a>

"stateless"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

gateway: optional object {requestId }

</summary>

requestId: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

outcome: optional string

<a href="#">Link to this property</a>

<details>

<summary>

preview: optional object {id, name, slug }

</summary>

id: optional string

<a href="#">Link to this property</a>

name: optional string

<a href="#">Link to this property</a>

slug: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

requestId: optional string

<a href="#">Link to this property</a>

<details>

<summary>

scriptVersion: optional object {id, message, tag }

</summary>

id: optional string

<a href="#">Link to this property</a>

message: optional string

<a href="#">Link to this property</a>

tag: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

spanId: optional string

<a href="#">Link to this property</a>

traceId: optional string

<a href="#">Link to this property</a>

truncated: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object {cpuTimeMs, eventType, outcome, 15 more }

</summary>

cpuTimeMs: number

<a href="#">Link to this property</a>

<details>

<summary>

eventType: "fetch"or "scheduled"or "alarm"or 9 more

</summary>

One of the following:

"fetch"

<a href="#">Link to this property</a>

"scheduled"

<a href="#">Link to this property</a>

"alarm"

<a href="#">Link to this property</a>

"cron"

<a href="#">Link to this property</a>

"queue"

<a href="#">Link to this property</a>

"email"

<a href="#">Link to this property</a>

"tail"

<a href="#">Link to this property</a>

"rpc"

<a href="#">Link to this property</a>

"jsrpc"

<a href="#">Link to this property</a>

"websocket"

<a href="#">Link to this property</a>

"workflow"

<a href="#">Link to this property</a>

"unknown"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

outcome: string

<a href="#">Link to this property</a>

scriptName: string

<a href="#">Link to this property</a>

wallTimeMs: number

<a href="#">Link to this property</a>

<details>

<summary>

diagnosticsChannelEvents: optional array of object {channel, message, timestamp }

</summary>

channel: string

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

timestamp: number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

dispatchNamespace: optional string

<a href="#">Link to this property</a>

durableObjectId: optional string

<a href="#">Link to this property</a>

entrypoint: optional string

<a href="#">Link to this property</a>

event: optional map\[unknown]

<a href="#">Link to this property</a>

<details>

<summary>

executionModel: optional "durableObject"or "stateless"

</summary>

One of the following:

"durableObject"

<a href="#">Link to this property</a>

"stateless"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

gateway: optional object {requestId }

</summary>

requestId: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

preview: optional object {id, name, slug }

</summary>

id: optional string

<a href="#">Link to this property</a>

name: optional string

<a href="#">Link to this property</a>

slug: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

requestId: optional string

<a href="#">Link to this property</a>

<details>

<summary>

scriptVersion: optional object {id, message, tag }

</summary>

id: optional string

<a href="#">Link to this property</a>

message: optional string

<a href="#">Link to this property</a>

tag: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

spanId: optional string

<a href="#">Link to this property</a>

traceId: optional string

<a href="#">Link to this property</a>

truncated: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20events%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

<details>

<summary>

result\_info: object {count, cursors, from, 2 more }

</summary>

count: number

Items returned on this page. Not a total: a page can be short or empty while more results remain.

minimum0

<a href="#">Link to this property</a>

<details>

<summary>

cursors: object {after }

</summary>

after: string

Opaque cursor for the next page. Only null means there are no more results; earlier pages can be short or empty.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

from: number

Effective start of the time window, after defaults and retention clamping.

minimum0

<a href="#">Link to this property</a>

per\_page: number

Maximum items requested for this page.

minimum1

<a href="#">Link to this property</a>

to: number

Effective end of the time window.

minimum0

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20events%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

success: true

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20events%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List Agent Trace events

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/workers/observability/agents/traces/$TRACE_ID/events \
    -H "X-Auth-Email: $CLOUDFLARE_EMAIL" \
    -H "X-Auth-Key: $CLOUDFLARE_API_KEY"
```

200 example

```
{
  "errors": [
    {
      "message": "message"
    }
  ],
  "messages": [
    {
      "message": "Successful request"
    }
  ],
  "result": [
    {
      "$metadata": {
        "id": "id",
        "account": "account",
        "cloudService": "cloudService",
        "coldStart": 1,
        "cost": 1,
        "duration": 1,
        "endTime": 0,
        "endTimeNs": "endTimeNs",
        "error": "error",
        "errorTemplate": "errorTemplate",
        "eventSize": 0,
        "fingerprint": "fingerprint",
        "level": "level",
        "message": "message",
        "messageTemplate": "messageTemplate",
        "metricName": "metricName",
        "origin": "origin",
        "parentSpanId": "parentSpanId",
        "provider": "provider",
        "rayId": "rayId",
        "region": "region",
        "requestId": "requestId",
        "service": "service",
        "spanId": "spanId",
        "spanName": "spanName",
        "spanStatus": "unset",
        "spanStatusMessage": "spanStatusMessage",
        "stackId": "stackId",
        "startTime": 0,
        "startTimeNs": "startTimeNs",
        "statusCode": 1,
        "timestampNs": "timestampNs",
        "traceDuration": 1,
        "traceId": "traceId",
        "transactionName": "transactionName",
        "trigger": "trigger",
        "type": "type",
        "url": "url"
      },
      "dataset": "dataset",
      "source": "string",
      "timestamp": 0,
      "$containers": {
        "foo": "bar"
      },
      "$workers": {
        "eventType": "fetch",
        "scriptName": "scriptName",
        "durableObjectId": "durableObjectId",
        "entrypoint": "entrypoint",
        "event": {
          "foo": "bar"
        },
        "executionModel": "durableObject",
        "gateway": {
          "requestId": "requestId"
        },
        "outcome": "outcome",
        "preview": {
          "id": "id",
          "name": "name",
          "slug": "slug"
        },
        "requestId": "requestId",
        "scriptVersion": {
          "id": "id",
          "message": "message",
          "tag": "tag"
        },
        "spanId": "spanId",
        "traceId": "traceId",
        "truncated": true
      }
    }
  ],
  "result_info": {
    "count": 0,
    "cursors": {
      "after": "after"
    },
    "from": 0,
    "per_page": 1,
    "to": 0
  },
  "success": true
}
```

##### Returns Examples

200 example

```
{
  "errors": [
    {
      "message": "message"
    }
  ],
  "messages": [
    {
      "message": "Successful request"
    }
  ],
  "result": [
    {
      "$metadata": {
        "id": "id",
        "account": "account",
        "cloudService": "cloudService",
        "coldStart": 1,
        "cost": 1,
        "duration": 1,
        "endTime": 0,
        "endTimeNs": "endTimeNs",
        "error": "error",
        "errorTemplate": "errorTemplate",
        "eventSize": 0,
        "fingerprint": "fingerprint",
        "level": "level",
        "message": "message",
        "messageTemplate": "messageTemplate",
        "metricName": "metricName",
        "origin": "origin",
        "parentSpanId": "parentSpanId",
        "provider": "provider",
        "rayId": "rayId",
        "region": "region",
        "requestId": "requestId",
        "service": "service",
        "spanId": "spanId",
        "spanName": "spanName",
        "spanStatus": "unset",
        "spanStatusMessage": "spanStatusMessage",
        "stackId": "stackId",
        "startTime": 0,
        "startTimeNs": "startTimeNs",
        "statusCode": 1,
        "timestampNs": "timestampNs",
        "traceDuration": 1,
        "traceId": "traceId",
        "transactionName": "transactionName",
        "trigger": "trigger",
        "type": "type",
        "url": "url"
      },
      "dataset": "dataset",
      "source": "string",
      "timestamp": 0,
      "$containers": {
        "foo": "bar"
      },
      "$workers": {
        "eventType": "fetch",
        "scriptName": "scriptName",
        "durableObjectId": "durableObjectId",
        "entrypoint": "entrypoint",
        "event": {
          "foo": "bar"
        },
        "executionModel": "durableObject",
        "gateway": {
          "requestId": "requestId"
        },
        "outcome": "outcome",
        "preview": {
          "id": "id",
          "name": "name",
          "slug": "slug"
        },
        "requestId": "requestId",
        "scriptVersion": {
          "id": "id",
          "message": "message",
          "tag": "tag"
        },
        "spanId": "spanId",
        "traceId": "traceId",
        "truncated": true
      }
    }
  ],
  "result_info": {
    "count": 0,
    "cursors": {
      "after": "after"
    },
    "from": 0,
    "per_page": 1,
    "to": 0
  },
  "success": true
}
```