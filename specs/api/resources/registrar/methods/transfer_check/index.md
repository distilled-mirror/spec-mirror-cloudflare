---
title: Check domain transfer eligibility
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Registrar](https://developers.cloudflare.com/api/resources/registrar)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Check domain transfer eligibility

POST/accounts/{account\_id}/registrar/domain-transfer-check

Performs real-time, authoritative eligibility checks directly against needed requirements. Use this endpoint to verify a domain is available before attempting a transfer via `POST /registrations/:domain_name/transfer-in`.

**Note:** This endpoint uses POST to accept a list of domains in the request body. It is a read-only operation — it does not create, modify, or reserve any domains.

### Behavior

- Maximum 10 domains per request
- Pricing is only returned for domains where `transferable: true`
- Results are not cached; each request queries the registry & other needed upstreams

## Extension Support

All `.uk` extensions (`.uk`, `.co.uk`, etc) do not support auth codes. As such, Cloudflare will ignore the `auth_code` section of this request for `.uk` domains.

This means that a `.uk` domain depends on public data to obtain domain information, so it might be a few minutes outdated.

### Workflow

1. Call this endpoint with domains the user wants to transfer.
2. For each domain where `transferable: true`, present pricing to the user.
3. For each domain where `transferable: false`, present reasons to the user
4. Proceed to `POST /registrations/:domain_name/transfer-in` only for the `transferable: true` domains.

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

Identifier.

maxLength32

[Link to this property](#)%20registrar%20%3E%20(method)%20transfer_check%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

<details>

<summary>

domains: array of object {domain\_name, auth\_code }

List of domain objects to evaluate for transfer eligibility.

</summary>

domain\_name: string

Fully qualified domain name (FQDN) to check for transfer eligibility.

<a href="#">Link to this property</a>

auth\_code: optional string

Base64-encoded auth/EPP code from the current registrar. Required for most TLDs. <code>.uk</code> namespaces do not use auth codes.

formatbyte

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20registrar%20%3E%20(method)%20transfer_check%20%3E%20(params)%200%20%3E%20(param)%20domains%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

errors: array of object {code, message, source }

</summary>

code: number

minimum1000

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

Location of the invalid value that caused the error.

</summary>

pointer: string

JSON Pointer to the invalid or missing request value.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20registrar%20%3E%20(method)%20transfer_check%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

messages: array of object {code, message, source }

</summary>

code: number

minimum1000

<a href="#">Link to this property</a>

message: string

<a href="#">Link to this property</a>

<details>

<summary>

source: optional object {pointer }

Location of the invalid value that caused the error.

</summary>

pointer: string

JSON Pointer to the invalid or missing request value.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20registrar%20%3E%20(method)%20transfer_check%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {domains }

Contains the transfer eligibility results.

</summary>

<details>

<summary>

domains: map\[object {pricing, transferable, name, reasons } or object {transferable, name, pricing, reasons } ]

Maps domain names to transfer eligibility results. Each value contains <code>name</code>, <code>transferable</code>, and <code>reasons</code>.

</summary>

One of the following:

<details>

<summary>

TransferableResult object {pricing, transferable, name, reasons }

</summary>

<details>

<summary>

pricing: object {currency, renewal\_cost, transfer\_cost }

Provides annual pricing information for a given domain. The API returns all per-year prices as strings to preserve decimal precision.

<code>renewal_cost</code> and <code>registration_cost</code> or <code>transfer_cost</code> are frequently the same value, but may differ due to premium rates for certain domains.

For a multi-year operations, the operation’s cost applies to the first year and <code>renewal_cost</code> applies to each subsequent year. The values reflect the current registry rate, which can change over time.

</summary>

currency: string

ISO-4217 currency code for the prices (e.g., “USD”, “EUR”, “GBP”).

<a href="#">Link to this property</a>

renewal\_cost: string

Per-year renewal cost for this domain. Applied to each year beyond the first year of a multi-year registration, and to each annual auto-renewal thereafter. May differ from <code>registration_cost</code>, especially for premium domains where initial registration often costs more than renewals.

<a href="#">Link to this property</a>

transfer\_cost: string

The first-year cost to transfer this domain.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

transferable: true

<a href="#">Link to this property</a>

name: optional string

The check evaluates this domain name.

<a href="#">Link to this property</a>

<details>

<summary>

reasons: optional array of object {code }

</summary>

<details>

<summary>

code: "extension\_not\_supported\_via\_api"or "extension\_not\_supported"or "domain\_premium"or 14 more

Transfer eligibility reason code.

- <code>extension_not_supported_via_api</code>: This API excludes the extension; dashboard flows support it.
- <code>extension_not_supported</code>: Cloudflare Registrar excludes the extension.
- <code>domain_premium</code>: This API currently excludes premium transfers.
- <code>extension_disallows_transfer</code>: Extension currently blocks transfer operations.
- <code>domain_not_exists</code>: No registration record exists for the domain.
- <code>domain_on_cloudflare</code>: Cloudflare already serves as the domain’s registrar.
- <code>domain_locked</code>: Losing registrar reports transfer-prohibited lock status.
- <code>registry_status</code>: Registry status currently blocks transfer (for example, pending transfer or deletion state).
- <code>domain_outside_transfer_window</code>: Domain is within a transfer wait window (for example, recently registered).
- <code>domain_max_term</code>: Completing transfer would exceed the registry maximum term.
- <code>invalid_auth_code</code>: The provided auth code is incorrect.
- <code>invalid_auth_code_format</code>: Auth code fails Base64 validation.
- <code>dnssec_enabled</code>: DNSSEC is enabled. It must be disabled before transfer.
- <code>zone_not_found</code>: The target account lacks a Cloudflare zone for the domain.
- <code>zone_status_invalid</code>: The Cloudflare zone cannot transfer in its current state.
- <code>invalid_zone_plan</code>: The zone plan fails transfer requirements.
- <code>domain_unsupported</code>: This endpoint rejects the domain name format.

</summary>

One of the following:

"extension\_not\_supported\_via\_api"

<a href="#">Link to this property</a>

"extension\_not\_supported"

<a href="#">Link to this property</a>

"domain\_premium"

<a href="#">Link to this property</a>

"extension\_disallows\_transfer"

<a href="#">Link to this property</a>

"domain\_not\_exists"

<a href="#">Link to this property</a>

"domain\_on\_cloudflare"

<a href="#">Link to this property</a>

"domain\_locked"

<a href="#">Link to this property</a>

"registry\_status"

<a href="#">Link to this property</a>

"domain\_outside\_transfer\_window"

<a href="#">Link to this property</a>

"domain\_max\_term"

<a href="#">Link to this property</a>

"invalid\_auth\_code"

<a href="#">Link to this property</a>

"invalid\_auth\_code\_format"

<a href="#">Link to this property</a>

"dnssec\_enabled"

<a href="#">Link to this property</a>

"zone\_not\_found"

<a href="#">Link to this property</a>

"zone\_status\_invalid"

<a href="#">Link to this property</a>

"invalid\_zone\_plan"

<a href="#">Link to this property</a>

"domain\_unsupported"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

NonTransferableResult object {transferable, name, pricing, reasons }

</summary>

transferable: false

<a href="#">Link to this property</a>

name: optional string

The check evaluates this domain name.

<a href="#">Link to this property</a>

<details>

<summary>

pricing: optional object {currency, renewal\_cost, transfer\_cost }

Provides annual pricing information for a given domain. The API returns all per-year prices as strings to preserve decimal precision.

<code>renewal_cost</code> and <code>registration_cost</code> or <code>transfer_cost</code> are frequently the same value, but may differ due to premium rates for certain domains.

For a multi-year operations, the operation’s cost applies to the first year and <code>renewal_cost</code> applies to each subsequent year. The values reflect the current registry rate, which can change over time.

</summary>

currency: string

ISO-4217 currency code for the prices (e.g., “USD”, “EUR”, “GBP”).

<a href="#">Link to this property</a>

renewal\_cost: string

Per-year renewal cost for this domain. Applied to each year beyond the first year of a multi-year registration, and to each annual auto-renewal thereafter. May differ from <code>registration_cost</code>, especially for premium domains where initial registration often costs more than renewals.

<a href="#">Link to this property</a>

transfer\_cost: string

The first-year cost to transfer this domain.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

reasons: optional array of object {code }

</summary>

<details>

<summary>

code: "extension\_not\_supported\_via\_api"or "extension\_not\_supported"or "domain\_premium"or 14 more

Transfer eligibility reason code.

- <code>extension_not_supported_via_api</code>: This API excludes the extension; dashboard flows support it.
- <code>extension_not_supported</code>: Cloudflare Registrar excludes the extension.
- <code>domain_premium</code>: This API currently excludes premium transfers.
- <code>extension_disallows_transfer</code>: Extension currently blocks transfer operations.
- <code>domain_not_exists</code>: No registration record exists for the domain.
- <code>domain_on_cloudflare</code>: Cloudflare already serves as the domain’s registrar.
- <code>domain_locked</code>: Losing registrar reports transfer-prohibited lock status.
- <code>registry_status</code>: Registry status currently blocks transfer (for example, pending transfer or deletion state).
- <code>domain_outside_transfer_window</code>: Domain is within a transfer wait window (for example, recently registered).
- <code>domain_max_term</code>: Completing transfer would exceed the registry maximum term.
- <code>invalid_auth_code</code>: The provided auth code is incorrect.
- <code>invalid_auth_code_format</code>: Auth code fails Base64 validation.
- <code>dnssec_enabled</code>: DNSSEC is enabled. It must be disabled before transfer.
- <code>zone_not_found</code>: The target account lacks a Cloudflare zone for the domain.
- <code>zone_status_invalid</code>: The Cloudflare zone cannot transfer in its current state.
- <code>invalid_zone_plan</code>: The zone plan fails transfer requirements.
- <code>domain_unsupported</code>: This endpoint rejects the domain name format.

</summary>

One of the following:

"extension\_not\_supported\_via\_api"

<a href="#">Link to this property</a>

"extension\_not\_supported"

<a href="#">Link to this property</a>

"domain\_premium"

<a href="#">Link to this property</a>

"extension\_disallows\_transfer"

<a href="#">Link to this property</a>

"domain\_not\_exists"

<a href="#">Link to this property</a>

"domain\_on\_cloudflare"

<a href="#">Link to this property</a>

"domain\_locked"

<a href="#">Link to this property</a>

"registry\_status"

<a href="#">Link to this property</a>

"domain\_outside\_transfer\_window"

<a href="#">Link to this property</a>

"domain\_max\_term"

<a href="#">Link to this property</a>

"invalid\_auth\_code"

<a href="#">Link to this property</a>

"invalid\_auth\_code\_format"

<a href="#">Link to this property</a>

"dnssec\_enabled"

<a href="#">Link to this property</a>

"zone\_not\_found"

<a href="#">Link to this property</a>

"zone\_status\_invalid"

<a href="#">Link to this property</a>

"invalid\_zone\_plan"

<a href="#">Link to this property</a>

"domain\_unsupported"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20registrar%20%3E%20(method)%20transfer_check%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

Whether the API call was successful.

[Link to this property](#)%20registrar%20%3E%20(method)%20transfer_check%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Check domain transfer eligibility

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/registrar/domain-transfer-check \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "domains": [
            {
              "domain_name": "example.co.uk"
            }
          ]
        }'
```

200 example

200 example

200 example

200 example

200 example

400 example

400 example

400 example

503 example

```
{
  "errors": [],
  "messages": [],
  "result": {
    "domains": {
      "example.com": {
        "name": "example.com",
        "pricing": {
          "currency": "USD",
          "renewal_cost": "10.11",
          "transfer_cost": "8.57"
        },
        "reasons": [],
        "transferable": true
      },
      "mybrand.net": {
        "name": "mybrand.net",
        "pricing": {
          "currency": "USD",
          "renewal_cost": "12.50",
          "transfer_cost": "9.99"
        },
        "reasons": [],
        "transferable": true
      }
    }
  },
  "success": true
}
```

```
{
  "errors": [],
  "messages": [],
  "result": {
    "domains": {
      "example.com": {
        "name": "example.com",
        "reasons": [
          {
            "code": "invalid_auth_code"
          }
        ],
        "transferable": false
      }
    }
  },
  "success": true
}
```

```
{
  "errors": [],
  "messages": [],
  "result": {
    "domains": {
      "cloudflare.com": {
        "name": "cloudflare.com",
        "reasons": [
          {
            "code": "domain_on_cloudflare"
          }
        ],
        "transferable": false
      },
      "locked-example.com": {
        "name": "locked-example.com",
        "reasons": [
          {
            "code": "domain_locked"
          }
        ],
        "transferable": false
      },
      "move-ready.net": {
        "name": "move-ready.net",
        "pricing": {
          "currency": "USD",
          "renewal_cost": "12.50",
          "transfer_cost": "9.99"
        },
        "reasons": [],
        "transferable": true
      },
      "pending-transfer.dev": {
        "name": "pending-transfer.dev",
        "reasons": [
          {
            "code": "registry_status"
          }
        ],
        "transferable": false
      }
    }
  },
  "success": true
}
```

```
{
  "errors": [
    {
      "code": 10000,
      "message": "Internal API failure for domain flaky-example.com",
      "source": {
        "pointer": "/domains/1"
      }
    }
  ],
  "messages": [],
  "result": {
    "domains": {
      "stable-example.com": {
        "name": "stable-example.com",
        "pricing": {
          "currency": "USD",
          "renewal_cost": "10.11",
          "transfer_cost": "8.57"
        },
        "reasons": [],
        "transferable": true
      }
    }
  },
  "success": true
}
```

```
{
  "errors": [],
  "messages": [],
  "result": {
    "domains": {
      "example.horse": {
        "name": "example.horse",
        "reasons": [
          {
            "code": "extension_not_supported"
          }
        ],
        "transferable": false
      },
      "invalid@@domain": {
        "name": "invalid@@domain",
        "reasons": [
          {
            "code": "domain_unsupported"
          }
        ],
        "transferable": false
      }
    }
  },
  "success": true
}
```

```
{
  "errors": [
    {
      "code": 10000,
      "message": "object at root is missing required properties: domains",
      "source": {
        "pointer": "/domains"
      }
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```

```
{
  "errors": [
    {
      "code": 10000,
      "message": "Duplicate domain name",
      "source": {
        "pointer": "/domains/1"
      }
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```

```
{
  "errors": [
    {
      "code": 10000,
      "message": "array at `/domains` is too long (maximum: 10)",
      "source": {
        "pointer": "/domains"
      }
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```

```
{
  "errors": [
    {
      "code": 10000,
      "message": "Internal API failure for domain example.com",
      "source": {
        "pointer": "/domains/0"
      }
    },
    {
      "code": 10000,
      "message": "Internal API failure for domain mybrand.net",
      "source": {
        "pointer": "/domains/1"
      }
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```

##### Returns Examples

200 example

200 example

200 example

200 example

200 example

400 example

400 example

400 example

503 example

```
{
  "errors": [],
  "messages": [],
  "result": {
    "domains": {
      "example.com": {
        "name": "example.com",
        "pricing": {
          "currency": "USD",
          "renewal_cost": "10.11",
          "transfer_cost": "8.57"
        },
        "reasons": [],
        "transferable": true
      },
      "mybrand.net": {
        "name": "mybrand.net",
        "pricing": {
          "currency": "USD",
          "renewal_cost": "12.50",
          "transfer_cost": "9.99"
        },
        "reasons": [],
        "transferable": true
      }
    }
  },
  "success": true
}
```

```
{
  "errors": [],
  "messages": [],
  "result": {
    "domains": {
      "example.com": {
        "name": "example.com",
        "reasons": [
          {
            "code": "invalid_auth_code"
          }
        ],
        "transferable": false
      }
    }
  },
  "success": true
}
```

```
{
  "errors": [],
  "messages": [],
  "result": {
    "domains": {
      "cloudflare.com": {
        "name": "cloudflare.com",
        "reasons": [
          {
            "code": "domain_on_cloudflare"
          }
        ],
        "transferable": false
      },
      "locked-example.com": {
        "name": "locked-example.com",
        "reasons": [
          {
            "code": "domain_locked"
          }
        ],
        "transferable": false
      },
      "move-ready.net": {
        "name": "move-ready.net",
        "pricing": {
          "currency": "USD",
          "renewal_cost": "12.50",
          "transfer_cost": "9.99"
        },
        "reasons": [],
        "transferable": true
      },
      "pending-transfer.dev": {
        "name": "pending-transfer.dev",
        "reasons": [
          {
            "code": "registry_status"
          }
        ],
        "transferable": false
      }
    }
  },
  "success": true
}
```

```
{
  "errors": [
    {
      "code": 10000,
      "message": "Internal API failure for domain flaky-example.com",
      "source": {
        "pointer": "/domains/1"
      }
    }
  ],
  "messages": [],
  "result": {
    "domains": {
      "stable-example.com": {
        "name": "stable-example.com",
        "pricing": {
          "currency": "USD",
          "renewal_cost": "10.11",
          "transfer_cost": "8.57"
        },
        "reasons": [],
        "transferable": true
      }
    }
  },
  "success": true
}
```

```
{
  "errors": [],
  "messages": [],
  "result": {
    "domains": {
      "example.horse": {
        "name": "example.horse",
        "reasons": [
          {
            "code": "extension_not_supported"
          }
        ],
        "transferable": false
      },
      "invalid@@domain": {
        "name": "invalid@@domain",
        "reasons": [
          {
            "code": "domain_unsupported"
          }
        ],
        "transferable": false
      }
    }
  },
  "success": true
}
```

```
{
  "errors": [
    {
      "code": 10000,
      "message": "object at root is missing required properties: domains",
      "source": {
        "pointer": "/domains"
      }
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```

```
{
  "errors": [
    {
      "code": 10000,
      "message": "Duplicate domain name",
      "source": {
        "pointer": "/domains/1"
      }
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```

```
{
  "errors": [
    {
      "code": 10000,
      "message": "array at `/domains` is too long (maximum: 10)",
      "source": {
        "pointer": "/domains"
      }
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```

```
{
  "errors": [
    {
      "code": 10000,
      "message": "Internal API failure for domain example.com",
      "source": {
        "pointer": "/domains/0"
      }
    },
    {
      "code": 10000,
      "message": "Internal API failure for domain mybrand.net",
      "source": {
        "pointer": "/domains/1"
      }
    }
  ],
  "messages": [],
  "result": null,
  "success": false
}
```