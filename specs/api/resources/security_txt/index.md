---
title: Security TXT
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Security TXT

##### [Retrieves security.txt](https://developers.cloudflare.com/api/resources/security_txt/methods/get)

GET/zones/{zone\_id}/security-center/securitytxt

##### [Updates security.txt](https://developers.cloudflare.com/api/resources/security_txt/methods/update)

PUT/zones/{zone\_id}/security-center/securitytxt

##### [Deletes security.txt](https://developers.cloudflare.com/api/resources/security_txt/methods/delete)

DELETE/zones/{zone\_id}/security-center/securitytxt

##### ModelsExpand Collapse

<details>

<summary>

SecurityTXTGetResponse object {contact, expires, acknowledgments, 6 more }

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

[Link to this property](#)%20security_txt%20%3E%20(model)%20security_txt_get_response%20%3E%20(schema)>)

<details>

<summary>

SecurityTXTUpdateResponse object {errors, messages, success }

</summary>

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

<a href="#">Link to this property</a>

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

<a href="#">Link to this property</a>

success: true

Whether the API call was successful.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20security_txt%20%3E%20(model)%20security_txt_update_response%20%3E%20(schema)>)

<details>

<summary>

SecurityTXTDeleteResponse object {errors, messages, success }

</summary>

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

<a href="#">Link to this property</a>

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

<a href="#">Link to this property</a>

success: true

Whether the API call was successful.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20security_txt%20%3E%20(model)%20security_txt_delete_response%20%3E%20(schema)>)