---
title: Replace Zero Trust organization trust settings
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Organizations](https://developers.cloudflare.com/api/resources/zero_trust/subresources/organizations)

[Trust Settings](https://developers.cloudflare.com/api/resources/zero_trust/subresources/organizations/subresources/trust_settings)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Replace Zero Trust organization trust settings

PUT/accounts/{account\_id}/access/organizations/trust\_settings

Replaces the trust settings for your Zero Trust organization.

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

`Access: Organizations, Identity Providers, and Groups Write`

##### P ath ParametersExpand Collapse

account\_id: string

Identifier.

maxLength32

[Link to this property](#)%20zero_trust.organizations.trust_settings%20%3E%20(method)%20replace%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

grant\_trust\_to\_all\_accounts\_in\_org: boolean

Whether all accounts in the organization are trusted to use this account’s cross-account Access resources.

[Link to this property](#)%20zero_trust.organizations.trust_settings%20%3E%20(method)%20replace%20%3E%20(params)%200%20%3E%20(param)%20grant_trust_to_all_accounts_in_org%20%3E%20(schema)>)

trusting\_accounts: optional array of string

Explicit account IDs trusted to use this account’s cross-account Access resources. At most 100 unique valid account IDs are accepted. Omitted from responses when empty.

[Link to this property](#)%20zero_trust.organizations.trust_settings%20%3E%20(method)%20replace%20%3E%20(params)%200%20%3E%20(param)%20trusting_accounts%20%3E%20(schema)>)

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

[Link to this property](#)%20zero_trust.organizations.trust_settings%20%3E%20(method)%20replace%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20zero_trust.organizations.trust_settings%20%3E%20(method)%20replace%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: true

Whether the API call was successful.

[Link to this property](#)%20zero_trust.organizations.trust_settings%20%3E%20(method)%20replace%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional object {grant\_trust\_to\_all\_accounts\_in\_org, trusting\_accounts }

</summary>

grant\_trust\_to\_all\_accounts\_in\_org: boolean

Whether all accounts in the organization are trusted to use this account’s cross-account Access resources.

<a href="#">Link to this property</a>

trusting\_accounts: optional array of string

Explicit account IDs trusted to use this account’s cross-account Access resources. At most 100 unique valid account IDs are accepted. Omitted from responses when empty.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.organizations.trust_settings%20%3E%20(method)%20replace%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

### Replace Zero Trust organization trust settings

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/access/organizations/trust_settings \
    -X PUT \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "grant_trust_to_all_accounts_in_org": false,
          "trusting_accounts": [
            "023e105f4ecef8ad9ca31a8372d0c353"
          ]
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
    "grant_trust_to_all_accounts_in_org": false,
    "trusting_accounts": [
      "023e105f4ecef8ad9ca31a8372d0c353"
    ]
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
    "grant_trust_to_all_accounts_in_org": false,
    "trusting_accounts": [
      "023e105f4ecef8ad9ca31a8372d0c353"
    ]
  }
}
```