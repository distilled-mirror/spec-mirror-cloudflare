---
title: Delete a basic-auth secret
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Cloud Workload Security](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws)

[Basic Auth Credentials](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/basic_auth_credentials)

[Secrets](https://developers.cloudflare.com/api/resources/zero_trust/subresources/cws/subresources/basic_auth_credentials/subresources/secrets)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Delete a basic-auth secret

DELETE/accounts/{account\_id}/cws/basic-auth-credentials/{credential\_id}/secrets/{secret\_id}

Deletes the specified secret from the credential.

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

Cloudflare account ID (32-character hexadecimal string)

maxLength32

minLength32

[Link to this property](#)%20zero_trust.cws.basic_auth_credentials.secrets%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

credential\_id: string

ID of the parent credential

formatuuid

[Link to this property](#)%20zero_trust.cws.basic_auth_credentials.secrets%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20credential_id%20%3E%20(schema)>)

secret\_id: string

ID of the secret to delete

formatuuid

[Link to this property](#)%20zero_trust.cws.basic_auth_credentials.secrets%20%3E%20(method)%20delete%20%3E%20(params)%20default%20%3E%20(param)%20secret_id%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {code, message, source }

</summary>

code: number

formatint64

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.basic_auth_credentials.secrets%20%3E%20(method)%20delete%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {code, message, source }

</summary>

code: number

formatint64

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

</summary>

pointer: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.basic_auth_credentials.secrets%20%3E%20(method)%20delete%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {id }

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.cws.basic_auth_credentials.secrets%20%3E%20(method)%20delete%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: boolean

[Link to this property](#)%20zero_trust.cws.basic_auth_credentials.secrets%20%3E%20(method)%20delete%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Delete a basic-auth secret

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/cws/basic-auth-credentials/$CREDENTIAL_ID/secrets/$SECRET_ID \
    -X DELETE \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
```

200 example

```
{
  "errors": [
    {
      "code": 0,
      "message": "message",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    {
      "code": 0,
      "message": "message",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "result": {
    "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
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
      "code": 0,
      "message": "message",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "messages": [
    {
      "code": 0,
      "message": "message",
      "source": {
        "pointer": "pointer"
      }
    }
  ],
  "result": {
    "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e"
  },
  "success": true
}
```