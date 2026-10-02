---
title: List Custom Nameserver Sets
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[DNS](https://developers.cloudflare.com/api/resources/dns)

[Settings](https://developers.cloudflare.com/api/resources/dns/subresources/settings)

[Account](https://developers.cloudflare.com/api/resources/dns/subresources/settings/subresources/account)

[Nameserver Sets](https://developers.cloudflare.com/api/resources/dns/subresources/settings/subresources/account/subresources/nameserver_sets)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# List Custom Nameserver Sets

GET/accounts/{account\_id}/dns\_settings/nameserver\_sets

Lists an account’s Custom Nameserver Sets.

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

`Account DNS Settings Write``Account DNS Settings Read`

##### P ath ParametersExpand Collapse

account\_id: string

Identifier.

maxLength32

[Link to this property](#)%20dns.settings.account.nameserver_sets%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

page: optional number

Page number of paginated results.

minimum1

[Link to this property](#)%20dns.settings.account.nameserver_sets%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20page%20%3E%20(schema)>)

per\_page: optional number

Number of results per page.

maximum5000000

minimum1

[Link to this property](#)%20dns.settings.account.nameserver_sets%20%3E%20(method)%20list%20%3E%20(params)%20default%20%3E%20(param)%20per_page%20%3E%20(schema)>)

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

[Link to this property](#)%20dns.settings.account.nameserver_sets%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20dns.settings.account.nameserver_sets%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: array of object {id, advanced, created\_on, 2 more } or object {id, advanced, created\_on, 2 more }

</summary>

One of the following:

<details>

<summary>

DNSSettingsNameserverSetStandardResponse object {id, advanced, created\_on, 2 more }

</summary>

id: string

Identifier for a nameserver set.

maxLength32

minLength32

<a href="#">Link to this property</a>

advanced: false

Whether the nameserver set uses Advanced anycast groups.

<a href="#">Link to this property</a>

created\_on: string

When the nameserver set was created.

formatdate-time

<a href="#">Link to this property</a>

ip\_set: number

Selects the account-specific IP set that supplies the nameserver addresses. The account’s entitlement determines the maximum value. Nameserver sets with the same <code>ip_set</code> and <code>advanced</code> value may reuse addresses; otherwise, they use disjoint address groups.

formatint64

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

nameservers: array of object {ipv4, ipv6, name }

</summary>

ipv4: array of string

IPv4 addresses assigned to the nameserver.

<a href="#">Link to this property</a>

ipv6: array of string

IPv6 addresses assigned to the nameserver.

<a href="#">Link to this property</a>

name: string

A unique lowercase Punycode nameserver name within the set.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

DNSSettingsNameserverSetAdvancedResponse object {id, advanced, created\_on, 2 more }

</summary>

id: string

Identifier for a nameserver set.

maxLength32

minLength32

<a href="#">Link to this property</a>

advanced: true

Whether the nameserver set uses Advanced anycast groups.

<a href="#">Link to this property</a>

created\_on: string

When the nameserver set was created.

formatdate-time

<a href="#">Link to this property</a>

ip\_set: number

Selects the account-specific IP set that supplies the nameserver addresses. The account’s entitlement determines the maximum value. Nameserver sets with the same <code>ip_set</code> and <code>advanced</code> value may reuse addresses; otherwise, they use disjoint address groups.

formatint64

minimum1

<a href="#">Link to this property</a>

<details>

<summary>

nameservers: array of object {ipv4, ipv4\_groups, ipv6, 2 more }

</summary>

ipv4: array of string

IPv4 addresses assigned to the nameserver.

<a href="#">Link to this property</a>

<details>

<summary>

ipv4\_groups: array of "a"or "b"or "c"

Advanced anycast group for each address in the corresponding address array. Entries have the same order as, and correspond one-to-one with, the addresses.

</summary>

One of the following:

"a"

<a href="#">Link to this property</a>

"b"

<a href="#">Link to this property</a>

"c"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

ipv6: array of string

IPv6 addresses assigned to the nameserver.

<a href="#">Link to this property</a>

<details>

<summary>

ipv6\_groups: array of "a"or "b"or "c"

Advanced anycast group for each address in the corresponding address array. Entries have the same order as, and correspond one-to-one with, the addresses.

</summary>

One of the following:

"a"

<a href="#">Link to this property</a>

"b"

<a href="#">Link to this property</a>

"c"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

name: string

A unique lowercase Punycode nameserver name within the set.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20dns.settings.account.nameserver_sets%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

<details>

<summary>

result\_info: object {count, page, per\_page, 2 more }

</summary>

count: optional number

Total number of results for the requested service.

<a href="#">Link to this property</a>

page: optional number

Current page within paginated list of results.

<a href="#">Link to this property</a>

per\_page: optional number

Number of results per page of results.

<a href="#">Link to this property</a>

total\_count: optional number

Total results available without any search parameters.

<a href="#">Link to this property</a>

total\_pages: optional number

The number of total pages in the entire result set.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20dns.settings.account.nameserver_sets%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20result_info>)

success: true

Whether the API call was successful.

[Link to this property](#)%20dns.settings.account.nameserver_sets%20%3E%20(method)%20list%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### List Custom Nameserver Sets

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/dns_settings/nameserver_sets \
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
  "result": [
    {
      "id": "0123456789abcdef0123456789abcdef",
      "advanced": false,
      "created_on": "2026-09-01T12:00:00Z",
      "ip_set": 1,
      "nameservers": [
        {
          "ipv4": [
            "192.0.2.1"
          ],
          "ipv6": [
            "2001:db8::1"
          ],
          "name": "ns1.example.com"
        },
        {
          "ipv4": [
            "192.0.2.1"
          ],
          "ipv6": [
            "2001:db8::1"
          ],
          "name": "ns1.example.com"
        }
      ]
    }
  ],
  "result_info": {
    "count": 1,
    "page": 1,
    "per_page": 20,
    "total_count": 2000,
    "total_pages": 100
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
  "result": [
    {
      "id": "0123456789abcdef0123456789abcdef",
      "advanced": false,
      "created_on": "2026-09-01T12:00:00Z",
      "ip_set": 1,
      "nameservers": [
        {
          "ipv4": [
            "192.0.2.1"
          ],
          "ipv6": [
            "2001:db8::1"
          ],
          "name": "ns1.example.com"
        },
        {
          "ipv4": [
            "192.0.2.1"
          ],
          "ipv6": [
            "2001:db8::1"
          ],
          "name": "ns1.example.com"
        }
      ]
    }
  ],
  "result_info": {
    "count": 1,
    "page": 1,
    "per_page": 20,
    "total_count": 2000,
    "total_pages": 100
  },
  "success": true
}
```