---
title: Update a service token
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Access](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access)

[Service Tokens](https://developers.cloudflare.com/api/resources/zero_trust/subresources/access/subresources/service_tokens)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Update a service token

PUT/{accounts\_or\_zones}/{account\_or\_zone\_id}/access/service\_tokens/{service\_token\_id}

Updates a configured service token.

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

##### Accepted Permissions (at least one required)

`Access: Service Tokens Write`

##### P ath ParametersExpand Collapse

service\_token\_id: string

UUID.

maxLength36

[Link to this property](#)%20zero_trust.access.service_tokens%20%3E%20(method)%20update%20%3E%20(params)%20default%20%3E%20(param)%20service_token_id%20%3E%20(schema)>)

account\_id: optional string

The Account ID to use for this endpoint. Mutually exclusive with the Zone ID.

[Link to this property](#)%20zero_trust.access.service_tokens%20%3E%20(method)%20update%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

zone\_id: optional string

The Zone ID to use for this endpoint. Mutually exclusive with the Account ID.

[Link to this property](#)%20zero_trust.access.service_tokens%20%3E%20(method)%20update%20%3E%20(params)%20default%20%3E%20(param)%20zone_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

client\_secret\_version: optional number

A version number identifying the current `client_secret` associated with the service token. Incrementing it triggers a rotation; the previous secret will still be accepted until the time indicated by `previous_client_secret_expires_at`. If the service token was reported as leaked, `previous_client_secret_expires_at` is not required, may not be in the future, and the previous secret is discarded immediately.

[Link to this property](#)%20zero_trust.access.service_tokens%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20client_secret_version%20%3E%20(schema)>)

duration: optional string

The duration for how long the service token will be valid. Must be in the format `300ms` or `2h45m`, or the special value `forever` for non-expiring tokens. Valid time units are: ns, us (or µs), ms, s, m, h. The default is 1 year in hours (8760h).

[Link to this property](#)%20zero_trust.access.service_tokens%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20duration%20%3E%20(schema)>)

enabled: optional boolean

Whether the service token is enabled. A disabled service token cannot be used to authenticate; both its current and previous `client_secret` stop being accepted, but the token itself is preserved and can be re-enabled. A service token reported as leaked is disabled automatically and cannot be re-enabled until its secret is rotated; attempting to do so returns a 409. Defaults to enabled when omitted on create.

[Link to this property](#)%20zero_trust.access.service_tokens%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20enabled%20%3E%20(schema)>)

name: optional string

The name of the service token.

[Link to this property](#)%20zero_trust.access.service_tokens%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20name%20%3E%20(schema)>)

previous\_client\_secret\_expires\_at: optional string

The expiration of the previous `client_secret`. This can be modified at any point after a rotation. For example, you may extend it further into the future if you need more time to update services with the new secret; or move it into the past to immediately invalidate the previous token in case of compromise. Rotating a service token that was reported as leaked discards the previous secret entirely, so no grace period can be set.

formatdate-time

[Link to this property](#)%20zero_trust.access.service_tokens%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20previous_client_secret_expires_at%20%3E%20(schema)>)

tags: optional map\[string]

Tags associated with the service token, as key-value pairs. On update, replaces all existing tags.

[Link to this property](#)%20zero_trust.access.service_tokens%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20tags%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {code, message, documentation\_url, source }

</summary>

code: number

minimum1000

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

documentation\_url: optional string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.service_tokens%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {code, message, documentation\_url, source }

</summary>

code: number

minimum1000

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

documentation\_url: optional string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.service_tokens%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: true

Whether the API call was successful.

[Link to this property](#)%20zero_trust.access.service_tokens%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.access.service_tokens%20%3E%20(model)%20service_token%20%3E%20(schema)">ServiceToken</a> { id, client\_id, duration, 7 more }

</summary>

id: optional string

The ID of the service token.

maxLength36

<a href="#">Link to this property</a>

client\_id: optional string

The Client ID for the service token. Access will check for this value in the <code>CF-Access-Client-ID</code> request header.

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

tags: optional map\[string]

Tags associated with the service token, as key-value pairs. On update, replaces all existing tags.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.access.service_tokens%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

### Update a service token

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/$ACCOUNTS_OR_ZONES/$ACCOUNT_OR_ZONE_ID/access/service_tokens/$SERVICE_TOKEN_ID \
    -X PUT \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "duration": "60m",
          "name": "CI/CD token",
          "previous_client_secret_expires_at": "2014-01-01T05:20:00.12345Z",
          "tags": {
            "environment": "production"
          }
        }'
```

200 example

```
{
  "errors": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "success": true,
  "result": {
    "id": "f174e90a-fafe-4643-bbbc-4a0ed4fc8415",
    "client_id": "88bf3b6d86161464f6509f7219099e57.access.example.com",
    "created_at": "2014-01-01T05:20:00.12345Z",
    "duration": "60m",
    "enabled": true,
    "expires_at": "2014-01-01T05:20:00.12345Z",
    "last_seen_at": "2014-01-01T05:20:00.12345Z",
    "leak_report_url": "https://github.com/example/repo/blob/main/config.yaml",
    "leak_reported_at": "2014-01-01T05:20:00.12345Z",
    "leak_reporter": "github",
    "name": "CI/CD token",
    "tags": {
      "environment": "production"
    },
    "updated_at": "2014-01-01T05:20:00.12345Z"
  }
}
```

##### Returns Examples

200 example

```
{
  "errors": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    {
      "code": 1000,
      "message": "message",
      "documentation_url": "documentation_url",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "success": true,
  "result": {
    "id": "f174e90a-fafe-4643-bbbc-4a0ed4fc8415",
    "client_id": "88bf3b6d86161464f6509f7219099e57.access.example.com",
    "created_at": "2014-01-01T05:20:00.12345Z",
    "duration": "60m",
    "enabled": true,
    "expires_at": "2014-01-01T05:20:00.12345Z",
    "last_seen_at": "2014-01-01T05:20:00.12345Z",
    "leak_report_url": "https://github.com/example/repo/blob/main/config.yaml",
    "leak_reported_at": "2014-01-01T05:20:00.12345Z",
    "leak_reporter": "github",
    "name": "CI/CD token",
    "tags": {
      "environment": "production"
    },
    "updated_at": "2014-01-01T05:20:00.12345Z"
  }
}
```