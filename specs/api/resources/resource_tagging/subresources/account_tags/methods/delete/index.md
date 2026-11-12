---
title: Delete tags from an account-level resource
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Resource Tagging](https://developers.cloudflare.com/api/resources/resource_tagging)

[Account Tags](https://developers.cloudflare.com/api/resources/resource_tagging/subresources/account_tags)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Delete tags from an account-level resource

DELETE/accounts/{account\_id}/tags

Removes all tags from a specific account-level resource.

##### Security

API Email + API Key

The previous authorization scheme for interacting with the Cloudflare API, used in conjunction with a Global API key.

**Example:**`X-Auth-Email: user@example.com`

The previous authorization scheme for interacting with the Cloudflare API. When possible, use API tokens instead of Global API keys.

**Example:**`X-Auth-Key: 144c9defac04969c7bfad8efaa8ea194`

##### P ath ParametersExpand Collapse

account\_id: string

Identifier.

maxLength32

minLength32

[Link to this property](#)%20resource_tagging.account_tags%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

resource\_id: string

The ID of the resource to remove tags from.

[Link to this property](#)%20resource_tagging.account_tags%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20resource_id%20%3E%20(schema)>)

<details>

<summary>

resource\_type: "access\_application"or "access\_group"or "access\_service\_token"or 32 more

The type of the resource.

</summary>

One of the following:

"access\_application"

<a href="#">Link to this property</a>

"access\_group"

<a href="#">Link to this property</a>

"access\_service\_token"

<a href="#">Link to this property</a>

"account"

<a href="#">Link to this property</a>

"account\_ruleset"

<a href="#">Link to this property</a>

"ai\_gateway"

<a href="#">Link to this property</a>

"ai\_search\_instance"

<a href="#">Link to this property</a>

"ai\_search\_namespace"

<a href="#">Link to this property</a>

"alerting\_policy"

<a href="#">Link to this property</a>

"alerting\_webhook"

<a href="#">Link to this property</a>

"cloudflared\_tunnel"

<a href="#">Link to this property</a>

"cws\_deployment"

<a href="#">Link to this property</a>

"cws\_policy"

<a href="#">Link to this property</a>

"cws\_policy\_set"

<a href="#">Link to this property</a>

"cws\_workload"

<a href="#">Link to this property</a>

"d1\_database"

<a href="#">Link to this property</a>

"device"

<a href="#">Link to this property</a>

"durable\_object\_namespace"

<a href="#">Link to this property</a>

"gateway\_list"

<a href="#">Link to this property</a>

"gateway\_rule"

<a href="#">Link to this property</a>

"image"

<a href="#">Link to this property</a>

"infrastructure\_target"

<a href="#">Link to this property</a>

"kv\_namespace"

<a href="#">Link to this property</a>

"load\_balancer\_monitor"

<a href="#">Link to this property</a>

"load\_balancer\_pool"

<a href="#">Link to this property</a>

"namespace\_worker"

<a href="#">Link to this property</a>

"pages\_project"

<a href="#">Link to this property</a>

"queue"

<a href="#">Link to this property</a>

"r2\_bucket"

<a href="#">Link to this property</a>

"resource\_share"

<a href="#">Link to this property</a>

"stream\_live\_input"

<a href="#">Link to this property</a>

"stream\_video"

<a href="#">Link to this property</a>

"vectorize\_index"

<a href="#">Link to this property</a>

"worker"

<a href="#">Link to this property</a>

"worker\_version"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20resource_tagging.account_tags%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20resource_type%20%3E%20(schema)>)

worker\_id: optional string

Worker identifier. Required for worker\_version resources.

[Link to this property](#)%20resource_tagging.account_tags%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20worker_id%20%3E%20(schema)>)

##### H eader ParametersExpand Collapse

"If-Match": optional string

[Link to this property](#)%20resource_tagging.account_tags%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20If-Match%20%3E%20(schema)>)

### Delete tags from an account-level resource

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/tags \
    -X DELETE \
    -H "X-Auth-Email: $CLOUDFLARE_EMAIL" \
    -H "X-Auth-Key: $CLOUDFLARE_API_KEY"
```

##### Returns Examples