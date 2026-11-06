---
title: Agents
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Workers](https://developers.cloudflare.com/api/resources/workers)

[Observability](https://developers.cloudflare.com/api/resources/workers/subresources/observability)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Agents

#### AgentsTraces

##### [List Agent Traces](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/agents/subresources/traces/methods/list)

GET/accounts/{account\_id}/workers/observability/agents/traces

##### [Get an Agent Trace](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/agents/subresources/traces/methods/get)

GET/accounts/{account\_id}/workers/observability/agents/traces/{traceId}

##### [List Agent Trace events](https://developers.cloudflare.com/api/resources/workers/subresources/observability/subresources/agents/subresources/traces/methods/events)

GET/accounts/{account\_id}/workers/observability/agents/traces/{traceId}/events

##### ModelsExpand Collapse

<details>

<summary>

TraceListResponse object {agents, conversationIds, errorCount, 19 more }

</summary>

agents: array of string

Sorted distinct gen\_ai.agent.name values of authorized Agent invocations in the Trace within the effective window. Includes every Agent in the Trace, not only those matching the agent filter.

<a href="#">Link to this property</a>

conversationIds: array of string

Sorted distinct gen\_ai.conversation.id values of authorized Agent invocations in the Trace within the effective window. Empty when none are recorded.

<a href="#">Link to this property</a>

errorCount: number

Recorded spans with a nonempty error or ERROR status. Counts spans, not distinct messages or incidents.

minimum0

<a href="#">Link to this property</a>

inputTokens: number

Input tokens reported by chat spans in the authorized Trace window; null when none report input usage. Informational, not billing data.

minimum0

<a href="#">Link to this property</a>

lastActivityMs: number

Latest start of an authorized Agent invocation in the Trace within the effective window, as Unix epoch milliseconds. The Trace list is ordered by this value, newest first.

minimum0

<a href="#">Link to this property</a>

llmCallCount: number

Recorded chat spans in the authorized Trace window.

minimum0

<a href="#">Link to this property</a>

llmErrorCount: number

Recorded chat spans with a nonempty error or ERROR status.

minimum0

<a href="#">Link to this property</a>

models: array of string

Sorted distinct response models, falling back to request models, from chat spans in the authorized Trace window.

<a href="#">Link to this property</a>

outputTokens: number

Output tokens reported by chat spans in the authorized Trace window; null when none report output usage. Informational, not billing data.

minimum0

<a href="#">Link to this property</a>

providers: array of string

Sorted distinct GenAI providers from chat spans in the authorized Trace window.

<a href="#">Link to this property</a>

rootSpanName: string

Name of the root span that initiated the trace.

<a href="#">Link to this property</a>

rootTransactionName: string

Logical transaction name for the root span.

<a href="#">Link to this property</a>

services: array of string

Authorized Worker services represented in the trace.

<a href="#">Link to this property</a>

spans: number

Total number of spans in the trace.

<a href="#">Link to this property</a>

toolCallCount: number

Recorded execute\_tool spans in the authorized Trace window. Custom-named approval spans are not counted.

minimum0

<a href="#">Link to this property</a>

toolErrorCount: number

Recorded execute\_tool spans with a nonempty error or ERROR status.

minimum0

<a href="#">Link to this property</a>

totalTokens: number

Input plus output tokens; null if either direction is unreported. Does not add cache or reasoning breakdowns.

minimum0

<a href="#">Link to this property</a>

traceDurationMs: number

Total duration of the trace in milliseconds.

<a href="#">Link to this property</a>

traceEndMs: number

Trace end time as a Unix epoch in milliseconds.

<a href="#">Link to this property</a>

traceId: string

Unique identifier for the distributed trace.

<a href="#">Link to this property</a>

traceStartMs: number

Trace start time as a Unix epoch in milliseconds.

<a href="#">Link to this property</a>

errors: optional array of string

Error messages encountered during the trace, if any.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(model)%20trace_list_response%20%3E%20(schema)>)

<details>

<summary>

TraceGetResponse object {agents, conversationIds, errorCount, 19 more }

</summary>

agents: array of string

Sorted distinct gen\_ai.agent.name values of authorized Agent invocations in the Trace within the effective window. Includes every Agent in the Trace, not only those matching the agent filter.

<a href="#">Link to this property</a>

conversationIds: array of string

Sorted distinct gen\_ai.conversation.id values of authorized Agent invocations in the Trace within the effective window. Empty when none are recorded.

<a href="#">Link to this property</a>

errorCount: number

Recorded spans with a nonempty error or ERROR status. Counts spans, not distinct messages or incidents.

minimum0

<a href="#">Link to this property</a>

inputTokens: number

Input tokens reported by chat spans in the authorized Trace window; null when none report input usage. Informational, not billing data.

minimum0

<a href="#">Link to this property</a>

lastActivityMs: number

Latest start of an authorized Agent invocation in the Trace within the effective window, as Unix epoch milliseconds. The Trace list is ordered by this value, newest first.

minimum0

<a href="#">Link to this property</a>

llmCallCount: number

Recorded chat spans in the authorized Trace window.

minimum0

<a href="#">Link to this property</a>

llmErrorCount: number

Recorded chat spans with a nonempty error or ERROR status.

minimum0

<a href="#">Link to this property</a>

models: array of string

Sorted distinct response models, falling back to request models, from chat spans in the authorized Trace window.

<a href="#">Link to this property</a>

outputTokens: number

Output tokens reported by chat spans in the authorized Trace window; null when none report output usage. Informational, not billing data.

minimum0

<a href="#">Link to this property</a>

providers: array of string

Sorted distinct GenAI providers from chat spans in the authorized Trace window.

<a href="#">Link to this property</a>

rootSpanName: string

Name of the root span that initiated the trace.

<a href="#">Link to this property</a>

rootTransactionName: string

Logical transaction name for the root span.

<a href="#">Link to this property</a>

services: array of string

Authorized Worker services represented in the trace.

<a href="#">Link to this property</a>

spans: number

Total number of spans in the trace.

<a href="#">Link to this property</a>

toolCallCount: number

Recorded execute\_tool spans in the authorized Trace window. Custom-named approval spans are not counted.

minimum0

<a href="#">Link to this property</a>

toolErrorCount: number

Recorded execute\_tool spans with a nonempty error or ERROR status.

minimum0

<a href="#">Link to this property</a>

totalTokens: number

Input plus output tokens; null if either direction is unreported. Does not add cache or reasoning breakdowns.

minimum0

<a href="#">Link to this property</a>

traceDurationMs: number

Total duration of the trace in milliseconds.

<a href="#">Link to this property</a>

traceEndMs: number

Trace end time as a Unix epoch in milliseconds.

<a href="#">Link to this property</a>

traceId: string

Unique identifier for the distributed trace.

<a href="#">Link to this property</a>

traceStartMs: number

Trace start time as a Unix epoch in milliseconds.

<a href="#">Link to this property</a>

errors: optional array of string

Error messages encountered during the trace, if any.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(model)%20trace_get_response%20%3E%20(schema)>)

<details>

<summary>

TraceEventsResponse = array of object {"$metadata", dataset, source, 3 more }

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

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(model)%20trace_events_response%20%3E%20(schema)>)