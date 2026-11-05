---
title: Logo Matches
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Brand Protection](https://developers.cloudflare.com/api/resources/brand_protection)

[V2](https://developers.cloudflare.com/api/resources/brand_protection/subresources/v2)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Logo Matches

##### [List logo matches](https://developers.cloudflare.com/api/resources/brand_protection/subresources/v2/subresources/logo_matches/methods/get)

GET/accounts/{account\_id}/cloudforce-one/v2/brand-protection/logo/matches

##### ModelsExpand Collapse

<details>

<summary>

LogoMatchGetResponse object {matches, total }

</summary>

<details>

<summary>

matches: array of object {id, domain, matched\_at, 6 more }

</summary>

id: number

ID of the logo match.

<a href="#">Link to this property</a>

domain: string

Domain where the matching image was found, if known.

<a href="#">Link to this property</a>

matched\_at: string

When the match was recorded.

<a href="#">Link to this property</a>

query\_id: number

ID of the logo query that produced this match.

<a href="#">Link to this property</a>

registrar: string

Registrar of <code>domain</code>, if known.

<a href="#">Link to this property</a>

similarity\_score: number

Visual similarity between the matched image and the query logo. Higher is closer.

<a href="#">Link to this property</a>

url\_scan\_id: string

<a href="#">Link to this property</a>

content\_type: optional string

MIME type of the matched image (only present when download=true)

<a href="#">Link to this property</a>

image\_data: optional string

Base64-encoded matched image (only present when download=true)

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

total: number

minimum0

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20brand_protection.v2.logo_matches%20%3E%20(model)%20logo_match_get_response%20%3E%20(schema)>)