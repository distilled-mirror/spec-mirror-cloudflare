---
title: List Agent Traces
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

# List Agent Traces

GET/accounts/{account\_id}/workers/observability/agents/traces

Lists Traces with Agent activity in the window, newest activity first, including work without a Conversation ID. The window defaults to the last 24 hours. Each summary covers the Trace’s Agent spans (invoke\_agent, chat, execute\_tool): the Agents and Conversation IDs seen, duration, token usage, models, providers, and LLM call, tool call and error counts.

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

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

agent: optional string

Only include work in which an Agent with this gen\_ai.agent.name took part. With service, both must match the same Agent.

maxLength512

minLength1

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20agent%20%3E%20(schema)>)

cursor: optional string

Opaque cursor from result\_info.cursors.after in the previous response. Send it with the same filters; its window replaces from and to.

maxLength4096

minLength1

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20cursor%20%3E%20(schema)>)

from: optional number

Start of the search window, as Unix epoch milliseconds. Defaults to 24 hours before to. Clamped to the 7-day retention boundary; the effective value is in result\_info.from.

minimum0

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20from%20%3E%20(schema)>)

per\_page: optional number

Maximum items to return per page. Defaults to 20.

maximum100

minimum1

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20per_page%20%3E%20(schema)>)

service: optional string

Only include work in which an Agent of this Worker service took part.

maxLength512

minLength1

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20service%20%3E%20(schema)>)

to: optional number

End of the search window, as Unix epoch milliseconds. Defaults to now.

minimum0

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20to%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {message }

</summary>

message: "Successful request"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: array of object {agents, conversationIds, errorCount, 19 more }

</summary>

agents: array of string

Sorted distinct gen\_ai.agent.name values of authorized Agent invocations in the Trace within the effective window. Includes every Agent in the Trace, not only those matching the agent filter.

<a href="#">Link to this property</a>

conversationIds: array of string

Sorted distinct gen\_ai.conversation.id values of authorized Agent invocations in the Trace within the effective window. Empty when none are recorded.

<a href="#">Link to this property</a>

errorCount: number

Agent spans that recorded an error.

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

Name of the first Agent span in the Trace.

<a href="#">Link to this property</a>

rootTransactionName: string

Transaction name of the first Agent span in the Trace.

<a href="#">Link to this property</a>

services: array of string

Authorized Worker services represented in the trace.

<a href="#">Link to this property</a>

spans: number

Agent spans in the Trace.

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

Duration of the Trace’s Agent activity, in milliseconds.

<a href="#">Link to this property</a>

traceEndMs: number

End of the Trace’s Agent activity, as Unix epoch milliseconds.

<a href="#">Link to this property</a>

traceId: string

Unique identifier for the distributed trace.

<a href="#">Link to this property</a>

traceStartMs: number

Start of the Trace’s Agent activity, as Unix epoch milliseconds.

<a href="#">Link to this property</a>

errors: optional array of string

Error messages encountered during the trace, if any.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

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

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

success: true

[Link to this property](#)%20workers.observability.agents.traces%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List Agent Traces

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/workers/observability/agents/traces \
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
      "agents": [
        "string"
      ],
      "conversationIds": [
        "string"
      ],
      "errorCount": 0,
      "inputTokens": 0,
      "lastActivityMs": 0,
      "llmCallCount": 0,
      "llmErrorCount": 0,
      "models": [
        "string"
      ],
      "outputTokens": 0,
      "providers": [
        "string"
      ],
      "rootSpanName": "rootSpanName",
      "rootTransactionName": "rootTransactionName",
      "services": [
        "string"
      ],
      "spans": 0,
      "toolCallCount": 0,
      "toolErrorCount": 0,
      "totalTokens": 0,
      "traceDurationMs": 0,
      "traceEndMs": 0,
      "traceId": "traceId",
      "traceStartMs": 0,
      "errors": [
        "string"
      ]
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
      "agents": [
        "string"
      ],
      "conversationIds": [
        "string"
      ],
      "errorCount": 0,
      "inputTokens": 0,
      "lastActivityMs": 0,
      "llmCallCount": 0,
      "llmErrorCount": 0,
      "models": [
        "string"
      ],
      "outputTokens": 0,
      "providers": [
        "string"
      ],
      "rootSpanName": "rootSpanName",
      "rootTransactionName": "rootTransactionName",
      "services": [
        "string"
      ],
      "spans": 0,
      "toolCallCount": 0,
      "toolErrorCount": 0,
      "totalTokens": 0,
      "traceDurationMs": 0,
      "traceEndMs": 0,
      "traceId": "traceId",
      "traceStartMs": 0,
      "errors": [
        "string"
      ]
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