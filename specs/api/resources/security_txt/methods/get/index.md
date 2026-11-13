---
title: Retrieves security.txt
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Security TXT](https://developers.cloudflare.com/api/resources/security_txt)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Retrieves security.txt

GET/zones/{zone\_id}/security-center/securitytxt

Retrieves the current security.txt file configuration for a zone, used for security vulnerability reporting.

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

`Zone Settings Write``Zone Settings Read`

##### P ath ParametersExpand Collapse

zone\_id: string

Identifier.

maxLength32

[Link to this property](#)%20security_txt%20%3E%20(method)%20get%20%3E%20(params)%20default%20%3E%20(param)%20zone_id%20%3E%20(schema)>)

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

[Link to this property](#)%20security_txt%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20security_txt%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: true

Whether the API call was successful.

[Link to this property](#)%20security_txt%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional object {contact, expires, acknowledgments, 6 more }

Configuration of the zone security.txt file

</summary>

contact: array of string

Methods that researchers should use for reporting vulnerabilities. Can be a URI for an email address, phone number, or URL.

<a href="#">Link to this property</a>

expires: string

RFC3339-formatted date and time string indicating the time that, after which, the contents of the security.txt file should be considered stale. It is recommended that this value is less than a year into the future.

formatdate-time

<a href="#">Link to this property</a>

acknowledgments: optional array of string

Link(s) to a page where security researchers are recognised for their reports.

<a href="#">Link to this property</a>

canonical: optional array of string

Canonical URI where the security.txt file is located.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether or not to serve the security.txt file in this zone. If false, security.txt requests will pass through to the origin server.

<a href="#">Link to this property</a>

encryption: optional array of string

URI(s) pointing to a location where an encryption key that researchers should use for encrypted communications can be retrieved. The key itself must not appear in this field.

<a href="#">Link to this property</a>

hiring: optional array of string

Link(s) to any security-related job positions.

<a href="#">Link to this property</a>

policy: optional array of string

Link(s) to where a vulnerability disclosure policy is located.

<a href="#">Link to this property</a>

preferred\_languages: optional string

Comma-separated list of natural languages that are preferred when submitting security reports. Language codes should be as defined in RFC5646.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20security_txt%20%3E%20(method)%20get%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

### Retrieves security.txt

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/zones/$ZONE_ID/security-center/securitytxt \
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
  "result": {
    "contact": [
      "mailto:security@example.com",
      "tel:+1-201-555-0123",
      "https://example.com/security-contact.html"
    ],
    "expires": "2027-12-31T23:59:59Z",
    "acknowledgments": [
      "https://example.com/hall-of-fame.html"
    ],
    "canonical": [
      "https://www.example.com/.well-known/security.txt"
    ],
    "enabled": true,
    "encryption": [
      "https://example.com/pgp-key.txt",
      "dns:5d2d37ab76d47d36._openpgpkey.example.com?type=OPENPGPKEY",
      "openpgp4fpr:5f2de5521c63a801ab59ccb603d49de44b29100f"
    ],
    "hiring": [
      "https://example.com/jobs.html"
    ],
    "policy": [
      "https://example.com/disclosure-policy.html"
    ],
    "preferred_languages": "en, es, fr"
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
    "contact": [
      "mailto:security@example.com",
      "tel:+1-201-555-0123",
      "https://example.com/security-contact.html"
    ],
    "expires": "2027-12-31T23:59:59Z",
    "acknowledgments": [
      "https://example.com/hall-of-fame.html"
    ],
    "canonical": [
      "https://www.example.com/.well-known/security.txt"
    ],
    "enabled": true,
    "encryption": [
      "https://example.com/pgp-key.txt",
      "dns:5d2d37ab76d47d36._openpgpkey.example.com?type=OPENPGPKEY",
      "openpgp4fpr:5f2de5521c63a801ab59ccb603d49de44b29100f"
    ],
    "hiring": [
      "https://example.com/jobs.html"
    ],
    "policy": [
      "https://example.com/disclosure-policy.html"
    ],
    "preferred_languages": "en, es, fr"
  }
}
```