---
title: List Prefixes
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Addressing](https://developers.cloudflare.com/api/resources/addressing)

[Prefixes](https://developers.cloudflare.com/api/resources/addressing/subresources/prefixes)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List Prefixes

GET/accounts/{account\_id}/addressing/prefixes

List all prefixes owned by the account.

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

`Magic Transit Read``Magic Transit Write``IP Prefixes: Write``IP Prefixes: Read``IP Prefixes: BGP On Demand Write``IP Prefixes: BGP On Demand Read`

##### P ath ParametersExpand Collapse

account\_id: string

Identifier of a Cloudflare account.

maxLength32

[Link to this property](#)%20addressing.prefixes%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

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

[Link to this property](#)%20addressing.prefixes%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20addressing.prefixes%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: true

Whether the API call was successful.

[Link to this property](#)%20addressing.prefixes%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional array of <a href="https://developers.cloudflare.com/api/resources/addressing#(resource)%20addressing.prefixes%20%3E%20(model)%20prefix%20%3E%20(schema)">Prefix</a> { id, account\_id, advertised, 17 more }

</summary>

id: optional string

Identifier of an IP Prefix.

maxLength32

<a href="#">Link to this property</a>

account\_id: optional string

Identifier of a Cloudflare account.

maxLength32

<a href="#">Link to this property</a>

Deprecatedadvertised: optional boolean

Prefer the <a href="https://developers.cloudflare.com/api/resources/addressing/subresources/prefixes/subresources/bgp_prefixes/">BGP Prefixes API</a> instead, which allows for advertising multiple BGP routes within a single IP Prefix.

Prefix advertisement status to the Internet. This field is only not ‘null’ if on demand is enabled.

<a href="#">Link to this property</a>

Deprecatedadvertised\_modified\_at: optional string

Prefer the <a href="https://developers.cloudflare.com/api/resources/addressing/subresources/prefixes/subresources/bgp_prefixes/">BGP Prefixes API</a> instead, which allows for advertising multiple BGP routes within a single IP Prefix.

Last time the advertisement status was changed. This field is only not ‘null’ if on demand is enabled.

formatdate-time

<a href="#">Link to this property</a>

approved: optional string

Approval state of the prefix (P = pending, V = approved). Approval does not advertise the prefix or activate traffic.

<a href="#">Link to this property</a>

asn: optional number

Autonomous System Number (ASN) the prefix will be advertised under. Use 13335 for Cloudflare’s ASN, or your own ASN as an integer without the AS prefix. The IRR route and RPKI ROA must authorize this ASN.

<a href="#">Link to this property</a>

<details>

<summary>

asn\_ownership\_validation\_state: optional "pending"or "valid"or "missing"or "invalid"

State of ASN ownership validation for a customer-owned Autonomous System Number (ASN). Returned when an ASN ownership validation result exists. Omitted when validation does not apply, such as for Cloudflare-owned ASNs. Verification is reused for prefixes with the same account and ASN. Refer to <a href="https://developers.cloudflare.com/byoip/troubleshooting/prefix-validation/#asn-ownership-validation">ASN ownership validation states</a> for state meanings and resolutions.

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"valid"

<a href="#">Link to this property</a>

"missing"

<a href="#">Link to this property</a>

"invalid"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

aspa\_validation\_state: optional "pending"or "valid"or "invalid"

State of Autonomous System Provider Authorization (ASPA) validation for a customer-owned ASN. Returned when an ASPA validation result exists. Publishing an ASPA is optional. A published ASPA must authorize AS13335 as a provider. An invalid result blocks approval. If omitted, no ASPA validation result is available. Omission does not indicate successful validation or confirm that no ASPA exists. Refer to <a href="https://developers.cloudflare.com/byoip/troubleshooting/prefix-validation/#aspa-validation">ASPA validation states</a> for state meanings and resolutions, and <a href="https://developers.cloudflare.com/byoip/concepts/route-filtering-rpki/#aspa-authorization">ASPA authorization</a> for publication guidance.

</summary>

One of the following:

"pending"

<a href="#">Link to this property</a>

"valid"

<a href="#">Link to this property</a>

"invalid"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

cidr: optional string

IP Prefix in Classless Inter-Domain Routing format.

<a href="#">Link to this property</a>

created\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

delegate\_loa\_creation: optional boolean

Whether Cloudflare is allowed to generate the LOA document on behalf of the prefix owner.

<a href="#">Link to this property</a>

description: optional string

Description of the prefix.

maxLength1000

<a href="#">Link to this property</a>

irr\_validation\_state: optional string

State of one kind of validation for an IP prefix.

<a href="#">Link to this property</a>

loa\_document\_id: optional string

Identifier for the uploaded LOA document.

maxLength32

<a href="#">Link to this property</a>

modified\_at: optional string

formatdate-time

<a href="#">Link to this property</a>

Deprecatedon\_demand\_enabled: optional boolean

Prefer the <a href="https://developers.cloudflare.com/api/resources/addressing/subresources/prefixes/subresources/bgp_prefixes/">BGP Prefixes API</a> instead, which allows for advertising multiple BGP routes within a single IP Prefix.

Whether advertisement of the prefix to the Internet may be dynamically enabled or disabled.

<a href="#">Link to this property</a>

Deprecatedon\_demand\_locked: optional boolean

Prefer the <a href="https://developers.cloudflare.com/api/resources/addressing/subresources/prefixes/subresources/bgp_prefixes/">BGP Prefixes API</a> instead, which allows for advertising multiple BGP routes within a single IP Prefix.

Whether advertisement status of the prefix is locked, meaning it cannot be changed.

<a href="#">Link to this property</a>

ownership\_validation\_state: optional string

State of one kind of validation for an IP prefix.

<a href="#">Link to this property</a>

ownership\_validation\_token: optional string

Token used to verify ownership of the prefix and, when applicable, its ASN. Use the same token for both checks. Refer to the <a href="https://developers.cloudflare.com/byoip/get-started/">BYOIP onboarding guide</a> for verification instructions.

<a href="#">Link to this property</a>

rpki\_validation\_state: optional string

State of one kind of validation for an IP prefix.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20addressing.prefixes%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

### List Prefixes

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/addressing/prefixes \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN"
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
  "result": [
    {
      "id": "2af39739cc4e3b5910c918468bb89828",
      "account_id": "258def64c72dae45f3e4c8516e2111f2",
      "advertised": true,
      "advertised_modified_at": "2014-01-01T05:20:00.12345Z",
      "approved": "P",
      "asn": 13335,
      "asn_ownership_validation_state": "pending",
      "aspa_validation_state": "pending",
      "cidr": "192.0.2.0/24",
      "created_at": "2014-01-01T05:20:00.12345Z",
      "delegate_loa_creation": true,
      "description": "Internal test prefix",
      "irr_validation_state": "pending",
      "loa_document_id": "d933b1530bc56c9953cf8ce166da8004",
      "modified_at": "2014-01-01T05:20:00.12345Z",
      "on_demand_enabled": true,
      "on_demand_locked": false,
      "ownership_validation_state": "pending",
      "ownership_validation_token": "1234a5b6-1234-1abc-12a3-1234a5b6789c",
      "rpki_validation_state": "pending"
    }
  ]
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
  "result": [
    {
      "id": "2af39739cc4e3b5910c918468bb89828",
      "account_id": "258def64c72dae45f3e4c8516e2111f2",
      "advertised": true,
      "advertised_modified_at": "2014-01-01T05:20:00.12345Z",
      "approved": "P",
      "asn": 13335,
      "asn_ownership_validation_state": "pending",
      "aspa_validation_state": "pending",
      "cidr": "192.0.2.0/24",
      "created_at": "2014-01-01T05:20:00.12345Z",
      "delegate_loa_creation": true,
      "description": "Internal test prefix",
      "irr_validation_state": "pending",
      "loa_document_id": "d933b1530bc56c9953cf8ce166da8004",
      "modified_at": "2014-01-01T05:20:00.12345Z",
      "on_demand_enabled": true,
      "on_demand_locked": false,
      "ownership_validation_state": "pending",
      "ownership_validation_token": "1234a5b6-1234-1abc-12a3-1234a5b6789c",
      "rpki_validation_state": "pending"
    }
  ]
}
```