---
title: List issue occurrences
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

# List issue occurrences

GET/accounts/{account\_id}/workers/observability/issues/{issueId}/occurrences

List the retained error occurrences grouped into an issue, newest first.

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

[Link to this property](#)%20workers.observability.issues%20%3E%20(method)%20occurrences%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

issueId: string

Issue ID returned by the issues API.

minLength1

[Link to this property](#)%20workers.observability.issues%20%3E%20(method)%20occurrences%20%3E%20(params)%20default%20%3E%20(param)%20issueId%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

cursor: optional string

Opaque cursor returned in result\_info.cursors.after.

maxLength512

minLength1

[Link to this property](#)%20workers.observability.issues%20%3E%20(method)%20occurrences%20%3E%20(params)%20default%20%3E%20(param)%20cursor%20%3E%20(schema)>)

per\_page: optional number

maximum100

minimum1

[Link to this property](#)%20workers.observability.issues%20%3E%20(method)%20occurrences%20%3E%20(params)%20default%20%3E%20(param)%20per_page%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {message }

</summary>

message: string

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues%20%3E%20(method)%20occurrences%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {message }

</summary>

message: "Successful request"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues%20%3E%20(method)%20occurrences%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: array of object {id, error, invocation, 5 more }

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

[Link to this property](#)%20workers.observability.issues%20%3E%20(method)%20occurrences%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

<details>

<summary>

result\_info: object {count, cursors, per\_page }

</summary>

count: number

minimum0

<a href="#">Link to this property</a>

<details>

<summary>

cursors: object {after }

</summary>

after: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

per\_page: number

minimum1

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.observability.issues%20%3E%20(method)%20occurrences%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

success: true

[Link to this property](#)%20workers.observability.issues%20%3E%20(method)%20occurrences%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List issue occurrences

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/workers/observability/issues/$ISSUE_ID/occurrences \
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
      "id": "id",
      "error": {
        "handled": true,
        "mechanism": "structured-log",
        "message": "message",
        "name": "name",
        "signature": "signature",
        "stack": "stack"
      },
      "invocation": {
        "id": "id",
        "traceId": "traceId",
        "type": "type",
        "batchSize": 0,
        "cron": "cron",
        "jsrpcMethod": "jsrpcMethod",
        "mailFrom": "mailFrom",
        "method": "method",
        "path": "path",
        "queue": "queue",
        "rawSize": 0,
        "rayId": "rayId",
        "rcptTo": "rcptTo",
        "scheduledTime": 0,
        "spanId": "spanId",
        "statusCode": 0,
        "url": "url",
        "websocketCloseCode": 0,
        "websocketEvent": "websocketEvent"
      },
      "timestamp": 0,
      "trail": [
        {
          "level": "level",
          "message": "message",
          "timestamp": 0,
          "type": "log"
        }
      ],
      "worker": {
        "executionModel": "executionModel",
        "scriptName": "scriptName",
        "scriptTags": [
          "string"
        ],
        "dispatchNamespace": "dispatchNamespace",
        "entrypoint": "entrypoint",
        "scriptVersion": {
          "id": "id",
          "tag": "tag"
        }
      },
      "context": {
        "account": "account",
        "session": "session",
        "user": "user"
      },
      "request": {
        "headers": {
          "foo": "string"
        }
      }
    }
  ],
  "result_info": {
    "count": 0,
    "cursors": {
      "after": "after"
    },
    "per_page": 1
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
      "id": "id",
      "error": {
        "handled": true,
        "mechanism": "structured-log",
        "message": "message",
        "name": "name",
        "signature": "signature",
        "stack": "stack"
      },
      "invocation": {
        "id": "id",
        "traceId": "traceId",
        "type": "type",
        "batchSize": 0,
        "cron": "cron",
        "jsrpcMethod": "jsrpcMethod",
        "mailFrom": "mailFrom",
        "method": "method",
        "path": "path",
        "queue": "queue",
        "rawSize": 0,
        "rayId": "rayId",
        "rcptTo": "rcptTo",
        "scheduledTime": 0,
        "spanId": "spanId",
        "statusCode": 0,
        "url": "url",
        "websocketCloseCode": 0,
        "websocketEvent": "websocketEvent"
      },
      "timestamp": 0,
      "trail": [
        {
          "level": "level",
          "message": "message",
          "timestamp": 0,
          "type": "log"
        }
      ],
      "worker": {
        "executionModel": "executionModel",
        "scriptName": "scriptName",
        "scriptTags": [
          "string"
        ],
        "dispatchNamespace": "dispatchNamespace",
        "entrypoint": "entrypoint",
        "scriptVersion": {
          "id": "id",
          "tag": "tag"
        }
      },
      "context": {
        "account": "account",
        "session": "session",
        "user": "user"
      },
      "request": {
        "headers": {
          "foo": "string"
        }
      }
    }
  ],
  "result_info": {
    "count": 0,
    "cursors": {
      "after": "after"
    },
    "per_page": 1
  },
  "success": true
}
```