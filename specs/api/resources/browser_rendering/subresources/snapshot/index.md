---
title: Snapshot
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Browser Rendering](https://developers.cloudflare.com/api/resources/browser_rendering)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Snapshot

##### [Capture multiple page formats.](https://developers.cloudflare.com/api/resources/browser_rendering/subresources/snapshot/methods/create)

POST/accounts/{account\_id}/browser-rendering/snapshot

##### ModelsExpand Collapse

<details>

<summary>

SnapshotCreateResponse object { accessibilityTree, content, json, 5 more }

</summary>

<details>

<summary>

accessibilityTree: optional object { role, autocomplete, checked, 23 more }

Accessibility tree node

</summary>

role: string

<a href="#">Link to this property</a>

autocomplete: optional string

<a href="#">Link to this property</a>

<details>

<summary>

checked: optional boolean or "mixed"

</summary>

One of the following:

boolean

<a href="#">Link to this property</a>

"mixed"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

children: optional array of unknown

<a href="#">Link to this property</a>

description: optional string

<a href="#">Link to this property</a>

disabled: optional boolean

<a href="#">Link to this property</a>

expanded: optional boolean

<a href="#">Link to this property</a>

focused: optional boolean

<a href="#">Link to this property</a>

haspopup: optional string

<a href="#">Link to this property</a>

invalid: optional string

<a href="#">Link to this property</a>

keyshortcuts: optional string

<a href="#">Link to this property</a>

level: optional number

<a href="#">Link to this property</a>

modal: optional boolean

<a href="#">Link to this property</a>

multiline: optional boolean

<a href="#">Link to this property</a>

multiselectable: optional boolean

<a href="#">Link to this property</a>

name: optional string

<a href="#">Link to this property</a>

orientation: optional string

<a href="#">Link to this property</a>

<details>

<summary>

pressed: optional boolean or "mixed"

</summary>

One of the following:

boolean

<a href="#">Link to this property</a>

"mixed"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

readonly: optional boolean

<a href="#">Link to this property</a>

required: optional boolean

<a href="#">Link to this property</a>

roledescription: optional string

<a href="#">Link to this property</a>

selected: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

value: optional string or number

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

valuemax: optional number

<a href="#">Link to this property</a>

valuemin: optional number

<a href="#">Link to this property</a>

valuetext: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

content: optional string

HTML content.

<a href="#">Link to this property</a>

<details>

<summary>

json: optional map\[unknown] or array of unknown

Data extracted from the page HTML by the requested prompt.

</summary>

One of the following:

map\[unknown]

<a href="#">Link to this property</a>

array of unknown

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

links: optional array of string

Links found on the page.

<a href="#">Link to this property</a>

markdown: optional string

Markdown content. Prefixed with YAML frontmatter (e.g. <code>title</code>) when the page provides that metadata.

<a href="#">Link to this property</a>

pdf: optional string

Base64 encoded PDF.

<a href="#">Link to this property</a>

<details>

<summary>

scrape: optional array of object { results, selector }

Elements matched by the requested selectors.

</summary>

<details>

<summary>

results: array of object { attributes, html, left, 4 more }

</summary>

<details>

<summary>

attributes: array of object { name, value }

</summary>

name: string

<a href="#">Link to this property</a>

value: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

html: string

<a href="#">Link to this property</a>

left: number

<a href="#">Link to this property</a>

top: number

<a href="#">Link to this property</a>

height: optional number

<a href="#">Link to this property</a>

text: optional string

<a href="#">Link to this property</a>

width: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

selector: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

screenshot: optional string

Base64 encoded image.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20browser_rendering.snapshot%20%3E%20(model)%20snapshot_create_response%20%3E%20(schema)>)