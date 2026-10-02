---
title: Access
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Access

#### AccessAI Controls

#### AccessAI ControlsMcp

#### AccessAI ControlsMcpPortals

##### [List MCP Portals](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/ai_controls/subresources/mcp/subresources/portals/methods/list)

GET/accounts/{account\_id}/access/ai-controls/mcp/portals

##### [Create a new MCP Portal](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/ai_controls/subresources/mcp/subresources/portals/methods/create)

POST/accounts/{account\_id}/access/ai-controls/mcp/portals

##### [Read details of an MCP Portal](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/ai_controls/subresources/mcp/subresources/portals/methods/read)

GET/accounts/{account\_id}/access/ai-controls/mcp/portals/{id}

##### [Update an MCP Portal](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/ai_controls/subresources/mcp/subresources/portals/methods/update)

PUT/accounts/{account\_id}/access/ai-controls/mcp/portals/{id}

##### [Delete an MCP Portal](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/ai_controls/subresources/mcp/subresources/portals/methods/delete)

DELETE/accounts/{account\_id}/access/ai-controls/mcp/portals/{id}

##### ModelsExpand Collapse

<details>

<summary>

PortalListResponse object {id, hostname, name, 9 more }

</summary>

id: string

Unique identifier for the MCP portal.

maxLength32

minLength1

<a href="#">Link to this property</a>

hostname: string

Hostname where the MCP portal is available.

<a href="#">Link to this property</a>

name: string

Display name for the MCP portal.

maxLength350

<a href="#">Link to this property</a>

<details>

<summary>

servers: array of object {id, auth\_type, hostname, 22 more }

</summary>

id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

auth\_type: "oauth"or "bearer"or "unauthenticated"

Authentication method used to connect to the upstream MCP server.

</summary>

One of the following:

"oauth"

<a href="#">Link to this property</a>

"bearer"

<a href="#">Link to this property</a>

"unauthenticated"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

hostname: string

URL of the upstream MCP endpoint.

formaturi

<a href="#">Link to this property</a>

name: string

Display name for the MCP server.

maxLength350

<a href="#">Link to this property</a>

prompts: array of map\[unknown]

<a href="#">Link to this property</a>

server\_id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

tools: array of map\[unknown]

<a href="#">Link to this property</a>

<details>

<summary>

auth\_config\_summary: optional object {auth\_mode, client\_secret\_version, config, 2 more }

Safe subset of auth\_credentials surfaced to the dashboard. Includes auth\_mode (dcr|manual), has\_client\_secret, client\_secret\_version, and the OAuth endpoints + client\_id for manual servers. Never includes the secret value.

</summary>

<details>

<summary>

auth\_mode: optional "dcr"or "manual"

</summary>

One of the following:

"dcr"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

client\_secret\_version: optional number

<a href="#">Link to this property</a>

<details>

<summary>

config: optional object {authorization\_endpoint, issuer, resource, 2 more }

</summary>

authorization\_endpoint: optional string

<a href="#">Link to this property</a>

issuer: optional string

<a href="#">Link to this property</a>

resource: optional string

<a href="#">Link to this property</a>

revocation\_endpoint: optional string

<a href="#">Link to this property</a>

token\_endpoint: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

has\_client\_secret: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

registration\_info: optional object {client\_id, redirect\_uris, scope, token\_endpoint\_auth\_method }

</summary>

client\_id: optional string

<a href="#">Link to this property</a>

redirect\_uris: optional array of string

<a href="#">Link to this property</a>

scope: optional string

<a href="#">Link to this property</a>

token\_endpoint\_auth\_method: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

authentication\_status: optional "not\_required"or "required"or "connected"or 2 more

Whether administrative authentication is required before capabilities can be synced. Manual OAuth is user-managed and has no administrative authentication flow.

</summary>

One of the following:

"not\_required"

<a href="#">Link to this property</a>

"required"

<a href="#">Link to this property</a>

"connected"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

default\_disabled: optional boolean

Hide this server’s tools and prompts by default. To expose specific capabilities, set enabled: true for them in updated\_tools or updated\_prompts.

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP server.

maxLength512

<a href="#">Link to this property</a>

error: optional string

<a href="#">Link to this property</a>

<details>

<summary>

error\_details: optional object {cause, is\_upstream, mcp\_code, 2 more }

</summary>

cause: optional string

Underlying error message

<a href="#">Link to this property</a>

is\_upstream: optional boolean

True = MCP server returned an error. False = couldn’t reach the server

<a href="#">Link to this property</a>

mcp\_code: optional number

MCP protocol error code

<a href="#">Link to this property</a>

retryable: optional boolean

Whether the error is transient and worth retrying

<a href="#">Link to this property</a>

status\_code: optional number

HTTP status code from the server

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

is\_shared\_oauth\_callback\_enabled: optional boolean

When true, the gateway worker uses the shared Cloudflare-owned OAuth callback endpoint as the redirect\_uri for upstream on-behalf OAuth, instead of the customer portal hostname. Defaults to false (off); opt in per server by setting true.

<a href="#">Link to this property</a>

last\_successful\_sync: optional string

formatdate-time

<a href="#">Link to this property</a>

last\_synced: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

on\_behalf: optional boolean

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound traffic to this MCP server through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "waiting"or "ready"or "stale"or "error"

Current sync state of the server

</summary>

One of the following:

"waiting"

<a href="#">Link to this property</a>

"ready"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_prompts: optional array of object {name, enabled, portal\_alias, 3 more }

</summary>

name: string

<a href="#">Link to this property</a>

enabled: optional boolean

<a href="#">Link to this property</a>

portal\_alias: optional string

<a href="#">Link to this property</a>

portal\_description: optional string

<a href="#">Link to this property</a>

server\_alias: optional string

<a href="#">Link to this property</a>

server\_description: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_tools: optional array of object {name, enabled, portal\_alias, 3 more }

</summary>

name: string

<a href="#">Link to this property</a>

enabled: optional boolean

<a href="#">Link to this property</a>

portal\_alias: optional string

<a href="#">Link to this property</a>

portal\_description: optional string

<a href="#">Link to this property</a>

server\_alias: optional string

<a href="#">Link to this property</a>

server\_description: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

Deprecatedallow\_code\_mode: optional boolean

Deprecated: use <code>code_mode</code> for new integrations. <code>true</code> maps to any non-off Code Mode policy; <code>false</code> maps to <code>code_mode: off</code>. If both fields are sent, they must be consistent or the request returns a 400.

<a href="#">Link to this property</a>

<details>

<summary>

code\_mode: optional "off"or "opt\_in"or "default\_on"or "enforced"

Code Mode policy for this portal. <code>off</code>: Code Mode is unavailable; query parameters are ignored. <code>opt_in</code>: Code Mode is off by default; clients turn it on with <code>?codemode=search_and_execute</code>. <code>default_on</code>: Code Mode is on by default; clients can opt out with <code>?codemode=off</code>. <code>enforced</code>: Code Mode is always on; query parameters are ignored. Defaults to <code>opt_in</code> when omitted on create. If both <code>code_mode</code> and <code>allow_code_mode</code> are sent, they must be consistent or the request returns a 400.

</summary>

One of the following:

"off"

<a href="#">Link to this property</a>

"opt\_in"

<a href="#">Link to this property</a>

"default\_on"

<a href="#">Link to this property</a>

"enforced"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP portal.

maxLength512

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound MCP traffic through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.ai_controls.mcp.portals%20%3E%20(model)%20portal_list_response%20%3E%20(schema)>)

<details>

<summary>

PortalCreateResponse object {id, hostname, name, 9 more }

</summary>

id: string

Unique identifier for the MCP portal.

maxLength32

minLength1

<a href="#">Link to this property</a>

hostname: string

Hostname where the MCP portal is available.

<a href="#">Link to this property</a>

name: string

Display name for the MCP portal.

maxLength350

<a href="#">Link to this property</a>

<details>

<summary>

servers: array of object {id, auth\_type, hostname, 22 more }

</summary>

id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

auth\_type: "oauth"or "bearer"or "unauthenticated"

Authentication method used to connect to the upstream MCP server.

</summary>

One of the following:

"oauth"

<a href="#">Link to this property</a>

"bearer"

<a href="#">Link to this property</a>

"unauthenticated"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

hostname: string

URL of the upstream MCP endpoint.

formaturi

<a href="#">Link to this property</a>

name: string

Display name for the MCP server.

maxLength350

<a href="#">Link to this property</a>

prompts: array of map\[unknown]

<a href="#">Link to this property</a>

server\_id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

tools: array of map\[unknown]

<a href="#">Link to this property</a>

<details>

<summary>

auth\_config\_summary: optional object {auth\_mode, client\_secret\_version, config, 2 more }

Safe subset of auth\_credentials surfaced to the dashboard. Includes auth\_mode (dcr|manual), has\_client\_secret, client\_secret\_version, and the OAuth endpoints + client\_id for manual servers. Never includes the secret value.

</summary>

<details>

<summary>

auth\_mode: optional "dcr"or "manual"

</summary>

One of the following:

"dcr"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

client\_secret\_version: optional number

<a href="#">Link to this property</a>

<details>

<summary>

config: optional object {authorization\_endpoint, issuer, resource, 2 more }

</summary>

authorization\_endpoint: optional string

<a href="#">Link to this property</a>

issuer: optional string

<a href="#">Link to this property</a>

resource: optional string

<a href="#">Link to this property</a>

revocation\_endpoint: optional string

<a href="#">Link to this property</a>

token\_endpoint: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

has\_client\_secret: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

registration\_info: optional object {client\_id, redirect\_uris, scope, token\_endpoint\_auth\_method }

</summary>

client\_id: optional string

<a href="#">Link to this property</a>

redirect\_uris: optional array of string

<a href="#">Link to this property</a>

scope: optional string

<a href="#">Link to this property</a>

token\_endpoint\_auth\_method: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

authentication\_status: optional "not\_required"or "required"or "connected"or 2 more

Whether administrative authentication is required before capabilities can be synced. Manual OAuth is user-managed and has no administrative authentication flow.

</summary>

One of the following:

"not\_required"

<a href="#">Link to this property</a>

"required"

<a href="#">Link to this property</a>

"connected"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

default\_disabled: optional boolean

Hide this server’s tools and prompts by default. To expose specific capabilities, set enabled: true for them in updated\_tools or updated\_prompts.

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP server.

maxLength512

<a href="#">Link to this property</a>

error: optional string

<a href="#">Link to this property</a>

<details>

<summary>

error\_details: optional object {cause, is\_upstream, mcp\_code, 2 more }

</summary>

cause: optional string

Underlying error message

<a href="#">Link to this property</a>

is\_upstream: optional boolean

True = MCP server returned an error. False = couldn’t reach the server

<a href="#">Link to this property</a>

mcp\_code: optional number

MCP protocol error code

<a href="#">Link to this property</a>

retryable: optional boolean

Whether the error is transient and worth retrying

<a href="#">Link to this property</a>

status\_code: optional number

HTTP status code from the server

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

is\_shared\_oauth\_callback\_enabled: optional boolean

When true, the gateway worker uses the shared Cloudflare-owned OAuth callback endpoint as the redirect\_uri for upstream on-behalf OAuth, instead of the customer portal hostname. Defaults to false (off); opt in per server by setting true.

<a href="#">Link to this property</a>

last\_successful\_sync: optional string

formatdate-time

<a href="#">Link to this property</a>

last\_synced: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

on\_behalf: optional boolean

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound traffic to this MCP server through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "waiting"or "ready"or "stale"or "error"

Current sync state of the server

</summary>

One of the following:

"waiting"

<a href="#">Link to this property</a>

"ready"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_prompts: optional array of object {name, enabled, portal\_alias, 3 more }

</summary>

name: string

<a href="#">Link to this property</a>

enabled: optional boolean

<a href="#">Link to this property</a>

portal\_alias: optional string

<a href="#">Link to this property</a>

portal\_description: optional string

<a href="#">Link to this property</a>

server\_alias: optional string

<a href="#">Link to this property</a>

server\_description: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_tools: optional array of object {name, enabled, portal\_alias, 3 more }

</summary>

name: string

<a href="#">Link to this property</a>

enabled: optional boolean

<a href="#">Link to this property</a>

portal\_alias: optional string

<a href="#">Link to this property</a>

portal\_description: optional string

<a href="#">Link to this property</a>

server\_alias: optional string

<a href="#">Link to this property</a>

server\_description: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

Deprecatedallow\_code\_mode: optional boolean

Deprecated: use <code>code_mode</code> for new integrations. <code>true</code> maps to any non-off Code Mode policy; <code>false</code> maps to <code>code_mode: off</code>. If both fields are sent, they must be consistent or the request returns a 400.

<a href="#">Link to this property</a>

<details>

<summary>

code\_mode: optional "off"or "opt\_in"or "default\_on"or "enforced"

Code Mode policy for this portal. <code>off</code>: Code Mode is unavailable; query parameters are ignored. <code>opt_in</code>: Code Mode is off by default; clients turn it on with <code>?codemode=search_and_execute</code>. <code>default_on</code>: Code Mode is on by default; clients can opt out with <code>?codemode=off</code>. <code>enforced</code>: Code Mode is always on; query parameters are ignored. Defaults to <code>opt_in</code> when omitted on create. If both <code>code_mode</code> and <code>allow_code_mode</code> are sent, they must be consistent or the request returns a 400.

</summary>

One of the following:

"off"

<a href="#">Link to this property</a>

"opt\_in"

<a href="#">Link to this property</a>

"default\_on"

<a href="#">Link to this property</a>

"enforced"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP portal.

maxLength512

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound MCP traffic through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.ai_controls.mcp.portals%20%3E%20(model)%20portal_create_response%20%3E%20(schema)>)

<details>

<summary>

PortalReadResponse object {id, hostname, name, 9 more }

</summary>

id: string

Unique identifier for the MCP portal.

maxLength32

minLength1

<a href="#">Link to this property</a>

hostname: string

Hostname where the MCP portal is available.

<a href="#">Link to this property</a>

name: string

Display name for the MCP portal.

maxLength350

<a href="#">Link to this property</a>

<details>

<summary>

servers: array of object {id, auth\_type, hostname, 22 more }

</summary>

id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

auth\_type: "oauth"or "bearer"or "unauthenticated"

Authentication method used to connect to the upstream MCP server.

</summary>

One of the following:

"oauth"

<a href="#">Link to this property</a>

"bearer"

<a href="#">Link to this property</a>

"unauthenticated"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

hostname: string

URL of the upstream MCP endpoint.

formaturi

<a href="#">Link to this property</a>

name: string

Display name for the MCP server.

maxLength350

<a href="#">Link to this property</a>

prompts: array of map\[unknown]

<a href="#">Link to this property</a>

server\_id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

tools: array of map\[unknown]

<a href="#">Link to this property</a>

<details>

<summary>

auth\_config\_summary: optional object {auth\_mode, client\_secret\_version, config, 2 more }

Safe subset of auth\_credentials surfaced to the dashboard. Includes auth\_mode (dcr|manual), has\_client\_secret, client\_secret\_version, and the OAuth endpoints + client\_id for manual servers. Never includes the secret value.

</summary>

<details>

<summary>

auth\_mode: optional "dcr"or "manual"

</summary>

One of the following:

"dcr"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

client\_secret\_version: optional number

<a href="#">Link to this property</a>

<details>

<summary>

config: optional object {authorization\_endpoint, issuer, resource, 2 more }

</summary>

authorization\_endpoint: optional string

<a href="#">Link to this property</a>

issuer: optional string

<a href="#">Link to this property</a>

resource: optional string

<a href="#">Link to this property</a>

revocation\_endpoint: optional string

<a href="#">Link to this property</a>

token\_endpoint: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

has\_client\_secret: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

registration\_info: optional object {client\_id, redirect\_uris, scope, token\_endpoint\_auth\_method }

</summary>

client\_id: optional string

<a href="#">Link to this property</a>

redirect\_uris: optional array of string

<a href="#">Link to this property</a>

scope: optional string

<a href="#">Link to this property</a>

token\_endpoint\_auth\_method: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

authentication\_status: optional "not\_required"or "required"or "connected"or 2 more

Whether administrative authentication is required before capabilities can be synced. Manual OAuth is user-managed and has no administrative authentication flow.

</summary>

One of the following:

"not\_required"

<a href="#">Link to this property</a>

"required"

<a href="#">Link to this property</a>

"connected"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

default\_disabled: optional boolean

Hide this server’s tools and prompts by default. To expose specific capabilities, set enabled: true for them in updated\_tools or updated\_prompts.

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP server.

maxLength512

<a href="#">Link to this property</a>

error: optional string

<a href="#">Link to this property</a>

<details>

<summary>

error\_details: optional object {cause, is\_upstream, mcp\_code, 2 more }

</summary>

cause: optional string

Underlying error message

<a href="#">Link to this property</a>

is\_upstream: optional boolean

True = MCP server returned an error. False = couldn’t reach the server

<a href="#">Link to this property</a>

mcp\_code: optional number

MCP protocol error code

<a href="#">Link to this property</a>

retryable: optional boolean

Whether the error is transient and worth retrying

<a href="#">Link to this property</a>

status\_code: optional number

HTTP status code from the server

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

is\_shared\_oauth\_callback\_enabled: optional boolean

When true, the gateway worker uses the shared Cloudflare-owned OAuth callback endpoint as the redirect\_uri for upstream on-behalf OAuth, instead of the customer portal hostname. Defaults to false (off); opt in per server by setting true.

<a href="#">Link to this property</a>

last\_successful\_sync: optional string

formatdate-time

<a href="#">Link to this property</a>

last\_synced: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

on\_behalf: optional boolean

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound traffic to this MCP server through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "waiting"or "ready"or "stale"or "error"

Current sync state of the server

</summary>

One of the following:

"waiting"

<a href="#">Link to this property</a>

"ready"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_prompts: optional array of object {name, enabled, portal\_alias, 3 more }

</summary>

name: string

<a href="#">Link to this property</a>

enabled: optional boolean

<a href="#">Link to this property</a>

portal\_alias: optional string

<a href="#">Link to this property</a>

portal\_description: optional string

<a href="#">Link to this property</a>

server\_alias: optional string

<a href="#">Link to this property</a>

server\_description: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_tools: optional array of object {name, enabled, portal\_alias, 3 more }

</summary>

name: string

<a href="#">Link to this property</a>

enabled: optional boolean

<a href="#">Link to this property</a>

portal\_alias: optional string

<a href="#">Link to this property</a>

portal\_description: optional string

<a href="#">Link to this property</a>

server\_alias: optional string

<a href="#">Link to this property</a>

server\_description: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

Deprecatedallow\_code\_mode: optional boolean

Deprecated: use <code>code_mode</code> for new integrations. <code>true</code> maps to any non-off Code Mode policy; <code>false</code> maps to <code>code_mode: off</code>. If both fields are sent, they must be consistent or the request returns a 400.

<a href="#">Link to this property</a>

<details>

<summary>

code\_mode: optional "off"or "opt\_in"or "default\_on"or "enforced"

Code Mode policy for this portal. <code>off</code>: Code Mode is unavailable; query parameters are ignored. <code>opt_in</code>: Code Mode is off by default; clients turn it on with <code>?codemode=search_and_execute</code>. <code>default_on</code>: Code Mode is on by default; clients can opt out with <code>?codemode=off</code>. <code>enforced</code>: Code Mode is always on; query parameters are ignored. Defaults to <code>opt_in</code> when omitted on create. If both <code>code_mode</code> and <code>allow_code_mode</code> are sent, they must be consistent or the request returns a 400.

</summary>

One of the following:

"off"

<a href="#">Link to this property</a>

"opt\_in"

<a href="#">Link to this property</a>

"default\_on"

<a href="#">Link to this property</a>

"enforced"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP portal.

maxLength512

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound MCP traffic through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.ai_controls.mcp.portals%20%3E%20(model)%20portal_read_response%20%3E%20(schema)>)

<details>

<summary>

PortalUpdateResponse object {id, hostname, name, 9 more }

</summary>

id: string

Unique identifier for the MCP portal.

maxLength32

minLength1

<a href="#">Link to this property</a>

hostname: string

Hostname where the MCP portal is available.

<a href="#">Link to this property</a>

name: string

Display name for the MCP portal.

maxLength350

<a href="#">Link to this property</a>

<details>

<summary>

servers: array of object {id, auth\_type, hostname, 22 more }

</summary>

id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

auth\_type: "oauth"or "bearer"or "unauthenticated"

Authentication method used to connect to the upstream MCP server.

</summary>

One of the following:

"oauth"

<a href="#">Link to this property</a>

"bearer"

<a href="#">Link to this property</a>

"unauthenticated"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

hostname: string

URL of the upstream MCP endpoint.

formaturi

<a href="#">Link to this property</a>

name: string

Display name for the MCP server.

maxLength350

<a href="#">Link to this property</a>

prompts: array of map\[unknown]

<a href="#">Link to this property</a>

server\_id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

tools: array of map\[unknown]

<a href="#">Link to this property</a>

<details>

<summary>

auth\_config\_summary: optional object {auth\_mode, client\_secret\_version, config, 2 more }

Safe subset of auth\_credentials surfaced to the dashboard. Includes auth\_mode (dcr|manual), has\_client\_secret, client\_secret\_version, and the OAuth endpoints + client\_id for manual servers. Never includes the secret value.

</summary>

<details>

<summary>

auth\_mode: optional "dcr"or "manual"

</summary>

One of the following:

"dcr"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

client\_secret\_version: optional number

<a href="#">Link to this property</a>

<details>

<summary>

config: optional object {authorization\_endpoint, issuer, resource, 2 more }

</summary>

authorization\_endpoint: optional string

<a href="#">Link to this property</a>

issuer: optional string

<a href="#">Link to this property</a>

resource: optional string

<a href="#">Link to this property</a>

revocation\_endpoint: optional string

<a href="#">Link to this property</a>

token\_endpoint: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

has\_client\_secret: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

registration\_info: optional object {client\_id, redirect\_uris, scope, token\_endpoint\_auth\_method }

</summary>

client\_id: optional string

<a href="#">Link to this property</a>

redirect\_uris: optional array of string

<a href="#">Link to this property</a>

scope: optional string

<a href="#">Link to this property</a>

token\_endpoint\_auth\_method: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

authentication\_status: optional "not\_required"or "required"or "connected"or 2 more

Whether administrative authentication is required before capabilities can be synced. Manual OAuth is user-managed and has no administrative authentication flow.

</summary>

One of the following:

"not\_required"

<a href="#">Link to this property</a>

"required"

<a href="#">Link to this property</a>

"connected"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

default\_disabled: optional boolean

Hide this server’s tools and prompts by default. To expose specific capabilities, set enabled: true for them in updated\_tools or updated\_prompts.

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP server.

maxLength512

<a href="#">Link to this property</a>

error: optional string

<a href="#">Link to this property</a>

<details>

<summary>

error\_details: optional object {cause, is\_upstream, mcp\_code, 2 more }

</summary>

cause: optional string

Underlying error message

<a href="#">Link to this property</a>

is\_upstream: optional boolean

True = MCP server returned an error. False = couldn’t reach the server

<a href="#">Link to this property</a>

mcp\_code: optional number

MCP protocol error code

<a href="#">Link to this property</a>

retryable: optional boolean

Whether the error is transient and worth retrying

<a href="#">Link to this property</a>

status\_code: optional number

HTTP status code from the server

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

is\_shared\_oauth\_callback\_enabled: optional boolean

When true, the gateway worker uses the shared Cloudflare-owned OAuth callback endpoint as the redirect\_uri for upstream on-behalf OAuth, instead of the customer portal hostname. Defaults to false (off); opt in per server by setting true.

<a href="#">Link to this property</a>

last\_successful\_sync: optional string

formatdate-time

<a href="#">Link to this property</a>

last\_synced: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

on\_behalf: optional boolean

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound traffic to this MCP server through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "waiting"or "ready"or "stale"or "error"

Current sync state of the server

</summary>

One of the following:

"waiting"

<a href="#">Link to this property</a>

"ready"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_prompts: optional array of object {name, enabled, portal\_alias, 3 more }

</summary>

name: string

<a href="#">Link to this property</a>

enabled: optional boolean

<a href="#">Link to this property</a>

portal\_alias: optional string

<a href="#">Link to this property</a>

portal\_description: optional string

<a href="#">Link to this property</a>

server\_alias: optional string

<a href="#">Link to this property</a>

server\_description: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_tools: optional array of object {name, enabled, portal\_alias, 3 more }

</summary>

name: string

<a href="#">Link to this property</a>

enabled: optional boolean

<a href="#">Link to this property</a>

portal\_alias: optional string

<a href="#">Link to this property</a>

portal\_description: optional string

<a href="#">Link to this property</a>

server\_alias: optional string

<a href="#">Link to this property</a>

server\_description: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

Deprecatedallow\_code\_mode: optional boolean

Deprecated: use <code>code_mode</code> for new integrations. <code>true</code> maps to any non-off Code Mode policy; <code>false</code> maps to <code>code_mode: off</code>. If both fields are sent, they must be consistent or the request returns a 400.

<a href="#">Link to this property</a>

<details>

<summary>

code\_mode: optional "off"or "opt\_in"or "default\_on"or "enforced"

Code Mode policy for this portal. <code>off</code>: Code Mode is unavailable; query parameters are ignored. <code>opt_in</code>: Code Mode is off by default; clients turn it on with <code>?codemode=search_and_execute</code>. <code>default_on</code>: Code Mode is on by default; clients can opt out with <code>?codemode=off</code>. <code>enforced</code>: Code Mode is always on; query parameters are ignored. Defaults to <code>opt_in</code> when omitted on create. If both <code>code_mode</code> and <code>allow_code_mode</code> are sent, they must be consistent or the request returns a 400.

</summary>

One of the following:

"off"

<a href="#">Link to this property</a>

"opt\_in"

<a href="#">Link to this property</a>

"default\_on"

<a href="#">Link to this property</a>

"enforced"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP portal.

maxLength512

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound MCP traffic through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.ai_controls.mcp.portals%20%3E%20(model)%20portal_update_response%20%3E%20(schema)>)

<details>

<summary>

PortalDeleteResponse object {id, hostname, name, 8 more }

</summary>

id: string

Unique identifier for the MCP portal.

maxLength32

minLength1

<a href="#">Link to this property</a>

hostname: string

Hostname where the MCP portal is available.

<a href="#">Link to this property</a>

name: string

Display name for the MCP portal.

maxLength350

<a href="#">Link to this property</a>

Deprecatedallow\_code\_mode: optional boolean

Deprecated: use <code>code_mode</code> for new integrations. <code>true</code> maps to any non-off Code Mode policy; <code>false</code> maps to <code>code_mode: off</code>. If both fields are sent, they must be consistent or the request returns a 400.

<a href="#">Link to this property</a>

<details>

<summary>

code\_mode: optional "off"or "opt\_in"or "default\_on"or "enforced"

Code Mode policy for this portal. <code>off</code>: Code Mode is unavailable; query parameters are ignored. <code>opt_in</code>: Code Mode is off by default; clients turn it on with <code>?codemode=search_and_execute</code>. <code>default_on</code>: Code Mode is on by default; clients can opt out with <code>?codemode=off</code>. <code>enforced</code>: Code Mode is always on; query parameters are ignored. Defaults to <code>opt_in</code> when omitted on create. If both <code>code_mode</code> and <code>allow_code_mode</code> are sent, they must be consistent or the request returns a 400.

</summary>

One of the following:

"off"

<a href="#">Link to this property</a>

"opt\_in"

<a href="#">Link to this property</a>

"default\_on"

<a href="#">Link to this property</a>

"enforced"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP portal.

maxLength512

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound MCP traffic through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.ai_controls.mcp.portals%20%3E%20(model)%20portal_delete_response%20%3E%20(schema)>)

#### AccessAI ControlsMcpServers

##### [List MCP Servers](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/ai_controls/subresources/mcp/subresources/servers/methods/list)

GET/accounts/{account\_id}/access/ai-controls/mcp/servers

##### [Create a new MCP Server](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/ai_controls/subresources/mcp/subresources/servers/methods/create)

POST/accounts/{account\_id}/access/ai-controls/mcp/servers

##### [Read the details of an MCP Server](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/ai_controls/subresources/mcp/subresources/servers/methods/read)

GET/accounts/{account\_id}/access/ai-controls/mcp/servers/{id}

##### [Update an MCP Server](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/ai_controls/subresources/mcp/subresources/servers/methods/update)

PUT/accounts/{account\_id}/access/ai-controls/mcp/servers/{id}

##### [Delete an MCP Server](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/ai_controls/subresources/mcp/subresources/servers/methods/delete)

DELETE/accounts/{account\_id}/access/ai-controls/mcp/servers/{id}

##### [Sync MCP Server Capabilities](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/ai_controls/subresources/mcp/subresources/servers/methods/sync)

POST/accounts/{account\_id}/access/ai-controls/mcp/servers/{id}/sync

##### ModelsExpand Collapse

<details>

<summary>

ServerListResponse object {id, auth\_type, hostname, 19 more }

</summary>

id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

auth\_type: "oauth"or "bearer"or "unauthenticated"

Authentication method used to connect to the upstream MCP server.

</summary>

One of the following:

"oauth"

<a href="#">Link to this property</a>

"bearer"

<a href="#">Link to this property</a>

"unauthenticated"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

hostname: string

URL of the upstream MCP endpoint.

formaturi

<a href="#">Link to this property</a>

name: string

Display name for the MCP server.

maxLength350

<a href="#">Link to this property</a>

prompts: array of map\[unknown]

<a href="#">Link to this property</a>

tools: array of map\[unknown]

<a href="#">Link to this property</a>

<details>

<summary>

auth\_config\_summary: optional object {auth\_mode, client\_secret\_version, config, 2 more }

Safe subset of auth\_credentials surfaced to the dashboard. Includes auth\_mode (dcr|manual), has\_client\_secret, client\_secret\_version, and the OAuth endpoints + client\_id for manual servers. Never includes the secret value.

</summary>

<details>

<summary>

auth\_mode: optional "dcr"or "manual"

</summary>

One of the following:

"dcr"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

client\_secret\_version: optional number

<a href="#">Link to this property</a>

<details>

<summary>

config: optional object {authorization\_endpoint, issuer, resource, 2 more }

</summary>

authorization\_endpoint: optional string

<a href="#">Link to this property</a>

issuer: optional string

<a href="#">Link to this property</a>

resource: optional string

<a href="#">Link to this property</a>

revocation\_endpoint: optional string

<a href="#">Link to this property</a>

token\_endpoint: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

has\_client\_secret: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

registration\_info: optional object {client\_id, redirect\_uris, scope, token\_endpoint\_auth\_method }

</summary>

client\_id: optional string

<a href="#">Link to this property</a>

redirect\_uris: optional array of string

<a href="#">Link to this property</a>

scope: optional string

<a href="#">Link to this property</a>

token\_endpoint\_auth\_method: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

authentication\_status: optional "not\_required"or "required"or "connected"or 2 more

Whether administrative authentication is required before capabilities can be synced. Manual OAuth is user-managed and has no administrative authentication flow.

</summary>

One of the following:

"not\_required"

<a href="#">Link to this property</a>

"required"

<a href="#">Link to this property</a>

"connected"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP server.

maxLength512

<a href="#">Link to this property</a>

error: optional string

<a href="#">Link to this property</a>

<details>

<summary>

error\_details: optional object {cause, is\_upstream, mcp\_code, 2 more }

</summary>

cause: optional string

Underlying error message

<a href="#">Link to this property</a>

is\_upstream: optional boolean

True = MCP server returned an error. False = couldn’t reach the server

<a href="#">Link to this property</a>

mcp\_code: optional number

MCP protocol error code

<a href="#">Link to this property</a>

retryable: optional boolean

Whether the error is transient and worth retrying

<a href="#">Link to this property</a>

status\_code: optional number

HTTP status code from the server

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

is\_shared\_oauth\_callback\_enabled: optional boolean

When true, the gateway worker uses the shared Cloudflare-owned OAuth callback endpoint as the redirect\_uri for upstream on-behalf OAuth, instead of the customer portal hostname. Defaults to false (off); opt in per server by setting true.

<a href="#">Link to this property</a>

last\_successful\_sync: optional string

formatdate-time

<a href="#">Link to this property</a>

last\_synced: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound traffic to this MCP server through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "waiting"or "ready"or "stale"or "error"

Current sync state of the server

</summary>

One of the following:

"waiting"

<a href="#">Link to this property</a>

"ready"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_prompts: optional array of object {name, alias, description, enabled }

Server-wide prompt capability overrides.

</summary>

name: string

Name of the tool or prompt capability to override.

<a href="#">Link to this property</a>

alias: optional string

Custom name exposed for the capability.

maxLength40

<a href="#">Link to this property</a>

description: optional string

Custom description exposed for the capability.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the capability is available through the MCP server.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_tools: optional array of object {name, alias, description, enabled }

Server-wide tool capability overrides.

</summary>

name: string

Name of the tool or prompt capability to override.

<a href="#">Link to this property</a>

alias: optional string

Custom name exposed for the capability.

maxLength40

<a href="#">Link to this property</a>

description: optional string

Custom description exposed for the capability.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the capability is available through the MCP server.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.ai_controls.mcp.servers%20%3E%20(model)%20server_list_response%20%3E%20(schema)>)

<details>

<summary>

ServerCreateResponse object {id, auth\_type, hostname, 19 more }

</summary>

id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

auth\_type: "oauth"or "bearer"or "unauthenticated"

Authentication method used to connect to the upstream MCP server.

</summary>

One of the following:

"oauth"

<a href="#">Link to this property</a>

"bearer"

<a href="#">Link to this property</a>

"unauthenticated"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

hostname: string

URL of the upstream MCP endpoint.

formaturi

<a href="#">Link to this property</a>

name: string

Display name for the MCP server.

maxLength350

<a href="#">Link to this property</a>

prompts: array of map\[unknown]

<a href="#">Link to this property</a>

tools: array of map\[unknown]

<a href="#">Link to this property</a>

<details>

<summary>

auth\_config\_summary: optional object {auth\_mode, client\_secret\_version, config, 2 more }

Safe subset of auth\_credentials surfaced to the dashboard. Includes auth\_mode (dcr|manual), has\_client\_secret, client\_secret\_version, and the OAuth endpoints + client\_id for manual servers. Never includes the secret value.

</summary>

<details>

<summary>

auth\_mode: optional "dcr"or "manual"

</summary>

One of the following:

"dcr"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

client\_secret\_version: optional number

<a href="#">Link to this property</a>

<details>

<summary>

config: optional object {authorization\_endpoint, issuer, resource, 2 more }

</summary>

authorization\_endpoint: optional string

<a href="#">Link to this property</a>

issuer: optional string

<a href="#">Link to this property</a>

resource: optional string

<a href="#">Link to this property</a>

revocation\_endpoint: optional string

<a href="#">Link to this property</a>

token\_endpoint: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

has\_client\_secret: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

registration\_info: optional object {client\_id, redirect\_uris, scope, token\_endpoint\_auth\_method }

</summary>

client\_id: optional string

<a href="#">Link to this property</a>

redirect\_uris: optional array of string

<a href="#">Link to this property</a>

scope: optional string

<a href="#">Link to this property</a>

token\_endpoint\_auth\_method: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

authentication\_status: optional "not\_required"or "required"or "connected"or 2 more

Whether administrative authentication is required before capabilities can be synced. Manual OAuth is user-managed and has no administrative authentication flow.

</summary>

One of the following:

"not\_required"

<a href="#">Link to this property</a>

"required"

<a href="#">Link to this property</a>

"connected"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP server.

maxLength512

<a href="#">Link to this property</a>

error: optional string

<a href="#">Link to this property</a>

<details>

<summary>

error\_details: optional object {cause, is\_upstream, mcp\_code, 2 more }

</summary>

cause: optional string

Underlying error message

<a href="#">Link to this property</a>

is\_upstream: optional boolean

True = MCP server returned an error. False = couldn’t reach the server

<a href="#">Link to this property</a>

mcp\_code: optional number

MCP protocol error code

<a href="#">Link to this property</a>

retryable: optional boolean

Whether the error is transient and worth retrying

<a href="#">Link to this property</a>

status\_code: optional number

HTTP status code from the server

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

is\_shared\_oauth\_callback\_enabled: optional boolean

When true, the gateway worker uses the shared Cloudflare-owned OAuth callback endpoint as the redirect\_uri for upstream on-behalf OAuth, instead of the customer portal hostname. Defaults to false (off); opt in per server by setting true.

<a href="#">Link to this property</a>

last\_successful\_sync: optional string

formatdate-time

<a href="#">Link to this property</a>

last\_synced: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound traffic to this MCP server through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "waiting"or "ready"or "stale"or "error"

Current sync state of the server

</summary>

One of the following:

"waiting"

<a href="#">Link to this property</a>

"ready"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_prompts: optional array of object {name, alias, description, enabled }

Server-wide prompt capability overrides.

</summary>

name: string

Name of the tool or prompt capability to override.

<a href="#">Link to this property</a>

alias: optional string

Custom name exposed for the capability.

maxLength40

<a href="#">Link to this property</a>

description: optional string

Custom description exposed for the capability.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the capability is available through the MCP server.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_tools: optional array of object {name, alias, description, enabled }

Server-wide tool capability overrides.

</summary>

name: string

Name of the tool or prompt capability to override.

<a href="#">Link to this property</a>

alias: optional string

Custom name exposed for the capability.

maxLength40

<a href="#">Link to this property</a>

description: optional string

Custom description exposed for the capability.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the capability is available through the MCP server.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.ai_controls.mcp.servers%20%3E%20(model)%20server_create_response%20%3E%20(schema)>)

<details>

<summary>

ServerReadResponse object {id, auth\_type, hostname, 19 more }

</summary>

id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

auth\_type: "oauth"or "bearer"or "unauthenticated"

Authentication method used to connect to the upstream MCP server.

</summary>

One of the following:

"oauth"

<a href="#">Link to this property</a>

"bearer"

<a href="#">Link to this property</a>

"unauthenticated"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

hostname: string

URL of the upstream MCP endpoint.

formaturi

<a href="#">Link to this property</a>

name: string

Display name for the MCP server.

maxLength350

<a href="#">Link to this property</a>

prompts: array of map\[unknown]

<a href="#">Link to this property</a>

tools: array of map\[unknown]

<a href="#">Link to this property</a>

<details>

<summary>

auth\_config\_summary: optional object {auth\_mode, client\_secret\_version, config, 2 more }

Safe subset of auth\_credentials surfaced to the dashboard. Includes auth\_mode (dcr|manual), has\_client\_secret, client\_secret\_version, and the OAuth endpoints + client\_id for manual servers. Never includes the secret value.

</summary>

<details>

<summary>

auth\_mode: optional "dcr"or "manual"

</summary>

One of the following:

"dcr"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

client\_secret\_version: optional number

<a href="#">Link to this property</a>

<details>

<summary>

config: optional object {authorization\_endpoint, issuer, resource, 2 more }

</summary>

authorization\_endpoint: optional string

<a href="#">Link to this property</a>

issuer: optional string

<a href="#">Link to this property</a>

resource: optional string

<a href="#">Link to this property</a>

revocation\_endpoint: optional string

<a href="#">Link to this property</a>

token\_endpoint: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

has\_client\_secret: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

registration\_info: optional object {client\_id, redirect\_uris, scope, token\_endpoint\_auth\_method }

</summary>

client\_id: optional string

<a href="#">Link to this property</a>

redirect\_uris: optional array of string

<a href="#">Link to this property</a>

scope: optional string

<a href="#">Link to this property</a>

token\_endpoint\_auth\_method: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

authentication\_status: optional "not\_required"or "required"or "connected"or 2 more

Whether administrative authentication is required before capabilities can be synced. Manual OAuth is user-managed and has no administrative authentication flow.

</summary>

One of the following:

"not\_required"

<a href="#">Link to this property</a>

"required"

<a href="#">Link to this property</a>

"connected"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP server.

maxLength512

<a href="#">Link to this property</a>

error: optional string

<a href="#">Link to this property</a>

<details>

<summary>

error\_details: optional object {cause, is\_upstream, mcp\_code, 2 more }

</summary>

cause: optional string

Underlying error message

<a href="#">Link to this property</a>

is\_upstream: optional boolean

True = MCP server returned an error. False = couldn’t reach the server

<a href="#">Link to this property</a>

mcp\_code: optional number

MCP protocol error code

<a href="#">Link to this property</a>

retryable: optional boolean

Whether the error is transient and worth retrying

<a href="#">Link to this property</a>

status\_code: optional number

HTTP status code from the server

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

is\_shared\_oauth\_callback\_enabled: optional boolean

When true, the gateway worker uses the shared Cloudflare-owned OAuth callback endpoint as the redirect\_uri for upstream on-behalf OAuth, instead of the customer portal hostname. Defaults to false (off); opt in per server by setting true.

<a href="#">Link to this property</a>

last\_successful\_sync: optional string

formatdate-time

<a href="#">Link to this property</a>

last\_synced: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound traffic to this MCP server through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "waiting"or "ready"or "stale"or "error"

Current sync state of the server

</summary>

One of the following:

"waiting"

<a href="#">Link to this property</a>

"ready"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_prompts: optional array of object {name, alias, description, enabled }

Server-wide prompt capability overrides.

</summary>

name: string

Name of the tool or prompt capability to override.

<a href="#">Link to this property</a>

alias: optional string

Custom name exposed for the capability.

maxLength40

<a href="#">Link to this property</a>

description: optional string

Custom description exposed for the capability.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the capability is available through the MCP server.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_tools: optional array of object {name, alias, description, enabled }

Server-wide tool capability overrides.

</summary>

name: string

Name of the tool or prompt capability to override.

<a href="#">Link to this property</a>

alias: optional string

Custom name exposed for the capability.

maxLength40

<a href="#">Link to this property</a>

description: optional string

Custom description exposed for the capability.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the capability is available through the MCP server.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.ai_controls.mcp.servers%20%3E%20(model)%20server_read_response%20%3E%20(schema)>)

<details>

<summary>

ServerUpdateResponse object {id, auth\_type, hostname, 19 more }

</summary>

id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

auth\_type: "oauth"or "bearer"or "unauthenticated"

Authentication method used to connect to the upstream MCP server.

</summary>

One of the following:

"oauth"

<a href="#">Link to this property</a>

"bearer"

<a href="#">Link to this property</a>

"unauthenticated"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

hostname: string

URL of the upstream MCP endpoint.

formaturi

<a href="#">Link to this property</a>

name: string

Display name for the MCP server.

maxLength350

<a href="#">Link to this property</a>

prompts: array of map\[unknown]

<a href="#">Link to this property</a>

tools: array of map\[unknown]

<a href="#">Link to this property</a>

<details>

<summary>

auth\_config\_summary: optional object {auth\_mode, client\_secret\_version, config, 2 more }

Safe subset of auth\_credentials surfaced to the dashboard. Includes auth\_mode (dcr|manual), has\_client\_secret, client\_secret\_version, and the OAuth endpoints + client\_id for manual servers. Never includes the secret value.

</summary>

<details>

<summary>

auth\_mode: optional "dcr"or "manual"

</summary>

One of the following:

"dcr"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

client\_secret\_version: optional number

<a href="#">Link to this property</a>

<details>

<summary>

config: optional object {authorization\_endpoint, issuer, resource, 2 more }

</summary>

authorization\_endpoint: optional string

<a href="#">Link to this property</a>

issuer: optional string

<a href="#">Link to this property</a>

resource: optional string

<a href="#">Link to this property</a>

revocation\_endpoint: optional string

<a href="#">Link to this property</a>

token\_endpoint: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

has\_client\_secret: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

registration\_info: optional object {client\_id, redirect\_uris, scope, token\_endpoint\_auth\_method }

</summary>

client\_id: optional string

<a href="#">Link to this property</a>

redirect\_uris: optional array of string

<a href="#">Link to this property</a>

scope: optional string

<a href="#">Link to this property</a>

token\_endpoint\_auth\_method: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

authentication\_status: optional "not\_required"or "required"or "connected"or 2 more

Whether administrative authentication is required before capabilities can be synced. Manual OAuth is user-managed and has no administrative authentication flow.

</summary>

One of the following:

"not\_required"

<a href="#">Link to this property</a>

"required"

<a href="#">Link to this property</a>

"connected"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP server.

maxLength512

<a href="#">Link to this property</a>

error: optional string

<a href="#">Link to this property</a>

<details>

<summary>

error\_details: optional object {cause, is\_upstream, mcp\_code, 2 more }

</summary>

cause: optional string

Underlying error message

<a href="#">Link to this property</a>

is\_upstream: optional boolean

True = MCP server returned an error. False = couldn’t reach the server

<a href="#">Link to this property</a>

mcp\_code: optional number

MCP protocol error code

<a href="#">Link to this property</a>

retryable: optional boolean

Whether the error is transient and worth retrying

<a href="#">Link to this property</a>

status\_code: optional number

HTTP status code from the server

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

is\_shared\_oauth\_callback\_enabled: optional boolean

When true, the gateway worker uses the shared Cloudflare-owned OAuth callback endpoint as the redirect\_uri for upstream on-behalf OAuth, instead of the customer portal hostname. Defaults to false (off); opt in per server by setting true.

<a href="#">Link to this property</a>

last\_successful\_sync: optional string

formatdate-time

<a href="#">Link to this property</a>

last\_synced: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound traffic to this MCP server through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "waiting"or "ready"or "stale"or "error"

Current sync state of the server

</summary>

One of the following:

"waiting"

<a href="#">Link to this property</a>

"ready"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_prompts: optional array of object {name, alias, description, enabled }

Server-wide prompt capability overrides.

</summary>

name: string

Name of the tool or prompt capability to override.

<a href="#">Link to this property</a>

alias: optional string

Custom name exposed for the capability.

maxLength40

<a href="#">Link to this property</a>

description: optional string

Custom description exposed for the capability.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the capability is available through the MCP server.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_tools: optional array of object {name, alias, description, enabled }

Server-wide tool capability overrides.

</summary>

name: string

Name of the tool or prompt capability to override.

<a href="#">Link to this property</a>

alias: optional string

Custom name exposed for the capability.

maxLength40

<a href="#">Link to this property</a>

description: optional string

Custom description exposed for the capability.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the capability is available through the MCP server.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.ai_controls.mcp.servers%20%3E%20(model)%20server_update_response%20%3E%20(schema)>)

<details>

<summary>

ServerDeleteResponse object {id, auth\_type, hostname, 19 more }

</summary>

id: string

Unique identifier for the MCP server.

maxLength32

minLength1

<a href="#">Link to this property</a>

<details>

<summary>

auth\_type: "oauth"or "bearer"or "unauthenticated"

Authentication method used to connect to the upstream MCP server.

</summary>

One of the following:

"oauth"

<a href="#">Link to this property</a>

"bearer"

<a href="#">Link to this property</a>

"unauthenticated"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

hostname: string

URL of the upstream MCP endpoint.

formaturi

<a href="#">Link to this property</a>

name: string

Display name for the MCP server.

maxLength350

<a href="#">Link to this property</a>

prompts: array of map\[unknown]

<a href="#">Link to this property</a>

tools: array of map\[unknown]

<a href="#">Link to this property</a>

<details>

<summary>

auth\_config\_summary: optional object {auth\_mode, client\_secret\_version, config, 2 more }

Safe subset of auth\_credentials surfaced to the dashboard. Includes auth\_mode (dcr|manual), has\_client\_secret, client\_secret\_version, and the OAuth endpoints + client\_id for manual servers. Never includes the secret value.

</summary>

<details>

<summary>

auth\_mode: optional "dcr"or "manual"

</summary>

One of the following:

"dcr"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

client\_secret\_version: optional number

<a href="#">Link to this property</a>

<details>

<summary>

config: optional object {authorization\_endpoint, issuer, resource, 2 more }

</summary>

authorization\_endpoint: optional string

<a href="#">Link to this property</a>

issuer: optional string

<a href="#">Link to this property</a>

resource: optional string

<a href="#">Link to this property</a>

revocation\_endpoint: optional string

<a href="#">Link to this property</a>

token\_endpoint: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

has\_client\_secret: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

registration\_info: optional object {client\_id, redirect\_uris, scope, token\_endpoint\_auth\_method }

</summary>

client\_id: optional string

<a href="#">Link to this property</a>

redirect\_uris: optional array of string

<a href="#">Link to this property</a>

scope: optional string

<a href="#">Link to this property</a>

token\_endpoint\_auth\_method: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

authentication\_status: optional "not\_required"or "required"or "connected"or 2 more

Whether administrative authentication is required before capabilities can be synced. Manual OAuth is user-managed and has no administrative authentication flow.

</summary>

One of the following:

"not\_required"

<a href="#">Link to this property</a>

"required"

<a href="#">Link to this property</a>

"connected"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"manual"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

created\_by: optional string

<a href="#">Link to this property</a>

description: optional string

Optional description of the MCP server.

maxLength512

<a href="#">Link to this property</a>

error: optional string

<a href="#">Link to this property</a>

<details>

<summary>

error\_details: optional object {cause, is\_upstream, mcp\_code, 2 more }

</summary>

cause: optional string

Underlying error message

<a href="#">Link to this property</a>

is\_upstream: optional boolean

True = MCP server returned an error. False = couldn’t reach the server

<a href="#">Link to this property</a>

mcp\_code: optional number

MCP protocol error code

<a href="#">Link to this property</a>

retryable: optional boolean

Whether the error is transient and worth retrying

<a href="#">Link to this property</a>

status\_code: optional number

HTTP status code from the server

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

is\_shared\_oauth\_callback\_enabled: optional boolean

When true, the gateway worker uses the shared Cloudflare-owned OAuth callback endpoint as the redirect\_uri for upstream on-behalf OAuth, instead of the customer portal hostname. Defaults to false (off); opt in per server by setting true.

<a href="#">Link to this property</a>

last\_successful\_sync: optional string

formatdate-time

<a href="#">Link to this property</a>

last\_synced: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

modified\_by: optional string

<a href="#">Link to this property</a>

secure\_web\_gateway: optional boolean

Route outbound traffic to this MCP server through Zero Trust Secure Web Gateway.

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "waiting"or "ready"or "stale"or "error"

Current sync state of the server

</summary>

One of the following:

"waiting"

<a href="#">Link to this property</a>

"ready"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_prompts: optional array of object {name, alias, description, enabled }

Server-wide prompt capability overrides.

</summary>

name: string

Name of the tool or prompt capability to override.

<a href="#">Link to this property</a>

alias: optional string

Custom name exposed for the capability.

maxLength40

<a href="#">Link to this property</a>

description: optional string

Custom description exposed for the capability.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the capability is available through the MCP server.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

updated\_tools: optional array of object {name, alias, description, enabled }

Server-wide tool capability overrides.

</summary>

name: string

Name of the tool or prompt capability to override.

<a href="#">Link to this property</a>

alias: optional string

Custom name exposed for the capability.

maxLength40

<a href="#">Link to this property</a>

description: optional string

Custom description exposed for the capability.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the capability is available through the MCP server.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.ai_controls.mcp.servers%20%3E%20(model)%20server_delete_response%20%3E%20(schema)>)

<details>

<summary>

ServerSyncResponse object {error, error\_details, status }

</summary>

error: optional string

<a href="#">Link to this property</a>

<details>

<summary>

error\_details: optional object {cause, is\_upstream, mcp\_code, 2 more }

</summary>

cause: optional string

Underlying error message

<a href="#">Link to this property</a>

is\_upstream: optional boolean

True = MCP server returned an error. False = couldn’t reach the server

<a href="#">Link to this property</a>

mcp\_code: optional number

MCP protocol error code

<a href="#">Link to this property</a>

retryable: optional boolean

Whether the error is transient and worth retrying

<a href="#">Link to this property</a>

status\_code: optional number

HTTP status code from the server

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

status: optional "waiting"or "ready"or "stale"or "error"

</summary>

One of the following:

"waiting"

<a href="#">Link to this property</a>

"ready"

<a href="#">Link to this property</a>

"stale"

<a href="#">Link to this property</a>

"error"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.ai_controls.mcp.servers%20%3E%20(model)%20server_sync_response%20%3E%20(schema)>)

#### AccessGateway CA

##### [List SSH Certificate Authorities (CA)](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/gateway_ca/methods/list)

GET/accounts/{account\_id}/access/gateway\_ca

##### [Add a new SSH Certificate Authority (CA)](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/gateway_ca/methods/create)

POST/accounts/{account\_id}/access/gateway\_ca

##### [Delete an SSH Certificate Authority (CA)](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/gateway_ca/methods/delete)

DELETE/accounts/{account\_id}/access/gateway\_ca/{certificate\_id}

##### ModelsExpand Collapse

<details>

<summary>

GatewayCAListResponse object {id, public\_key }

</summary>

id: optional string

The key ID of this certificate.

<a href="#">Link to this property</a>

public\_key: optional string

The public key of this certificate.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.gateway_ca%20%3E%20(model)%20gateway_ca_list_response%20%3E%20(schema)>)

<details>

<summary>

GatewayCACreateResponse object {id, public\_key }

</summary>

id: optional string

The key ID of this certificate.

<a href="#">Link to this property</a>

public\_key: optional string

The public key of this certificate.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.gateway_ca%20%3E%20(model)%20gateway_ca_create_response%20%3E%20(schema)>)

<details>

<summary>

GatewayCADeleteResponse object {id }

</summary>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.gateway_ca%20%3E%20(model)%20gateway_ca_delete_response%20%3E%20(schema)>)

#### AccessIdP Federation Grants

##### [List IdP federation grants](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/idp_federation_grants/methods/list)

GET/accounts/{account\_id}/access/idp\_federation\_grants

##### [Create an IdP federation grant](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/idp_federation_grants/methods/create)

POST/accounts/{account\_id}/access/idp\_federation\_grants

##### [Get an IdP federation grant](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/idp_federation_grants/methods/get)

GET/accounts/{account\_id}/access/idp\_federation\_grants/{grant\_id}

##### [Delete an IdP federation grant](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/idp_federation_grants/methods/delete)

DELETE/accounts/{account\_id}/access/idp\_federation\_grants/{grant\_id}

##### ModelsExpand Collapse

<details>

<summary>

IdPFederationGrant object {id, idp\_id }

</summary>

id: string

UID of the IdP federation grant.

maxLength32

<a href="#">Link to this property</a>

idp\_id: string

UID of the identity provider being federated.

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.idp_federation_grants%20%3E%20(model)%20idp_federation_grant%20%3E%20(schema)>)

<details>

<summary>

IdPFederationGrantListResponse = array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.idp_federation_grants%20%3E%20(model)%20idp_federation_grant%20%3E%20(schema)">IdPFederationGrant</a> { id, idp\_id }

</summary>

id: string

UID of the IdP federation grant.

maxLength32

<a href="#">Link to this property</a>

idp\_id: string

UID of the identity provider being federated.

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.idp_federation_grants%20%3E%20(model)%20idp_federation_grant_list_response%20%3E%20(schema)>)

<details>

<summary>

IdPFederationGrantDeleteResponse object {id }

</summary>

id: optional string

UID of the deleted IdP federation grant.

maxLength32

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.idp_federation_grants%20%3E%20(model)%20idp_federation_grant_delete_response%20%3E%20(schema)>)

#### AccessSAML Certificates

##### [List SAML certificate sets](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/saml_certificates/methods/list)

GET/accounts/{account\_id}/access/saml\_certificates

##### [Get SAML certificate set](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/saml_certificates/methods/get)

GET/accounts/{account\_id}/access/saml\_certificates/{saml\_cert\_set\_id}

##### [Rotate SAML certificate](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/saml_certificates/methods/rotate)

POST/accounts/{account\_id}/access/saml\_certificates/{saml\_cert\_set\_id}/rotate

##### [Download current certificate in PEM format](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/saml_certificates/methods/get_pem)

GET/accounts/{account\_id}/access/saml\_certificates/{saml\_cert\_set\_id}/pem

##### ModelsExpand Collapse

<details>

<summary>

SAMLCertificateListResponse object {created\_at, uid, updated\_at, 2 more }

</summary>

created\_at: string

When the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

<a href="#">Link to this property</a>

updated\_at: string

When the certificate set was last updated

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The current active certificate

</summary>

is\_current: boolean

Indicates whether the certificate can be used for IdP configuration.

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

The public certificate in PEM format

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate (maintained during rotation period). May be null when no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.saml_certificates%20%3E%20(model)%20saml_certificate_list_response%20%3E%20(schema)>)

<details>

<summary>

SAMLCertificateGetResponse object {created\_at, uid, updated\_at, 2 more }

</summary>

created\_at: string

When the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

<a href="#">Link to this property</a>

updated\_at: string

When the certificate set was last updated

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The current active certificate

</summary>

is\_current: boolean

Indicates whether the certificate can be used for IdP configuration.

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

The public certificate in PEM format

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate (maintained during rotation period). May be null when no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.saml_certificates%20%3E%20(model)%20saml_certificate_get_response%20%3E%20(schema)>)

<details>

<summary>

SAMLCertificateRotateResponse object {created\_at, uid, updated\_at, 2 more }

</summary>

created\_at: string

When the certificate set was created

formatdate-time

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate set

<a href="#">Link to this property</a>

updated\_at: string

When the certificate set was last updated

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

current\_certificate: optional object {is\_current, not\_after, public\_certificate, uid }

The current active certificate

</summary>

is\_current: boolean

Indicates whether the certificate can be used for IdP configuration.

<a href="#">Link to this property</a>

not\_after: string

Certificate expiration date

formatdate-time

<a href="#">Link to this property</a>

public\_certificate: string

The public certificate in PEM format

<a href="#">Link to this property</a>

uid: string

Unique identifier for the certificate

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

previous\_certificate: optional unknown

The previous certificate (maintained during rotation period). May be null when no rotation has occurred. Mirrors the structure of <code>saml_certificate</code>.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.saml_certificates%20%3E%20(model)%20saml_certificate_rotate_response%20%3E%20(schema)>)

#### AccessInfrastructure

#### AccessInfrastructureTargets

##### [List all targets](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/infrastructure/subresources/targets/methods/list)

GET/accounts/{account\_id}/infrastructure/targets

##### [Get target](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/infrastructure/subresources/targets/methods/get)

GET/accounts/{account\_id}/infrastructure/targets/{target\_id}

##### [Create new target](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/infrastructure/subresources/targets/methods/create)

POST/accounts/{account\_id}/infrastructure/targets

##### [Update target](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/infrastructure/subresources/targets/methods/update)

PUT/accounts/{account\_id}/infrastructure/targets/{target\_id}

##### [Delete target](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/infrastructure/subresources/targets/methods/delete)

DELETE/accounts/{account\_id}/infrastructure/targets/{target\_id}

##### [Create new targets](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/infrastructure/subresources/targets/methods/bulk_update)

PUT/accounts/{account\_id}/infrastructure/targets/batch

##### [Delete targets (Deprecated)](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/infrastructure/subresources/targets/methods/bulk_delete)

Deprecated

DELETE/accounts/{account\_id}/infrastructure/targets/batch

##### [Delete targets](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/infrastructure/subresources/targets/methods/bulk_delete_v2)

POST/accounts/{account\_id}/infrastructure/targets/batch\_delete

##### ModelsExpand Collapse

<details>

<summary>

TargetListResponse object {id, created\_at, hostname, 3 more }

</summary>

id: string

Target identifier

formatuuid

maxLength36

<a href="#">Link to this property</a>

created\_at: string

Date and time at which the target was created

formatdate-time

<a href="#">Link to this property</a>

hostname: string

A non-unique field that refers to a target

<a href="#">Link to this property</a>

<details>

<summary>

ip: object {ipv4, ipv6 }

The IPv4/IPv6 address that identifies where to reach a target

</summary>

<details>

<summary>

ipv4: optional object {ip\_addr, virtual\_network\_id }

The target’s IPv4 address

</summary>

ip\_addr: optional string

IP address of the target

<a href="#">Link to this property</a>

virtual\_network\_id: optional string

(optional) Private virtual network identifier for the target. If omitted, the default virtual network ID will be used.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ipv6: optional object {ip\_addr, virtual\_network\_id }

The target’s IPv6 address

</summary>

ip\_addr: optional string

IP address of the target

<a href="#">Link to this property</a>

virtual\_network\_id: optional string

(optional) Private virtual network identifier for the target. If omitted, the default virtual network ID will be used.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

modified\_at: string

Date and time at which the target was modified

formatdate-time

<a href="#">Link to this property</a>

tags: optional map\[string]

Tags assigned to the target. Empty when no tags are assigned.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.infrastructure.targets%20%3E%20(model)%20target_list_response%20%3E%20(schema)>)

<details>

<summary>

TargetGetResponse object {id, created\_at, hostname, 3 more }

</summary>

id: string

Target identifier

formatuuid

maxLength36

<a href="#">Link to this property</a>

created\_at: string

Date and time at which the target was created

formatdate-time

<a href="#">Link to this property</a>

hostname: string

A non-unique field that refers to a target

<a href="#">Link to this property</a>

<details>

<summary>

ip: object {ipv4, ipv6 }

The IPv4/IPv6 address that identifies where to reach a target

</summary>

<details>

<summary>

ipv4: optional object {ip\_addr, virtual\_network\_id }

The target’s IPv4 address

</summary>

ip\_addr: optional string

IP address of the target

<a href="#">Link to this property</a>

virtual\_network\_id: optional string

(optional) Private virtual network identifier for the target. If omitted, the default virtual network ID will be used.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ipv6: optional object {ip\_addr, virtual\_network\_id }

The target’s IPv6 address

</summary>

ip\_addr: optional string

IP address of the target

<a href="#">Link to this property</a>

virtual\_network\_id: optional string

(optional) Private virtual network identifier for the target. If omitted, the default virtual network ID will be used.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

modified\_at: string

Date and time at which the target was modified

formatdate-time

<a href="#">Link to this property</a>

tags: optional map\[string]

Tags assigned to the target. Empty when no tags are assigned.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.infrastructure.targets%20%3E%20(model)%20target_get_response%20%3E%20(schema)>)

<details>

<summary>

TargetCreateResponse object {id, created\_at, hostname, 3 more }

</summary>

id: string

Target identifier

formatuuid

maxLength36

<a href="#">Link to this property</a>

created\_at: string

Date and time at which the target was created

formatdate-time

<a href="#">Link to this property</a>

hostname: string

A non-unique field that refers to a target

<a href="#">Link to this property</a>

<details>

<summary>

ip: object {ipv4, ipv6 }

The IPv4/IPv6 address that identifies where to reach a target

</summary>

<details>

<summary>

ipv4: optional object {ip\_addr, virtual\_network\_id }

The target’s IPv4 address

</summary>

ip\_addr: optional string

IP address of the target

<a href="#">Link to this property</a>

virtual\_network\_id: optional string

(optional) Private virtual network identifier for the target. If omitted, the default virtual network ID will be used.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ipv6: optional object {ip\_addr, virtual\_network\_id }

The target’s IPv6 address

</summary>

ip\_addr: optional string

IP address of the target

<a href="#">Link to this property</a>

virtual\_network\_id: optional string

(optional) Private virtual network identifier for the target. If omitted, the default virtual network ID will be used.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

modified\_at: string

Date and time at which the target was modified

formatdate-time

<a href="#">Link to this property</a>

tags: optional map\[string]

Tags assigned to the target. Empty when no tags are assigned.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.infrastructure.targets%20%3E%20(model)%20target_create_response%20%3E%20(schema)>)

<details>

<summary>

TargetUpdateResponse object {id, created\_at, hostname, 3 more }

</summary>

id: string

Target identifier

formatuuid

maxLength36

<a href="#">Link to this property</a>

created\_at: string

Date and time at which the target was created

formatdate-time

<a href="#">Link to this property</a>

hostname: string

A non-unique field that refers to a target

<a href="#">Link to this property</a>

<details>

<summary>

ip: object {ipv4, ipv6 }

The IPv4/IPv6 address that identifies where to reach a target

</summary>

<details>

<summary>

ipv4: optional object {ip\_addr, virtual\_network\_id }

The target’s IPv4 address

</summary>

ip\_addr: optional string

IP address of the target

<a href="#">Link to this property</a>

virtual\_network\_id: optional string

(optional) Private virtual network identifier for the target. If omitted, the default virtual network ID will be used.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ipv6: optional object {ip\_addr, virtual\_network\_id }

The target’s IPv6 address

</summary>

ip\_addr: optional string

IP address of the target

<a href="#">Link to this property</a>

virtual\_network\_id: optional string

(optional) Private virtual network identifier for the target. If omitted, the default virtual network ID will be used.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

modified\_at: string

Date and time at which the target was modified

formatdate-time

<a href="#">Link to this property</a>

tags: optional map\[string]

Tags assigned to the target. Empty when no tags are assigned.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.infrastructure.targets%20%3E%20(model)%20target_update_response%20%3E%20(schema)>)

<details>

<summary>

TargetBulkUpdateResponse object {id, created\_at, hostname, 3 more }

</summary>

id: string

Target identifier

formatuuid

maxLength36

<a href="#">Link to this property</a>

created\_at: string

Date and time at which the target was created

formatdate-time

<a href="#">Link to this property</a>

hostname: string

A non-unique field that refers to a target

<a href="#">Link to this property</a>

<details>

<summary>

ip: object {ipv4, ipv6 }

The IPv4/IPv6 address that identifies where to reach a target

</summary>

<details>

<summary>

ipv4: optional object {ip\_addr, virtual\_network\_id }

The target’s IPv4 address

</summary>

ip\_addr: optional string

IP address of the target

<a href="#">Link to this property</a>

virtual\_network\_id: optional string

(optional) Private virtual network identifier for the target. If omitted, the default virtual network ID will be used.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ipv6: optional object {ip\_addr, virtual\_network\_id }

The target’s IPv6 address

</summary>

ip\_addr: optional string

IP address of the target

<a href="#">Link to this property</a>

virtual\_network\_id: optional string

(optional) Private virtual network identifier for the target. If omitted, the default virtual network ID will be used.

formatuuid

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

modified\_at: string

Date and time at which the target was modified

formatdate-time

<a href="#">Link to this property</a>

tags: optional map\[string]

Tags assigned to the target. Empty when no tags are assigned.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.infrastructure.targets%20%3E%20(model)%20target_bulk_update_response%20%3E%20(schema)>)

#### AccessApplications

##### [List Access applications](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/applications/methods/list)

GET/{accounts\_or\_zones}/{account\_or\_zone\_id}/access/apps

##### [Get an Access application](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/applications/methods/get)

GET/{accounts\_or\_zones}/{account\_or\_zone\_id}/access/apps/{app\_id}

##### [Add an Access application](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/applications/methods/create)

POST/{accounts\_or\_zones}/{account\_or\_zone\_id}/access/apps

##### [Update an Access application](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/applications/methods/update)

PUT/{accounts\_or\_zones}/{account\_or\_zone\_id}/access/apps/{app\_id}

##### [Delete an Access application](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/applications/methods/delete)

DELETE/{accounts\_or\_zones}/{account\_or\_zone\_id}/access/apps/{app\_id}

##### [Revoke application tokens](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/applications/methods/revoke_tokens)

POST/{accounts\_or\_zones}/{account\_or\_zone\_id}/access/apps/{app\_id}/revoke\_tokens

##### ModelsExpand Collapse

AllowedHeaders = string

[Link to this property](#)%20zero_trust.access.applications%20%3E%20(model)%20allowed_headers%20%3E%20(schema)>)

AllowedIdPs = string

The identity providers selected for application.

[Link to this property](#)%20zero_trust.access.applications%20%3E%20(model)%20allowed_idps%20%3E%20(schema)>)

<details>

<summary>

AllowedMethods = "GET"or "POST"or "HEAD"or 6 more

</summary>

One of the following:

"GET"

<a href="#">Link to this property</a>

"POST"

<a href="#">Link to this property</a>

"HEAD"

<a href="#">Link to this property</a>

"PUT"

<a href="#">Link to this property</a>

"DELETE"

<a href="#">Link to this property</a>

"CONNECT"

<a href="#">Link to this property</a>

"OPTIONS"

<a href="#">Link to this property</a>

"TRACE"

<a href="#">Link to this property</a>

"PATCH"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.applications%20%3E%20(model)%20allowed_methods%20%3E%20(schema)>)

AllowedOrigins = string

[Link to this property](#)%20zero_trust.access.applications%20%3E%20(model)%20allowed_origins%20%3E%20(schema)>)

AppID = string

Identifier.

[Link to this property](#)%20zero_trust.access.applications%20%3E%20(model)%20app_id%20%3E%20(schema)>)

<details>

<summary>

Application = object {domain, type, id, 22 more } or object {id, allowed\_idps, app\_launcher\_visible, 9 more } or object {domain, type, id, 22 more } or 5 more

</summary>

One of the following:

<details>

<summary>

SelfHostedApplication object {domain, type, id, 22 more }

</summary>

domain: string

The domain and path that Access will secure.

<a href="#">Link to this property</a>

type: string

The application type.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

allow\_iframe: optional boolean

Enables loading application content in an iFrame.

<a href="#">Link to this property</a>

allowed\_idps: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20allowed_idps%20%3E%20(schema)">AllowedIdPs</a>

The identity providers your users can select when connecting to this application. Defaults to all IdPs configured in your account.

<a href="#">Link to this property</a>

app\_launcher\_visible: optional boolean

Displays the application in the App Launcher.

<a href="#">Link to this property</a>

aud: optional string

Audience tag.

maxLength64

<a href="#">Link to this property</a>

auto\_redirect\_to\_identity: optional boolean

When set to <code>true</code>, users skip the identity provider selection step during login. You must specify only one identity provider in allowed\_idps.

<a href="#">Link to this property</a>

cors\_headers: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20cors_headers%20%3E%20(schema)">CORSHeaders</a> { allow\_all\_headers, allow\_all\_methods, allow\_all\_origins, 5 more }

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

custom\_deny\_message: optional string

The custom error message shown to a user when they are denied access to the application.

<a href="#">Link to this property</a>

custom\_deny\_url: optional string

The custom URL a user is redirected to when they are denied access to the application.

<a href="#">Link to this property</a>

eager\_redirect\_cookie\_setting: optional boolean

Preemptively sets the Access session cookie on every hostname in a multi-hostname self-hosted application during the initial redirect chain, rather than setting it lazily on first visit. Defaults to true. Set to false to disable the eager redirect cookie behavior.

<a href="#">Link to this property</a>

enable\_binding\_cookie: optional boolean

Enables the binding cookie, which increases security against compromised authorization tokens and CSRF attacks.

<a href="#">Link to this property</a>

http\_only\_cookie\_attribute: optional boolean

Enables the HttpOnly cookie attribute, which increases security against XSS attacks.

<a href="#">Link to this property</a>

logo\_url: optional string

The image URL for the logo shown in the App Launcher dashboard.

<a href="#">Link to this property</a>

name: optional string

The name of the application.

<a href="#">Link to this property</a>

options\_preflight\_bypass: optional boolean

Allows options preflight requests to bypass Access authentication and go directly to the origin. Cannot turn on if cors\_headers is set.

<a href="#">Link to this property</a>

same\_site\_cookie\_attribute: optional string

Sets the SameSite cookie setting, which provides increased security against CSRF attacks.

<a href="#">Link to this property</a>

<details>

<summary>

scim\_config: optional object {idp\_uid, remote\_uri, authentication, 3 more }

Configuration for provisioning to this application via SCIM. This is currently in closed beta.

</summary>

idp\_uid: string

The UID of the IdP to use as the source for SCIM resources to provision to this application.

<a href="#">Link to this property</a>

remote\_uri: string

The base URI for the application’s SCIM-compatible API.

<a href="#">Link to this property</a>

<details>

<summary>

authentication: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_http_basic%20%3E%20(schema)">SCIMConfigAuthenticationHTTPBasic</a> { password, scheme, user } or object {token, scheme } or <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_oauth2%20%3E%20(schema)">SCIMConfigAuthenticationOauth2</a> { authorization\_url, client\_id, client\_secret, 3 more } or 2 more

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

One of the following:

<details>

<summary>

SCIMConfigAuthenticationHTTPBasic object {password, scheme, user }

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

password: string

Password used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "httpbasic"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

user: string

User name used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationOAuthBearerToken2 object {token, scheme }

Attributes for configuring OAuth Bearer Token authentication scheme for SCIM provisioning to an application.

</summary>

token: string

Token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "oauthbearertoken"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SCIMConfigAuthenticationOauth2 object {authorization\_url, client\_id, client\_secret, 3 more }

Attributes for configuring OAuth 2 authentication scheme for SCIM provisioning to an application.

</summary>

authorization\_url: string

URL used to generate the auth code used during token generation.

<a href="#">Link to this property</a>

client\_id: string

Client ID used to authenticate when generating a token for authenticating with the remote SCIM service.

<a href="#">Link to this property</a>

client\_secret: string

Secret used to authenticate when generating a token for authenticating with the remove SCIM service.

<a href="#">Link to this property</a>

scheme: "oauth2"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

token\_url: string

URL used to generate the token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scopes: optional array of string

The authorization scopes to request when generating the token used to authenticate with the remove SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationAccessServiceToken object {client\_id, client\_secret, scheme }

Attributes for configuring Access Service Token authentication scheme for SCIM provisioning to an application.

</summary>

client\_id: string

Client ID of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

client\_secret: string

Client secret of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

scheme: "access\_service\_token"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigMultiAuthentication2 = array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_http_basic%20%3E%20(schema)">SCIMConfigAuthenticationHTTPBasic</a> { password, scheme, user } or object {token, scheme } or <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_oauth2%20%3E%20(schema)">SCIMConfigAuthenticationOauth2</a> { authorization\_url, client\_id, client\_secret, 3 more } or object {client\_id, client\_secret, scheme }

Multiple authentication schemes

</summary>

One of the following:

<details>

<summary>

SCIMConfigAuthenticationHTTPBasic object {password, scheme, user }

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

password: string

Password used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "httpbasic"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

user: string

User name used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationOAuthBearerToken2 object {token, scheme }

Attributes for configuring OAuth Bearer Token authentication scheme for SCIM provisioning to an application.

</summary>

token: string

Token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "oauthbearertoken"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SCIMConfigAuthenticationOauth2 object {authorization\_url, client\_id, client\_secret, 3 more }

Attributes for configuring OAuth 2 authentication scheme for SCIM provisioning to an application.

</summary>

authorization\_url: string

URL used to generate the auth code used during token generation.

<a href="#">Link to this property</a>

client\_id: string

Client ID used to authenticate when generating a token for authenticating with the remote SCIM service.

<a href="#">Link to this property</a>

client\_secret: string

Secret used to authenticate when generating a token for authenticating with the remove SCIM service.

<a href="#">Link to this property</a>

scheme: "oauth2"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

token\_url: string

URL used to generate the token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scopes: optional array of string

The authorization scopes to request when generating the token used to authenticate with the remove SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationAccessServiceToken object {client\_id, client\_secret, scheme }

Attributes for configuring Access Service Token authentication scheme for SCIM provisioning to an application.

</summary>

client\_id: string

Client ID of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

client\_secret: string

Client secret of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

scheme: "access\_service\_token"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

deactivate\_on\_delete: optional boolean

If false, we propagate DELETE requests to the target application for SCIM resources. If true, we only set <code>active</code> to false on the SCIM resource. This is useful because some targets do not support DELETE operations.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether SCIM provisioning is turned on for this application.

<a href="#">Link to this property</a>

<details>

<summary>

mappings: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_mapping%20%3E%20(schema)">SCIMConfigMapping</a> { schema, enabled, filter, 3 more }

A list of mappings to apply to SCIM resources before provisioning them in this application. These can transform or filter the resources to be provisioned.

</summary>

schema: string

Which SCIM resource type this mapping applies to.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether or not this mapping is enabled.

<a href="#">Link to this property</a>

filter: optional string

A <a href="https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2.2">SCIM filter expression</a> that matches resources that should be provisioned to this application.

<a href="#">Link to this property</a>

<details>

<summary>

operations: optional object {create, delete, update }

Whether or not this mapping applies to creates, updates, or deletes.

</summary>

create: optional boolean

Whether or not this mapping applies to create (POST) operations.

<a href="#">Link to this property</a>

delete: optional boolean

Whether or not this mapping applies to DELETE operations.

<a href="#">Link to this property</a>

update: optional boolean

Whether or not this mapping applies to update (PATCH/PUT) operations.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

strictness: optional "strict"or "passthrough"

The level of adherence to outbound resource schemas when provisioning to this mapping. ‘Strict’ removes unknown values, while ‘passthrough’ passes unknown values to the target.

</summary>

One of the following:

"strict"

<a href="#">Link to this property</a>

"passthrough"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

transform\_jsonata: optional string

A <a href="https://jsonata.org/">JSONata</a> expression that transforms the resource before provisioning it in the application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

service\_auth\_401\_redirect: optional boolean

Returns a 401 status code when the request is blocked by a Service Auth policy.

<a href="#">Link to this property</a>

session\_duration: optional string

The amount of time that tokens issued for this application will be valid. Must be in the format <code>300ms</code> or <code>2h45m</code>. Valid time units are: ns, us (or µs), ms, s, m, h.

<a href="#">Link to this property</a>

skip\_interstitial: optional boolean

Enables automatic authentication through cloudflared.

<a href="#">Link to this property</a>

updated\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

use\_clientless\_isolation\_app\_launcher\_url: optional boolean

Determines if users can access this application via a clientless browser isolation URL. This allows users to access private domains without connecting to Gateway. The option requires Clientless Browser Isolation to be set up with policies that allow users of this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SaaSApplication object {id, allowed\_idps, app\_launcher\_visible, 9 more }

</summary>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

allowed\_idps: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20allowed_idps%20%3E%20(schema)">AllowedIdPs</a>

The identity providers your users can select when connecting to this application. Defaults to all IdPs configured in your account.

<a href="#">Link to this property</a>

app\_launcher\_visible: optional boolean

Displays the application in the App Launcher.

<a href="#">Link to this property</a>

aud: optional string

Audience tag.

maxLength64

<a href="#">Link to this property</a>

auto\_redirect\_to\_identity: optional boolean

When set to <code>true</code>, users skip the identity provider selection step during login. You must specify only one identity provider in allowed\_idps.

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

logo\_url: optional string

The image URL for the logo shown in the App Launcher dashboard.

<a href="#">Link to this property</a>

name: optional string

The name of the application.

<a href="#">Link to this property</a>

<details>

<summary>

saas\_app: optional object {auth\_type, consumer\_service\_url, created\_at, 8 more } or object {access\_token\_lifetime, allow\_pkce\_without\_client\_secret, app\_launcher\_url, 13 more }

</summary>

One of the following:

<details>

<summary>

AccessSAMLSaaSApp2 object {auth\_type, consumer\_service\_url, created\_at, 8 more }

</summary>

<details>

<summary>

auth\_type: optional "saml"or "oidc"

Optional identifier indicating the authentication protocol used for the saas app. Required for OIDC. Default if unset is “saml”

</summary>

One of the following:

"saml"

<a href="#">Link to this property</a>

"oidc"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

consumer\_service\_url: optional string

The service provider’s endpoint that is responsible for receiving and parsing a SAML assertion.

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

custom\_attributes: optional array of object {friendly\_name, name, name\_format, 2 more }

</summary>

friendly\_name: optional string

The SAML FriendlyName of the attribute.

<a href="#">Link to this property</a>

name: optional string

The name of the attribute.

<a href="#">Link to this property</a>

<details>

<summary>

name\_format: optional "urn:oasis:names:tc:SAML:2.0:attrname-format:unspecified"or "urn:oasis:names:tc:SAML:2.0:attrname-format:basic"or "urn:oasis:names:tc:SAML:2.0:attrname-format:uri"

A globally unique name for an identity or service provider.

</summary>

One of the following:

"urn:oasis:names:tc:SAML:2.0:attrname-format:unspecified"

<a href="#">Link to this property</a>

"urn:oasis:names:tc:SAML:2.0:attrname-format:basic"

<a href="#">Link to this property</a>

"urn:oasis:names:tc:SAML:2.0:attrname-format:uri"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

required: optional boolean

If the attribute is required when building a SAML assertion.

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {name, name\_by\_idp }

</summary>

name: optional string

The name of the IdP attribute.

<a href="#">Link to this property</a>

name\_by\_idp: optional map\[string]

A mapping from IdP ID to attribute name.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

idp\_entity\_id: optional string

The unique identifier for your SaaS application.

<a href="#">Link to this property</a>

name\_id\_format: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20saas_app_name_id_format%20%3E%20(schema)">SaaSAppNameIDFormat</a>

The format of the name identifier sent to the SaaS application.

<a href="#">Link to this property</a>

name\_id\_transform\_jsonata: optional string

A <a href="https://jsonata.org/">JSONata</a> expression that transforms an application’s user identities into a NameID value for its SAML assertion. This expression should evaluate to a singular string. The output of this expression can override the <code>name_id_format</code> setting.

<a href="#">Link to this property</a>

public\_key: optional string

The Access public certificate that will be used to verify your identity.

<a href="#">Link to this property</a>

sp\_entity\_id: optional string

A globally unique name for an identity or service provider.

<a href="#">Link to this property</a>

sso\_endpoint: optional string

The endpoint where your SaaS application will send login requests.

<a href="#">Link to this property</a>

updated\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessOIDCSaaSApp2 object {access\_token\_lifetime, allow\_pkce\_without\_client\_secret, app\_launcher\_url, 13 more }

</summary>

access\_token\_lifetime: optional string

The lifetime of the OIDC Access Token after creation. Valid units are m,h. Must be greater than or equal to 1m and less than or equal to 24h.

<a href="#">Link to this property</a>

allow\_pkce\_without\_client\_secret: optional boolean

If client secret should be required on the token endpoint when authorization\_code\_with\_pkce grant is used.

<a href="#">Link to this property</a>

app\_launcher\_url: optional string

The URL where this applications tile redirects users

<a href="#">Link to this property</a>

<details>

<summary>

auth\_type: optional "saml"or "oidc"

Identifier of the authentication protocol used for the saas app. Required for OIDC.

</summary>

One of the following:

"saml"

<a href="#">Link to this property</a>

"oidc"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

client\_id: optional string

The application client id

<a href="#">Link to this property</a>

client\_secret: optional string

The application client secret, only returned on POST request.

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

custom\_claims: optional array of object {name, required, scope, source }

</summary>

name: optional string

The name of the claim.

<a href="#">Link to this property</a>

required: optional boolean

If the claim is required when building an OIDC token.

<a href="#">Link to this property</a>

<details>

<summary>

scope: optional "groups"or "profile"or "email"or "openid"

The scope of the claim.

</summary>

One of the following:

"groups"

<a href="#">Link to this property</a>

"profile"

<a href="#">Link to this property</a>

"email"

<a href="#">Link to this property</a>

"openid"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {name, name\_by\_idp }

</summary>

name: optional string

The name of the IdP claim.

<a href="#">Link to this property</a>

<details>

<summary>

name\_by\_idp: optional array of object {idp\_id, source\_name }

A mapping from IdP ID to attribute name.

</summary>

idp\_id: optional string

The UID of the IdP.

<a href="#">Link to this property</a>

source\_name: optional string

The name of the IdP provided attribute.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

grant\_types: optional array of "authorization\_code"or "authorization\_code\_with\_pkce"or "refresh\_tokens"or 2 more

The OIDC flows supported by this application

</summary>

One of the following:

"authorization\_code"

<a href="#">Link to this property</a>

"authorization\_code\_with\_pkce"

<a href="#">Link to this property</a>

"refresh\_tokens"

<a href="#">Link to this property</a>

"hybrid"

<a href="#">Link to this property</a>

"implicit"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

group\_filter\_regex: optional string

A regex to filter Cloudflare groups returned in ID token and userinfo endpoint.

<a href="#">Link to this property</a>

<details>

<summary>

hybrid\_and\_implicit\_options: optional object {return\_access\_token\_from\_authorization\_endpoint, return\_id\_token\_from\_authorization\_endpoint }

</summary>

return\_access\_token\_from\_authorization\_endpoint: optional boolean

If an Access Token should be returned from the OIDC Authorization endpoint

<a href="#">Link to this property</a>

return\_id\_token\_from\_authorization\_endpoint: optional boolean

If an ID Token should be returned from the OIDC Authorization endpoint

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

public\_key: optional string

The Access public certificate that will be used to verify your identity.

<a href="#">Link to this property</a>

redirect\_uris: optional array of string

The permitted URL’s for Cloudflare to return Authorization codes and Access/ID tokens

<a href="#">Link to this property</a>

<details>

<summary>

refresh\_token\_options: optional object {lifetime }

</summary>

lifetime: optional string

How long a refresh token will be valid for after creation. Valid units are m,h,d. Must be longer than 1m.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

scopes: optional array of "openid"or "groups"or "email"or "profile"

Define the user information shared with access, “offline\_access” scope will be automatically enabled if refresh tokens are enabled

</summary>

One of the following:

"openid"

<a href="#">Link to this property</a>

"groups"

<a href="#">Link to this property</a>

"email"

<a href="#">Link to this property</a>

"profile"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

scim\_config: optional object {idp\_uid, remote\_uri, authentication, 3 more }

Configuration for provisioning to this application via SCIM. This is currently in closed beta.

</summary>

idp\_uid: string

The UID of the IdP to use as the source for SCIM resources to provision to this application.

<a href="#">Link to this property</a>

remote\_uri: string

The base URI for the application’s SCIM-compatible API.

<a href="#">Link to this property</a>

<details>

<summary>

authentication: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_http_basic%20%3E%20(schema)">SCIMConfigAuthenticationHTTPBasic</a> { password, scheme, user } or object {token, scheme } or <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_oauth2%20%3E%20(schema)">SCIMConfigAuthenticationOauth2</a> { authorization\_url, client\_id, client\_secret, 3 more } or 2 more

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

One of the following:

<details>

<summary>

SCIMConfigAuthenticationHTTPBasic object {password, scheme, user }

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

password: string

Password used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "httpbasic"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

user: string

User name used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationOAuthBearerToken2 object {token, scheme }

Attributes for configuring OAuth Bearer Token authentication scheme for SCIM provisioning to an application.

</summary>

token: string

Token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "oauthbearertoken"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SCIMConfigAuthenticationOauth2 object {authorization\_url, client\_id, client\_secret, 3 more }

Attributes for configuring OAuth 2 authentication scheme for SCIM provisioning to an application.

</summary>

authorization\_url: string

URL used to generate the auth code used during token generation.

<a href="#">Link to this property</a>

client\_id: string

Client ID used to authenticate when generating a token for authenticating with the remote SCIM service.

<a href="#">Link to this property</a>

client\_secret: string

Secret used to authenticate when generating a token for authenticating with the remove SCIM service.

<a href="#">Link to this property</a>

scheme: "oauth2"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

token\_url: string

URL used to generate the token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scopes: optional array of string

The authorization scopes to request when generating the token used to authenticate with the remove SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationAccessServiceToken object {client\_id, client\_secret, scheme }

Attributes for configuring Access Service Token authentication scheme for SCIM provisioning to an application.

</summary>

client\_id: string

Client ID of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

client\_secret: string

Client secret of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

scheme: "access\_service\_token"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigMultiAuthentication2 = array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_http_basic%20%3E%20(schema)">SCIMConfigAuthenticationHTTPBasic</a> { password, scheme, user } or object {token, scheme } or <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_oauth2%20%3E%20(schema)">SCIMConfigAuthenticationOauth2</a> { authorization\_url, client\_id, client\_secret, 3 more } or object {client\_id, client\_secret, scheme }

Multiple authentication schemes

</summary>

One of the following:

<details>

<summary>

SCIMConfigAuthenticationHTTPBasic object {password, scheme, user }

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

password: string

Password used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "httpbasic"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

user: string

User name used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationOAuthBearerToken2 object {token, scheme }

Attributes for configuring OAuth Bearer Token authentication scheme for SCIM provisioning to an application.

</summary>

token: string

Token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "oauthbearertoken"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SCIMConfigAuthenticationOauth2 object {authorization\_url, client\_id, client\_secret, 3 more }

Attributes for configuring OAuth 2 authentication scheme for SCIM provisioning to an application.

</summary>

authorization\_url: string

URL used to generate the auth code used during token generation.

<a href="#">Link to this property</a>

client\_id: string

Client ID used to authenticate when generating a token for authenticating with the remote SCIM service.

<a href="#">Link to this property</a>

client\_secret: string

Secret used to authenticate when generating a token for authenticating with the remove SCIM service.

<a href="#">Link to this property</a>

scheme: "oauth2"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

token\_url: string

URL used to generate the token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scopes: optional array of string

The authorization scopes to request when generating the token used to authenticate with the remove SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationAccessServiceToken object {client\_id, client\_secret, scheme }

Attributes for configuring Access Service Token authentication scheme for SCIM provisioning to an application.

</summary>

client\_id: string

Client ID of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

client\_secret: string

Client secret of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

scheme: "access\_service\_token"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

deactivate\_on\_delete: optional boolean

If false, we propagate DELETE requests to the target application for SCIM resources. If true, we only set <code>active</code> to false on the SCIM resource. This is useful because some targets do not support DELETE operations.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether SCIM provisioning is turned on for this application.

<a href="#">Link to this property</a>

<details>

<summary>

mappings: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_mapping%20%3E%20(schema)">SCIMConfigMapping</a> { schema, enabled, filter, 3 more }

A list of mappings to apply to SCIM resources before provisioning them in this application. These can transform or filter the resources to be provisioned.

</summary>

schema: string

Which SCIM resource type this mapping applies to.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether or not this mapping is enabled.

<a href="#">Link to this property</a>

filter: optional string

A <a href="https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2.2">SCIM filter expression</a> that matches resources that should be provisioned to this application.

<a href="#">Link to this property</a>

<details>

<summary>

operations: optional object {create, delete, update }

Whether or not this mapping applies to creates, updates, or deletes.

</summary>

create: optional boolean

Whether or not this mapping applies to create (POST) operations.

<a href="#">Link to this property</a>

delete: optional boolean

Whether or not this mapping applies to DELETE operations.

<a href="#">Link to this property</a>

update: optional boolean

Whether or not this mapping applies to update (PATCH/PUT) operations.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

strictness: optional "strict"or "passthrough"

The level of adherence to outbound resource schemas when provisioning to this mapping. ‘Strict’ removes unknown values, while ‘passthrough’ passes unknown values to the target.

</summary>

One of the following:

"strict"

<a href="#">Link to this property</a>

"passthrough"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

transform\_jsonata: optional string

A <a href="https://jsonata.org/">JSONata</a> expression that transforms the resource before provisioning it in the application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

type: optional string

The application type.

<a href="#">Link to this property</a>

updated\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

BrowserSSHApplication object {domain, type, id, 22 more }

</summary>

domain: string

The domain and path that Access will secure.

<a href="#">Link to this property</a>

type: string

The application type.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

allow\_iframe: optional boolean

Enables loading application content in an iFrame.

<a href="#">Link to this property</a>

allowed\_idps: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20allowed_idps%20%3E%20(schema)">AllowedIdPs</a>

The identity providers your users can select when connecting to this application. Defaults to all IdPs configured in your account.

<a href="#">Link to this property</a>

app\_launcher\_visible: optional boolean

Displays the application in the App Launcher.

<a href="#">Link to this property</a>

aud: optional string

Audience tag.

maxLength64

<a href="#">Link to this property</a>

auto\_redirect\_to\_identity: optional boolean

When set to <code>true</code>, users skip the identity provider selection step during login. You must specify only one identity provider in allowed\_idps.

<a href="#">Link to this property</a>

cors\_headers: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20cors_headers%20%3E%20(schema)">CORSHeaders</a> { allow\_all\_headers, allow\_all\_methods, allow\_all\_origins, 5 more }

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

custom\_deny\_message: optional string

The custom error message shown to a user when they are denied access to the application.

<a href="#">Link to this property</a>

custom\_deny\_url: optional string

The custom URL a user is redirected to when they are denied access to the application.

<a href="#">Link to this property</a>

eager\_redirect\_cookie\_setting: optional boolean

Preemptively sets the Access session cookie on every hostname in a multi-hostname self-hosted application during the initial redirect chain, rather than setting it lazily on first visit. Defaults to true. Set to false to disable the eager redirect cookie behavior.

<a href="#">Link to this property</a>

enable\_binding\_cookie: optional boolean

Enables the binding cookie, which increases security against compromised authorization tokens and CSRF attacks.

<a href="#">Link to this property</a>

http\_only\_cookie\_attribute: optional boolean

Enables the HttpOnly cookie attribute, which increases security against XSS attacks.

<a href="#">Link to this property</a>

logo\_url: optional string

The image URL for the logo shown in the App Launcher dashboard.

<a href="#">Link to this property</a>

name: optional string

The name of the application.

<a href="#">Link to this property</a>

options\_preflight\_bypass: optional boolean

Allows options preflight requests to bypass Access authentication and go directly to the origin. Cannot turn on if cors\_headers is set.

<a href="#">Link to this property</a>

same\_site\_cookie\_attribute: optional string

Sets the SameSite cookie setting, which provides increased security against CSRF attacks.

<a href="#">Link to this property</a>

<details>

<summary>

scim\_config: optional object {idp\_uid, remote\_uri, authentication, 3 more }

Configuration for provisioning to this application via SCIM. This is currently in closed beta.

</summary>

idp\_uid: string

The UID of the IdP to use as the source for SCIM resources to provision to this application.

<a href="#">Link to this property</a>

remote\_uri: string

The base URI for the application’s SCIM-compatible API.

<a href="#">Link to this property</a>

<details>

<summary>

authentication: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_http_basic%20%3E%20(schema)">SCIMConfigAuthenticationHTTPBasic</a> { password, scheme, user } or object {token, scheme } or <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_oauth2%20%3E%20(schema)">SCIMConfigAuthenticationOauth2</a> { authorization\_url, client\_id, client\_secret, 3 more } or 2 more

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

One of the following:

<details>

<summary>

SCIMConfigAuthenticationHTTPBasic object {password, scheme, user }

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

password: string

Password used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "httpbasic"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

user: string

User name used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationOAuthBearerToken2 object {token, scheme }

Attributes for configuring OAuth Bearer Token authentication scheme for SCIM provisioning to an application.

</summary>

token: string

Token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "oauthbearertoken"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SCIMConfigAuthenticationOauth2 object {authorization\_url, client\_id, client\_secret, 3 more }

Attributes for configuring OAuth 2 authentication scheme for SCIM provisioning to an application.

</summary>

authorization\_url: string

URL used to generate the auth code used during token generation.

<a href="#">Link to this property</a>

client\_id: string

Client ID used to authenticate when generating a token for authenticating with the remote SCIM service.

<a href="#">Link to this property</a>

client\_secret: string

Secret used to authenticate when generating a token for authenticating with the remove SCIM service.

<a href="#">Link to this property</a>

scheme: "oauth2"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

token\_url: string

URL used to generate the token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scopes: optional array of string

The authorization scopes to request when generating the token used to authenticate with the remove SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationAccessServiceToken object {client\_id, client\_secret, scheme }

Attributes for configuring Access Service Token authentication scheme for SCIM provisioning to an application.

</summary>

client\_id: string

Client ID of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

client\_secret: string

Client secret of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

scheme: "access\_service\_token"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigMultiAuthentication2 = array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_http_basic%20%3E%20(schema)">SCIMConfigAuthenticationHTTPBasic</a> { password, scheme, user } or object {token, scheme } or <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_oauth2%20%3E%20(schema)">SCIMConfigAuthenticationOauth2</a> { authorization\_url, client\_id, client\_secret, 3 more } or object {client\_id, client\_secret, scheme }

Multiple authentication schemes

</summary>

One of the following:

<details>

<summary>

SCIMConfigAuthenticationHTTPBasic object {password, scheme, user }

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

password: string

Password used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "httpbasic"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

user: string

User name used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationOAuthBearerToken2 object {token, scheme }

Attributes for configuring OAuth Bearer Token authentication scheme for SCIM provisioning to an application.

</summary>

token: string

Token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "oauthbearertoken"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SCIMConfigAuthenticationOauth2 object {authorization\_url, client\_id, client\_secret, 3 more }

Attributes for configuring OAuth 2 authentication scheme for SCIM provisioning to an application.

</summary>

authorization\_url: string

URL used to generate the auth code used during token generation.

<a href="#">Link to this property</a>

client\_id: string

Client ID used to authenticate when generating a token for authenticating with the remote SCIM service.

<a href="#">Link to this property</a>

client\_secret: string

Secret used to authenticate when generating a token for authenticating with the remove SCIM service.

<a href="#">Link to this property</a>

scheme: "oauth2"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

token\_url: string

URL used to generate the token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scopes: optional array of string

The authorization scopes to request when generating the token used to authenticate with the remove SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationAccessServiceToken object {client\_id, client\_secret, scheme }

Attributes for configuring Access Service Token authentication scheme for SCIM provisioning to an application.

</summary>

client\_id: string

Client ID of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

client\_secret: string

Client secret of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

scheme: "access\_service\_token"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

deactivate\_on\_delete: optional boolean

If false, we propagate DELETE requests to the target application for SCIM resources. If true, we only set <code>active</code> to false on the SCIM resource. This is useful because some targets do not support DELETE operations.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether SCIM provisioning is turned on for this application.

<a href="#">Link to this property</a>

<details>

<summary>

mappings: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_mapping%20%3E%20(schema)">SCIMConfigMapping</a> { schema, enabled, filter, 3 more }

A list of mappings to apply to SCIM resources before provisioning them in this application. These can transform or filter the resources to be provisioned.

</summary>

schema: string

Which SCIM resource type this mapping applies to.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether or not this mapping is enabled.

<a href="#">Link to this property</a>

filter: optional string

A <a href="https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2.2">SCIM filter expression</a> that matches resources that should be provisioned to this application.

<a href="#">Link to this property</a>

<details>

<summary>

operations: optional object {create, delete, update }

Whether or not this mapping applies to creates, updates, or deletes.

</summary>

create: optional boolean

Whether or not this mapping applies to create (POST) operations.

<a href="#">Link to this property</a>

delete: optional boolean

Whether or not this mapping applies to DELETE operations.

<a href="#">Link to this property</a>

update: optional boolean

Whether or not this mapping applies to update (PATCH/PUT) operations.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

strictness: optional "strict"or "passthrough"

The level of adherence to outbound resource schemas when provisioning to this mapping. ‘Strict’ removes unknown values, while ‘passthrough’ passes unknown values to the target.

</summary>

One of the following:

"strict"

<a href="#">Link to this property</a>

"passthrough"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

transform\_jsonata: optional string

A <a href="https://jsonata.org/">JSONata</a> expression that transforms the resource before provisioning it in the application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

service\_auth\_401\_redirect: optional boolean

Returns a 401 status code when the request is blocked by a Service Auth policy.

<a href="#">Link to this property</a>

session\_duration: optional string

The amount of time that tokens issued for this application will be valid. Must be in the format <code>300ms</code> or <code>2h45m</code>. Valid time units are: ns, us (or µs), ms, s, m, h.

<a href="#">Link to this property</a>

skip\_interstitial: optional boolean

Enables automatic authentication through cloudflared.

<a href="#">Link to this property</a>

updated\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

use\_clientless\_isolation\_app\_launcher\_url: optional boolean

Determines if users can access this application via a clientless browser isolation URL. This allows users to access private domains without connecting to Gateway. The option requires Clientless Browser Isolation to be set up with policies that allow users of this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

BrowserVNCApplication object {domain, type, id, 22 more }

</summary>

domain: string

The domain and path that Access will secure.

<a href="#">Link to this property</a>

type: string

The application type.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

allow\_iframe: optional boolean

Enables loading application content in an iFrame.

<a href="#">Link to this property</a>

allowed\_idps: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20allowed_idps%20%3E%20(schema)">AllowedIdPs</a>

The identity providers your users can select when connecting to this application. Defaults to all IdPs configured in your account.

<a href="#">Link to this property</a>

app\_launcher\_visible: optional boolean

Displays the application in the App Launcher.

<a href="#">Link to this property</a>

aud: optional string

Audience tag.

maxLength64

<a href="#">Link to this property</a>

auto\_redirect\_to\_identity: optional boolean

When set to <code>true</code>, users skip the identity provider selection step during login. You must specify only one identity provider in allowed\_idps.

<a href="#">Link to this property</a>

cors\_headers: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20cors_headers%20%3E%20(schema)">CORSHeaders</a> { allow\_all\_headers, allow\_all\_methods, allow\_all\_origins, 5 more }

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

custom\_deny\_message: optional string

The custom error message shown to a user when they are denied access to the application.

<a href="#">Link to this property</a>

custom\_deny\_url: optional string

The custom URL a user is redirected to when they are denied access to the application.

<a href="#">Link to this property</a>

eager\_redirect\_cookie\_setting: optional boolean

Preemptively sets the Access session cookie on every hostname in a multi-hostname self-hosted application during the initial redirect chain, rather than setting it lazily on first visit. Defaults to true. Set to false to disable the eager redirect cookie behavior.

<a href="#">Link to this property</a>

enable\_binding\_cookie: optional boolean

Enables the binding cookie, which increases security against compromised authorization tokens and CSRF attacks.

<a href="#">Link to this property</a>

http\_only\_cookie\_attribute: optional boolean

Enables the HttpOnly cookie attribute, which increases security against XSS attacks.

<a href="#">Link to this property</a>

logo\_url: optional string

The image URL for the logo shown in the App Launcher dashboard.

<a href="#">Link to this property</a>

name: optional string

The name of the application.

<a href="#">Link to this property</a>

options\_preflight\_bypass: optional boolean

Allows options preflight requests to bypass Access authentication and go directly to the origin. Cannot turn on if cors\_headers is set.

<a href="#">Link to this property</a>

same\_site\_cookie\_attribute: optional string

Sets the SameSite cookie setting, which provides increased security against CSRF attacks.

<a href="#">Link to this property</a>

<details>

<summary>

scim\_config: optional object {idp\_uid, remote\_uri, authentication, 3 more }

Configuration for provisioning to this application via SCIM. This is currently in closed beta.

</summary>

idp\_uid: string

The UID of the IdP to use as the source for SCIM resources to provision to this application.

<a href="#">Link to this property</a>

remote\_uri: string

The base URI for the application’s SCIM-compatible API.

<a href="#">Link to this property</a>

<details>

<summary>

authentication: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_http_basic%20%3E%20(schema)">SCIMConfigAuthenticationHTTPBasic</a> { password, scheme, user } or object {token, scheme } or <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_oauth2%20%3E%20(schema)">SCIMConfigAuthenticationOauth2</a> { authorization\_url, client\_id, client\_secret, 3 more } or 2 more

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

One of the following:

<details>

<summary>

SCIMConfigAuthenticationHTTPBasic object {password, scheme, user }

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

password: string

Password used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "httpbasic"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

user: string

User name used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationOAuthBearerToken2 object {token, scheme }

Attributes for configuring OAuth Bearer Token authentication scheme for SCIM provisioning to an application.

</summary>

token: string

Token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "oauthbearertoken"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SCIMConfigAuthenticationOauth2 object {authorization\_url, client\_id, client\_secret, 3 more }

Attributes for configuring OAuth 2 authentication scheme for SCIM provisioning to an application.

</summary>

authorization\_url: string

URL used to generate the auth code used during token generation.

<a href="#">Link to this property</a>

client\_id: string

Client ID used to authenticate when generating a token for authenticating with the remote SCIM service.

<a href="#">Link to this property</a>

client\_secret: string

Secret used to authenticate when generating a token for authenticating with the remove SCIM service.

<a href="#">Link to this property</a>

scheme: "oauth2"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

token\_url: string

URL used to generate the token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scopes: optional array of string

The authorization scopes to request when generating the token used to authenticate with the remove SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationAccessServiceToken object {client\_id, client\_secret, scheme }

Attributes for configuring Access Service Token authentication scheme for SCIM provisioning to an application.

</summary>

client\_id: string

Client ID of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

client\_secret: string

Client secret of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

scheme: "access\_service\_token"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigMultiAuthentication2 = array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_http_basic%20%3E%20(schema)">SCIMConfigAuthenticationHTTPBasic</a> { password, scheme, user } or object {token, scheme } or <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_oauth2%20%3E%20(schema)">SCIMConfigAuthenticationOauth2</a> { authorization\_url, client\_id, client\_secret, 3 more } or object {client\_id, client\_secret, scheme }

Multiple authentication schemes

</summary>

One of the following:

<details>

<summary>

SCIMConfigAuthenticationHTTPBasic object {password, scheme, user }

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

password: string

Password used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "httpbasic"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

user: string

User name used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationOAuthBearerToken2 object {token, scheme }

Attributes for configuring OAuth Bearer Token authentication scheme for SCIM provisioning to an application.

</summary>

token: string

Token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "oauthbearertoken"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SCIMConfigAuthenticationOauth2 object {authorization\_url, client\_id, client\_secret, 3 more }

Attributes for configuring OAuth 2 authentication scheme for SCIM provisioning to an application.

</summary>

authorization\_url: string

URL used to generate the auth code used during token generation.

<a href="#">Link to this property</a>

client\_id: string

Client ID used to authenticate when generating a token for authenticating with the remote SCIM service.

<a href="#">Link to this property</a>

client\_secret: string

Secret used to authenticate when generating a token for authenticating with the remove SCIM service.

<a href="#">Link to this property</a>

scheme: "oauth2"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

token\_url: string

URL used to generate the token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scopes: optional array of string

The authorization scopes to request when generating the token used to authenticate with the remove SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationAccessServiceToken object {client\_id, client\_secret, scheme }

Attributes for configuring Access Service Token authentication scheme for SCIM provisioning to an application.

</summary>

client\_id: string

Client ID of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

client\_secret: string

Client secret of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

scheme: "access\_service\_token"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

deactivate\_on\_delete: optional boolean

If false, we propagate DELETE requests to the target application for SCIM resources. If true, we only set <code>active</code> to false on the SCIM resource. This is useful because some targets do not support DELETE operations.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether SCIM provisioning is turned on for this application.

<a href="#">Link to this property</a>

<details>

<summary>

mappings: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_mapping%20%3E%20(schema)">SCIMConfigMapping</a> { schema, enabled, filter, 3 more }

A list of mappings to apply to SCIM resources before provisioning them in this application. These can transform or filter the resources to be provisioned.

</summary>

schema: string

Which SCIM resource type this mapping applies to.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether or not this mapping is enabled.

<a href="#">Link to this property</a>

filter: optional string

A <a href="https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2.2">SCIM filter expression</a> that matches resources that should be provisioned to this application.

<a href="#">Link to this property</a>

<details>

<summary>

operations: optional object {create, delete, update }

Whether or not this mapping applies to creates, updates, or deletes.

</summary>

create: optional boolean

Whether or not this mapping applies to create (POST) operations.

<a href="#">Link to this property</a>

delete: optional boolean

Whether or not this mapping applies to DELETE operations.

<a href="#">Link to this property</a>

update: optional boolean

Whether or not this mapping applies to update (PATCH/PUT) operations.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

strictness: optional "strict"or "passthrough"

The level of adherence to outbound resource schemas when provisioning to this mapping. ‘Strict’ removes unknown values, while ‘passthrough’ passes unknown values to the target.

</summary>

One of the following:

"strict"

<a href="#">Link to this property</a>

"passthrough"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

transform\_jsonata: optional string

A <a href="https://jsonata.org/">JSONata</a> expression that transforms the resource before provisioning it in the application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

service\_auth\_401\_redirect: optional boolean

Returns a 401 status code when the request is blocked by a Service Auth policy.

<a href="#">Link to this property</a>

session\_duration: optional string

The amount of time that tokens issued for this application will be valid. Must be in the format <code>300ms</code> or <code>2h45m</code>. Valid time units are: ns, us (or µs), ms, s, m, h.

<a href="#">Link to this property</a>

skip\_interstitial: optional boolean

Enables automatic authentication through cloudflared.

<a href="#">Link to this property</a>

updated\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

use\_clientless\_isolation\_app\_launcher\_url: optional boolean

Determines if users can access this application via a clientless browser isolation URL. This allows users to access private domains without connecting to Gateway. The option requires Clientless Browser Isolation to be set up with policies that allow users of this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AppLauncherApplication object {type, id, allowed\_idps, 8 more }

</summary>

<details>

<summary>

type: "self\_hosted"or "saas"or "ssh"or 6 more

The application type.

</summary>

One of the following:

"self\_hosted"

<a href="#">Link to this property</a>

"saas"

<a href="#">Link to this property</a>

"ssh"

<a href="#">Link to this property</a>

"vnc"

<a href="#">Link to this property</a>

"app\_launcher"

<a href="#">Link to this property</a>

"warp"

<a href="#">Link to this property</a>

"biso"

<a href="#">Link to this property</a>

"bookmark"

<a href="#">Link to this property</a>

"dash\_sso"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

allowed\_idps: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20allowed_idps%20%3E%20(schema)">AllowedIdPs</a>

The identity providers your users can select when connecting to this application. Defaults to all IdPs configured in your account.

<a href="#">Link to this property</a>

aud: optional string

Audience tag.

maxLength64

<a href="#">Link to this property</a>

auto\_redirect\_to\_identity: optional boolean

When set to <code>true</code>, users skip the identity provider selection step during login. You must specify only one identity provider in allowed\_idps.

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

domain: optional string

The domain and path that Access will secure.

<a href="#">Link to this property</a>

name: optional string

The name of the application.

<a href="#">Link to this property</a>

<details>

<summary>

scim\_config: optional object {idp\_uid, remote\_uri, authentication, 3 more }

Configuration for provisioning to this application via SCIM. This is currently in closed beta.

</summary>

idp\_uid: string

The UID of the IdP to use as the source for SCIM resources to provision to this application.

<a href="#">Link to this property</a>

remote\_uri: string

The base URI for the application’s SCIM-compatible API.

<a href="#">Link to this property</a>

<details>

<summary>

authentication: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_http_basic%20%3E%20(schema)">SCIMConfigAuthenticationHTTPBasic</a> { password, scheme, user } or object {token, scheme } or <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_oauth2%20%3E%20(schema)">SCIMConfigAuthenticationOauth2</a> { authorization\_url, client\_id, client\_secret, 3 more } or 2 more

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

One of the following:

<details>

<summary>

SCIMConfigAuthenticationHTTPBasic object {password, scheme, user }

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

password: string

Password used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "httpbasic"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

user: string

User name used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationOAuthBearerToken2 object {token, scheme }

Attributes for configuring OAuth Bearer Token authentication scheme for SCIM provisioning to an application.

</summary>

token: string

Token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "oauthbearertoken"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SCIMConfigAuthenticationOauth2 object {authorization\_url, client\_id, client\_secret, 3 more }

Attributes for configuring OAuth 2 authentication scheme for SCIM provisioning to an application.

</summary>

authorization\_url: string

URL used to generate the auth code used during token generation.

<a href="#">Link to this property</a>

client\_id: string

Client ID used to authenticate when generating a token for authenticating with the remote SCIM service.

<a href="#">Link to this property</a>

client\_secret: string

Secret used to authenticate when generating a token for authenticating with the remove SCIM service.

<a href="#">Link to this property</a>

scheme: "oauth2"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

token\_url: string

URL used to generate the token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scopes: optional array of string

The authorization scopes to request when generating the token used to authenticate with the remove SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationAccessServiceToken object {client\_id, client\_secret, scheme }

Attributes for configuring Access Service Token authentication scheme for SCIM provisioning to an application.

</summary>

client\_id: string

Client ID of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

client\_secret: string

Client secret of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

scheme: "access\_service\_token"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigMultiAuthentication2 = array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_http_basic%20%3E%20(schema)">SCIMConfigAuthenticationHTTPBasic</a> { password, scheme, user } or object {token, scheme } or <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_oauth2%20%3E%20(schema)">SCIMConfigAuthenticationOauth2</a> { authorization\_url, client\_id, client\_secret, 3 more } or object {client\_id, client\_secret, scheme }

Multiple authentication schemes

</summary>

One of the following:

<details>

<summary>

SCIMConfigAuthenticationHTTPBasic object {password, scheme, user }

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

password: string

Password used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "httpbasic"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

user: string

User name used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationOAuthBearerToken2 object {token, scheme }

Attributes for configuring OAuth Bearer Token authentication scheme for SCIM provisioning to an application.

</summary>

token: string

Token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "oauthbearertoken"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SCIMConfigAuthenticationOauth2 object {authorization\_url, client\_id, client\_secret, 3 more }

Attributes for configuring OAuth 2 authentication scheme for SCIM provisioning to an application.

</summary>

authorization\_url: string

URL used to generate the auth code used during token generation.

<a href="#">Link to this property</a>

client\_id: string

Client ID used to authenticate when generating a token for authenticating with the remote SCIM service.

<a href="#">Link to this property</a>

client\_secret: string

Secret used to authenticate when generating a token for authenticating with the remove SCIM service.

<a href="#">Link to this property</a>

scheme: "oauth2"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

token\_url: string

URL used to generate the token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scopes: optional array of string

The authorization scopes to request when generating the token used to authenticate with the remove SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationAccessServiceToken object {client\_id, client\_secret, scheme }

Attributes for configuring Access Service Token authentication scheme for SCIM provisioning to an application.

</summary>

client\_id: string

Client ID of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

client\_secret: string

Client secret of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

scheme: "access\_service\_token"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

deactivate\_on\_delete: optional boolean

If false, we propagate DELETE requests to the target application for SCIM resources. If true, we only set <code>active</code> to false on the SCIM resource. This is useful because some targets do not support DELETE operations.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether SCIM provisioning is turned on for this application.

<a href="#">Link to this property</a>

<details>

<summary>

mappings: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_mapping%20%3E%20(schema)">SCIMConfigMapping</a> { schema, enabled, filter, 3 more }

A list of mappings to apply to SCIM resources before provisioning them in this application. These can transform or filter the resources to be provisioned.

</summary>

schema: string

Which SCIM resource type this mapping applies to.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether or not this mapping is enabled.

<a href="#">Link to this property</a>

filter: optional string

A <a href="https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2.2">SCIM filter expression</a> that matches resources that should be provisioned to this application.

<a href="#">Link to this property</a>

<details>

<summary>

operations: optional object {create, delete, update }

Whether or not this mapping applies to creates, updates, or deletes.

</summary>

create: optional boolean

Whether or not this mapping applies to create (POST) operations.

<a href="#">Link to this property</a>

delete: optional boolean

Whether or not this mapping applies to DELETE operations.

<a href="#">Link to this property</a>

update: optional boolean

Whether or not this mapping applies to update (PATCH/PUT) operations.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

strictness: optional "strict"or "passthrough"

The level of adherence to outbound resource schemas when provisioning to this mapping. ‘Strict’ removes unknown values, while ‘passthrough’ passes unknown values to the target.

</summary>

One of the following:

"strict"

<a href="#">Link to this property</a>

"passthrough"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

transform\_jsonata: optional string

A <a href="https://jsonata.org/">JSONata</a> expression that transforms the resource before provisioning it in the application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

session\_duration: optional string

The amount of time that tokens issued for this application will be valid. Must be in the format <code>300ms</code> or <code>2h45m</code>. Valid time units are: ns, us (or µs), ms, s, m, h.

<a href="#">Link to this property</a>

updated\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

DeviceEnrollmentPermissionsApplication object {type, id, allowed\_idps, 8 more }

</summary>

<details>

<summary>

type: "self\_hosted"or "saas"or "ssh"or 6 more

The application type.

</summary>

One of the following:

"self\_hosted"

<a href="#">Link to this property</a>

"saas"

<a href="#">Link to this property</a>

"ssh"

<a href="#">Link to this property</a>

"vnc"

<a href="#">Link to this property</a>

"app\_launcher"

<a href="#">Link to this property</a>

"warp"

<a href="#">Link to this property</a>

"biso"

<a href="#">Link to this property</a>

"bookmark"

<a href="#">Link to this property</a>

"dash\_sso"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

allowed\_idps: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20allowed_idps%20%3E%20(schema)">AllowedIdPs</a>

The identity providers your users can select when connecting to this application. Defaults to all IdPs configured in your account.

<a href="#">Link to this property</a>

aud: optional string

Audience tag.

maxLength64

<a href="#">Link to this property</a>

auto\_redirect\_to\_identity: optional boolean

When set to <code>true</code>, users skip the identity provider selection step during login. You must specify only one identity provider in allowed\_idps.

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

domain: optional string

The domain and path that Access will secure.

<a href="#">Link to this property</a>

name: optional string

The name of the application.

<a href="#">Link to this property</a>

<details>

<summary>

scim\_config: optional object {idp\_uid, remote\_uri, authentication, 3 more }

Configuration for provisioning to this application via SCIM. This is currently in closed beta.

</summary>

idp\_uid: string

The UID of the IdP to use as the source for SCIM resources to provision to this application.

<a href="#">Link to this property</a>

remote\_uri: string

The base URI for the application’s SCIM-compatible API.

<a href="#">Link to this property</a>

<details>

<summary>

authentication: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_http_basic%20%3E%20(schema)">SCIMConfigAuthenticationHTTPBasic</a> { password, scheme, user } or object {token, scheme } or <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_oauth2%20%3E%20(schema)">SCIMConfigAuthenticationOauth2</a> { authorization\_url, client\_id, client\_secret, 3 more } or 2 more

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

One of the following:

<details>

<summary>

SCIMConfigAuthenticationHTTPBasic object {password, scheme, user }

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

password: string

Password used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "httpbasic"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

user: string

User name used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationOAuthBearerToken2 object {token, scheme }

Attributes for configuring OAuth Bearer Token authentication scheme for SCIM provisioning to an application.

</summary>

token: string

Token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "oauthbearertoken"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SCIMConfigAuthenticationOauth2 object {authorization\_url, client\_id, client\_secret, 3 more }

Attributes for configuring OAuth 2 authentication scheme for SCIM provisioning to an application.

</summary>

authorization\_url: string

URL used to generate the auth code used during token generation.

<a href="#">Link to this property</a>

client\_id: string

Client ID used to authenticate when generating a token for authenticating with the remote SCIM service.

<a href="#">Link to this property</a>

client\_secret: string

Secret used to authenticate when generating a token for authenticating with the remove SCIM service.

<a href="#">Link to this property</a>

scheme: "oauth2"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

token\_url: string

URL used to generate the token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scopes: optional array of string

The authorization scopes to request when generating the token used to authenticate with the remove SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationAccessServiceToken object {client\_id, client\_secret, scheme }

Attributes for configuring Access Service Token authentication scheme for SCIM provisioning to an application.

</summary>

client\_id: string

Client ID of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

client\_secret: string

Client secret of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

scheme: "access\_service\_token"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigMultiAuthentication2 = array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_http_basic%20%3E%20(schema)">SCIMConfigAuthenticationHTTPBasic</a> { password, scheme, user } or object {token, scheme } or <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_oauth2%20%3E%20(schema)">SCIMConfigAuthenticationOauth2</a> { authorization\_url, client\_id, client\_secret, 3 more } or object {client\_id, client\_secret, scheme }

Multiple authentication schemes

</summary>

One of the following:

<details>

<summary>

SCIMConfigAuthenticationHTTPBasic object {password, scheme, user }

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

password: string

Password used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "httpbasic"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

user: string

User name used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationOAuthBearerToken2 object {token, scheme }

Attributes for configuring OAuth Bearer Token authentication scheme for SCIM provisioning to an application.

</summary>

token: string

Token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "oauthbearertoken"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SCIMConfigAuthenticationOauth2 object {authorization\_url, client\_id, client\_secret, 3 more }

Attributes for configuring OAuth 2 authentication scheme for SCIM provisioning to an application.

</summary>

authorization\_url: string

URL used to generate the auth code used during token generation.

<a href="#">Link to this property</a>

client\_id: string

Client ID used to authenticate when generating a token for authenticating with the remote SCIM service.

<a href="#">Link to this property</a>

client\_secret: string

Secret used to authenticate when generating a token for authenticating with the remove SCIM service.

<a href="#">Link to this property</a>

scheme: "oauth2"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

token\_url: string

URL used to generate the token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scopes: optional array of string

The authorization scopes to request when generating the token used to authenticate with the remove SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationAccessServiceToken object {client\_id, client\_secret, scheme }

Attributes for configuring Access Service Token authentication scheme for SCIM provisioning to an application.

</summary>

client\_id: string

Client ID of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

client\_secret: string

Client secret of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

scheme: "access\_service\_token"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

deactivate\_on\_delete: optional boolean

If false, we propagate DELETE requests to the target application for SCIM resources. If true, we only set <code>active</code> to false on the SCIM resource. This is useful because some targets do not support DELETE operations.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether SCIM provisioning is turned on for this application.

<a href="#">Link to this property</a>

<details>

<summary>

mappings: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_mapping%20%3E%20(schema)">SCIMConfigMapping</a> { schema, enabled, filter, 3 more }

A list of mappings to apply to SCIM resources before provisioning them in this application. These can transform or filter the resources to be provisioned.

</summary>

schema: string

Which SCIM resource type this mapping applies to.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether or not this mapping is enabled.

<a href="#">Link to this property</a>

filter: optional string

A <a href="https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2.2">SCIM filter expression</a> that matches resources that should be provisioned to this application.

<a href="#">Link to this property</a>

<details>

<summary>

operations: optional object {create, delete, update }

Whether or not this mapping applies to creates, updates, or deletes.

</summary>

create: optional boolean

Whether or not this mapping applies to create (POST) operations.

<a href="#">Link to this property</a>

delete: optional boolean

Whether or not this mapping applies to DELETE operations.

<a href="#">Link to this property</a>

update: optional boolean

Whether or not this mapping applies to update (PATCH/PUT) operations.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

strictness: optional "strict"or "passthrough"

The level of adherence to outbound resource schemas when provisioning to this mapping. ‘Strict’ removes unknown values, while ‘passthrough’ passes unknown values to the target.

</summary>

One of the following:

"strict"

<a href="#">Link to this property</a>

"passthrough"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

transform\_jsonata: optional string

A <a href="https://jsonata.org/">JSONata</a> expression that transforms the resource before provisioning it in the application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

session\_duration: optional string

The amount of time that tokens issued for this application will be valid. Must be in the format <code>300ms</code> or <code>2h45m</code>. Valid time units are: ns, us (or µs), ms, s, m, h.

<a href="#">Link to this property</a>

updated\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

BrowserIsolationPermissionsApplication object {type, id, allowed\_idps, 8 more }

</summary>

<details>

<summary>

type: "self\_hosted"or "saas"or "ssh"or 6 more

The application type.

</summary>

One of the following:

"self\_hosted"

<a href="#">Link to this property</a>

"saas"

<a href="#">Link to this property</a>

"ssh"

<a href="#">Link to this property</a>

"vnc"

<a href="#">Link to this property</a>

"app\_launcher"

<a href="#">Link to this property</a>

"warp"

<a href="#">Link to this property</a>

"biso"

<a href="#">Link to this property</a>

"bookmark"

<a href="#">Link to this property</a>

"dash\_sso"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

allowed\_idps: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20allowed_idps%20%3E%20(schema)">AllowedIdPs</a>

The identity providers your users can select when connecting to this application. Defaults to all IdPs configured in your account.

<a href="#">Link to this property</a>

aud: optional string

Audience tag.

maxLength64

<a href="#">Link to this property</a>

auto\_redirect\_to\_identity: optional boolean

When set to <code>true</code>, users skip the identity provider selection step during login. You must specify only one identity provider in allowed\_idps.

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

domain: optional string

The domain and path that Access will secure.

<a href="#">Link to this property</a>

name: optional string

The name of the application.

<a href="#">Link to this property</a>

<details>

<summary>

scim\_config: optional object {idp\_uid, remote\_uri, authentication, 3 more }

Configuration for provisioning to this application via SCIM. This is currently in closed beta.

</summary>

idp\_uid: string

The UID of the IdP to use as the source for SCIM resources to provision to this application.

<a href="#">Link to this property</a>

remote\_uri: string

The base URI for the application’s SCIM-compatible API.

<a href="#">Link to this property</a>

<details>

<summary>

authentication: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_http_basic%20%3E%20(schema)">SCIMConfigAuthenticationHTTPBasic</a> { password, scheme, user } or object {token, scheme } or <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_oauth2%20%3E%20(schema)">SCIMConfigAuthenticationOauth2</a> { authorization\_url, client\_id, client\_secret, 3 more } or 2 more

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

One of the following:

<details>

<summary>

SCIMConfigAuthenticationHTTPBasic object {password, scheme, user }

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

password: string

Password used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "httpbasic"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

user: string

User name used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationOAuthBearerToken2 object {token, scheme }

Attributes for configuring OAuth Bearer Token authentication scheme for SCIM provisioning to an application.

</summary>

token: string

Token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "oauthbearertoken"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SCIMConfigAuthenticationOauth2 object {authorization\_url, client\_id, client\_secret, 3 more }

Attributes for configuring OAuth 2 authentication scheme for SCIM provisioning to an application.

</summary>

authorization\_url: string

URL used to generate the auth code used during token generation.

<a href="#">Link to this property</a>

client\_id: string

Client ID used to authenticate when generating a token for authenticating with the remote SCIM service.

<a href="#">Link to this property</a>

client\_secret: string

Secret used to authenticate when generating a token for authenticating with the remove SCIM service.

<a href="#">Link to this property</a>

scheme: "oauth2"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

token\_url: string

URL used to generate the token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scopes: optional array of string

The authorization scopes to request when generating the token used to authenticate with the remove SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationAccessServiceToken object {client\_id, client\_secret, scheme }

Attributes for configuring Access Service Token authentication scheme for SCIM provisioning to an application.

</summary>

client\_id: string

Client ID of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

client\_secret: string

Client secret of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

scheme: "access\_service\_token"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigMultiAuthentication2 = array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_http_basic%20%3E%20(schema)">SCIMConfigAuthenticationHTTPBasic</a> { password, scheme, user } or object {token, scheme } or <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_oauth2%20%3E%20(schema)">SCIMConfigAuthenticationOauth2</a> { authorization\_url, client\_id, client\_secret, 3 more } or object {client\_id, client\_secret, scheme }

Multiple authentication schemes

</summary>

One of the following:

<details>

<summary>

SCIMConfigAuthenticationHTTPBasic object {password, scheme, user }

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

password: string

Password used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "httpbasic"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

user: string

User name used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationOAuthBearerToken2 object {token, scheme }

Attributes for configuring OAuth Bearer Token authentication scheme for SCIM provisioning to an application.

</summary>

token: string

Token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "oauthbearertoken"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SCIMConfigAuthenticationOauth2 object {authorization\_url, client\_id, client\_secret, 3 more }

Attributes for configuring OAuth 2 authentication scheme for SCIM provisioning to an application.

</summary>

authorization\_url: string

URL used to generate the auth code used during token generation.

<a href="#">Link to this property</a>

client\_id: string

Client ID used to authenticate when generating a token for authenticating with the remote SCIM service.

<a href="#">Link to this property</a>

client\_secret: string

Secret used to authenticate when generating a token for authenticating with the remove SCIM service.

<a href="#">Link to this property</a>

scheme: "oauth2"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

token\_url: string

URL used to generate the token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scopes: optional array of string

The authorization scopes to request when generating the token used to authenticate with the remove SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationAccessServiceToken object {client\_id, client\_secret, scheme }

Attributes for configuring Access Service Token authentication scheme for SCIM provisioning to an application.

</summary>

client\_id: string

Client ID of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

client\_secret: string

Client secret of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

scheme: "access\_service\_token"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

deactivate\_on\_delete: optional boolean

If false, we propagate DELETE requests to the target application for SCIM resources. If true, we only set <code>active</code> to false on the SCIM resource. This is useful because some targets do not support DELETE operations.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether SCIM provisioning is turned on for this application.

<a href="#">Link to this property</a>

<details>

<summary>

mappings: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_mapping%20%3E%20(schema)">SCIMConfigMapping</a> { schema, enabled, filter, 3 more }

A list of mappings to apply to SCIM resources before provisioning them in this application. These can transform or filter the resources to be provisioned.

</summary>

schema: string

Which SCIM resource type this mapping applies to.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether or not this mapping is enabled.

<a href="#">Link to this property</a>

filter: optional string

A <a href="https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2.2">SCIM filter expression</a> that matches resources that should be provisioned to this application.

<a href="#">Link to this property</a>

<details>

<summary>

operations: optional object {create, delete, update }

Whether or not this mapping applies to creates, updates, or deletes.

</summary>

create: optional boolean

Whether or not this mapping applies to create (POST) operations.

<a href="#">Link to this property</a>

delete: optional boolean

Whether or not this mapping applies to DELETE operations.

<a href="#">Link to this property</a>

update: optional boolean

Whether or not this mapping applies to update (PATCH/PUT) operations.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

strictness: optional "strict"or "passthrough"

The level of adherence to outbound resource schemas when provisioning to this mapping. ‘Strict’ removes unknown values, while ‘passthrough’ passes unknown values to the target.

</summary>

One of the following:

"strict"

<a href="#">Link to this property</a>

"passthrough"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

transform\_jsonata: optional string

A <a href="https://jsonata.org/">JSONata</a> expression that transforms the resource before provisioning it in the application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

session\_duration: optional string

The amount of time that tokens issued for this application will be valid. Must be in the format <code>300ms</code> or <code>2h45m</code>. Valid time units are: ns, us (or µs), ms, s, m, h.

<a href="#">Link to this property</a>

updated\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

BookmarkApplication object {domain, type, id, 7 more }

</summary>

domain: string

The URL or domain of the bookmark.

<a href="#">Link to this property</a>

type: string

The application type.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

app\_launcher\_visible: optional boolean

<a href="#">Link to this property</a>

aud: optional string

Audience tag.

maxLength64

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

logo\_url: optional string

The image URL for the logo shown in the App Launcher dashboard.

<a href="#">Link to this property</a>

name: optional string

The name of the application.

<a href="#">Link to this property</a>

<details>

<summary>

scim\_config: optional object {idp\_uid, remote\_uri, authentication, 3 more }

Configuration for provisioning to this application via SCIM. This is currently in closed beta.

</summary>

idp\_uid: string

The UID of the IdP to use as the source for SCIM resources to provision to this application.

<a href="#">Link to this property</a>

remote\_uri: string

The base URI for the application’s SCIM-compatible API.

<a href="#">Link to this property</a>

<details>

<summary>

authentication: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_http_basic%20%3E%20(schema)">SCIMConfigAuthenticationHTTPBasic</a> { password, scheme, user } or object {token, scheme } or <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_oauth2%20%3E%20(schema)">SCIMConfigAuthenticationOauth2</a> { authorization\_url, client\_id, client\_secret, 3 more } or 2 more

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

One of the following:

<details>

<summary>

SCIMConfigAuthenticationHTTPBasic object {password, scheme, user }

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

password: string

Password used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "httpbasic"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

user: string

User name used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationOAuthBearerToken2 object {token, scheme }

Attributes for configuring OAuth Bearer Token authentication scheme for SCIM provisioning to an application.

</summary>

token: string

Token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "oauthbearertoken"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SCIMConfigAuthenticationOauth2 object {authorization\_url, client\_id, client\_secret, 3 more }

Attributes for configuring OAuth 2 authentication scheme for SCIM provisioning to an application.

</summary>

authorization\_url: string

URL used to generate the auth code used during token generation.

<a href="#">Link to this property</a>

client\_id: string

Client ID used to authenticate when generating a token for authenticating with the remote SCIM service.

<a href="#">Link to this property</a>

client\_secret: string

Secret used to authenticate when generating a token for authenticating with the remove SCIM service.

<a href="#">Link to this property</a>

scheme: "oauth2"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

token\_url: string

URL used to generate the token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scopes: optional array of string

The authorization scopes to request when generating the token used to authenticate with the remove SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationAccessServiceToken object {client\_id, client\_secret, scheme }

Attributes for configuring Access Service Token authentication scheme for SCIM provisioning to an application.

</summary>

client\_id: string

Client ID of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

client\_secret: string

Client secret of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

scheme: "access\_service\_token"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigMultiAuthentication2 = array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_http_basic%20%3E%20(schema)">SCIMConfigAuthenticationHTTPBasic</a> { password, scheme, user } or object {token, scheme } or <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_oauth2%20%3E%20(schema)">SCIMConfigAuthenticationOauth2</a> { authorization\_url, client\_id, client\_secret, 3 more } or object {client\_id, client\_secret, scheme }

Multiple authentication schemes

</summary>

One of the following:

<details>

<summary>

SCIMConfigAuthenticationHTTPBasic object {password, scheme, user }

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

password: string

Password used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "httpbasic"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

user: string

User name used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationOAuthBearerToken2 object {token, scheme }

Attributes for configuring OAuth Bearer Token authentication scheme for SCIM provisioning to an application.

</summary>

token: string

Token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "oauthbearertoken"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SCIMConfigAuthenticationOauth2 object {authorization\_url, client\_id, client\_secret, 3 more }

Attributes for configuring OAuth 2 authentication scheme for SCIM provisioning to an application.

</summary>

authorization\_url: string

URL used to generate the auth code used during token generation.

<a href="#">Link to this property</a>

client\_id: string

Client ID used to authenticate when generating a token for authenticating with the remote SCIM service.

<a href="#">Link to this property</a>

client\_secret: string

Secret used to authenticate when generating a token for authenticating with the remove SCIM service.

<a href="#">Link to this property</a>

scheme: "oauth2"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

token\_url: string

URL used to generate the token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scopes: optional array of string

The authorization scopes to request when generating the token used to authenticate with the remove SCIM service.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessSCIMConfigAuthenticationAccessServiceToken object {client\_id, client\_secret, scheme }

Attributes for configuring Access Service Token authentication scheme for SCIM provisioning to an application.

</summary>

client\_id: string

Client ID of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

client\_secret: string

Client secret of the Access service token used to authenticate with the remote service.

<a href="#">Link to this property</a>

scheme: "access\_service\_token"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

deactivate\_on\_delete: optional boolean

If false, we propagate DELETE requests to the target application for SCIM resources. If true, we only set <code>active</code> to false on the SCIM resource. This is useful because some targets do not support DELETE operations.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether SCIM provisioning is turned on for this application.

<a href="#">Link to this property</a>

<details>

<summary>

mappings: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_mapping%20%3E%20(schema)">SCIMConfigMapping</a> { schema, enabled, filter, 3 more }

A list of mappings to apply to SCIM resources before provisioning them in this application. These can transform or filter the resources to be provisioned.

</summary>

schema: string

Which SCIM resource type this mapping applies to.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether or not this mapping is enabled.

<a href="#">Link to this property</a>

filter: optional string

A <a href="https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2.2">SCIM filter expression</a> that matches resources that should be provisioned to this application.

<a href="#">Link to this property</a>

<details>

<summary>

operations: optional object {create, delete, update }

Whether or not this mapping applies to creates, updates, or deletes.

</summary>

create: optional boolean

Whether or not this mapping applies to create (POST) operations.

<a href="#">Link to this property</a>

delete: optional boolean

Whether or not this mapping applies to DELETE operations.

<a href="#">Link to this property</a>

update: optional boolean

Whether or not this mapping applies to update (PATCH/PUT) operations.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

strictness: optional "strict"or "passthrough"

The level of adherence to outbound resource schemas when provisioning to this mapping. ‘Strict’ removes unknown values, while ‘passthrough’ passes unknown values to the target.

</summary>

One of the following:

"strict"

<a href="#">Link to this property</a>

"passthrough"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

transform\_jsonata: optional string

A <a href="https://jsonata.org/">JSONata</a> expression that transforms the resource before provisioning it in the application.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.applications%20%3E%20(model)%20application%20%3E%20(schema)>)

<details>

<summary>

ApplicationPolicy object {id, approval\_groups, approval\_required, 13 more }

</summary>

id: optional string

The UUID of the policy

maxLength36

<a href="#">Link to this property</a>

<details>

<summary>

approval\_groups: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.policies%20%3E%20(model)%20approval_group%20%3E%20(schema)">ApprovalGroup</a> { approvals\_needed, email\_addresses, email\_list\_uuid }

Administrators who can approve a temporary authentication request.

</summary>

approvals\_needed: number

The number of approvals needed to obtain access.

minimum0

<a href="#">Link to this property</a>

email\_addresses: optional array of string

A list of emails that can approve the access request.

<a href="#">Link to this property</a>

email\_list\_uuid: optional string

The UUID of an re-usable email list.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

approval\_required: optional boolean

Requires the user to request access from an administrator at the start of each session.

<a href="#">Link to this property</a>

<details>

<summary>

connection\_rules: optional object {rdp }

The rules that define how users may connect to targets secured by your application.

</summary>

<details>

<summary>

rdp: optional object {allowed\_clipboard\_local\_to\_remote\_formats, allowed\_clipboard\_remote\_to\_local\_formats }

The RDP-specific rules that define clipboard behavior for RDP connections.

</summary>

<details>

<summary>

allowed\_clipboard\_local\_to\_remote\_formats: optional array of "text"or "file"

Clipboard formats allowed when copying from local machine to remote RDP session.

</summary>

One of the following:

"text"

<a href="#">Link to this property</a>

"file"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

allowed\_clipboard\_remote\_to\_local\_formats: optional array of "text"or "file"

Clipboard formats allowed when copying from remote RDP session to local machine.

</summary>

One of the following:

"text"

<a href="#">Link to this property</a>

"file"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

decision: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20decision%20%3E%20(schema)">Decision</a>

The action Access will take if a user matches this policy. Infrastructure application policies can only use the Allow action.

<a href="#">Link to this property</a>

<details>

<summary>

exclude: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications.policies%20%3E%20(model)%20access_rule%20%3E%20(schema)">AccessRule</a>

Rules evaluated with a NOT logical operator. To match the policy, a user cannot meet any of the Exclude rules.

</summary>

One of the following:

<details>

<summary>

GroupRule object {group }

Matches an Access group.

</summary>

<details>

<summary>

group: object {id }

</summary>

id: string

The ID of a previously created Access group.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AnyValidServiceTokenRule object {any\_valid\_service\_token }

Matches any valid Access Service Token

</summary>

any\_valid\_service\_token: object {}

An empty object which matches on all service tokens.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessAuthContextRule object {auth\_context }

Matches an Azure Authentication Context. Requires an Azure identity provider.

</summary>

<details>

<summary>

auth\_context: object {id, ac\_id, identity\_provider\_id }

</summary>

id: string

The ID of an Authentication context.

<a href="#">Link to this property</a>

ac\_id: string

The ACID of an Authentication context.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your Azure identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AuthenticationMethodRule object {auth\_method }

Enforce different MFA options

</summary>

<details>

<summary>

auth\_method: object {auth\_method }

</summary>

auth\_method: string

The type of authentication method <a href="https://datatracker.ietf.org/doc/html/rfc8176#section-2">https://datatracker.ietf.org/doc/html/rfc8176#section-2</a>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AzureGroupRule object {azureAD }

Matches an Azure group. Requires an Azure identity provider.

</summary>

<details>

<summary>

azureAD: object {id, identity\_provider\_id }

</summary>

id: string

The ID of an Azure group.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your Azure identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CertificateRule object {certificate }

Matches any valid client certificate.

</summary>

certificate: object {}

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessCommonNameRule object {common\_name }

Matches a specific common name.

</summary>

<details>

<summary>

common\_name: object {common\_name }

</summary>

common\_name: string

The common name to match.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CountryRule object {geo }

Matches a specific country

</summary>

<details>

<summary>

geo: object {country\_code }

</summary>

country\_code: string

The country code that should be matched.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessDevicePostureRule object {device\_posture }

Enforces a device posture rule has run successfully

</summary>

<details>

<summary>

device\_posture: object {integration\_uid, account\_id }

</summary>

integration\_uid: string

The ID of a device posture integration.

<a href="#">Link to this property</a>

account\_id: optional string

The ID of the account that owns the device posture integration.

maxLength32

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

DomainRule object {email\_domain }

Match an entire email domain.

</summary>

<details>

<summary>

email\_domain: object {domain }

</summary>

domain: string

The email domain to match.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

EmailListRule object {email\_list }

Matches an email address from a list.

</summary>

<details>

<summary>

email\_list: object {id }

</summary>

id: string

The ID of a previously created email list.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

EmailRule object {email }

Matches a specific email.

</summary>

<details>

<summary>

email: object {email }

</summary>

email: string

The email of the user.

formatemail

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

EveryoneRule object {everyone }

Matches everyone.

</summary>

everyone: object {}

An empty object which matches on all users.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ExternalEvaluationRule object {external\_evaluation }

Create Allow or Block policies which evaluate the user based on custom criteria.

</summary>

<details>

<summary>

external\_evaluation: object {evaluate\_url, keys\_url }

</summary>

evaluate\_url: string

The API endpoint containing your business logic.

<a href="#">Link to this property</a>

keys\_url: string

The API endpoint containing the key that Access uses to verify that the response came from your API.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

GitHubOrganizationRule object {"github-organization" }

Matches a Github organization. Requires a Github identity provider.

</summary>

<details>

<summary>

"github-organization": object {identity\_provider\_id, name, team }

</summary>

identity\_provider\_id: string

The ID of your Github identity provider.

<a href="#">Link to this property</a>

name: string

The name of the organization.

<a href="#">Link to this property</a>

team: optional string

The name of the team

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

GSuiteGroupRule object {gsuite }

Matches a group in Google Workspace. Requires a Google Workspace identity provider.

</summary>

<details>

<summary>

gsuite: object {email, identity\_provider\_id }

</summary>

email: string

The email of the Google Workspace group.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your Google Workspace identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessLoginMethodRule object {login\_method }

Matches a specific identity provider id.

</summary>

<details>

<summary>

login\_method: object {id }

</summary>

id: string

The ID of an identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

IPListRule object {ip\_list }

Matches an IP address from a list.

</summary>

<details>

<summary>

ip\_list: object {id }

</summary>

id: string

The ID of a previously created IP list.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

IPRule object {ip }

Matches an IP address block.

</summary>

<details>

<summary>

ip: object {ip }

</summary>

ip: string

An IPv4 or IPv6 CIDR block.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

OktaGroupRule object {okta }

Matches an Okta group. Requires an Okta identity provider.

</summary>

<details>

<summary>

okta: object {identity\_provider\_id, name }

</summary>

identity\_provider\_id: string

The ID of your Okta identity provider.

<a href="#">Link to this property</a>

name: string

The name of the Okta group.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SAMLGroupRule object {saml }

Matches a SAML group. Requires a SAML identity provider.

</summary>

<details>

<summary>

saml: object {attribute\_name, attribute\_value, identity\_provider\_id }

</summary>

attribute\_name: string

The name of the SAML attribute.

<a href="#">Link to this property</a>

attribute\_value: string

The SAML attribute value to look for.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your SAML identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessOIDCClaimRule object {oidc }

Matches an OIDC claim. Requires an OIDC identity provider.

</summary>

<details>

<summary>

oidc: object {claim\_name, claim\_value, identity\_provider\_id }

</summary>

claim\_name: string

The name of the OIDC claim.

<a href="#">Link to this property</a>

claim\_value: string

The OIDC claim value to look for.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your OIDC identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ServiceTokenRule object {service\_token }

Matches a specific Access Service Token

</summary>

<details>

<summary>

service\_token: object {token\_id }

</summary>

token\_id: string

The ID of a Service Token.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessLinkedAppTokenRule object {linked\_app\_token }

Matches OAuth 2.0 access tokens issued by the specified Access OIDC SaaS application. Only compatible with non\_identity and bypass decisions.

</summary>

<details>

<summary>

linked\_app\_token: object {app\_uid }

</summary>

app\_uid: string

The ID of an Access OIDC SaaS application

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessUserRiskScoreRule object {user\_risk\_score }

Matches a user’s risk score.

</summary>

<details>

<summary>

user\_risk\_score: object {user\_risk\_score }

</summary>

<details>

<summary>

user\_risk\_score: array of "low"or "medium"or "high"or "unscored"

A list of risk score levels to match. Values can be low, medium, high, or unscored.

</summary>

One of the following:

"low"

<a href="#">Link to this property</a>

"medium"

<a href="#">Link to this property</a>

"high"

<a href="#">Link to this property</a>

"unscored"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessCloudflareAccountMemberRule object {cloudflare\_account\_member }

Matches users who are members of a specific Cloudflare account. Requires a Cloudflare identity provider.

</summary>

<details>

<summary>

cloudflare\_account\_member: object {account\_id }

</summary>

account\_id: optional string

Identifier.

maxLength32

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

include: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications.policies%20%3E%20(model)%20access_rule%20%3E%20(schema)">AccessRule</a>

Rules evaluated with an OR logical operator. A user needs to meet only one of the Include rules.

</summary>

One of the following:

<details>

<summary>

GroupRule object {group }

Matches an Access group.

</summary>

<details>

<summary>

group: object {id }

</summary>

id: string

The ID of a previously created Access group.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AnyValidServiceTokenRule object {any\_valid\_service\_token }

Matches any valid Access Service Token

</summary>

any\_valid\_service\_token: object {}

An empty object which matches on all service tokens.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessAuthContextRule object {auth\_context }

Matches an Azure Authentication Context. Requires an Azure identity provider.

</summary>

<details>

<summary>

auth\_context: object {id, ac\_id, identity\_provider\_id }

</summary>

id: string

The ID of an Authentication context.

<a href="#">Link to this property</a>

ac\_id: string

The ACID of an Authentication context.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your Azure identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AuthenticationMethodRule object {auth\_method }

Enforce different MFA options

</summary>

<details>

<summary>

auth\_method: object {auth\_method }

</summary>

auth\_method: string

The type of authentication method <a href="https://datatracker.ietf.org/doc/html/rfc8176#section-2">https://datatracker.ietf.org/doc/html/rfc8176#section-2</a>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AzureGroupRule object {azureAD }

Matches an Azure group. Requires an Azure identity provider.

</summary>

<details>

<summary>

azureAD: object {id, identity\_provider\_id }

</summary>

id: string

The ID of an Azure group.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your Azure identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CertificateRule object {certificate }

Matches any valid client certificate.

</summary>

certificate: object {}

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessCommonNameRule object {common\_name }

Matches a specific common name.

</summary>

<details>

<summary>

common\_name: object {common\_name }

</summary>

common\_name: string

The common name to match.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CountryRule object {geo }

Matches a specific country

</summary>

<details>

<summary>

geo: object {country\_code }

</summary>

country\_code: string

The country code that should be matched.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessDevicePostureRule object {device\_posture }

Enforces a device posture rule has run successfully

</summary>

<details>

<summary>

device\_posture: object {integration\_uid, account\_id }

</summary>

integration\_uid: string

The ID of a device posture integration.

<a href="#">Link to this property</a>

account\_id: optional string

The ID of the account that owns the device posture integration.

maxLength32

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

DomainRule object {email\_domain }

Match an entire email domain.

</summary>

<details>

<summary>

email\_domain: object {domain }

</summary>

domain: string

The email domain to match.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

EmailListRule object {email\_list }

Matches an email address from a list.

</summary>

<details>

<summary>

email\_list: object {id }

</summary>

id: string

The ID of a previously created email list.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

EmailRule object {email }

Matches a specific email.

</summary>

<details>

<summary>

email: object {email }

</summary>

email: string

The email of the user.

formatemail

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

EveryoneRule object {everyone }

Matches everyone.

</summary>

everyone: object {}

An empty object which matches on all users.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ExternalEvaluationRule object {external\_evaluation }

Create Allow or Block policies which evaluate the user based on custom criteria.

</summary>

<details>

<summary>

external\_evaluation: object {evaluate\_url, keys\_url }

</summary>

evaluate\_url: string

The API endpoint containing your business logic.

<a href="#">Link to this property</a>

keys\_url: string

The API endpoint containing the key that Access uses to verify that the response came from your API.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

GitHubOrganizationRule object {"github-organization" }

Matches a Github organization. Requires a Github identity provider.

</summary>

<details>

<summary>

"github-organization": object {identity\_provider\_id, name, team }

</summary>

identity\_provider\_id: string

The ID of your Github identity provider.

<a href="#">Link to this property</a>

name: string

The name of the organization.

<a href="#">Link to this property</a>

team: optional string

The name of the team

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

GSuiteGroupRule object {gsuite }

Matches a group in Google Workspace. Requires a Google Workspace identity provider.

</summary>

<details>

<summary>

gsuite: object {email, identity\_provider\_id }

</summary>

email: string

The email of the Google Workspace group.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your Google Workspace identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessLoginMethodRule object {login\_method }

Matches a specific identity provider id.

</summary>

<details>

<summary>

login\_method: object {id }

</summary>

id: string

The ID of an identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

IPListRule object {ip\_list }

Matches an IP address from a list.

</summary>

<details>

<summary>

ip\_list: object {id }

</summary>

id: string

The ID of a previously created IP list.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

IPRule object {ip }

Matches an IP address block.

</summary>

<details>

<summary>

ip: object {ip }

</summary>

ip: string

An IPv4 or IPv6 CIDR block.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

OktaGroupRule object {okta }

Matches an Okta group. Requires an Okta identity provider.

</summary>

<details>

<summary>

okta: object {identity\_provider\_id, name }

</summary>

identity\_provider\_id: string

The ID of your Okta identity provider.

<a href="#">Link to this property</a>

name: string

The name of the Okta group.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SAMLGroupRule object {saml }

Matches a SAML group. Requires a SAML identity provider.

</summary>

<details>

<summary>

saml: object {attribute\_name, attribute\_value, identity\_provider\_id }

</summary>

attribute\_name: string

The name of the SAML attribute.

<a href="#">Link to this property</a>

attribute\_value: string

The SAML attribute value to look for.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your SAML identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessOIDCClaimRule object {oidc }

Matches an OIDC claim. Requires an OIDC identity provider.

</summary>

<details>

<summary>

oidc: object {claim\_name, claim\_value, identity\_provider\_id }

</summary>

claim\_name: string

The name of the OIDC claim.

<a href="#">Link to this property</a>

claim\_value: string

The OIDC claim value to look for.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your OIDC identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ServiceTokenRule object {service\_token }

Matches a specific Access Service Token

</summary>

<details>

<summary>

service\_token: object {token\_id }

</summary>

token\_id: string

The ID of a Service Token.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessLinkedAppTokenRule object {linked\_app\_token }

Matches OAuth 2.0 access tokens issued by the specified Access OIDC SaaS application. Only compatible with non\_identity and bypass decisions.

</summary>

<details>

<summary>

linked\_app\_token: object {app\_uid }

</summary>

app\_uid: string

The ID of an Access OIDC SaaS application

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessUserRiskScoreRule object {user\_risk\_score }

Matches a user’s risk score.

</summary>

<details>

<summary>

user\_risk\_score: object {user\_risk\_score }

</summary>

<details>

<summary>

user\_risk\_score: array of "low"or "medium"or "high"or "unscored"

A list of risk score levels to match. Values can be low, medium, high, or unscored.

</summary>

One of the following:

"low"

<a href="#">Link to this property</a>

"medium"

<a href="#">Link to this property</a>

"high"

<a href="#">Link to this property</a>

"unscored"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessCloudflareAccountMemberRule object {cloudflare\_account\_member }

Matches users who are members of a specific Cloudflare account. Requires a Cloudflare identity provider.

</summary>

<details>

<summary>

cloudflare\_account\_member: object {account\_id }

</summary>

account\_id: optional string

Identifier.

maxLength32

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

isolation\_required: optional boolean

Require this application to be served in an isolated browser for users matching this policy. ‘Client Web Isolation’ must be on for the account in order to use this feature.

<a href="#">Link to this property</a>

<details>

<summary>

mfa\_config: optional object {allowed\_authenticators, mfa\_disabled, session\_duration }

Configures multi-factor authentication (MFA) settings.

</summary>

<details>

<summary>

allowed\_authenticators: optional array of "totp"or "biometrics"or "security\_key"

Lists the MFA methods that users can authenticate with.

</summary>

One of the following:

"totp"

<a href="#">Link to this property</a>

"biometrics"

<a href="#">Link to this property</a>

"security\_key"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

mfa\_disabled: optional boolean

Indicates whether to disable MFA for this resource. This option is available at the application and policy level.

<a href="#">Link to this property</a>

session\_duration: optional string

Defines the duration of an MFA session. Must be in minutes (m) or hours (h). Minimum: 0m. Maximum: 720h (30 days). Examples:<code>5m</code> or <code>24h</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: optional string

The name of the Access policy.

<a href="#">Link to this property</a>

purpose\_justification\_prompt: optional string

A custom message that will appear on the purpose justification screen.

<a href="#">Link to this property</a>

purpose\_justification\_required: optional boolean

Require users to enter a justification when they log in to the application.

<a href="#">Link to this property</a>

<details>

<summary>

require: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications.policies%20%3E%20(model)%20access_rule%20%3E%20(schema)">AccessRule</a>

Rules evaluated with an AND logical operator. To match the policy, a user must meet all of the Require rules.

</summary>

One of the following:

<details>

<summary>

GroupRule object {group }

Matches an Access group.

</summary>

<details>

<summary>

group: object {id }

</summary>

id: string

The ID of a previously created Access group.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AnyValidServiceTokenRule object {any\_valid\_service\_token }

Matches any valid Access Service Token

</summary>

any\_valid\_service\_token: object {}

An empty object which matches on all service tokens.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessAuthContextRule object {auth\_context }

Matches an Azure Authentication Context. Requires an Azure identity provider.

</summary>

<details>

<summary>

auth\_context: object {id, ac\_id, identity\_provider\_id }

</summary>

id: string

The ID of an Authentication context.

<a href="#">Link to this property</a>

ac\_id: string

The ACID of an Authentication context.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your Azure identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AuthenticationMethodRule object {auth\_method }

Enforce different MFA options

</summary>

<details>

<summary>

auth\_method: object {auth\_method }

</summary>

auth\_method: string

The type of authentication method <a href="https://datatracker.ietf.org/doc/html/rfc8176#section-2">https://datatracker.ietf.org/doc/html/rfc8176#section-2</a>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AzureGroupRule object {azureAD }

Matches an Azure group. Requires an Azure identity provider.

</summary>

<details>

<summary>

azureAD: object {id, identity\_provider\_id }

</summary>

id: string

The ID of an Azure group.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your Azure identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CertificateRule object {certificate }

Matches any valid client certificate.

</summary>

certificate: object {}

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessCommonNameRule object {common\_name }

Matches a specific common name.

</summary>

<details>

<summary>

common\_name: object {common\_name }

</summary>

common\_name: string

The common name to match.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CountryRule object {geo }

Matches a specific country

</summary>

<details>

<summary>

geo: object {country\_code }

</summary>

country\_code: string

The country code that should be matched.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessDevicePostureRule object {device\_posture }

Enforces a device posture rule has run successfully

</summary>

<details>

<summary>

device\_posture: object {integration\_uid, account\_id }

</summary>

integration\_uid: string

The ID of a device posture integration.

<a href="#">Link to this property</a>

account\_id: optional string

The ID of the account that owns the device posture integration.

maxLength32

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

DomainRule object {email\_domain }

Match an entire email domain.

</summary>

<details>

<summary>

email\_domain: object {domain }

</summary>

domain: string

The email domain to match.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

EmailListRule object {email\_list }

Matches an email address from a list.

</summary>

<details>

<summary>

email\_list: object {id }

</summary>

id: string

The ID of a previously created email list.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

EmailRule object {email }

Matches a specific email.

</summary>

<details>

<summary>

email: object {email }

</summary>

email: string

The email of the user.

formatemail

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

EveryoneRule object {everyone }

Matches everyone.

</summary>

everyone: object {}

An empty object which matches on all users.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ExternalEvaluationRule object {external\_evaluation }

Create Allow or Block policies which evaluate the user based on custom criteria.

</summary>

<details>

<summary>

external\_evaluation: object {evaluate\_url, keys\_url }

</summary>

evaluate\_url: string

The API endpoint containing your business logic.

<a href="#">Link to this property</a>

keys\_url: string

The API endpoint containing the key that Access uses to verify that the response came from your API.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

GitHubOrganizationRule object {"github-organization" }

Matches a Github organization. Requires a Github identity provider.

</summary>

<details>

<summary>

"github-organization": object {identity\_provider\_id, name, team }

</summary>

identity\_provider\_id: string

The ID of your Github identity provider.

<a href="#">Link to this property</a>

name: string

The name of the organization.

<a href="#">Link to this property</a>

team: optional string

The name of the team

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

GSuiteGroupRule object {gsuite }

Matches a group in Google Workspace. Requires a Google Workspace identity provider.

</summary>

<details>

<summary>

gsuite: object {email, identity\_provider\_id }

</summary>

email: string

The email of the Google Workspace group.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your Google Workspace identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessLoginMethodRule object {login\_method }

Matches a specific identity provider id.

</summary>

<details>

<summary>

login\_method: object {id }

</summary>

id: string

The ID of an identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

IPListRule object {ip\_list }

Matches an IP address from a list.

</summary>

<details>

<summary>

ip\_list: object {id }

</summary>

id: string

The ID of a previously created IP list.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

IPRule object {ip }

Matches an IP address block.

</summary>

<details>

<summary>

ip: object {ip }

</summary>

ip: string

An IPv4 or IPv6 CIDR block.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

OktaGroupRule object {okta }

Matches an Okta group. Requires an Okta identity provider.

</summary>

<details>

<summary>

okta: object {identity\_provider\_id, name }

</summary>

identity\_provider\_id: string

The ID of your Okta identity provider.

<a href="#">Link to this property</a>

name: string

The name of the Okta group.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SAMLGroupRule object {saml }

Matches a SAML group. Requires a SAML identity provider.

</summary>

<details>

<summary>

saml: object {attribute\_name, attribute\_value, identity\_provider\_id }

</summary>

attribute\_name: string

The name of the SAML attribute.

<a href="#">Link to this property</a>

attribute\_value: string

The SAML attribute value to look for.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your SAML identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessOIDCClaimRule object {oidc }

Matches an OIDC claim. Requires an OIDC identity provider.

</summary>

<details>

<summary>

oidc: object {claim\_name, claim\_value, identity\_provider\_id }

</summary>

claim\_name: string

The name of the OIDC claim.

<a href="#">Link to this property</a>

claim\_value: string

The OIDC claim value to look for.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your OIDC identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ServiceTokenRule object {service\_token }

Matches a specific Access Service Token

</summary>

<details>

<summary>

service\_token: object {token\_id }

</summary>

token\_id: string

The ID of a Service Token.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessLinkedAppTokenRule object {linked\_app\_token }

Matches OAuth 2.0 access tokens issued by the specified Access OIDC SaaS application. Only compatible with non\_identity and bypass decisions.

</summary>

<details>

<summary>

linked\_app\_token: object {app\_uid }

</summary>

app\_uid: string

The ID of an Access OIDC SaaS application

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessUserRiskScoreRule object {user\_risk\_score }

Matches a user’s risk score.

</summary>

<details>

<summary>

user\_risk\_score: object {user\_risk\_score }

</summary>

<details>

<summary>

user\_risk\_score: array of "low"or "medium"or "high"or "unscored"

A list of risk score levels to match. Values can be low, medium, high, or unscored.

</summary>

One of the following:

"low"

<a href="#">Link to this property</a>

"medium"

<a href="#">Link to this property</a>

"high"

<a href="#">Link to this property</a>

"unscored"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessCloudflareAccountMemberRule object {cloudflare\_account\_member }

Matches users who are members of a specific Cloudflare account. Requires a Cloudflare identity provider.

</summary>

<details>

<summary>

cloudflare\_account\_member: object {account\_id }

</summary>

account\_id: optional string

Identifier.

maxLength32

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

session\_duration: optional string

The amount of time that tokens issued for the application will be valid. Must be in the format <code>300ms</code> or <code>2h45m</code>. Valid time units are: ns, us (or µs), ms, s, m, h.

<a href="#">Link to this property</a>

updated\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.applications%20%3E%20(model)%20application_policy%20%3E%20(schema)>)

<details>

<summary>

ApplicationType = "self\_hosted"or "end\_user"or "saas"or 12 more

The application type.

</summary>

One of the following:

"self\_hosted"

<a href="#">Link to this property</a>

"end\_user"

<a href="#">Link to this property</a>

"saas"

<a href="#">Link to this property</a>

"ssh"

<a href="#">Link to this property</a>

"vnc"

<a href="#">Link to this property</a>

"app\_launcher"

<a href="#">Link to this property</a>

"warp"

<a href="#">Link to this property</a>

"biso"

<a href="#">Link to this property</a>

"bookmark"

<a href="#">Link to this property</a>

"dash\_sso"

<a href="#">Link to this property</a>

"infrastructure"

<a href="#">Link to this property</a>

"rdp"

<a href="#">Link to this property</a>

"mcp"

<a href="#">Link to this property</a>

"mcp\_portal"

<a href="#">Link to this property</a>

"proxy\_endpoint"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.applications%20%3E%20(model)%20application_type%20%3E%20(schema)>)

<details>

<summary>

CORSHeaders object {allow\_all\_headers, allow\_all\_methods, allow\_all\_origins, 5 more }

</summary>

allow\_all\_headers: optional boolean

Allows all HTTP request headers.

<a href="#">Link to this property</a>

allow\_all\_methods: optional boolean

Allows all HTTP request methods.

<a href="#">Link to this property</a>

allow\_all\_origins: optional boolean

Allows all origins.

<a href="#">Link to this property</a>

allow\_credentials: optional boolean

When set to <code>true</code>, includes credentials (cookies, authorization headers, or TLS client certificates) with requests.

<a href="#">Link to this property</a>

allowed\_headers: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20allowed_headers%20%3E%20(schema)">AllowedHeaders</a>

Allowed HTTP request headers.

<a href="#">Link to this property</a>

<details>

<summary>

allowed\_methods: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20allowed_methods%20%3E%20(schema)">AllowedMethods</a>

Allowed HTTP request methods.

</summary>

One of the following:

"GET"

<a href="#">Link to this property</a>

"POST"

<a href="#">Link to this property</a>

"HEAD"

<a href="#">Link to this property</a>

"PUT"

<a href="#">Link to this property</a>

"DELETE"

<a href="#">Link to this property</a>

"CONNECT"

<a href="#">Link to this property</a>

"OPTIONS"

<a href="#">Link to this property</a>

"TRACE"

<a href="#">Link to this property</a>

"PATCH"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

allowed\_origins: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20allowed_origins%20%3E%20(schema)">AllowedOrigins</a>

Allowed origins.

<a href="#">Link to this property</a>

max\_age: optional number

The maximum number of seconds the results of a preflight request can be cached.

maximum86400

minimum-1

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.applications%20%3E%20(model)%20cors_headers%20%3E%20(schema)>)

<details>

<summary>

Decision = "allow"or "deny"or "non\_identity"or "bypass"

The action Access will take if a user matches this policy. Infrastructure application policies can only use the Allow action.

</summary>

One of the following:

"allow"

<a href="#">Link to this property</a>

"deny"

<a href="#">Link to this property</a>

"non\_identity"

<a href="#">Link to this property</a>

"bypass"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.applications%20%3E%20(model)%20decision%20%3E%20(schema)>)

<details>

<summary>

OIDCSaaSApp object {access\_token\_lifetime, allow\_pkce\_without\_client\_secret, app\_launcher\_url, 11 more }

</summary>

access\_token\_lifetime: optional string

The lifetime of the OIDC Access Token after creation. Valid units are m,h. Must be greater than or equal to 1m and less than or equal to 24h.

<a href="#">Link to this property</a>

allow\_pkce\_without\_client\_secret: optional boolean

If client secret should be required on the token endpoint when authorization\_code\_with\_pkce grant is used.

<a href="#">Link to this property</a>

app\_launcher\_url: optional string

The URL where this applications tile redirects users

<a href="#">Link to this property</a>

<details>

<summary>

auth\_type: optional "saml"or "oidc"

Identifier of the authentication protocol used for the saas app. Required for OIDC.

</summary>

One of the following:

"saml"

<a href="#">Link to this property</a>

"oidc"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

client\_id: optional string

The application client id

<a href="#">Link to this property</a>

client\_secret: optional string

The application client secret, only returned on POST request.

<a href="#">Link to this property</a>

<details>

<summary>

custom\_claims: optional array of object {name, required, scope, source }

</summary>

name: optional string

The name of the claim.

<a href="#">Link to this property</a>

required: optional boolean

If the claim is required when building an OIDC token.

<a href="#">Link to this property</a>

<details>

<summary>

scope: optional "groups"or "profile"or "email"or "openid"

The scope of the claim.

</summary>

One of the following:

"groups"

<a href="#">Link to this property</a>

"profile"

<a href="#">Link to this property</a>

"email"

<a href="#">Link to this property</a>

"openid"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {name, name\_by\_idp }

</summary>

name: optional string

The name of the IdP claim.

<a href="#">Link to this property</a>

name\_by\_idp: optional map\[string]

A mapping from IdP ID to claim name.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

grant\_types: optional array of "authorization\_code"or "authorization\_code\_with\_pkce"or "refresh\_tokens"or 2 more

The OIDC flows supported by this application

</summary>

One of the following:

"authorization\_code"

<a href="#">Link to this property</a>

"authorization\_code\_with\_pkce"

<a href="#">Link to this property</a>

"refresh\_tokens"

<a href="#">Link to this property</a>

"hybrid"

<a href="#">Link to this property</a>

"implicit"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

group\_filter\_regex: optional string

A regex to filter Cloudflare groups returned in ID token and userinfo endpoint

<a href="#">Link to this property</a>

<details>

<summary>

hybrid\_and\_implicit\_options: optional object {return\_access\_token\_from\_authorization\_endpoint, return\_id\_token\_from\_authorization\_endpoint }

</summary>

return\_access\_token\_from\_authorization\_endpoint: optional boolean

If an Access Token should be returned from the OIDC Authorization endpoint

<a href="#">Link to this property</a>

return\_id\_token\_from\_authorization\_endpoint: optional boolean

If an ID Token should be returned from the OIDC Authorization endpoint

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

public\_key: optional string

The Access public certificate that will be used to verify your identity.

<a href="#">Link to this property</a>

redirect\_uris: optional array of string

The permitted URL’s for Cloudflare to return Authorization codes and Access/ID tokens

<a href="#">Link to this property</a>

<details>

<summary>

refresh\_token\_options: optional object {lifetime }

</summary>

lifetime: optional string

How long a refresh token will be valid for after creation. Valid units are m,h,d. Must be longer than 1m.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

scopes: optional array of "openid"or "groups"or "email"or "profile"

Define the user information shared with access, “offline\_access” scope will be automatically enabled if refresh tokens are enabled

</summary>

One of the following:

"openid"

<a href="#">Link to this property</a>

"groups"

<a href="#">Link to this property</a>

"email"

<a href="#">Link to this property</a>

"profile"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.applications%20%3E%20(model)%20oidc_saas_app%20%3E%20(schema)>)

<details>

<summary>

SaaSAppNameIDFormat = "id"or "email"

The format of the name identifier sent to the SaaS application.

</summary>

One of the following:

"id"

<a href="#">Link to this property</a>

"email"

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.applications%20%3E%20(model)%20saas_app_name_id_format%20%3E%20(schema)>)

<details>

<summary>

SAMLSaaSApp object {auth\_type, consumer\_service\_url, custom\_attributes, 8 more }

</summary>

<details>

<summary>

auth\_type: optional "saml"or "oidc"

Optional identifier indicating the authentication protocol used for the saas app. Required for OIDC. Default if unset is “saml”

</summary>

One of the following:

"saml"

<a href="#">Link to this property</a>

"oidc"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

consumer\_service\_url: optional string

The service provider’s endpoint that is responsible for receiving and parsing a SAML assertion.

<a href="#">Link to this property</a>

<details>

<summary>

custom\_attributes: optional array of object {friendly\_name, name, name\_format, 2 more }

</summary>

friendly\_name: optional string

The SAML FriendlyName of the attribute.

<a href="#">Link to this property</a>

name: optional string

The name of the attribute.

<a href="#">Link to this property</a>

<details>

<summary>

name\_format: optional "urn:oasis:names:tc:SAML:2.0:attrname-format:unspecified"or "urn:oasis:names:tc:SAML:2.0:attrname-format:basic"or "urn:oasis:names:tc:SAML:2.0:attrname-format:uri"

A globally unique name for an identity or service provider.

</summary>

One of the following:

"urn:oasis:names:tc:SAML:2.0:attrname-format:unspecified"

<a href="#">Link to this property</a>

"urn:oasis:names:tc:SAML:2.0:attrname-format:basic"

<a href="#">Link to this property</a>

"urn:oasis:names:tc:SAML:2.0:attrname-format:uri"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

required: optional boolean

If the attribute is required when building a SAML assertion.

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {name, name\_by\_idp }

</summary>

name: optional string

The name of the IdP attribute.

<a href="#">Link to this property</a>

<details>

<summary>

name\_by\_idp: optional array of object {idp\_id, source\_name }

A mapping from IdP ID to attribute name.

</summary>

idp\_id: optional string

The UID of the IdP.

<a href="#">Link to this property</a>

source\_name: optional string

The name of the IdP provided attribute.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

default\_relay\_state: optional string

The URL that the user will be redirected to after a successful login for IDP initiated logins.

<a href="#">Link to this property</a>

idp\_entity\_id: optional string

The unique identifier for your SaaS application.

<a href="#">Link to this property</a>

name\_id\_format: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20saas_app_name_id_format%20%3E%20(schema)">SaaSAppNameIDFormat</a>

The format of the name identifier sent to the SaaS application.

<a href="#">Link to this property</a>

name\_id\_transform\_jsonata: optional string

A <a href="https://jsonata.org/">JSONata</a> expression that transforms an application’s user identities into a NameID value for its SAML assertion. This expression should evaluate to a singular string. The output of this expression can override the <code>name_id_format</code> setting.

<a href="#">Link to this property</a>

public\_key: optional string

The Access public certificate that will be used to verify your identity.

<a href="#">Link to this property</a>

saml\_attribute\_transform\_jsonata: optional string

A \[JSONata] (<a href="https://jsonata.org/">https://jsonata.org/</a>) expression that transforms an application’s user identities into attribute assertions in the SAML response. The expression can transform id, email, name, and groups values. It can also transform fields listed in the saml\_attributes or oidc\_fields of the identity provider used to authenticate. The output of this expression must be a JSON object.

<a href="#">Link to this property</a>

sp\_entity\_id: optional string

A globally unique name for an identity or service provider.

<a href="#">Link to this property</a>

sso\_endpoint: optional string

The endpoint where your SaaS application will send login requests.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.applications%20%3E%20(model)%20saml_saas_app%20%3E%20(schema)>)

<details>

<summary>

SCIMConfigAuthenticationHTTPBasic object {password, scheme, user }

Attributes for configuring HTTP Basic authentication scheme for SCIM provisioning to an application.

</summary>

password: string

Password used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "httpbasic"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

user: string

User name used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_http_basic%20%3E%20(schema)>)

<details>

<summary>

SCIMConfigAuthenticationOAuthBearerToken object {token, scheme }

Attributes for configuring OAuth Bearer Token authentication scheme for SCIM provisioning to an application.

</summary>

token: string

Token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scheme: "oauthbearertoken"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_oauth_bearer_token%20%3E%20(schema)>)

<details>

<summary>

SCIMConfigAuthenticationOauth2 object {authorization\_url, client\_id, client\_secret, 3 more }

Attributes for configuring OAuth 2 authentication scheme for SCIM provisioning to an application.

</summary>

authorization\_url: string

URL used to generate the auth code used during token generation.

<a href="#">Link to this property</a>

client\_id: string

Client ID used to authenticate when generating a token for authenticating with the remote SCIM service.

<a href="#">Link to this property</a>

client\_secret: string

Secret used to authenticate when generating a token for authenticating with the remove SCIM service.

<a href="#">Link to this property</a>

scheme: "oauth2"

The authentication scheme to use when making SCIM requests to this application.

<a href="#">Link to this property</a>

token\_url: string

URL used to generate the token used to authenticate with the remote SCIM service.

<a href="#">Link to this property</a>

scopes: optional array of string

The authorization scopes to request when generating the token used to authenticate with the remove SCIM service.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_authentication_oauth2%20%3E%20(schema)>)

<details>

<summary>

SCIMConfigMapping object {schema, enabled, filter, 3 more }

Transformations and filters applied to resources before they are provisioned in the remote SCIM service.

</summary>

schema: string

Which SCIM resource type this mapping applies to.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether or not this mapping is enabled.

<a href="#">Link to this property</a>

filter: optional string

A <a href="https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2.2">SCIM filter expression</a> that matches resources that should be provisioned to this application.

<a href="#">Link to this property</a>

<details>

<summary>

operations: optional object {create, delete, update }

Whether or not this mapping applies to creates, updates, or deletes.

</summary>

create: optional boolean

Whether or not this mapping applies to create (POST) operations.

<a href="#">Link to this property</a>

delete: optional boolean

Whether or not this mapping applies to DELETE operations.

<a href="#">Link to this property</a>

update: optional boolean

Whether or not this mapping applies to update (PATCH/PUT) operations.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

strictness: optional "strict"or "passthrough"

The level of adherence to outbound resource schemas when provisioning to this mapping. ‘Strict’ removes unknown values, while ‘passthrough’ passes unknown values to the target.

</summary>

One of the following:

"strict"

<a href="#">Link to this property</a>

"passthrough"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

transform\_jsonata: optional string

A <a href="https://jsonata.org/">JSONata</a> expression that transforms the resource before provisioning it in the application.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.applications%20%3E%20(model)%20scim_config_mapping%20%3E%20(schema)>)

SelfHostedDomains = string

A domain that Access will secure.

[Link to this property](#)%20zero_trust.access.applications%20%3E%20(model)%20self_hosted_domains%20%3E%20(schema)>)

<details>

<summary>

ApplicationListResponse = object {oauth\_configuration, type, user\_populations, 7 more } or object {domain, type, id, 31 more } or object {id, allowed\_idps, app\_launcher\_visible, 10 more } or 11 more

</summary>

One of the following:

<details>

<summary>

EndUserApplication object {oauth\_configuration, type, user\_populations, 7 more }

</summary>

<details>

<summary>

oauth\_configuration: object {dynamic\_client\_registration, enabled, grant }

**Beta:** Optional configuration for managing an OAuth authorization flow controlled by Access. When set, Access will act as the OAuth authorization server for this application. Only compatible with OAuth clients that support <a href="https://datatracker.ietf.org/doc/html/rfc8707">RFC 8707</a> (Resource Indicators for OAuth 2.0). This feature is currently in beta.

</summary>

<details>

<summary>

dynamic\_client\_registration: optional object {allow\_any\_on\_localhost, allow\_any\_on\_loopback, allowed\_uris, enabled }

Settings for OAuth dynamic client registration.

</summary>

allow\_any\_on\_localhost: optional boolean

Allows any client with redirect URIs on localhost.

<a href="#">Link to this property</a>

allow\_any\_on\_loopback: optional boolean

Allows any client with redirect URIs on 127.0.0.1.

<a href="#">Link to this property</a>

allowed\_uris: optional array of string

The URIs that are allowed as redirect URIs for dynamically registered clients. HTTP and HTTPS paths may end in <code>/*</code> to match all sub-paths. Custom-scheme URIs must be explicitly configured and match exactly.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether dynamic client registration is enabled.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

enabled: optional true

Managed OAuth is required for end user applications and cannot be disabled.

<a href="#">Link to this property</a>

<details>

<summary>

grant: optional object {access\_token\_lifetime, session\_duration }

Settings for OAuth grant behavior.

</summary>

access\_token\_lifetime: optional string

The lifetime of the access token. Must be in the format <code>300ms</code> or <code>2h45m</code>. Valid time units are ns, us (or µs), ms, s, m, h.

<a href="#">Link to this property</a>

session\_duration: optional string

The duration of the OAuth session. Must be in the format <code>300ms</code> or <code>2h45m</code>. Valid time units are ns, us (or µs), ms, s, m, h.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

type: "self\_hosted"or "end\_user"or "saas"or 12 more

The application type.

</summary>

One of the following:

"self\_hosted"

<a href="#">Link to this property</a>

"end\_user"

<a href="#">Link to this property</a>

"saas"

<a href="#">Link to this property</a>

"ssh"

<a href="#">Link to this property</a>

"vnc"

<a href="#">Link to this property</a>

"app\_launcher"

<a href="#">Link to this property</a>

"warp"

<a href="#">Link to this property</a>

"biso"

<a href="#">Link to this property</a>

"bookmark"

<a href="#">Link to this property</a>

"dash\_sso"

<a href="#">Link to this property</a>

"infrastructure"

<a href="#">Link to this property</a>

"rdp"

<a href="#">Link to this property</a>

"mcp"

<a href="#">Link to this property</a>

"mcp\_portal"

<a href="#">Link to this property</a>

"proxy\_endpoint"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

user\_populations: array of string

The single user population associated with this application.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

allowed\_idps: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20allowed_idps%20%3E%20(schema)">AllowedIdPs</a>

The identity providers your users can select when connecting to this application. Defaults to all IdPs configured in your account.

<a href="#">Link to this property</a>

aud: optional string

Audience tag.

maxLength64

<a href="#">Link to this property</a>

<details>

<summary>

destinations: optional array of object {uri, overrides, type } or object {type, worker\_id, overrides } or object {type, worker\_id, overrides } or 2 more

Public hostname and Workers destinations secured by Access.

</summary>

One of the following:

<details>

<summary>

AccessEndUserPublicDestination object {uri, overrides, type }

</summary>

uri: string

The public hostname and optional path to secure.

<a href="#">Link to this property</a>

<details>

<summary>

overrides: optional array of object {behavior, path\_pattern }

Rules that override how Access handles requests to this destination. Each rule can make a matching path public, bypassing Access authentication. Overrides are supported for public destinations and Worker destinations.

</summary>

behavior: "public"

The behavior to apply to matching requests.

<a href="#">Link to this property</a>

path\_pattern: string

The request path pattern to match. Wildcards (<code>*</code>) are supported, but each path segment may have at most one wildcard. Unlike the <code>uri</code> in public destinations, override path patterns do not implicitly cover subpaths; to do that, use a wildcard.

maxLength512

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

type: optional "public"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessEndUserWorkerDestination object {type, worker\_id, overrides }

</summary>

type: "worker"

<a href="#">Link to this property</a>

worker\_id: string

The ID of the Cloudflare Worker to secure.

<a href="#">Link to this property</a>

<details>

<summary>

overrides: optional array of object {behavior, path\_pattern }

Rules that override how Access handles requests to this destination. Each rule can make a matching path public, bypassing Access authentication. Overrides are supported for public destinations and Worker destinations.

</summary>

behavior: "public"

The behavior to apply to matching requests.

<a href="#">Link to this property</a>

path\_pattern: string

The request path pattern to match. Wildcards (<code>*</code>) are supported, but each path segment may have at most one wildcard. Unlike the <code>uri</code> in public destinations, override path patterns do not implicitly cover subpaths; to do that, use a wildcard.

maxLength512

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessEndUserPreviewWorkerDestination object {type, worker\_id, overrides }

</summary>

type: "preview\_worker"

<a href="#">Link to this property</a>

worker\_id: string

The ID of the Cloudflare Worker whose previews to secure.

<a href="#">Link to this property</a>

<details>

<summary>

overrides: optional array of object {behavior, path\_pattern }

Rules that override how Access handles requests to this destination. Each rule can make a matching path public, bypassing Access authentication. Overrides are supported for public destinations and Worker destinations.

</summary>

behavior: "public"

The behavior to apply to matching requests.

<a href="#">Link to this property</a>

path\_pattern: string

The request path pattern to match. Wildcards (<code>*</code>) are supported, but each path segment may have at most one wildcard. Unlike the <code>uri</code> in public destinations, override path patterns do not implicitly cover subpaths; to do that, use a wildcard.

maxLength512

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessEndUserAllWorkersDestination object {type, overrides }

</summary>

type: "all\_workers"

<a href="#">Link to this property</a>

<details>

<summary>

overrides: optional array of object {behavior, path\_pattern }

Rules that override how Access handles requests to this destination. Each rule can make a matching path public, bypassing Access authentication. Overrides are supported for public destinations and Worker destinations.

</summary>

behavior: "public"

The behavior to apply to matching requests.

<a href="#">Link to this property</a>

path\_pattern: string

The request path pattern to match. Wildcards (<code>*</code>) are supported, but each path segment may have at most one wildcard. Unlike the <code>uri</code> in public destinations, override path patterns do not implicitly cover subpaths; to do that, use a wildcard.

maxLength512

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessEndUserAllPreviewWorkersDestination object {type, overrides }

</summary>

type: "all\_preview\_workers"

<a href="#">Link to this property</a>

<details>

<summary>

overrides: optional array of object {behavior, path\_pattern }

Rules that override how Access handles requests to this destination. Each rule can make a matching path public, bypassing Access authentication. Overrides are supported for public destinations and Worker destinations.

</summary>

behavior: "public"

The behavior to apply to matching requests.

<a href="#">Link to this property</a>

path\_pattern: string

The request path pattern to match. Wildcards (<code>*</code>) are supported, but each path segment may have at most one wildcard. Unlike the <code>uri</code> in public destinations, override path patterns do not implicitly cover subpaths; to do that, use a wildcard.

maxLength512

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

domain: optional string

The primary hostname and path secured by Access. This domain will be displayed if the app is visible in the App Launcher.

<a href="#">Link to this property</a>

name: optional string

The name of the application.

<a href="#">Link to this property</a>

Deprecatedself\_hosted\_domains: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20self_hosted_domains%20%3E%20(schema)">SelfHostedDomains</a>

List of public domains that Access will secure. This field is deprecated in favor of <code>destinations</code> and will be supported until **November 21, 2025.** If <code>destinations</code> are provided, then <code>self_hosted_domains</code> will be ignored.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SelfHostedApplication object {domain, type, id, 31 more }

</summary>

domain: string

The primary hostname and path secured by Access. This domain will be displayed if the app is visible in the App Launcher.

<a href="#">Link to this property</a>

type: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20application_type%20%3E%20(schema)">ApplicationType</a>

The application type.

<a href="#">Link to this property</a>

id: optional string

UUID.

maxLength36

<a href="#">Link to this property</a>

allow\_authenticate\_via\_warp: optional boolean

When set to true, users can authenticate to this application using their WARP session. When set to false this application will always require direct IdP authentication. This setting always overrides the organization setting for WARP authentication.

<a href="#">Link to this property</a>

allow\_iframe: optional boolean

Enables loading application content in an iFrame.

<a href="#">Link to this property</a>

allowed\_idps: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20allowed_idps%20%3E%20(schema)">AllowedIdPs</a>

The identity providers your users can select when connecting to this application. Defaults to all IdPs configured in your account.

<a href="#">Link to this property</a>

app\_launcher\_visible: optional boolean

Displays the application in the App Launcher.

<a href="#">Link to this property</a>

aud: optional string

Audience tag.

maxLength64

<a href="#">Link to this property</a>

auto\_redirect\_to\_identity: optional boolean

When set to <code>true</code>, users skip the identity provider selection step during login. You must specify only one identity provider in allowed\_idps.

<a href="#">Link to this property</a>

cors\_headers: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20cors_headers%20%3E%20(schema)">CORSHeaders</a> { allow\_all\_headers, allow\_all\_methods, allow\_all\_origins, 5 more }

<a href="#">Link to this property</a>

custom\_deny\_message: optional string

The custom error message shown to a user when they are denied access to the application.

<a href="#">Link to this property</a>

custom\_deny\_url: optional string

The custom URL a user is redirected to when they are denied access to the application when failing identity-based rules.

<a href="#">Link to this property</a>

custom\_non\_identity\_deny\_url: optional string

The custom URL a user is redirected to when they are denied access to the application when failing non-identity rules.

<a href="#">Link to this property</a>

custom\_pages: optional array of string

The custom pages that will be displayed when applicable for this application

<a href="#">Link to this property</a>

<details>

<summary>

destinations: optional array of object {overrides, type, uri } or object {cidr, hostname, l4\_protocol, 3 more } or object {mcp\_server\_id, type } or 4 more

List of destinations secured by Access. This supersedes <code>self_hosted_domains</code> to allow for more flexibility in defining different types of domains. If <code>destinations</code> are provided, then <code>self_hosted_domains</code> will be ignored.

</summary>

One of the following:

<details>

<summary>

PublicDestination object {overrides, type, uri }

A public hostname that Access will secure. Public destinations support sub-domain and path. Wildcard ’\*’ can be used in the definition.

</summary>

<details>

<summary>

overrides: optional array of object {behavior, path\_pattern }

Rules that override how Access handles requests to this destination. Each rule can make a matching path public, bypassing Access authentication. Overrides are supported for public destinations and Worker destinations.

</summary>

behavior: "public"

The behavior to apply to matching requests.

<a href="#">Link to this property</a>

path\_pattern: string

The request path pattern to match. Wildcards (<code>*</code>) are supported, but each path segment may have at most one wildcard. Unlike the <code>uri</code> in public destinations, override path patterns do not implicitly cover subpaths; to do that, use a wildcard.

maxLength512

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

type: optional "public"

<a href="#">Link to this property</a>

uri: optional string

The URI of the destination. Public destinations’ URIs can include a domain and path with <a href="https://developers.cloudflare.com/cloudflare-one/policies/access/app-paths/">wildcards</a>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

PrivateDestination object {cidr, hostname, l4\_protocol, 3 more }

</summary>

cidr: optional string

The CIDR range of the destination. Single IPs will be computed as /32.

<a href="#">Link to this property</a>

hostname: optional string

The hostname of the destination. Matches a valid SNI served by an HTTPS origin.

<a href="#">Link to this property</a>

<details>

<summary>

l4\_protocol: optional "tcp"or "udp"

The L4 protocol of the destination. When omitted, both UDP and TCP traffic will match.

</summary>

One of the following:

"tcp"

<a href="#">Link to this property</a>

"udp"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

port\_range: optional string

The port range of the destination. Can be a single port or a range of ports. When omitted, all ports will match.

<a href="#">Link to this property</a>

type: optional "private"

<a href="#">Link to this property</a>

vnet\_id: optional string

The VNET ID to match the destination. When omitted, all VNETs will match.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ViaMcpServerPortalDestination object {mcp\_server\_id, type }

A MCP server id configured in ai-controls. Access will secure the MCP server if accessed through a MCP portal.

</summary>

mcp\_server\_id: optional string

The MCP server id configured in ai-controls.

<a href="#">Link to this property</a>

type: optional "via\_mcp\_server\_portal"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

WorkerDestination object {type, worker\_id, overrides }

A specific Cloudflare Worker that Access will secure. All requests routed to the specified Worker, including its preview deployments, will be protected. The <code>preview_worker</code> and <code>public</code> destination types takes precedence, so you can create separate applications to override the policies for the Worker’s previews or specific paths.

</summary>

type: "worker"

<a href="#">Link to this property</a>

worker\_id: string

The ID of the Cloudflare Worker to protect with Access.

<a href="#">Link to this property</a>

<details>

<summary>

overrides: optional array of object {behavior, path\_pattern }

Rules that override how Access handles requests to this destination. Each rule can make a matching path public, bypassing Access authentication. Overrides are supported for public destinations and Worker destinations.

</summary>

behavior: "public"

The behavior to apply to matching requests.

<a href="#">Link to this property</a>

path\_pattern: string

The request path pattern to match. Wildcards (<code>*</code>) are supported, but each path segment may have at most one wildcard. Unlike the <code>uri</code> in public destinations, override path patterns do not implicitly cover subpaths; to do that, use a wildcard.

maxLength512

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

PreviewWorkerDestination object {type, worker\_id, overrides }

A specific Cloudflare Worker whose preview deployments Access will secure. Only requests routed to the preview deployments of the specified Worker will be protected. The <code>public</code> destination type takes precedence, so you can create separate applications to override the policies for specific paths.

</summary>

type: "preview\_worker"

<a href="#">Link to this property</a>

worker\_id: string

The ID of the Cloudflare Worker whose preview deployments to protect with Access.

<a href="#">Link to this property</a>

<details>

<summary>

overrides: optional array of object {behavior, path\_pattern }

Rules that override how Access handles requests to this destination. Each rule can make a matching path public, bypassing Access authentication. Overrides are supported for public destinations and Worker destinations.

</summary>

behavior: "public"

The behavior to apply to matching requests.

<a href="#">Link to this property</a>

path\_pattern: string

The request path pattern to match. Wildcards (<code>*</code>) are supported, but each path segment may have at most one wildcard. Unlike the <code>uri</code> in public destinations, override path patterns do not implicitly cover subpaths; to do that, use a wildcard.

maxLength512

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AllWorkersDestination object {type, overrides }

Protects all Cloudflare Workers on the account with Access, including their preview deployments. At most one destination of this type can exist per account. The <code>worker</code>, <code>preview_worker</code>, <code>all_preview_workers</code>, and <code>public</code> destination types take precedence, so you can create separate applications to override the policies for specific Workers, their previews, or specific paths.

</summary>

type: "all\_workers"

<a href="#">Link to this property</a>

<details>

<summary>

overrides: optional array of object {behavior, path\_pattern }

Rules that override how Access handles requests to this destination. Each rule can make a matching path public, bypassing Access authentication. Overrides are supported for public destinations and Worker destinations.

</summary>

behavior: "public"

The behavior to apply to matching requests.

<a href="#">Link to this property</a>

path\_pattern: string

The request path pattern to match. Wildcards (<code>*</code>) are supported, but each path segment may have at most one wildcard. Unlike the <code>uri</code> in public destinations, override path patterns do not implicitly cover subpaths; to do that, use a wildcard.

maxLength512

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AllPreviewWorkersDestination object {type, overrides }

Protects the preview deployments of all Cloudflare Workers on the account with Access. At most one destination of this type can exist per account. The <code>worker</code>, <code>preview_worker</code>, and <code>public</code> destination types take precedence, so you can create separate applications to override the policies for specific Workers, their previews, or specific paths.

</summary>

type: "all\_preview\_workers"

<a href="#">Link to this property</a>

<details>

<summary>

overrides: optional array of object {behavior, path\_pattern }

Rules that override how Access handles requests to this destination. Each rule can make a matching path public, bypassing Access authentication. Overrides are supported for public destinations and Worker destinations.

</summary>

behavior: "public"

The behavior to apply to matching requests.

<a href="#">Link to this property</a>

path\_pattern: string

The request path pattern to match. Wildcards (<code>*</code>) are supported, but each path segment may have at most one wildcard. Unlike the <code>uri</code> in public destinations, override path patterns do not implicitly cover subpaths; to do that, use a wildcard.

maxLength512

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

eager\_redirect\_cookie\_setting: optional boolean

Preemptively sets the Access session cookie on every hostname in a multi-hostname self-hosted application during the initial redirect chain, rather than setting it lazily on first visit. Defaults to true. Set to false to disable the eager redirect cookie behavior.

<a href="#">Link to this property</a>

enable\_binding\_cookie: optional boolean

Enables the binding cookie, which increases security against compromised authorization tokens and CSRF attacks.

<a href="#">Link to this property</a>

http\_only\_cookie\_attribute: optional boolean

Enables the HttpOnly cookie attribute, which increases security against XSS attacks.

<a href="#">Link to this property</a>

logo\_url: optional string

The image URL for the logo shown in the App Launcher dashboard.

<a href="#">Link to this property</a>

<details>

<summary>

mfa\_config: optional object {allowed\_authenticators, mfa\_disabled, session\_duration }

Configures multi-factor authentication (MFA) settings.

</summary>

<details>

<summary>

allowed\_authenticators: optional array of "totp"or "biometrics"or "security\_key"

Lists the MFA methods that users can authenticate with.

</summary>

One of the following:

"totp"

<a href="#">Link to this property</a>

"biometrics"

<a href="#">Link to this property</a>

"security\_key"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

mfa\_disabled: optional boolean

Indicates whether to disable MFA for this resource. This option is available at the application and policy level.

<a href="#">Link to this property</a>

session\_duration: optional string

Defines the duration of an MFA session. Must be in minutes (m) or hours (h). Minimum: 0m. Maximum: 720h (30 days). Examples:<code>5m</code> or <code>24h</code>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: optional string

The name of the application.

<a href="#">Link to this property</a>

<details>

<summary>

oauth\_configuration: optional object {dynamic\_client\_registration, enabled, grant }

**Beta:** Optional configuration for managing an OAuth authorization flow controlled by Access. When set, Access will act as the OAuth authorization server for this application. Only compatible with OAuth clients that support <a href="https://datatracker.ietf.org/doc/html/rfc8707">RFC 8707</a> (Resource Indicators for OAuth 2.0). This feature is currently in beta.

</summary>

<details>

<summary>

dynamic\_client\_registration: optional object {allow\_any\_on\_localhost, allow\_any\_on\_loopback, allowed\_uris, enabled }

Settings for OAuth dynamic client registration.

</summary>

allow\_any\_on\_localhost: optional boolean

Allows any client with redirect URIs on localhost.

<a href="#">Link to this property</a>

allow\_any\_on\_loopback: optional boolean

Allows any client with redirect URIs on 127.0.0.1.

<a href="#">Link to this property</a>

allowed\_uris: optional array of string

The URIs that are allowed as redirect URIs for dynamically registered clients. HTTP and HTTPS paths may end in <code>/*</code> to match all sub-paths. Custom-scheme URIs must be explicitly configured and match exactly.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether dynamic client registration is enabled.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the OAuth configuration is enabled for this application. When set to <code>false</code>, Access will not handle OAuth for this application. Defaults to <code>true</code> if omitted.

<a href="#">Link to this property</a>

<details>

<summary>

grant: optional object {access\_token\_lifetime, session\_duration }

Settings for OAuth grant behavior.

</summary>

access\_token\_lifetime: optional string

The lifetime of the access token. Must be in the format <code>300ms</code> or <code>2h45m</code>. Valid time units are ns, us (or µs), ms, s, m, h.

<a href="#">Link to this property</a>

session\_duration: optional string

The duration of the OAuth session. Must be in the format <code>300ms</code> or <code>2h45m</code>. Valid time units are ns, us (or µs), ms, s, m, h.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

options\_preflight\_bypass: optional boolean

Allows options preflight requests to bypass Access authentication and go directly to the origin. Cannot turn on if cors\_headers is set.

<a href="#">Link to this property</a>

path\_cookie\_attribute: optional boolean

Enables cookie paths to scope an application’s JWT to the application path. If disabled, the JWT will scope to the hostname by default

<a href="#">Link to this property</a>

<details>

<summary>

policies: optional array of object {id, account\_id, approval\_groups, 15 more }

</summary>

id: optional string

The UUID of the policy

maxLength36

<a href="#">Link to this property</a>

account\_id: optional string

Identifier.

maxLength32

<a href="#">Link to this property</a>

<details>

<summary>

approval\_groups: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.policies%20%3E%20(model)%20approval_group%20%3E%20(schema)">ApprovalGroup</a> { approvals\_needed, email\_addresses, email\_list\_uuid }

Administrators who can approve a temporary authentication request.

</summary>

approvals\_needed: number

The number of approvals needed to obtain access.

minimum0

<a href="#">Link to this property</a>

email\_addresses: optional array of string

A list of emails that can approve the access request.

<a href="#">Link to this property</a>

email\_list\_uuid: optional string

The UUID of an re-usable email list.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

approval\_required: optional boolean

Requires the user to request access from an administrator at the start of each session.

<a href="#">Link to this property</a>

<details>

<summary>

connection\_rules: optional object {rdp }

The rules that define how users may connect to targets secured by your application.

</summary>

<details>

<summary>

rdp: optional object {allowed\_clipboard\_local\_to\_remote\_formats, allowed\_clipboard\_remote\_to\_local\_formats }

The RDP-specific rules that define clipboard behavior for RDP connections.

</summary>

<details>

<summary>

allowed\_clipboard\_local\_to\_remote\_formats: optional array of "text"or "file"

Clipboard formats allowed when copying from local machine to remote RDP session.

</summary>

One of the following:

"text"

<a href="#">Link to this property</a>

"file"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

allowed\_clipboard\_remote\_to\_local\_formats: optional array of "text"or "file"

Clipboard formats allowed when copying from remote RDP session to local machine.

</summary>

One of the following:

"text"

<a href="#">Link to this property</a>

"file"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

decision: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications%20%3E%20(model)%20decision%20%3E%20(schema)">Decision</a>

The action Access will take if a user matches this policy. Infrastructure application policies can only use the Allow action.

<a href="#">Link to this property</a>

<details>

<summary>

exclude: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications.policies%20%3E%20(model)%20access_rule%20%3E%20(schema)">AccessRule</a>

Rules evaluated with a NOT logical operator. To match the policy, a user cannot meet any of the Exclude rules.

</summary>

One of the following:

<details>

<summary>

GroupRule object {group }

Matches an Access group.

</summary>

<details>

<summary>

group: object {id }

</summary>

id: string

The ID of a previously created Access group.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AnyValidServiceTokenRule object {any\_valid\_service\_token }

Matches any valid Access Service Token

</summary>

any\_valid\_service\_token: object {}

An empty object which matches on all service tokens.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessAuthContextRule object {auth\_context }

Matches an Azure Authentication Context. Requires an Azure identity provider.

</summary>

<details>

<summary>

auth\_context: object {id, ac\_id, identity\_provider\_id }

</summary>

id: string

The ID of an Authentication context.

<a href="#">Link to this property</a>

ac\_id: string

The ACID of an Authentication context.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your Azure identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AuthenticationMethodRule object {auth\_method }

Enforce different MFA options

</summary>

<details>

<summary>

auth\_method: object {auth\_method }

</summary>

auth\_method: string

The type of authentication method <a href="https://datatracker.ietf.org/doc/html/rfc8176#section-2">https://datatracker.ietf.org/doc/html/rfc8176#section-2</a>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AzureGroupRule object {azureAD }

Matches an Azure group. Requires an Azure identity provider.

</summary>

<details>

<summary>

azureAD: object {id, identity\_provider\_id }

</summary>

id: string

The ID of an Azure group.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your Azure identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CertificateRule object {certificate }

Matches any valid client certificate.

</summary>

certificate: object {}

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessCommonNameRule object {common\_name }

Matches a specific common name.

</summary>

<details>

<summary>

common\_name: object {common\_name }

</summary>

common\_name: string

The common name to match.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CountryRule object {geo }

Matches a specific country

</summary>

<details>

<summary>

geo: object {country\_code }

</summary>

country\_code: string

The country code that should be matched.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessDevicePostureRule object {device\_posture }

Enforces a device posture rule has run successfully

</summary>

<details>

<summary>

device\_posture: object {integration\_uid, account\_id }

</summary>

integration\_uid: string

The ID of a device posture integration.

<a href="#">Link to this property</a>

account\_id: optional string

The ID of the account that owns the device posture integration.

maxLength32

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

DomainRule object {email\_domain }

Match an entire email domain.

</summary>

<details>

<summary>

email\_domain: object {domain }

</summary>

domain: string

The email domain to match.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

EmailListRule object {email\_list }

Matches an email address from a list.

</summary>

<details>

<summary>

email\_list: object {id }

</summary>

id: string

The ID of a previously created email list.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

EmailRule object {email }

Matches a specific email.

</summary>

<details>

<summary>

email: object {email }

</summary>

email: string

The email of the user.

formatemail

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

EveryoneRule object {everyone }

Matches everyone.

</summary>

everyone: object {}

An empty object which matches on all users.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ExternalEvaluationRule object {external\_evaluation }

Create Allow or Block policies which evaluate the user based on custom criteria.

</summary>

<details>

<summary>

external\_evaluation: object {evaluate\_url, keys\_url }

</summary>

evaluate\_url: string

The API endpoint containing your business logic.

<a href="#">Link to this property</a>

keys\_url: string

The API endpoint containing the key that Access uses to verify that the response came from your API.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

GitHubOrganizationRule object {"github-organization" }

Matches a Github organization. Requires a Github identity provider.

</summary>

<details>

<summary>

"github-organization": object {identity\_provider\_id, name, team }

</summary>

identity\_provider\_id: string

The ID of your Github identity provider.

<a href="#">Link to this property</a>

name: string

The name of the organization.

<a href="#">Link to this property</a>

team: optional string

The name of the team

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

GSuiteGroupRule object {gsuite }

Matches a group in Google Workspace. Requires a Google Workspace identity provider.

</summary>

<details>

<summary>

gsuite: object {email, identity\_provider\_id }

</summary>

email: string

The email of the Google Workspace group.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your Google Workspace identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessLoginMethodRule object {login\_method }

Matches a specific identity provider id.

</summary>

<details>

<summary>

login\_method: object {id }

</summary>

id: string

The ID of an identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

IPListRule object {ip\_list }

Matches an IP address from a list.

</summary>

<details>

<summary>

ip\_list: object {id }

</summary>

id: string

The ID of a previously created IP list.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

IPRule object {ip }

Matches an IP address block.

</summary>

<details>

<summary>

ip: object {ip }

</summary>

ip: string

An IPv4 or IPv6 CIDR block.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

OktaGroupRule object {okta }

Matches an Okta group. Requires an Okta identity provider.

</summary>

<details>

<summary>

okta: object {identity\_provider\_id, name }

</summary>

identity\_provider\_id: string

The ID of your Okta identity provider.

<a href="#">Link to this property</a>

name: string

The name of the Okta group.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SAMLGroupRule object {saml }

Matches a SAML group. Requires a SAML identity provider.

</summary>

<details>

<summary>

saml: object {attribute\_name, attribute\_value, identity\_provider\_id }

</summary>

attribute\_name: string

The name of the SAML attribute.

<a href="#">Link to this property</a>

attribute\_value: string

The SAML attribute value to look for.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your SAML identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessOIDCClaimRule object {oidc }

Matches an OIDC claim. Requires an OIDC identity provider.

</summary>

<details>

<summary>

oidc: object {claim\_name, claim\_value, identity\_provider\_id }

</summary>

claim\_name: string

The name of the OIDC claim.

<a href="#">Link to this property</a>

claim\_value: string

The OIDC claim value to look for.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your OIDC identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ServiceTokenRule object {service\_token }

Matches a specific Access Service Token

</summary>

<details>

<summary>

service\_token: object {token\_id }

</summary>

token\_id: string

The ID of a Service Token.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessLinkedAppTokenRule object {linked\_app\_token }

Matches OAuth 2.0 access tokens issued by the specified Access OIDC SaaS application. Only compatible with non\_identity and bypass decisions.

</summary>

<details>

<summary>

linked\_app\_token: object {app\_uid }

</summary>

app\_uid: string

The ID of an Access OIDC SaaS application

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessUserRiskScoreRule object {user\_risk\_score }

Matches a user’s risk score.

</summary>

<details>

<summary>

user\_risk\_score: object {user\_risk\_score }

</summary>

<details>

<summary>

user\_risk\_score: array of "low"or "medium"or "high"or "unscored"

A list of risk score levels to match. Values can be low, medium, high, or unscored.

</summary>

One of the following:

"low"

<a href="#">Link to this property</a>

"medium"

<a href="#">Link to this property</a>

"high"

<a href="#">Link to this property</a>

"unscored"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessCloudflareAccountMemberRule object {cloudflare\_account\_member }

Matches users who are members of a specific Cloudflare account. Requires a Cloudflare identity provider.

</summary>

<details>

<summary>

cloudflare\_account\_member: object {account\_id }

</summary>

account\_id: optional string

Identifier.

maxLength32

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

include: optional array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.applications.policies%20%3E%20(model)%20access_rule%20%3E%20(schema)">AccessRule</a>

Rules evaluated with an OR logical operator. A user needs to meet only one of the Include rules.

</summary>

One of the following:

<details>

<summary>

GroupRule object {group }

Matches an Access group.

</summary>

<details>

<summary>

group: object {id }

</summary>

id: string

The ID of a previously created Access group.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AnyValidServiceTokenRule object {any\_valid\_service\_token }

Matches any valid Access Service Token

</summary>

any\_valid\_service\_token: object {}

An empty object which matches on all service tokens.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessAuthContextRule object {auth\_context }

Matches an Azure Authentication Context. Requires an Azure identity provider.

</summary>

<details>

<summary>

auth\_context: object {id, ac\_id, identity\_provider\_id }

</summary>

id: string

The ID of an Authentication context.

<a href="#">Link to this property</a>

ac\_id: string

The ACID of an Authentication context.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your Azure identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AuthenticationMethodRule object {auth\_method }

Enforce different MFA options

</summary>

<details>

<summary>

auth\_method: object {auth\_method }

</summary>

auth\_method: string

The type of authentication method <a href="https://datatracker.ietf.org/doc/html/rfc8176#section-2">https://datatracker.ietf.org/doc/html/rfc8176#section-2</a>.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AzureGroupRule object {azureAD }

Matches an Azure group. Requires an Azure identity provider.

</summary>

<details>

<summary>

azureAD: object {id, identity\_provider\_id }

</summary>

id: string

The ID of an Azure group.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your Azure identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CertificateRule object {certificate }

Matches any valid client certificate.

</summary>

certificate: object {}

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessCommonNameRule object {common\_name }

Matches a specific common name.

</summary>

<details>

<summary>

common\_name: object {common\_name }

</summary>

common\_name: string

The common name to match.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

CountryRule object {geo }

Matches a specific country

</summary>

<details>

<summary>

geo: object {country\_code }

</summary>

country\_code: string

The country code that should be matched.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessDevicePostureRule object {device\_posture }

Enforces a device posture rule has run successfully

</summary>

<details>

<summary>

device\_posture: object {integration\_uid, account\_id }

</summary>

integration\_uid: string

The ID of a device posture integration.

<a href="#">Link to this property</a>

account\_id: optional string

The ID of the account that owns the device posture integration.

maxLength32

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

DomainRule object {email\_domain }

Match an entire email domain.

</summary>

<details>

<summary>

email\_domain: object {domain }

</summary>

domain: string

The email domain to match.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

EmailListRule object {email\_list }

Matches an email address from a list.

</summary>

<details>

<summary>

email\_list: object {id }

</summary>

id: string

The ID of a previously created email list.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

EmailRule object {email }

Matches a specific email.

</summary>

<details>

<summary>

email: object {email }

</summary>

email: string

The email of the user.

formatemail

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

EveryoneRule object {everyone }

Matches everyone.

</summary>

everyone: object {}

An empty object which matches on all users.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ExternalEvaluationRule object {external\_evaluation }

Create Allow or Block policies which evaluate the user based on custom criteria.

</summary>

<details>

<summary>

external\_evaluation: object {evaluate\_url, keys\_url }

</summary>

evaluate\_url: string

The API endpoint containing your business logic.

<a href="#">Link to this property</a>

keys\_url: string

The API endpoint containing the key that Access uses to verify that the response came from your API.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

GitHubOrganizationRule object {"github-organization" }

Matches a Github organization. Requires a Github identity provider.

</summary>

<details>

<summary>

"github-organization": object {identity\_provider\_id, name, team }

</summary>

identity\_provider\_id: string

The ID of your Github identity provider.

<a href="#">Link to this property</a>

name: string

The name of the organization.

<a href="#">Link to this property</a>

team: optional string

The name of the team

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

GSuiteGroupRule object {gsuite }

Matches a group in Google Workspace. Requires a Google Workspace identity provider.

</summary>

<details>

<summary>

gsuite: object {email, identity\_provider\_id }

</summary>

email: string

The email of the Google Workspace group.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your Google Workspace identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessLoginMethodRule object {login\_method }

Matches a specific identity provider id.

</summary>

<details>

<summary>

login\_method: object {id }

</summary>

id: string

The ID of an identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

IPListRule object {ip\_list }

Matches an IP address from a list.

</summary>

<details>

<summary>

ip\_list: object {id }

</summary>

id: string

The ID of a previously created IP list.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

IPRule object {ip }

Matches an IP address block.

</summary>

<details>

<summary>

ip: object {ip }

</summary>

ip: string

An IPv4 or IPv6 CIDR block.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

OktaGroupRule object {okta }

Matches an Okta group. Requires an Okta identity provider.

</summary>

<details>

<summary>

okta: object {identity\_provider\_id, name }

</summary>

identity\_provider\_id: string

The ID of your Okta identity provider.

<a href="#">Link to this property</a>

name: string

The name of the Okta group.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

SAMLGroupRule object {saml }

Matches a SAML group. Requires a SAML identity provider.

</summary>

<details>

<summary>

saml: object {attribute\_name, attribute\_value, identity\_provider\_id }

</summary>

attribute\_name: string

The name of the SAML attribute.

<a href="#">Link to this property</a>

attribute\_value: string

The SAML attribute value to look for.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your SAML identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessOIDCClaimRule object {oidc }

Matches an OIDC claim. Requires an OIDC identity provider.

</summary>

<details>

<summary>

oidc: object {claim\_name, claim\_value, identity\_provider\_id }

</summary>

claim\_name: string

The name of the OIDC claim.

<a href="#">Link to this property</a>

claim\_value: string

The OIDC claim value to look for.

<a href="#">Link to this property</a>

identity\_provider\_id: string

The ID of your OIDC identity provider.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

ServiceTokenRule object {service\_token }

Matches a specific Access Service Token

</summary>

<details>

<summary>

service\_token: object {token\_id }

</summary>

token\_id: string

The ID of a Service Token.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessLinkedAppTokenRule object {linked\_app\_token }

Matches OAuth 2.0 access tokens issued by the specified Access OIDC SaaS application. Only compatible with non\_identity and bypass decisions.

</summary>

<details>

<summary>

linked\_app\_token: object {app\_uid }

</summary>

app\_uid: string

The ID of an Access OIDC SaaS application

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

AccessUserRiskScoreRule object {user\_risk\_score }

Matches a user’s risk score.

</summary>

<details>

<summary>

user\_risk\_score: object {user\_risk\_score }

</summary>

<details>

<summary>

</summary>

</details>

</details>

</details>

</details>

</details>

</details>

</details>

<!-- Cloudflare Markdown for Agents: incomplete conversion; source HTML truncated at the conversion size limit -->
