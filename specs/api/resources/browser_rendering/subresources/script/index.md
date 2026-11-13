---
title: Script
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Browser Rendering](https://developers.cloudflare.com/api/resources/browser_rendering)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Script

##### [Dynamic Script - execute code and return browser session details.](https://developers.cloudflare.com/api/resources/browser_rendering/subresources/script/methods/create)

POST/accounts/{account\_id}/browser-rendering/script

##### [Dynamic Script - execute code in an existing browser session.](https://developers.cloudflare.com/api/resources/browser_rendering/subresources/script/methods/execute)

POST/accounts/{account\_id}/browser-rendering/script/{session\_id}

##### ModelsExpand Collapse

<details>

<summary>

ScriptCreateResponse = stringor numberor booleanor 2 more

The script’s return value, or null when it returned nothing. Arrays nested inside arrays are also returned, but this schema does not describe them.

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

boolean

<a href="#">Link to this property</a>

map\[unknown]

<a href="#">Link to this property</a>

<details>

<summary>

array of stringor numberor booleanor map\[unknown]

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

boolean

<a href="#">Link to this property</a>

map\[unknown]

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20browser_rendering.script%20%3E%20(model)%20script_create_response%20%3E%20(schema)>)

<details>

<summary>

ScriptExecuteResponse = stringor numberor booleanor 2 more

The script’s return value, or null when it returned nothing. Arrays nested inside arrays are also returned, but this schema does not describe them.

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

boolean

<a href="#">Link to this property</a>

map\[unknown]

<a href="#">Link to this property</a>

<details>

<summary>

array of stringor numberor booleanor map\[unknown]

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

boolean

<a href="#">Link to this property</a>

map\[unknown]

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20browser_rendering.script%20%3E%20(model)%20script_execute_response%20%3E%20(schema)>)