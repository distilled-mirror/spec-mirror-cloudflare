# Get an account or zone entry point ruleset version

GET/{accounts_or_zones}/{account_or_zone_id}/rulesets/phases/{ruleset_phase}/entrypoint/versions/{ruleset_version}

Fetches a specific version of an account or zone entry point ruleset.

##### Path Parameters

<details>

<summary>

ruleset_phase: [Phase](/api/resources/rulesets#(resource)%20rulesets%20%3E%20(model)%20phase%20%3E%20(schema))

The phase of the ruleset.

</summary>

One of the following:

"ddos_l4"

[Link to this property](#)

"ddos_l7"

[Link to this property](#)

"http_config_settings"

[Link to this property](#)

"http_custom_errors"

[Link to this property](#)

"http_log_custom_fields"

[Link to this property](#)

"http_ratelimit"

[Link to this property](#)

"http_request_cache_settings"

[Link to this property](#)

"http_request_dynamic_redirect"

[Link to this property](#)

"http_request_firewall_custom"

[Link to this property](#)

"http_request_firewall_managed"

[Link to this property](#)

"http_request_late_transform"

[Link to this property](#)

"http_request_origin"

[Link to this property](#)

"http_request_redirect"

[Link to this property](#)

"http_request_sanitize"

[Link to this property](#)

"http_request_sbfm"

[Link to this property](#)

"http_request_transform"

[Link to this property](#)

"http_response_cache_settings"

[Link to this property](#)

"http_response_compression"

[Link to this property](#)

"http_response_firewall_custom"

[Link to this property](#)

"http_response_firewall_managed"

[Link to this property](#)

"http_response_headers_transform"

[Link to this property](#)

"magic_transit"

[Link to this property](#)

"magic_transit_ids_managed"

[Link to this property](#)

"magic_transit_managed"

[Link to this property](#)

"magic_transit_ratelimit"

[Link to this property](#)

</details>

[Link to this property](#)

ruleset_version: string

The version of the ruleset.

[Link to this property](#)

account_id: optional string

The Account ID to use for this endpoint. Mutually exclusive with the Zone ID.

[Link to this property](#)

zone_id: optional string

The Zone ID to use for this endpoint. Mutually exclusive with the Account ID.

[Link to this property](#)

##### Returns

<details>

<summary>

errors: array of object { message, code, source }

A list of error messages.

</summary>

message: string

A text description of this message.

minLength1

[Link to this property](#)

code: optional number

A unique code for this message.

[Link to this property](#)

<details>

<summary>

source: optional object { pointer }

The source of this message.

</summary>

pointer: string

A JSON pointer to the field that is the source of the message.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

messages: array of object { message, code, source }

A list of warning messages.

</summary>

message: string

A text description of this message.

minLength1

[Link to this property](#)

code: optional number

A unique code for this message.

[Link to this property](#)

<details>

<summary>

source: optional object { pointer }

The source of this message.

</summary>

pointer: string

A JSON pointer to the field that is the source of the message.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

result: object { id, description, kind, 5 more } or object { id, description, kind, 5 more } or object { id, description, kind, 5 more } or 2 more

A result.

</summary>

One of the following:

<details>

<summary>

object { id, description, kind, 5 more }

</summary>

id: optional string

The unique ID of the ruleset.

[Link to this property](#)

description: optional string

An informative description of the ruleset.

[Link to this property](#)

<details>

<summary>

kind: optional [Kind](/api/resources/rulesets#(resource)%20rulesets%20%3E%20(model)%20kind%20%3E%20(schema))

The kind of the ruleset.

</summary>

One of the following:

"managed"

[Link to this property](#)

"custom"

[Link to this property](#)

"root"

[Link to this property](#)

"zone"

[Link to this property](#)

</details>

[Link to this property](#)

last_updated: optional string

The timestamp of when the ruleset was last modified.

formatdate-time

[Link to this property](#)

name: optional string

The human-readable name of the ruleset.

minLength1

[Link to this property](#)

<details>

<summary>

phase: optional [Phase](/api/resources/rulesets#(resource)%20rulesets%20%3E%20(model)%20phase%20%3E%20(schema))

The phase of the ruleset.

</summary>

One of the following:

"ddos_l4"

[Link to this property](#)

"ddos_l7"

[Link to this property](#)

"http_config_settings"

[Link to this property](#)

"http_custom_errors"

[Link to this property](#)

"http_log_custom_fields"

[Link to this property](#)

"http_ratelimit"

[Link to this property](#)

"http_request_cache_settings"

[Link to this property](#)

"http_request_dynamic_redirect"

[Link to this property](#)

"http_request_firewall_custom"

[Link to this property](#)

"http_request_firewall_managed"

[Link to this property](#)

"http_request_late_transform"

[Link to this property](#)

"http_request_origin"

[Link to this property](#)

"http_request_redirect"

[Link to this property](#)

"http_request_sanitize"

[Link to this property](#)

"http_request_sbfm"

[Link to this property](#)

"http_request_transform"

[Link to this property](#)

"http_response_cache_settings"

[Link to this property](#)

"http_response_compression"

[Link to this property](#)

"http_response_firewall_custom"

[Link to this property](#)

"http_response_firewall_managed"

[Link to this property](#)

"http_response_headers_transform"

[Link to this property](#)

"magic_transit"

[Link to this property](#)

"magic_transit_ids_managed"

[Link to this property](#)

"magic_transit_managed"

[Link to this property](#)

"magic_transit_ratelimit"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

rules: optional array of [BlockRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20block_rule%20%3E%20(schema)) { last_updated, version, id, 10 more } or object { id, action, enabled, 10 more } or [CompressResponseRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20compress_response_rule%20%3E%20(schema)) { last_updated, version, id, 10 more } or 18 more

The list of rules in the ruleset.

</summary>

One of the following:

<details>

<summary>

BlockRule = [BlockRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20block_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ChallengeRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "challenge"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

Whether the rule should be executed.

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

action_parameters: optional unknown

The parameters configuring the rule’s action.

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ResponseCompressionRule = [CompressResponseRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20compress_response_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DDoSDynamicRule = [DDoSDynamicRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20ddos_dynamic_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ExecuteRule = [ExecuteRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20execute_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ForceConnectionCloseRule = [ForceConnectionCloseRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20force_connection_close_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

JavaScriptChallengeRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "js_challenge"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

Whether the rule should be executed.

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

action_parameters: optional unknown

The parameters configuring the rule’s action.

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

LogRule = [LogRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20log_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

LogCustomFieldRule = [LogCustomFieldRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20log_custom_field_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ManagedChallengeRule = [ManagedChallengeRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20managed_challenge_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RedirectRule = [RedirectRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20redirect_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RewriteRule = [RewriteRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20rewrite_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RouteRule = [RouteRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20route_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ScoreRule = [ScoreRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20score_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ServeErrorRule = [ServeErrorRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20serve_error_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheControlRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "set_cache_control"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

<details>

<summary>

action_parameters: optional object { immutable, "max-age", "must-revalidate", 10 more }

The parameters configuring the rule’s action.

</summary>

<details>

<summary>

immutable: optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"max-age": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"must-revalidate": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"must-understand": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"no-cache": optional object { operation, cloudflare_only, qualifiers } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts optional qualifiers (header names).

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only, qualifiers }

Set the directive with optional qualifiers.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

qualifiers: optional array of string

Optional list of header names to qualify the directive (e.g., for “private” or “no-cache” directives).

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"no-store": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"no-transform": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

private: optional object { operation, cloudflare_only, qualifiers } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts optional qualifiers (header names).

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only, qualifiers }

Set the directive with optional qualifiers.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

qualifiers: optional array of string

Optional list of header names to qualify the directive (e.g., for “private” or “no-cache” directives).

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"proxy-revalidate": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

public: optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"s-maxage": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"stale-if-error": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"stale-while-revalidate": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheSettingsRule = [SetCacheSettingsRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20set_cache_settings_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheTagsRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "set_cache_tags"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

<details>

<summary>

action_parameters: optional object { operation, values } or object { expression, operation } or object { operation, values } or 3 more

The parameters configuring the rule’s action.

</summary>

One of the following:

<details>

<summary>

AddCacheTagsValues object { operation, values }

Add cache tags using a list of values.

</summary>

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

values: array of string

A list of cache tag values.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

AddCacheTagsExpression object { expression, operation }

Add cache tags using an expression.

</summary>

expression: string

An expression that evaluates to an array of cache tag values.

minLength1

[Link to this property](#)

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveCacheTagsValues object { operation, values }

Remove cache tags using a list of values.

</summary>

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

values: array of string

A list of cache tag values.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveCacheTagsExpression object { expression, operation }

Remove cache tags using an expression.

</summary>

expression: string

An expression that evaluates to an array of cache tag values.

minLength1

[Link to this property](#)

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheTagsValues object { operation, values }

Set cache tags using a list of values.

</summary>

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

values: array of string

A list of cache tag values.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheTagsExpression object { expression, operation }

Set cache tags using an expression.

</summary>

expression: string

An expression that evaluates to an array of cache tag values.

minLength1

[Link to this property](#)

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetConfigurationRule = [SetConfigRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20set_config_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SkipRule = [SkipRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20skip_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

TransformResponseHTMLRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "transform_response_html"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

<details>

<summary>

action_parameters: optional object { link_maze }

The parameters configuring the rule’s action.

</summary>

link_maze: unknown

Enables the link maze transformation on the response.

[Link to this property](#)

</details>

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

version: optional string

The version of the ruleset.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, description, kind, 5 more }

</summary>

id: optional string

The unique ID of the ruleset.

[Link to this property](#)

description: optional string

An informative description of the ruleset.

[Link to this property](#)

<details>

<summary>

kind: optional [Kind](/api/resources/rulesets#(resource)%20rulesets%20%3E%20(model)%20kind%20%3E%20(schema))

The kind of the ruleset.

</summary>

One of the following:

"managed"

[Link to this property](#)

"custom"

[Link to this property](#)

"root"

[Link to this property](#)

"zone"

[Link to this property](#)

</details>

[Link to this property](#)

last_updated: optional string

The timestamp of when the ruleset was last modified.

formatdate-time

[Link to this property](#)

name: optional string

The human-readable name of the ruleset.

minLength1

[Link to this property](#)

<details>

<summary>

phase: optional [Phase](/api/resources/rulesets#(resource)%20rulesets%20%3E%20(model)%20phase%20%3E%20(schema))

The phase of the ruleset.

</summary>

One of the following:

"ddos_l4"

[Link to this property](#)

"ddos_l7"

[Link to this property](#)

"http_config_settings"

[Link to this property](#)

"http_custom_errors"

[Link to this property](#)

"http_log_custom_fields"

[Link to this property](#)

"http_ratelimit"

[Link to this property](#)

"http_request_cache_settings"

[Link to this property](#)

"http_request_dynamic_redirect"

[Link to this property](#)

"http_request_firewall_custom"

[Link to this property](#)

"http_request_firewall_managed"

[Link to this property](#)

"http_request_late_transform"

[Link to this property](#)

"http_request_origin"

[Link to this property](#)

"http_request_redirect"

[Link to this property](#)

"http_request_sanitize"

[Link to this property](#)

"http_request_sbfm"

[Link to this property](#)

"http_request_transform"

[Link to this property](#)

"http_response_cache_settings"

[Link to this property](#)

"http_response_compression"

[Link to this property](#)

"http_response_firewall_custom"

[Link to this property](#)

"http_response_firewall_managed"

[Link to this property](#)

"http_response_headers_transform"

[Link to this property](#)

"magic_transit"

[Link to this property](#)

"magic_transit_ids_managed"

[Link to this property](#)

"magic_transit_managed"

[Link to this property](#)

"magic_transit_ratelimit"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

rules: optional array of [BlockRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20block_rule%20%3E%20(schema)) { last_updated, version, id, 10 more } or object { id, action, enabled, 10 more } or [CompressResponseRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20compress_response_rule%20%3E%20(schema)) { last_updated, version, id, 10 more } or 18 more

The list of rules in the ruleset.

</summary>

One of the following:

<details>

<summary>

BlockRule = [BlockRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20block_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ChallengeRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "challenge"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

Whether the rule should be executed.

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

action_parameters: optional unknown

The parameters configuring the rule’s action.

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ResponseCompressionRule = [CompressResponseRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20compress_response_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DDoSDynamicRule = [DDoSDynamicRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20ddos_dynamic_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ExecuteRule = [ExecuteRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20execute_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ForceConnectionCloseRule = [ForceConnectionCloseRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20force_connection_close_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

JavaScriptChallengeRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "js_challenge"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

Whether the rule should be executed.

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

action_parameters: optional unknown

The parameters configuring the rule’s action.

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

LogRule = [LogRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20log_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

LogCustomFieldRule = [LogCustomFieldRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20log_custom_field_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ManagedChallengeRule = [ManagedChallengeRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20managed_challenge_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RedirectRule = [RedirectRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20redirect_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RewriteRule = [RewriteRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20rewrite_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RouteRule = [RouteRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20route_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ScoreRule = [ScoreRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20score_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ServeErrorRule = [ServeErrorRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20serve_error_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheControlRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "set_cache_control"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

<details>

<summary>

action_parameters: optional object { immutable, "max-age", "must-revalidate", 10 more }

The parameters configuring the rule’s action.

</summary>

<details>

<summary>

immutable: optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"max-age": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"must-revalidate": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"must-understand": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"no-cache": optional object { operation, cloudflare_only, qualifiers } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts optional qualifiers (header names).

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only, qualifiers }

Set the directive with optional qualifiers.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

qualifiers: optional array of string

Optional list of header names to qualify the directive (e.g., for “private” or “no-cache” directives).

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"no-store": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"no-transform": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

private: optional object { operation, cloudflare_only, qualifiers } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts optional qualifiers (header names).

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only, qualifiers }

Set the directive with optional qualifiers.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

qualifiers: optional array of string

Optional list of header names to qualify the directive (e.g., for “private” or “no-cache” directives).

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"proxy-revalidate": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

public: optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"s-maxage": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"stale-if-error": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"stale-while-revalidate": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheSettingsRule = [SetCacheSettingsRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20set_cache_settings_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheTagsRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "set_cache_tags"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

<details>

<summary>

action_parameters: optional object { operation, values } or object { expression, operation } or object { operation, values } or 3 more

The parameters configuring the rule’s action.

</summary>

One of the following:

<details>

<summary>

AddCacheTagsValues object { operation, values }

Add cache tags using a list of values.

</summary>

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

values: array of string

A list of cache tag values.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

AddCacheTagsExpression object { expression, operation }

Add cache tags using an expression.

</summary>

expression: string

An expression that evaluates to an array of cache tag values.

minLength1

[Link to this property](#)

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveCacheTagsValues object { operation, values }

Remove cache tags using a list of values.

</summary>

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

values: array of string

A list of cache tag values.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveCacheTagsExpression object { expression, operation }

Remove cache tags using an expression.

</summary>

expression: string

An expression that evaluates to an array of cache tag values.

minLength1

[Link to this property](#)

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheTagsValues object { operation, values }

Set cache tags using a list of values.

</summary>

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

values: array of string

A list of cache tag values.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheTagsExpression object { expression, operation }

Set cache tags using an expression.

</summary>

expression: string

An expression that evaluates to an array of cache tag values.

minLength1

[Link to this property](#)

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetConfigurationRule = [SetConfigRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20set_config_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SkipRule = [SkipRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20skip_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

TransformResponseHTMLRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "transform_response_html"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

<details>

<summary>

action_parameters: optional object { link_maze }

The parameters configuring the rule’s action.

</summary>

link_maze: unknown

Enables the link maze transformation on the response.

[Link to this property](#)

</details>

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

version: optional string

The version of the ruleset.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, description, kind, 5 more }

</summary>

id: optional string

The unique ID of the ruleset.

[Link to this property](#)

description: optional string

An informative description of the ruleset.

[Link to this property](#)

<details>

<summary>

kind: optional [Kind](/api/resources/rulesets#(resource)%20rulesets%20%3E%20(model)%20kind%20%3E%20(schema))

The kind of the ruleset.

</summary>

One of the following:

"managed"

[Link to this property](#)

"custom"

[Link to this property](#)

"root"

[Link to this property](#)

"zone"

[Link to this property](#)

</details>

[Link to this property](#)

last_updated: optional string

The timestamp of when the ruleset was last modified.

formatdate-time

[Link to this property](#)

name: optional string

The human-readable name of the ruleset.

minLength1

[Link to this property](#)

<details>

<summary>

phase: optional [Phase](/api/resources/rulesets#(resource)%20rulesets%20%3E%20(model)%20phase%20%3E%20(schema))

The phase of the ruleset.

</summary>

One of the following:

"ddos_l4"

[Link to this property](#)

"ddos_l7"

[Link to this property](#)

"http_config_settings"

[Link to this property](#)

"http_custom_errors"

[Link to this property](#)

"http_log_custom_fields"

[Link to this property](#)

"http_ratelimit"

[Link to this property](#)

"http_request_cache_settings"

[Link to this property](#)

"http_request_dynamic_redirect"

[Link to this property](#)

"http_request_firewall_custom"

[Link to this property](#)

"http_request_firewall_managed"

[Link to this property](#)

"http_request_late_transform"

[Link to this property](#)

"http_request_origin"

[Link to this property](#)

"http_request_redirect"

[Link to this property](#)

"http_request_sanitize"

[Link to this property](#)

"http_request_sbfm"

[Link to this property](#)

"http_request_transform"

[Link to this property](#)

"http_response_cache_settings"

[Link to this property](#)

"http_response_compression"

[Link to this property](#)

"http_response_firewall_custom"

[Link to this property](#)

"http_response_firewall_managed"

[Link to this property](#)

"http_response_headers_transform"

[Link to this property](#)

"magic_transit"

[Link to this property](#)

"magic_transit_ids_managed"

[Link to this property](#)

"magic_transit_managed"

[Link to this property](#)

"magic_transit_ratelimit"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

rules: optional array of [BlockRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20block_rule%20%3E%20(schema)) { last_updated, version, id, 10 more } or object { id, action, enabled, 10 more } or [CompressResponseRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20compress_response_rule%20%3E%20(schema)) { last_updated, version, id, 10 more } or 18 more

The list of rules in the ruleset.

</summary>

One of the following:

<details>

<summary>

BlockRule = [BlockRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20block_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ChallengeRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "challenge"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

Whether the rule should be executed.

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

action_parameters: optional unknown

The parameters configuring the rule’s action.

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ResponseCompressionRule = [CompressResponseRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20compress_response_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DDoSDynamicRule = [DDoSDynamicRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20ddos_dynamic_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ExecuteRule = [ExecuteRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20execute_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ForceConnectionCloseRule = [ForceConnectionCloseRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20force_connection_close_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

JavaScriptChallengeRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "js_challenge"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

Whether the rule should be executed.

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

action_parameters: optional unknown

The parameters configuring the rule’s action.

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

LogRule = [LogRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20log_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

LogCustomFieldRule = [LogCustomFieldRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20log_custom_field_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ManagedChallengeRule = [ManagedChallengeRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20managed_challenge_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RedirectRule = [RedirectRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20redirect_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RewriteRule = [RewriteRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20rewrite_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RouteRule = [RouteRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20route_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ScoreRule = [ScoreRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20score_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ServeErrorRule = [ServeErrorRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20serve_error_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheControlRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "set_cache_control"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

<details>

<summary>

action_parameters: optional object { immutable, "max-age", "must-revalidate", 10 more }

The parameters configuring the rule’s action.

</summary>

<details>

<summary>

immutable: optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"max-age": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"must-revalidate": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"must-understand": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"no-cache": optional object { operation, cloudflare_only, qualifiers } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts optional qualifiers (header names).

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only, qualifiers }

Set the directive with optional qualifiers.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

qualifiers: optional array of string

Optional list of header names to qualify the directive (e.g., for “private” or “no-cache” directives).

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"no-store": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"no-transform": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

private: optional object { operation, cloudflare_only, qualifiers } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts optional qualifiers (header names).

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only, qualifiers }

Set the directive with optional qualifiers.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

qualifiers: optional array of string

Optional list of header names to qualify the directive (e.g., for “private” or “no-cache” directives).

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"proxy-revalidate": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

public: optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"s-maxage": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"stale-if-error": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"stale-while-revalidate": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheSettingsRule = [SetCacheSettingsRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20set_cache_settings_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheTagsRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "set_cache_tags"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

<details>

<summary>

action_parameters: optional object { operation, values } or object { expression, operation } or object { operation, values } or 3 more

The parameters configuring the rule’s action.

</summary>

One of the following:

<details>

<summary>

AddCacheTagsValues object { operation, values }

Add cache tags using a list of values.

</summary>

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

values: array of string

A list of cache tag values.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

AddCacheTagsExpression object { expression, operation }

Add cache tags using an expression.

</summary>

expression: string

An expression that evaluates to an array of cache tag values.

minLength1

[Link to this property](#)

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveCacheTagsValues object { operation, values }

Remove cache tags using a list of values.

</summary>

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

values: array of string

A list of cache tag values.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveCacheTagsExpression object { expression, operation }

Remove cache tags using an expression.

</summary>

expression: string

An expression that evaluates to an array of cache tag values.

minLength1

[Link to this property](#)

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheTagsValues object { operation, values }

Set cache tags using a list of values.

</summary>

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

values: array of string

A list of cache tag values.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheTagsExpression object { expression, operation }

Set cache tags using an expression.

</summary>

expression: string

An expression that evaluates to an array of cache tag values.

minLength1

[Link to this property](#)

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetConfigurationRule = [SetConfigRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20set_config_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SkipRule = [SkipRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20skip_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

TransformResponseHTMLRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "transform_response_html"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

<details>

<summary>

action_parameters: optional object { link_maze }

The parameters configuring the rule’s action.

</summary>

link_maze: unknown

Enables the link maze transformation on the response.

[Link to this property](#)

</details>

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

version: optional string

The version of the ruleset.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, description, kind, 5 more }

</summary>

id: optional string

The unique ID of the ruleset.

[Link to this property](#)

description: optional string

An informative description of the ruleset.

[Link to this property](#)

<details>

<summary>

kind: optional [Kind](/api/resources/rulesets#(resource)%20rulesets%20%3E%20(model)%20kind%20%3E%20(schema))

The kind of the ruleset.

</summary>

One of the following:

"managed"

[Link to this property](#)

"custom"

[Link to this property](#)

"root"

[Link to this property](#)

"zone"

[Link to this property](#)

</details>

[Link to this property](#)

last_updated: optional string

The timestamp of when the ruleset was last modified.

formatdate-time

[Link to this property](#)

name: optional string

The human-readable name of the ruleset.

minLength1

[Link to this property](#)

<details>

<summary>

phase: optional [Phase](/api/resources/rulesets#(resource)%20rulesets%20%3E%20(model)%20phase%20%3E%20(schema))

The phase of the ruleset.

</summary>

One of the following:

"ddos_l4"

[Link to this property](#)

"ddos_l7"

[Link to this property](#)

"http_config_settings"

[Link to this property](#)

"http_custom_errors"

[Link to this property](#)

"http_log_custom_fields"

[Link to this property](#)

"http_ratelimit"

[Link to this property](#)

"http_request_cache_settings"

[Link to this property](#)

"http_request_dynamic_redirect"

[Link to this property](#)

"http_request_firewall_custom"

[Link to this property](#)

"http_request_firewall_managed"

[Link to this property](#)

"http_request_late_transform"

[Link to this property](#)

"http_request_origin"

[Link to this property](#)

"http_request_redirect"

[Link to this property](#)

"http_request_sanitize"

[Link to this property](#)

"http_request_sbfm"

[Link to this property](#)

"http_request_transform"

[Link to this property](#)

"http_response_cache_settings"

[Link to this property](#)

"http_response_compression"

[Link to this property](#)

"http_response_firewall_custom"

[Link to this property](#)

"http_response_firewall_managed"

[Link to this property](#)

"http_response_headers_transform"

[Link to this property](#)

"magic_transit"

[Link to this property](#)

"magic_transit_ids_managed"

[Link to this property](#)

"magic_transit_managed"

[Link to this property](#)

"magic_transit_ratelimit"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

rules: optional array of [BlockRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20block_rule%20%3E%20(schema)) { last_updated, version, id, 10 more } or object { id, action, enabled, 10 more } or [CompressResponseRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20compress_response_rule%20%3E%20(schema)) { last_updated, version, id, 10 more } or 18 more

The list of rules in the ruleset.

</summary>

One of the following:

<details>

<summary>

BlockRule = [BlockRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20block_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ChallengeRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "challenge"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

Whether the rule should be executed.

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

action_parameters: optional unknown

The parameters configuring the rule’s action.

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ResponseCompressionRule = [CompressResponseRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20compress_response_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DDoSDynamicRule = [DDoSDynamicRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20ddos_dynamic_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ExecuteRule = [ExecuteRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20execute_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ForceConnectionCloseRule = [ForceConnectionCloseRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20force_connection_close_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

JavaScriptChallengeRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "js_challenge"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

Whether the rule should be executed.

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

action_parameters: optional unknown

The parameters configuring the rule’s action.

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

LogRule = [LogRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20log_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

LogCustomFieldRule = [LogCustomFieldRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20log_custom_field_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ManagedChallengeRule = [ManagedChallengeRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20managed_challenge_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RedirectRule = [RedirectRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20redirect_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RewriteRule = [RewriteRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20rewrite_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RouteRule = [RouteRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20route_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ScoreRule = [ScoreRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20score_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ServeErrorRule = [ServeErrorRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20serve_error_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheControlRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "set_cache_control"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

<details>

<summary>

action_parameters: optional object { immutable, "max-age", "must-revalidate", 10 more }

The parameters configuring the rule’s action.

</summary>

<details>

<summary>

immutable: optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"max-age": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"must-revalidate": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"must-understand": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"no-cache": optional object { operation, cloudflare_only, qualifiers } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts optional qualifiers (header names).

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only, qualifiers }

Set the directive with optional qualifiers.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

qualifiers: optional array of string

Optional list of header names to qualify the directive (e.g., for “private” or “no-cache” directives).

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"no-store": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"no-transform": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

private: optional object { operation, cloudflare_only, qualifiers } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts optional qualifiers (header names).

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only, qualifiers }

Set the directive with optional qualifiers.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

qualifiers: optional array of string

Optional list of header names to qualify the directive (e.g., for “private” or “no-cache” directives).

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"proxy-revalidate": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

public: optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"s-maxage": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"stale-if-error": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"stale-while-revalidate": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheSettingsRule = [SetCacheSettingsRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20set_cache_settings_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheTagsRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "set_cache_tags"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

<details>

<summary>

action_parameters: optional object { operation, values } or object { expression, operation } or object { operation, values } or 3 more

The parameters configuring the rule’s action.

</summary>

One of the following:

<details>

<summary>

AddCacheTagsValues object { operation, values }

Add cache tags using a list of values.

</summary>

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

values: array of string

A list of cache tag values.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

AddCacheTagsExpression object { expression, operation }

Add cache tags using an expression.

</summary>

expression: string

An expression that evaluates to an array of cache tag values.

minLength1

[Link to this property](#)

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveCacheTagsValues object { operation, values }

Remove cache tags using a list of values.

</summary>

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

values: array of string

A list of cache tag values.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveCacheTagsExpression object { expression, operation }

Remove cache tags using an expression.

</summary>

expression: string

An expression that evaluates to an array of cache tag values.

minLength1

[Link to this property](#)

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheTagsValues object { operation, values }

Set cache tags using a list of values.

</summary>

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

values: array of string

A list of cache tag values.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheTagsExpression object { expression, operation }

Set cache tags using an expression.

</summary>

expression: string

An expression that evaluates to an array of cache tag values.

minLength1

[Link to this property](#)

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetConfigurationRule = [SetConfigRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20set_config_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SkipRule = [SkipRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20skip_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

TransformResponseHTMLRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "transform_response_html"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

<details>

<summary>

action_parameters: optional object { link_maze }

The parameters configuring the rule’s action.

</summary>

link_maze: unknown

Enables the link maze transformation on the response.

[Link to this property](#)

</details>

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

version: optional string

The version of the ruleset.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

object { id, description, kind, 5 more }

</summary>

id: optional string

The unique ID of the ruleset.

[Link to this property](#)

description: optional string

An informative description of the ruleset.

[Link to this property](#)

<details>

<summary>

kind: optional [Kind](/api/resources/rulesets#(resource)%20rulesets%20%3E%20(model)%20kind%20%3E%20(schema))

The kind of the ruleset.

</summary>

One of the following:

"managed"

[Link to this property](#)

"custom"

[Link to this property](#)

"root"

[Link to this property](#)

"zone"

[Link to this property](#)

</details>

[Link to this property](#)

last_updated: optional string

The timestamp of when the ruleset was last modified.

formatdate-time

[Link to this property](#)

name: optional string

The human-readable name of the ruleset.

minLength1

[Link to this property](#)

<details>

<summary>

phase: optional [Phase](/api/resources/rulesets#(resource)%20rulesets%20%3E%20(model)%20phase%20%3E%20(schema))

The phase of the ruleset.

</summary>

One of the following:

"ddos_l4"

[Link to this property](#)

"ddos_l7"

[Link to this property](#)

"http_config_settings"

[Link to this property](#)

"http_custom_errors"

[Link to this property](#)

"http_log_custom_fields"

[Link to this property](#)

"http_ratelimit"

[Link to this property](#)

"http_request_cache_settings"

[Link to this property](#)

"http_request_dynamic_redirect"

[Link to this property](#)

"http_request_firewall_custom"

[Link to this property](#)

"http_request_firewall_managed"

[Link to this property](#)

"http_request_late_transform"

[Link to this property](#)

"http_request_origin"

[Link to this property](#)

"http_request_redirect"

[Link to this property](#)

"http_request_sanitize"

[Link to this property](#)

"http_request_sbfm"

[Link to this property](#)

"http_request_transform"

[Link to this property](#)

"http_response_cache_settings"

[Link to this property](#)

"http_response_compression"

[Link to this property](#)

"http_response_firewall_custom"

[Link to this property](#)

"http_response_firewall_managed"

[Link to this property](#)

"http_response_headers_transform"

[Link to this property](#)

"magic_transit"

[Link to this property](#)

"magic_transit_ids_managed"

[Link to this property](#)

"magic_transit_managed"

[Link to this property](#)

"magic_transit_ratelimit"

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

rules: optional array of [BlockRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20block_rule%20%3E%20(schema)) { last_updated, version, id, 10 more } or object { id, action, enabled, 10 more } or [CompressResponseRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20compress_response_rule%20%3E%20(schema)) { last_updated, version, id, 10 more } or 18 more

The list of rules in the ruleset.

</summary>

One of the following:

<details>

<summary>

BlockRule = [BlockRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20block_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ChallengeRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "challenge"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

Whether the rule should be executed.

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

action_parameters: optional unknown

The parameters configuring the rule’s action.

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ResponseCompressionRule = [CompressResponseRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20compress_response_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

DDoSDynamicRule = [DDoSDynamicRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20ddos_dynamic_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ExecuteRule = [ExecuteRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20execute_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ForceConnectionCloseRule = [ForceConnectionCloseRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20force_connection_close_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

JavaScriptChallengeRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "js_challenge"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

Whether the rule should be executed.

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

action_parameters: optional unknown

The parameters configuring the rule’s action.

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

LogRule = [LogRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20log_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

LogCustomFieldRule = [LogCustomFieldRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20log_custom_field_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ManagedChallengeRule = [ManagedChallengeRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20managed_challenge_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RedirectRule = [RedirectRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20redirect_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RewriteRule = [RewriteRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20rewrite_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RouteRule = [RouteRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20route_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ScoreRule = [ScoreRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20score_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ServeErrorRule = [ServeErrorRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20serve_error_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheControlRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "set_cache_control"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

<details>

<summary>

action_parameters: optional object { immutable, "max-age", "must-revalidate", 10 more }

The parameters configuring the rule’s action.

</summary>

<details>

<summary>

immutable: optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"max-age": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"must-revalidate": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"must-understand": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"no-cache": optional object { operation, cloudflare_only, qualifiers } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts optional qualifiers (header names).

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only, qualifiers }

Set the directive with optional qualifiers.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

qualifiers: optional array of string

Optional list of header names to qualify the directive (e.g., for “private” or “no-cache” directives).

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"no-store": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"no-transform": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

private: optional object { operation, cloudflare_only, qualifiers } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts optional qualifiers (header names).

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only, qualifiers }

Set the directive with optional qualifiers.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

qualifiers: optional array of string

Optional list of header names to qualify the directive (e.g., for “private” or “no-cache” directives).

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"proxy-revalidate": optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

public: optional object { operation, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, cloudflare_only }

Set the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"s-maxage": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"stale-if-error": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

"stale-while-revalidate": optional object { operation, value, cloudflare_only } or object { operation, cloudflare_only }

A cache-control directive configuration that accepts a duration value in seconds.

</summary>

One of the following:

<details>

<summary>

SetDirective object { operation, value, cloudflare_only }

Set the directive with a duration value in seconds.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

value: number

The duration value in seconds for the directive.

minimum0

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveDirective object { operation, cloudflare_only }

Remove the directive.

</summary>

<details>

<summary>

operation: "set" or "remove"

The operation to perform on the cache-control directive.

</summary>

One of the following:

"set"

[Link to this property](#)

"remove"

[Link to this property](#)

</details>

[Link to this property](#)

cloudflare_only: optional boolean

Whether the directive should only be applied to the Cloudflare CDN cache.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheSettingsRule = [SetCacheSettingsRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20set_cache_settings_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheTagsRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "set_cache_tags"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

<details>

<summary>

action_parameters: optional object { operation, values } or object { expression, operation } or object { operation, values } or 3 more

The parameters configuring the rule’s action.

</summary>

One of the following:

<details>

<summary>

AddCacheTagsValues object { operation, values }

Add cache tags using a list of values.

</summary>

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

values: array of string

A list of cache tag values.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

AddCacheTagsExpression object { expression, operation }

Add cache tags using an expression.

</summary>

expression: string

An expression that evaluates to an array of cache tag values.

minLength1

[Link to this property](#)

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveCacheTagsValues object { operation, values }

Remove cache tags using a list of values.

</summary>

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

values: array of string

A list of cache tag values.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

RemoveCacheTagsExpression object { expression, operation }

Remove cache tags using an expression.

</summary>

expression: string

An expression that evaluates to an array of cache tag values.

minLength1

[Link to this property](#)

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheTagsValues object { operation, values }

Set cache tags using a list of values.

</summary>

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

values: array of string

A list of cache tag values.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetCacheTagsExpression object { expression, operation }

Set cache tags using an expression.

</summary>

expression: string

An expression that evaluates to an array of cache tag values.

minLength1

[Link to this property](#)

<details>

<summary>

operation: "add" or "remove" or "set"

The operation to perform on the cache tags.

</summary>

One of the following:

"add"

[Link to this property](#)

"remove"

[Link to this property](#)

"set"

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SetConfigurationRule = [SetConfigRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20set_config_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

SkipRule = [SkipRule](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20skip_rule%20%3E%20(schema)) { last_updated, version, id, 10 more }

</summary>

id: string

[Link to this property](#)

action: string

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

[Link to this property](#)

ref: string

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

TransformResponseHTMLRule object { id, action, enabled, 10 more }

</summary>

id: string

The unique ID of the rule.

[Link to this property](#)

action: "transform_response_html"

The action to perform when the rule matches.

[Link to this property](#)

enabled: boolean

[Link to this property](#)

expression: string

The expression defining which traffic will match the rule.

minLength1

[Link to this property](#)

last_updated: string

The timestamp of when the rule was last modified.

formatdate-time

[Link to this property](#)

ref: string

The reference of the rule (the rule’s ID by default).

minLength1

[Link to this property](#)

version: string

The version of the rule.

[Link to this property](#)

<details>

<summary>

action_parameters: optional object { link_maze }

The parameters configuring the rule’s action.

</summary>

link_maze: unknown

Enables the link maze transformation on the response.

[Link to this property](#)

</details>

[Link to this property](#)

categories: optional array of string

The categories of the rule.

[Link to this property](#)

description: optional string

An informative description of the rule.

[Link to this property](#)

<details>

<summary>

exposed_credential_check: optional object { password_expression, username_expression }

Configuration for exposed credential checking.

</summary>

password_expression: string

An expression that selects the password used in the credentials check.

minLength1

[Link to this property](#)

username_expression: string

An expression that selects the user ID used in the credentials check.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

logging: optional [Logging](/api/resources/rulesets#(resource)%20rulesets.rules%20%3E%20(model)%20logging%20%3E%20(schema)) { enabled }

An object configuring the rule’s logging behavior.

</summary>

enabled: boolean

Whether to generate a log when the rule matches.

[Link to this property](#)

</details>

[Link to this property](#)

<details>

<summary>

ratelimit: optional object { characteristics, period, counting_expression, 5 more }

An object configuring the rule’s rate limit behavior.

</summary>

characteristics: array of string

Characteristics of the request on which the rate limit counter will be incremented.

[Link to this property](#)

period: number

Period in seconds over which the counter is being incremented.

minimum0

[Link to this property](#)

counting_expression: optional string

An expression that defines when the rate limit counter should be incremented. It defaults to the same as the rule’s expression.

minLength1

[Link to this property](#)

mitigation_timeout: optional number

Period of time in seconds after which the action will be disabled following its first execution.

[Link to this property](#)

requests_per_period: optional number

The threshold of requests per period after which the action will be executed for the first time.

minimum1

[Link to this property](#)

requests_to_origin: optional boolean

Whether counting is only performed when an origin is reached.

[Link to this property](#)

score_per_period: optional number

The score threshold per period for which the action will be executed the first time.

[Link to this property](#)

score_response_header_name: optional string

A response header name provided by the origin, which contains the score to increment rate limit counter with.

minLength1

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

version: optional string

The version of the ruleset.

[Link to this property](#)

</details>

[Link to this property](#)

</details>

[Link to this property](#)

success: true

Whether the API call was successful.

[Link to this property](#)
