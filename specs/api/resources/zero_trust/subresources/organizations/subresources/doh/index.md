---
title: DOH
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Organizations](https://developers.cloudflare.com/api/resources/zero_trust/subresources/organizations)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# DOH

##### [Get your Zero Trust organization DoH settings](https://developers.cloudflare.com/api/resources/zero_trust/subresources/organizations/subresources/doh/methods/get)

GET/accounts/{account\_id}/access/organizations/doh

##### [Update your Zero Trust organization DoH settings](https://developers.cloudflare.com/api/resources/zero_trust/subresources/organizations/subresources/doh/methods/update)

PUT/accounts/{account\_id}/access/organizations/doh

##### ModelsExpand Collapse

<details>

<summary>

DOHGetResponse object {id, client\_id, doh\_jwt\_duration, 7 more }

</summary>

id: optional string

The ID of the service token.

maxLength36

<a href="#">Link to this property</a>

client\_id: optional string

The Client ID for the service token. Access will check for this value in the <code>CF-Access-Client-ID</code> request header.

<a href="#">Link to this property</a>

doh\_jwt\_duration: optional string

The duration the DoH JWT is valid for. Must be in the format <code>300ms</code> or <code>2h45m</code>. Valid time units are: ns, us (or µs), ms, s, m, h. Note that the maximum duration for this setting is the same as the key rotation period on the account.

<a href="#">Link to this property</a>

duration: optional string

The duration for how long the service token will be valid. Must be in the format <code>300ms</code> or <code>2h45m</code>, or the special value <code>forever</code> for non-expiring tokens. Valid time units are: ns, us (or µs), ms, s, m, h. The default is 1 year in hours (8760h).

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the service token is enabled. A disabled service token cannot be used to authenticate; both its current and previous <code>client_secret</code> stop being accepted, but the token itself is preserved and can be re-enabled. A service token reported as leaked is disabled automatically and cannot be re-enabled until its secret is rotated; attempting to do so returns a 409. Defaults to enabled when omitted on create.

<a href="#">Link to this property</a>

expires\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

leak\_report\_url: optional string

Where the leaked <code>client_secret</code> was found, if provided by the reporter. Omitted if the token has not been reported as leaked.

formaturi

<a href="#">Link to this property</a>

leak\_reported\_at: optional string

When a secret scanning partner reported this service token’s <code>client_secret</code> as leaked. A leaked service token is disabled and must be rotated before it can be re-enabled. Cleared once the secret is rotated. Omitted if the token has not been reported as leaked.

formatdate-time

<a href="#">Link to this property</a>

leak\_reporter: optional string

The secret scanning partner that reported the leak. Omitted if the token has not been reported as leaked.

<a href="#">Link to this property</a>

name: optional string

The name of the service token.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.organizations.doh%20%3E%20(model)%20doh_get_response%20%3E%20(schema)>)

<details>

<summary>

DOHUpdateResponse object {id, client\_id, doh\_jwt\_duration, 7 more }

</summary>

id: optional string

The ID of the service token.

maxLength36

<a href="#">Link to this property</a>

client\_id: optional string

The Client ID for the service token. Access will check for this value in the <code>CF-Access-Client-ID</code> request header.

<a href="#">Link to this property</a>

doh\_jwt\_duration: optional string

The duration the DoH JWT is valid for. Must be in the format <code>300ms</code> or <code>2h45m</code>. Valid time units are: ns, us (or µs), ms, s, m, h. Note that the maximum duration for this setting is the same as the key rotation period on the account. Default expiration is 24h

<a href="#">Link to this property</a>

duration: optional string

The duration for how long the service token will be valid. Must be in the format <code>300ms</code> or <code>2h45m</code>, or the special value <code>forever</code> for non-expiring tokens. Valid time units are: ns, us (or µs), ms, s, m, h. The default is 1 year in hours (8760h).

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the service token is enabled. A disabled service token cannot be used to authenticate; both its current and previous <code>client_secret</code> stop being accepted, but the token itself is preserved and can be re-enabled. A service token reported as leaked is disabled automatically and cannot be re-enabled until its secret is rotated; attempting to do so returns a 409. Defaults to enabled when omitted on create.

<a href="#">Link to this property</a>

expires\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

leak\_report\_url: optional string

Where the leaked <code>client_secret</code> was found, if provided by the reporter. Omitted if the token has not been reported as leaked.

formaturi

<a href="#">Link to this property</a>

leak\_reported\_at: optional string

When a secret scanning partner reported this service token’s <code>client_secret</code> as leaked. A leaked service token is disabled and must be rotated before it can be re-enabled. Cleared once the secret is rotated. Omitted if the token has not been reported as leaked.

formatdate-time

<a href="#">Link to this property</a>

leak\_reporter: optional string

The secret scanning partner that reported the leak. Omitted if the token has not been reported as leaked.

<a href="#">Link to this property</a>

name: optional string

The name of the service token.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.organizations.doh%20%3E%20(model)%20doh_update_response%20%3E%20(schema)>)