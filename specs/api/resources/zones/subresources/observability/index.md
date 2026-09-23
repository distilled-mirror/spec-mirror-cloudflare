---
title: Observability
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zones](https://developers.cloudflare.com/api/resources/zones)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Observability

#### ObservabilityTracing

#### ObservabilityTracingSettings

##### [View zone tracing settings](https://developers.cloudflare.com/api/resources/zones/subresources/observability/subresources/tracing/subresources/settings/methods/get)

GET/zones/{zone\_id}/observability/tracing/settings

##### [Update zone tracing settings](https://developers.cloudflare.com/api/resources/zones/subresources/observability/subresources/tracing/subresources/settings/methods/update)

PATCH/zones/{zone\_id}/observability/tracing/settings

##### [Reset zone tracing settings](https://developers.cloudflare.com/api/resources/zones/subresources/observability/subresources/tracing/subresources/settings/methods/delete)

DELETE/zones/{zone\_id}/observability/tracing/settings

##### ModelsExpand Collapse

<details>

<summary>

SettingGetResponse object {destinations, enabled, forward\_context, 3 more }

</summary>

destinations: array of string

Up to 100 OpenTelemetry destination identifiers that receive traces.

<a href="#">Link to this property</a>

enabled: boolean

Whether Cloudflare Traces is enabled for the zone.

<a href="#">Link to this property</a>

forward\_context: boolean

Whether trace context is sent externally or across a zone boundary.

<a href="#">Link to this property</a>

persist: boolean

Whether traces are persisted in Cloudflare.

<a href="#">Link to this property</a>

<details>

<summary>

propagation\_policy: "accept"or "authenticated"or "reject"

When inbound trace context may be continued. Authenticated propagation is not supported yet.

</summary>

One of the following:

"accept"

<a href="#">Link to this property</a>

"authenticated"

<a href="#">Link to this property</a>

"reject"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

sampling\_ratio: number

The ratio of requests sampled for tracing, from 0 to 1.

maximum1

minimum0

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zones.observability.tracing.settings%20%3E%20(model)%20setting_get_response%20%3E%20(schema)>)

<details>

<summary>

SettingUpdateResponse object {destinations, enabled, forward\_context, 3 more }

</summary>

destinations: array of string

Up to 100 OpenTelemetry destination identifiers that receive traces.

<a href="#">Link to this property</a>

enabled: boolean

Whether Cloudflare Traces is enabled for the zone.

<a href="#">Link to this property</a>

forward\_context: boolean

Whether trace context is sent externally or across a zone boundary.

<a href="#">Link to this property</a>

persist: boolean

Whether traces are persisted in Cloudflare.

<a href="#">Link to this property</a>

<details>

<summary>

propagation\_policy: "accept"or "authenticated"or "reject"

When inbound trace context may be continued. Authenticated propagation is not supported yet.

</summary>

One of the following:

"accept"

<a href="#">Link to this property</a>

"authenticated"

<a href="#">Link to this property</a>

"reject"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

sampling\_ratio: number

The ratio of requests sampled for tracing, from 0 to 1.

maximum1

minimum0

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zones.observability.tracing.settings%20%3E%20(model)%20setting_update_response%20%3E%20(schema)>)

<details>

<summary>

SettingDeleteResponse object {destinations, enabled, forward\_context, 3 more }

</summary>

destinations: array of string

Up to 100 OpenTelemetry destination identifiers that receive traces.

<a href="#">Link to this property</a>

enabled: boolean

Whether Cloudflare Traces is enabled for the zone.

<a href="#">Link to this property</a>

forward\_context: boolean

Whether trace context is sent externally or across a zone boundary.

<a href="#">Link to this property</a>

persist: boolean

Whether traces are persisted in Cloudflare.

<a href="#">Link to this property</a>

<details>

<summary>

propagation\_policy: "accept"or "authenticated"or "reject"

When inbound trace context may be continued. Authenticated propagation is not supported yet.

</summary>

One of the following:

"accept"

<a href="#">Link to this property</a>

"authenticated"

<a href="#">Link to this property</a>

"reject"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

sampling\_ratio: number

The ratio of requests sampled for tracing, from 0 to 1.

maximum1

minimum0

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zones.observability.tracing.settings%20%3E%20(model)%20setting_delete_response%20%3E%20(schema)>)

#### ObservabilityTracingRules

##### [View zone trace rules](https://developers.cloudflare.com/api/resources/zones/subresources/observability/subresources/tracing/subresources/rules/methods/get)

GET/zones/{zone\_id}/observability/tracing/rules

##### [Replace zone trace rules](https://developers.cloudflare.com/api/resources/zones/subresources/observability/subresources/tracing/subresources/rules/methods/update)

PUT/zones/{zone\_id}/observability/tracing/rules

##### [Delete zone trace rules](https://developers.cloudflare.com/api/resources/zones/subresources/observability/subresources/tracing/subresources/rules/methods/delete)

DELETE/zones/{zone\_id}/observability/tracing/rules

##### ModelsExpand Collapse

<details>

<summary>

RuleGetResponse object {rules }

</summary>

<details>

<summary>

rules: array of object {action, action\_parameters, description, 2 more }

Trace rules in evaluation order.

</summary>

action: "set\_trace\_settings"

<a href="#">Link to this property</a>

<details>

<summary>

action\_parameters: object {sampling\_ratio }

</summary>

sampling\_ratio: number

The ratio of requests sampled for tracing, from 0 to 1.

maximum1

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

description: string

maxLength1000

<a href="#">Link to this property</a>

enabled: boolean

<a href="#">Link to this property</a>

expression: string

A Rules language expression that selects requests.

maxLength4096

minLength1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zones.observability.tracing.rules%20%3E%20(model)%20rule_get_response%20%3E%20(schema)>)

<details>

<summary>

RuleUpdateResponse object {rules }

</summary>

<details>

<summary>

rules: array of object {action, action\_parameters, description, 2 more }

Trace rules in evaluation order.

</summary>

action: "set\_trace\_settings"

<a href="#">Link to this property</a>

<details>

<summary>

action\_parameters: object {sampling\_ratio }

</summary>

sampling\_ratio: number

The ratio of requests sampled for tracing, from 0 to 1.

maximum1

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

description: string

maxLength1000

<a href="#">Link to this property</a>

enabled: boolean

<a href="#">Link to this property</a>

expression: string

A Rules language expression that selects requests.

maxLength4096

minLength1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zones.observability.tracing.rules%20%3E%20(model)%20rule_update_response%20%3E%20(schema)>)

<details>

<summary>

RuleDeleteResponse object {rules }

</summary>

<details>

<summary>

rules: array of object {action, action\_parameters, description, 2 more }

Trace rules in evaluation order.

</summary>

action: "set\_trace\_settings"

<a href="#">Link to this property</a>

<details>

<summary>

action\_parameters: object {sampling\_ratio }

</summary>

sampling\_ratio: number

The ratio of requests sampled for tracing, from 0 to 1.

maximum1

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

description: string

maxLength1000

<a href="#">Link to this property</a>

enabled: boolean

<a href="#">Link to this property</a>

expression: string

A Rules language expression that selects requests.

maxLength4096

minLength1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zones.observability.tracing.rules%20%3E%20(model)%20rule_delete_response%20%3E%20(schema)>)