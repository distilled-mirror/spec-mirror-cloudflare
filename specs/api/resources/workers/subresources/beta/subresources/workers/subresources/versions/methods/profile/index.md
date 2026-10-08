---
title: Profile Worker Version
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Workers](https://developers.cloudflare.com/api/resources/workers)

[Beta](https://developers.cloudflare.com/api/resources/workers/subresources/beta)

[Workers](https://developers.cloudflare.com/api/resources/workers/subresources/beta/subresources/workers)

[Versions](https://developers.cloudflare.com/api/resources/workers/subresources/beta/subresources/workers/subresources/versions)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Profile Worker Version

POST/accounts/{account\_id}/workers/workers/{worker\_id}/versions/{version\_id}/profile

Captures a CPU or heap profile from a recently active isolate running the specified Worker version. This endpoint requires the Worker profiling feature to be enabled for the account.

##### Security

<details>

<summary>API Token</summary>



The preferred authorization scheme for interacting with the Cloudflare API. <a href="https://developers.cloudflare.com/fundamentals/api/get-started/create-token/">Create a token</a>.

**Example:**<code>Authorization: Bearer Sn3lZJTBX6kkg7OdcBUAxOO963GEIyGQqnFTOFYY</code>

</details>

<details>

<summary>API Email + API Key</summary>



The previous authorization scheme for interacting with the Cloudflare API, used in conjunction with a Global API key.

**Example:**<code>X-Auth-Email: user@example.com</code>

The previous authorization scheme for interacting with the Cloudflare API. When possible, use API tokens instead of Global API keys.

**Example:**<code>X-Auth-Key: 144c9defac04969c7bfad8efaa8ea194</code>

</details>

##### P ath ParametersExpand Collapse

account\_id: string

Identifier.

maxLength32

[Link to this property](#)%20workers.beta.workers.versions%20%3E%20(method)%20profile%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

worker\_id: string

Identifies the Worker by ID or name.

[Link to this property](#)%20workers.beta.workers.versions%20%3E%20(method)%20profile%20%3E%20(params)%20default%20%3E%20(param)%20worker_id%20%3E%20(schema)>)

version\_id: string

Identifies the version by UUID or UUID prefix with a minimum length of eight characters. Use “latest” to select the most recently created version.

[Link to this property](#)%20workers.beta.workers.versions%20%3E%20(method)%20profile%20%3E%20(params)%20default%20%3E%20(param)%20version_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

duration\_ms: number

Profile duration in milliseconds.

formatint32

maximum50000

minimum1000

[Link to this property](#)%20workers.beta.workers.versions%20%3E%20(method)%20profile%20%3E%20(params)%200%20%3E%20(param)%20duration_ms%20%3E%20(schema)>)

actor\_id: optional string

Identifies the exact Durable Object actor to profile. Must be specified together with namespace\_id. The actor must currently be active and running the requested Worker version.

[Link to this property](#)%20workers.beta.workers.versions%20%3E%20(method)%20profile%20%3E%20(params)%200%20%3E%20(param)%20actor_id%20%3E%20(schema)>)

namespace\_id: optional string

Identifies the Durable Object namespace containing the actor to profile. Must be specified together with actor\_id.

[Link to this property](#)%20workers.beta.workers.versions%20%3E%20(method)%20profile%20%3E%20(params)%200%20%3E%20(param)%20namespace_id%20%3E%20(schema)>)

<details>

<summary>

profile\_type: optional "cpu"or "heap"

</summary>

One of the following:

"cpu"

<a href="#">Link to this property</a>

"heap"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20workers.beta.workers.versions%20%3E%20(method)%20profile%20%3E%20(params)%200%20%3E%20(param)%20profile_type%20%3E%20(schema)>)

### Profile Worker Version

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/workers/workers/$WORKER_ID/versions/$VERSION_ID/profile \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "duration_ms": 1000
        }'
```

##### Returns Examples