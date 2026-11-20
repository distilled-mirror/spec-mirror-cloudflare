---
title: Create new submissions
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Email Security](https://developers.cloudflare.com/api/resources/email_security)

[Submissions](https://developers.cloudflare.com/api/resources/email_security/subresources/submissions)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Create new submissions

POST/accounts/{account\_id}/email-security/submissions

Submits messages for reclassification or to report missed detections.

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

[Link to this property](#)%20email_security.submissions%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

<details>

<summary>

body: object {messages, type } or object {messages, type }

</summary>

One of the following:

<details>

<summary>

Reclassification object {messages, type }

</summary>

<details>

<summary>

messages: array of object {alert\_id, expected\_disposition, escalated\_submission\_id }

</summary>

alert\_id: string

Alert ID of the detection to reclassify.

<a href="#">Link to this property</a>

<details>

<summary>

expected\_disposition: "MALICIOUS"or "SUSPICIOUS"or "SPOOF"or 3 more

The disposition a message is submitted to have.

</summary>

One of the following:

"MALICIOUS"

<a href="#">Link to this property</a>

"SUSPICIOUS"

<a href="#">Link to this property</a>

"SPOOF"

<a href="#">Link to this property</a>

"SPAM"

<a href="#">Link to this property</a>

"BULK"

<a href="#">Link to this property</a>

"NONE"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

escalated\_submission\_id: optional string

Submission ID of the original user submission, when reclassifying an escalated user report.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

type: "reclassification"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

MissedDetection object {messages, type }

</summary>

<details>

<summary>

messages: array of object {expected\_disposition, message\_id, postfix\_id, 3 more }

</summary>

<details>

<summary>

expected\_disposition: "MALICIOUS"or "SUSPICIOUS"or "SPOOF"or 3 more

The disposition a message is submitted to have.

</summary>

One of the following:

"MALICIOUS"

<a href="#">Link to this property</a>

"SUSPICIOUS"

<a href="#">Link to this property</a>

"SPOOF"

<a href="#">Link to this property</a>

"SPAM"

<a href="#">Link to this property</a>

"BULK"

<a href="#">Link to this property</a>

"NONE"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

message\_id: string

Message-ID header value of the reported message.

<a href="#">Link to this property</a>

postfix\_id: string

The identifier of the message.

<a href="#">Link to this property</a>

recipient\_emails: array of string

Recipient email addresses of the reported message.

<a href="#">Link to this property</a>

eml\_content: optional string

Base64 encoded content of the EML file.

<a href="#">Link to this property</a>

escalated\_submission\_id: optional string

Submission ID of the original user submission, when escalating an escalated user report.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

type: "missed\_detection"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20email_security.submissions%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20body%20%3E%20(schema)>)

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

[Link to this property](#)%20email_security.submissions%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20email_security.submissions%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

<details>

<summary>

result: object {results }

</summary>

<details>

<summary>

results: array of object {id, accepted, error }

</summary>

id: string

<a href="#">Link to this property</a>

accepted: boolean

<a href="#">Link to this property</a>

error: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20email_security.submissions%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

success: true

Whether the API call was successful.

[Link to this property](#)%20email_security.submissions%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

### Create new submissions

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/email-security/submissions \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "messages": [
            {
              "alert_id": "alert_id",
              "expected_disposition": "MALICIOUS"
            }
          ],
          "type": "reclassification"
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
  "result": {
    "results": [
      {
        "id": "id",
        "accepted": true,
        "error": "error"
      }
    ]
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
  "result": {
    "results": [
      {
        "id": "id",
        "accepted": true,
        "error": "error"
      }
    ]
  },
  "success": true
}
```