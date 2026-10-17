---
title: Update a proximity word validator
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[DLP](https://developers.cloudflare.com/api/resources/zero_trust/subresources/dlp)

[Validators](https://developers.cloudflare.com/api/resources/zero_trust/subresources/dlp/subresources/validators)

[Proximity Words](https://developers.cloudflare.com/api/resources/zero_trust/subresources/dlp/subresources/validators/subresources/proximity_words)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Update a proximity word validator

PUT/accounts/{account\_id}/dlp/validators/proximity\_words/{validator\_id}

Replaces the name and word list of a `proximity_words` validator. Attachments to detection entries are owned from the entry side and are not affected.

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

`Zero Trust Write`

##### P ath ParametersExpand Collapse

account\_id: string

[Link to this property](#)%20zero_trust.dlp.validators.proximity_words%20%3E%20(method)%20update%20%3E%20(params)%20default%20%3E%20(param)%20account_id%20%3E%20(schema)>)

validator\_id: string

formatuuid

[Link to this property](#)%20zero_trust.dlp.validators.proximity_words%20%3E%20(method)%20update%20%3E%20(params)%20default%20%3E%20(param)%20validator_id%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

name: string

A name for this validator, at most 50 characters.

[Link to this property](#)%20zero_trust.dlp.validators.proximity_words%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20name%20%3E%20(schema)>)

<details>

<summary>

words: array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.dlp.validators.proximity_words%20%3E%20(model)%20word%20%3E%20(schema)">Word</a> { weight, word }

The words that raise confidence when found near a match, at most 100 per validator. Matching ignores case, so the list may not contain the same word twice with different capitalisation. Words are stored as sent.

For example, a validator for medical record numbers might use <code>[{"word": "patient", "weight": "strong"}, {"word": "diagnosis", "weight": "moderate"}, {"word": "mrn", "weight": "weak"}]</code>.

</summary>

<details>

<summary>

weight: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.dlp.validators.proximity_words%20%3E%20(model)%20weight%20%3E%20(schema)">Weight</a>

How much a word contributes to a match’s confidence when it is found nearby.

Separate from a profile’s high/medium/low confidence threshold: this describes how telling the word is, not how confident the resulting match is.

</summary>

One of the following:

"strong"

<a href="#">Link to this property</a>

"moderate"

<a href="#">Link to this property</a>

"weak"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

word: string

The word or phrase to look for. Must contain 1–128 characters and is matched case-insensitively.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.dlp.validators.proximity_words%20%3E%20(method)%20update%20%3E%20(params)%200%20%3E%20(param)%20words%20%3E%20(schema)>)

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

[Link to this property](#)%20zero_trust.dlp.validators.proximity_words%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

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

[Link to this property](#)%20zero_trust.dlp.validators.proximity_words%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20messages>)

success: true

Whether the API call was successful.

[Link to this property](#)%20zero_trust.dlp.validators.proximity_words%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

result: optional <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.dlp.validators.proximity_words%20%3E%20(model)%20proximity_word_validator%20%3E%20(schema)">ProximityWordValidator</a> { id, created\_at, name, 3 more }

A reusable list of weighted words. Attaching it to a detection entry raises the confidence of that entry’s matches when one of the words appears nearby, and lowers it when none do.

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

created\_at: string

formatdate-time

<a href="#">Link to this property</a>

name: string

A name for this validator, at most 50 characters.

<a href="#">Link to this property</a>

<details>

<summary>

referenced\_by: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.dlp.validators%20%3E%20(model)%20references%20%3E%20(schema)">References</a> { entries, entry\_count }

What currently uses a validator. Deleting a validator that is still in use returns <code>409</code>, so check this first.

Read-only. A validator is attached or detached by updating the detection entry that uses it, not by writing this back.

</summary>

<details>

<summary>

entries: array of object {id, name, type }

The detection entries using this validator, ordered by name.

</summary>

id: string

formatuuid

<a href="#">Link to this property</a>

name: string

<a href="#">Link to this property</a>

<details>

<summary>

type: "custom"or "custom\_prompt\_topic"or "predefined"or 4 more

The type of a detection entry.

</summary>

One of the following:

"custom"

<a href="#">Link to this property</a>

"custom\_prompt\_topic"

<a href="#">Link to this property</a>

"predefined"

<a href="#">Link to this property</a>

"integration"

<a href="#">Link to this property</a>

"exact\_data"

<a href="#">Link to this property</a>

"document\_fingerprint"

<a href="#">Link to this property</a>

"word\_list"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

entry\_count: number

Number of detection entries this validator is attached to.

formatint32

minimum0

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

words: array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.dlp.validators.proximity_words%20%3E%20(model)%20word%20%3E%20(schema)">Word</a> { weight, word }

The words that raise confidence when found near a match.

</summary>

<details>

<summary>

weight: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.dlp.validators.proximity_words%20%3E%20(model)%20weight%20%3E%20(schema)">Weight</a>

How much a word contributes to a match’s confidence when it is found nearby.

Separate from a profile’s high/medium/low confidence threshold: this describes how telling the word is, not how confident the resulting match is.

</summary>

One of the following:

"strong"

<a href="#">Link to this property</a>

"moderate"

<a href="#">Link to this property</a>

"weak"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

word: string

The word or phrase to look for. Must contain 1–128 characters and is matched case-insensitively.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.dlp.validators.proximity_words%20%3E%20(method)%20update%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

### Update a proximity word validator

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/dlp/validators/proximity_words/$VALIDATOR_ID \
    -X PUT \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "name": "HIPAA context words",
          "words": [
            {
              "weight": "strong",
              "word": "social security number"
            }
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
    "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
    "created_at": "2019-12-27T18:11:19.117Z",
    "name": "HIPAA context words",
    "referenced_by": {
      "entries": [
        {
          "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
          "name": "US Social Security Number",
          "type": "custom"
        }
      ],
      "entry_count": 3
    },
    "updated_at": "2019-12-27T18:11:19.117Z",
    "words": [
      {
        "weight": "strong",
        "word": "social security number"
      }
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
    "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
    "created_at": "2019-12-27T18:11:19.117Z",
    "name": "HIPAA context words",
    "referenced_by": {
      "entries": [
        {
          "id": "182bd5e5-6e1a-4fe4-a799-aa6d9a6ab26e",
          "name": "US Social Security Number",
          "type": "custom"
        }
      ],
      "entry_count": 3
    },
    "updated_at": "2019-12-27T18:11:19.117Z",
    "words": [
      {
        "weight": "strong",
        "word": "social security number"
      }
    ]
  }
}
```