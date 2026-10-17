---
title: Proximity Words
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[DLP](https://developers.cloudflare.com/api/resources/zero_trust/subresources/dlp)

[Validators](https://developers.cloudflare.com/api/resources/zero_trust/subresources/dlp/subresources/validators)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Proximity Words

##### [List proximity word validators](https://developers.cloudflare.com/api/resources/zero_trust/subresources/dlp/subresources/validators/subresources/proximity_words/methods/list)

GET/accounts/{account\_id}/dlp/validators/proximity\_words

##### [Get a proximity word validator](https://developers.cloudflare.com/api/resources/zero_trust/subresources/dlp/subresources/validators/subresources/proximity_words/methods/get)

GET/accounts/{account\_id}/dlp/validators/proximity\_words/{validator\_id}

##### [Create a proximity word validator](https://developers.cloudflare.com/api/resources/zero_trust/subresources/dlp/subresources/validators/subresources/proximity_words/methods/create)

POST/accounts/{account\_id}/dlp/validators/proximity\_words

##### [Update a proximity word validator](https://developers.cloudflare.com/api/resources/zero_trust/subresources/dlp/subresources/validators/subresources/proximity_words/methods/update)

PUT/accounts/{account\_id}/dlp/validators/proximity\_words/{validator\_id}

##### [Delete a proximity word validator](https://developers.cloudflare.com/api/resources/zero_trust/subresources/dlp/subresources/validators/subresources/proximity_words/methods/delete)

DELETE/accounts/{account\_id}/dlp/validators/proximity\_words/{validator\_id}

##### ModelsExpand Collapse

<details>

<summary>

ProximityWordValidator object {id, created\_at, name, 3 more }

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

referenced\_by: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.dlp.validators%20%3E%20(model)%20references%20%3E%20(schema)">References</a> { entries, entry\_count }

What currently uses a validator. Deleting a validator that is still in use returns <code>409</code>, so check this first.

Read-only. A validator is attached or detached by updating the detection entry that uses it, not by writing this back.

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

words: array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.dlp.validators.proximity_words%20%3E%20(model)%20word%20%3E%20(schema)">Word</a> { weight, word }

The words that raise confidence when found near a match.

</summary>

weight: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.dlp.validators.proximity_words%20%3E%20(model)%20weight%20%3E%20(schema)">Weight</a>

How much a word contributes to a match’s confidence when it is found nearby.

Separate from a profile’s high/medium/low confidence threshold: this describes how telling the word is, not how confident the resulting match is.

<a href="#">Link to this property</a>

word: string

The word or phrase to look for. Must contain 1–128 characters and is matched case-insensitively.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.dlp.validators.proximity_words%20%3E%20(model)%20proximity_word_validator%20%3E%20(schema)>)

<details>

<summary>

ProximityWordValidatorArray = array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.dlp.validators.proximity_words%20%3E%20(model)%20proximity_word_validator%20%3E%20(schema)">ProximityWordValidator</a> { id, created\_at, name, 3 more }

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

referenced\_by: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.dlp.validators%20%3E%20(model)%20references%20%3E%20(schema)">References</a> { entries, entry\_count }

What currently uses a validator. Deleting a validator that is still in use returns <code>409</code>, so check this first.

Read-only. A validator is attached or detached by updating the detection entry that uses it, not by writing this back.

<a href="#">Link to this property</a>

updated\_at: string

formatdate-time

<a href="#">Link to this property</a>

<details>

<summary>

words: array of <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.dlp.validators.proximity_words%20%3E%20(model)%20word%20%3E%20(schema)">Word</a> { weight, word }

The words that raise confidence when found near a match.

</summary>

weight: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.dlp.validators.proximity_words%20%3E%20(model)%20weight%20%3E%20(schema)">Weight</a>

How much a word contributes to a match’s confidence when it is found nearby.

Separate from a profile’s high/medium/low confidence threshold: this describes how telling the word is, not how confident the resulting match is.

<a href="#">Link to this property</a>

word: string

The word or phrase to look for. Must contain 1–128 characters and is matched case-insensitively.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.dlp.validators.proximity_words%20%3E%20(model)%20proximity_word_validator_array%20%3E%20(schema)>)

<details>

<summary>

Weight = "strong"or "moderate"or "weak"

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

[Link to this property](#)%20zero_trust.dlp.validators.proximity_words%20%3E%20(model)%20weight%20%3E%20(schema)>)

<details>

<summary>

Word object {weight, word }

A word that raises a match’s confidence when it appears near the match.

</summary>

weight: <a href="https://developers.cloudflare.com/api/resources/zero_trust#(resource)%20zero_trust.dlp.validators.proximity_words%20%3E%20(model)%20weight%20%3E%20(schema)">Weight</a>

How much a word contributes to a match’s confidence when it is found nearby.

Separate from a profile’s high/medium/low confidence threshold: this describes how telling the word is, not how confident the resulting match is.

<a href="#">Link to this property</a>

word: string

The word or phrase to look for. Must contain 1–128 characters and is matched case-insensitively.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.dlp.validators.proximity_words%20%3E%20(model)%20word%20%3E%20(schema)>)

ProximityWordDeleteResponse = unknown

[Link to this property](#)%20zero_trust.dlp.validators.proximity_words%20%3E%20(model)%20proximity_word_delete_response%20%3E%20(schema)>)