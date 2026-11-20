---
title: Capture multiple page formats.
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Browser Rendering](https://developers.cloudflare.com/api/resources/browser_rendering)

[Snapshot](https://developers.cloudflare.com/api/resources/browser_rendering/subresources/snapshot)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Capture multiple page formats.

POST/accounts/{account\_id}/browser-rendering/snapshot

Capture at least two formats from one prepared page: HTML, screenshot, Markdown, accessibility tree, PDF, links, scrape, or JSON. Defaults to HTML and screenshot. Format-specific options use the same fields as standalone actions. Scrape requires elements. An origin 304 returns HTTP 200 with an empty result and meta.status 304, without captures or AI work, and is not cached. JSON snapshots share one actionTimeout budget across navigation, captures, retries, and AI (default 60 seconds, maximum 120 seconds). Other snapshots retain existing timeout behavior. Formats use a fixed capture order, not array order; a live page may change between captures. Any format failure fails the request.

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

`Browser Rendering Write`

##### P ath ParametersExpand Collapse

account\_id: string

Account ID.

[Link to this property](#)%20browser_rendering.snapshot%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20account_id%20%3E%20(schema)>)

##### Q uery ParametersExpand Collapse

browser: optional "kitesurf"

Rendering backend. Set to `kitesurf` to use Kitesurf (beta).

[Link to this property](#)%20browser_rendering.snapshot%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20browser%20%3E%20(schema)>)

cacheTTL: optional number

Cache TTL default is 5s. Set to 0 to disable.

maximum86400

minimum0

[Link to this property](#)%20browser_rendering.snapshot%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20cacheTTL%20%3E%20(schema)>)

##### Body ParametersJSONExpand Collapse

<details>

<summary>

body: object {url, actionTimeout, addScriptTag, 30 more } or object {html, actionTimeout, addScriptTag, 30 more }

</summary>

One of the following:

<details>

<summary>

object {url, actionTimeout, addScriptTag, 30 more }

</summary>

url: string

<a href="#">Link to this property</a>

actionTimeout: optional number

The maximum duration allowed for the browser action to complete after the page has loaded (such as taking screenshots, extracting content, or generating PDFs). If this time limit is exceeded, the action stops and returns a timeout error.

maximum120000

<a href="#">Link to this property</a>

<details>

<summary>

addScriptTag: optional array of object {id, content, type, url }

Adds a script element into the page with the desired URL or content.

</summary>

id: optional string

<a href="#">Link to this property</a>

content: optional string

<a href="#">Link to this property</a>

type: optional string

<a href="#">Link to this property</a>

url: optional string

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

addStyleTag: optional array of object {content, url }

Adds a <code>&lt;link rel="stylesheet"&gt;</code> tag into the page with the desired URL or a <code>&lt;style type="text/css"&gt;</code> tag with the content.

</summary>

content: optional string

<a href="#">Link to this property</a>

url: optional string

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

allowRequestPattern: optional array of string

Only allow requests that match the provided regex patterns, eg. ’/^.\*.(css)’. Reject rules are applied first.

<a href="#">Link to this property</a>

<details>

<summary>

allowResourceTypes: optional array of "document"or "stylesheet"or "image"or 15 more

Only allow requests that match the provided resource types, eg. ‘image’ or ‘script’. Reject rules are applied first.

</summary>

One of the following:

"document"

<a href="#">Link to this property</a>

"stylesheet"

<a href="#">Link to this property</a>

"image"

<a href="#">Link to this property</a>

"media"

<a href="#">Link to this property</a>

"font"

<a href="#">Link to this property</a>

"script"

<a href="#">Link to this property</a>

"texttrack"

<a href="#">Link to this property</a>

"xhr"

<a href="#">Link to this property</a>

"fetch"

<a href="#">Link to this property</a>

"prefetch"

<a href="#">Link to this property</a>

"eventsource"

<a href="#">Link to this property</a>

"websocket"

<a href="#">Link to this property</a>

"manifest"

<a href="#">Link to this property</a>

"signedexchange"

<a href="#">Link to this property</a>

"ping"

<a href="#">Link to this property</a>

"cspviolationreport"

<a href="#">Link to this property</a>

"preflight"

<a href="#">Link to this property</a>

"other"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

authenticate: optional object {password, username }

Provide credentials for HTTP authentication.

</summary>

password: string

minLength1

<a href="#">Link to this property</a>

username: string

minLength1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

bestAttempt: optional boolean

Attempt to proceed when ‘awaited’ events fail or timeout.

<a href="#">Link to this property</a>

<details>

<summary>

cookies: optional array of object {name, value, domain, 11 more }

Check <a href="https://pptr.dev/api/puppeteer.page.setcookie">options</a>.

</summary>

name: string

Cookie name.

<a href="#">Link to this property</a>

value: string

<a href="#">Link to this property</a>

domain: optional string

<a href="#">Link to this property</a>

expires: optional number

<a href="#">Link to this property</a>

httpOnly: optional boolean

<a href="#">Link to this property</a>

partitionKey: optional string

<a href="#">Link to this property</a>

path: optional string

<a href="#">Link to this property</a>

<details>

<summary>

priority: optional "Low"or "Medium"or "High"

</summary>

One of the following:

"Low"

<a href="#">Link to this property</a>

"Medium"

<a href="#">Link to this property</a>

"High"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

sameParty: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

sameSite: optional "Strict"or "Lax"or "None"

</summary>

One of the following:

"Strict"

<a href="#">Link to this property</a>

"Lax"

<a href="#">Link to this property</a>

"None"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

secure: optional boolean

<a href="#">Link to this property</a>

sourcePort: optional number

<a href="#">Link to this property</a>

<details>

<summary>

sourceScheme: optional "Unset"or "NonSecure"or "Secure"

</summary>

One of the following:

"Unset"

<a href="#">Link to this property</a>

"NonSecure"

<a href="#">Link to this property</a>

"Secure"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

url: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

custom\_ai: optional array of object {model, authorization }

Optional list of custom AI models to use for the request. The models will be tried in the order provided, and in case a model returns an error, the next one will be used as fallback.

</summary>

model: string

AI model to use for the request. Must be formed as <code>&lt;provider&gt;/&lt;model_name&gt;</code>, e.g. <code>workers-ai/@cf/meta/llama-3.3-70b-instruct-fp8-fast</code>.

<a href="#">Link to this property</a>

authorization: optional string

Authorization token for the AI model: <code>Bearer &lt;token&gt;</code>. Not needed for workers-ai models.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

elements: optional array of object {selector }

</summary>

selector: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

emulateMediaType: optional string

<a href="#">Link to this property</a>

excludeExternalLinks: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

formats: optional array of "content"or "screenshot"or "markdown"or 5 more

</summary>

One of the following:

"content"

<a href="#">Link to this property</a>

"screenshot"

<a href="#">Link to this property</a>

"markdown"

<a href="#">Link to this property</a>

"accessibilityTree"

<a href="#">Link to this property</a>

"pdf"

<a href="#">Link to this property</a>

"links"

<a href="#">Link to this property</a>

"scrape"

<a href="#">Link to this property</a>

"json"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

gotoOptions: optional object {referer, referrerPolicy, timeout, waitUntil }

Check <a href="https://pptr.dev/api/puppeteer.gotooptions">options</a>.

</summary>

referer: optional string

<a href="#">Link to this property</a>

referrerPolicy: optional string

<a href="#">Link to this property</a>

timeout: optional number

maximum60000

<a href="#">Link to this property</a>

<details>

<summary>

waitUntil: optional "load"or "domcontentloaded"or "networkidle0"or "networkidle2"or array of "load"or "domcontentloaded"or "networkidle0"or "networkidle2"

</summary>

One of the following:

<details>

<summary>

"load"or "domcontentloaded"or "networkidle0"or "networkidle2"

</summary>

One of the following:

"load"

<a href="#">Link to this property</a>

"domcontentloaded"

<a href="#">Link to this property</a>

"networkidle0"

<a href="#">Link to this property</a>

"networkidle2"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

array of "load"or "domcontentloaded"or "networkidle0"or "networkidle2"

</summary>

One of the following:

"load"

<a href="#">Link to this property</a>

"domcontentloaded"

<a href="#">Link to this property</a>

"networkidle0"

<a href="#">Link to this property</a>

"networkidle2"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

html: optional string

<a href="#">Link to this property</a>

interestingOnly: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

pdfOptions: optional object {displayHeaderFooter, footerTemplate, format, 13 more }

Check <a href="https://pptr.dev/api/puppeteer.pdfoptions">options</a>.

</summary>

displayHeaderFooter: optional boolean

Whether to show the header and footer.

<a href="#">Link to this property</a>

footerTemplate: optional string

HTML template for the print footer.

<a href="#">Link to this property</a>

<details>

<summary>

format: optional "letter"or "legal"or "tabloid"or 8 more

Paper format. Takes priority over width and height if set.

</summary>

One of the following:

"letter"

<a href="#">Link to this property</a>

"legal"

<a href="#">Link to this property</a>

"tabloid"

<a href="#">Link to this property</a>

"ledger"

<a href="#">Link to this property</a>

"a0"

<a href="#">Link to this property</a>

"a1"

<a href="#">Link to this property</a>

"a2"

<a href="#">Link to this property</a>

"a3"

<a href="#">Link to this property</a>

"a4"

<a href="#">Link to this property</a>

"a5"

<a href="#">Link to this property</a>

"a6"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

headerTemplate: optional string

HTML template for the print header.

<a href="#">Link to this property</a>

<details>

<summary>

height: optional stringor number

Sets the height of paper. Can be a number or string with unit.

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

landscape: optional boolean

Whether to print in landscape orientation.

<a href="#">Link to this property</a>

<details>

<summary>

margin: optional object {bottom, left, right, top }

Set the PDF margins. Useful when setting header and footer.

</summary>

<details>

<summary>

bottom: optional stringor number

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

left: optional stringor number

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

right: optional stringor number

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

top: optional stringor number

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

omitBackground: optional boolean

Hides default white background and allows generating pdfs with transparency.

<a href="#">Link to this property</a>

outline: optional boolean

Generate document outline.

<a href="#">Link to this property</a>

pageRanges: optional string

Paper ranges to print, e.g. ‘1-5, 8, 11-13’.

<a href="#">Link to this property</a>

preferCSSPageSize: optional boolean

Give CSS @page size priority over other size declarations.

<a href="#">Link to this property</a>

printBackground: optional boolean

Set to true to print background graphics.

<a href="#">Link to this property</a>

scale: optional number

Scales the rendering of the web page. Amount must be between 0.1 and 2.

maximum2

minimum0.1

<a href="#">Link to this property</a>

tagged: optional boolean

Generate tagged (accessible) PDF.

<a href="#">Link to this property</a>

timeout: optional number

Timeout in milliseconds.

<a href="#">Link to this property</a>

<details>

<summary>

width: optional stringor number

Sets the width of paper. Can be a number or string with unit.

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

prompt: optional string

<a href="#">Link to this property</a>

rejectRequestPattern: optional array of string

Block undesired requests that match the provided regex patterns, eg. ’/^.\*.(css)’.

<a href="#">Link to this property</a>

<details>

<summary>

rejectResourceTypes: optional array of "document"or "stylesheet"or "image"or 15 more

Block undesired requests that match the provided resource types, eg. ‘image’ or ‘script’.

</summary>

One of the following:

"document"

<a href="#">Link to this property</a>

"stylesheet"

<a href="#">Link to this property</a>

"image"

<a href="#">Link to this property</a>

"media"

<a href="#">Link to this property</a>

"font"

<a href="#">Link to this property</a>

"script"

<a href="#">Link to this property</a>

"texttrack"

<a href="#">Link to this property</a>

"xhr"

<a href="#">Link to this property</a>

"fetch"

<a href="#">Link to this property</a>

"prefetch"

<a href="#">Link to this property</a>

"eventsource"

<a href="#">Link to this property</a>

"websocket"

<a href="#">Link to this property</a>

"manifest"

<a href="#">Link to this property</a>

"signedexchange"

<a href="#">Link to this property</a>

"ping"

<a href="#">Link to this property</a>

"cspviolationreport"

<a href="#">Link to this property</a>

"preflight"

<a href="#">Link to this property</a>

"other"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

response\_format: optional object {type, json\_schema }

</summary>

type: string

<a href="#">Link to this property</a>

json\_schema: optional map\[unknown]

Schema for the response format. More information here: <a href="https://developers.cloudflare.com/workers-ai/json-mode/">https://developers.cloudflare.com/workers-ai/json-mode/</a>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

root: optional string

<a href="#">Link to this property</a>

<details>

<summary>

screenshotOptions: optional object {captureBeyondViewport, clip, fromSurface, 5 more }

</summary>

captureBeyondViewport: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

clip: optional object {height, width, x, 2 more }

</summary>

height: number

<a href="#">Link to this property</a>

width: number

<a href="#">Link to this property</a>

x: number

<a href="#">Link to this property</a>

y: number

<a href="#">Link to this property</a>

scale: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

fromSurface: optional boolean

<a href="#">Link to this property</a>

fullPage: optional boolean

<a href="#">Link to this property</a>

omitBackground: optional boolean

<a href="#">Link to this property</a>

optimizeForSpeed: optional boolean

<a href="#">Link to this property</a>

quality: optional number

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "png"or "jpeg"or "webp"

</summary>

One of the following:

"png"

<a href="#">Link to this property</a>

"jpeg"

<a href="#">Link to this property</a>

"webp"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

scrollPage: optional boolean

<a href="#">Link to this property</a>

selector: optional string

<a href="#">Link to this property</a>

setExtraHTTPHeaders: optional map\[string]

<a href="#">Link to this property</a>

setJavaScriptEnabled: optional boolean

<a href="#">Link to this property</a>

userAgent: optional string

<a href="#">Link to this property</a>

<details>

<summary>

viewport: optional object {height, width, deviceScaleFactor, 3 more }

Check <a href="https://pptr.dev/api/puppeteer.page.setviewport">options</a>.

</summary>

height: number

<a href="#">Link to this property</a>

width: number

<a href="#">Link to this property</a>

deviceScaleFactor: optional number

<a href="#">Link to this property</a>

hasTouch: optional boolean

<a href="#">Link to this property</a>

isLandscape: optional boolean

<a href="#">Link to this property</a>

isMobile: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

visibleLinksOnly: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

waitForSelector: optional object {selector, hidden, timeout, visible }

Wait for the selector to appear in page. Check <a href="https://pptr.dev/api/puppeteer.page.waitforselector">options</a>.

</summary>

selector: string

<a href="#">Link to this property</a>

hidden: optional true

<a href="#">Link to this property</a>

timeout: optional number

maximum120000

<a href="#">Link to this property</a>

visible: optional true

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

waitForTimeout: optional number

Waits for a specified timeout before continuing.

maximum120000

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

object {html, actionTimeout, addScriptTag, 30 more }

</summary>

html: string

<a href="#">Link to this property</a>

actionTimeout: optional number

The maximum duration allowed for the browser action to complete after the page has loaded (such as taking screenshots, extracting content, or generating PDFs). If this time limit is exceeded, the action stops and returns a timeout error.

maximum120000

<a href="#">Link to this property</a>

<details>

<summary>

addScriptTag: optional array of object {id, content, type, url }

Adds a script element into the page with the desired URL or content.

</summary>

id: optional string

<a href="#">Link to this property</a>

content: optional string

<a href="#">Link to this property</a>

type: optional string

<a href="#">Link to this property</a>

url: optional string

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

addStyleTag: optional array of object {content, url }

Adds a <code>&lt;link rel="stylesheet"&gt;</code> tag into the page with the desired URL or a <code>&lt;style type="text/css"&gt;</code> tag with the content.

</summary>

content: optional string

<a href="#">Link to this property</a>

url: optional string

formaturi

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

allowRequestPattern: optional array of string

Only allow requests that match the provided regex patterns, eg. ’/^.\*.(css)’. Reject rules are applied first.

<a href="#">Link to this property</a>

<details>

<summary>

allowResourceTypes: optional array of "document"or "stylesheet"or "image"or 15 more

Only allow requests that match the provided resource types, eg. ‘image’ or ‘script’. Reject rules are applied first.

</summary>

One of the following:

"document"

<a href="#">Link to this property</a>

"stylesheet"

<a href="#">Link to this property</a>

"image"

<a href="#">Link to this property</a>

"media"

<a href="#">Link to this property</a>

"font"

<a href="#">Link to this property</a>

"script"

<a href="#">Link to this property</a>

"texttrack"

<a href="#">Link to this property</a>

"xhr"

<a href="#">Link to this property</a>

"fetch"

<a href="#">Link to this property</a>

"prefetch"

<a href="#">Link to this property</a>

"eventsource"

<a href="#">Link to this property</a>

"websocket"

<a href="#">Link to this property</a>

"manifest"

<a href="#">Link to this property</a>

"signedexchange"

<a href="#">Link to this property</a>

"ping"

<a href="#">Link to this property</a>

"cspviolationreport"

<a href="#">Link to this property</a>

"preflight"

<a href="#">Link to this property</a>

"other"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

authenticate: optional object {password, username }

Provide credentials for HTTP authentication.

</summary>

password: string

minLength1

<a href="#">Link to this property</a>

username: string

minLength1

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

bestAttempt: optional boolean

Attempt to proceed when ‘awaited’ events fail or timeout.

<a href="#">Link to this property</a>

<details>

<summary>

cookies: optional array of object {name, value, domain, 11 more }

Check <a href="https://pptr.dev/api/puppeteer.page.setcookie">options</a>.

</summary>

name: string

Cookie name.

<a href="#">Link to this property</a>

value: string

<a href="#">Link to this property</a>

domain: optional string

<a href="#">Link to this property</a>

expires: optional number

<a href="#">Link to this property</a>

httpOnly: optional boolean

<a href="#">Link to this property</a>

partitionKey: optional string

<a href="#">Link to this property</a>

path: optional string

<a href="#">Link to this property</a>

<details>

<summary>

priority: optional "Low"or "Medium"or "High"

</summary>

One of the following:

"Low"

<a href="#">Link to this property</a>

"Medium"

<a href="#">Link to this property</a>

"High"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

sameParty: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

sameSite: optional "Strict"or "Lax"or "None"

</summary>

One of the following:

"Strict"

<a href="#">Link to this property</a>

"Lax"

<a href="#">Link to this property</a>

"None"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

secure: optional boolean

<a href="#">Link to this property</a>

sourcePort: optional number

<a href="#">Link to this property</a>

<details>

<summary>

sourceScheme: optional "Unset"or "NonSecure"or "Secure"

</summary>

One of the following:

"Unset"

<a href="#">Link to this property</a>

"NonSecure"

<a href="#">Link to this property</a>

"Secure"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

url: optional string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

custom\_ai: optional array of object {model, authorization }

Optional list of custom AI models to use for the request. The models will be tried in the order provided, and in case a model returns an error, the next one will be used as fallback.

</summary>

model: string

AI model to use for the request. Must be formed as <code>&lt;provider&gt;/&lt;model_name&gt;</code>, e.g. <code>workers-ai/@cf/meta/llama-3.3-70b-instruct-fp8-fast</code>.

<a href="#">Link to this property</a>

authorization: optional string

Authorization token for the AI model: <code>Bearer &lt;token&gt;</code>. Not needed for workers-ai models.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

elements: optional array of object {selector }

</summary>

selector: string

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

emulateMediaType: optional string

<a href="#">Link to this property</a>

excludeExternalLinks: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

formats: optional array of "content"or "screenshot"or "markdown"or 5 more

</summary>

One of the following:

"content"

<a href="#">Link to this property</a>

"screenshot"

<a href="#">Link to this property</a>

"markdown"

<a href="#">Link to this property</a>

"accessibilityTree"

<a href="#">Link to this property</a>

"pdf"

<a href="#">Link to this property</a>

"links"

<a href="#">Link to this property</a>

"scrape"

<a href="#">Link to this property</a>

"json"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

gotoOptions: optional object {referer, referrerPolicy, timeout, waitUntil }

Check <a href="https://pptr.dev/api/puppeteer.gotooptions">options</a>.

</summary>

referer: optional string

<a href="#">Link to this property</a>

referrerPolicy: optional string

<a href="#">Link to this property</a>

timeout: optional number

maximum60000

<a href="#">Link to this property</a>

<details>

<summary>

waitUntil: optional "load"or "domcontentloaded"or "networkidle0"or "networkidle2"or array of "load"or "domcontentloaded"or "networkidle0"or "networkidle2"

</summary>

One of the following:

<details>

<summary>

"load"or "domcontentloaded"or "networkidle0"or "networkidle2"

</summary>

One of the following:

"load"

<a href="#">Link to this property</a>

"domcontentloaded"

<a href="#">Link to this property</a>

"networkidle0"

<a href="#">Link to this property</a>

"networkidle2"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

array of "load"or "domcontentloaded"or "networkidle0"or "networkidle2"

</summary>

One of the following:

"load"

<a href="#">Link to this property</a>

"domcontentloaded"

<a href="#">Link to this property</a>

"networkidle0"

<a href="#">Link to this property</a>

"networkidle2"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

interestingOnly: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

pdfOptions: optional object {displayHeaderFooter, footerTemplate, format, 13 more }

Check <a href="https://pptr.dev/api/puppeteer.pdfoptions">options</a>.

</summary>

displayHeaderFooter: optional boolean

Whether to show the header and footer.

<a href="#">Link to this property</a>

footerTemplate: optional string

HTML template for the print footer.

<a href="#">Link to this property</a>

<details>

<summary>

format: optional "letter"or "legal"or "tabloid"or 8 more

Paper format. Takes priority over width and height if set.

</summary>

One of the following:

"letter"

<a href="#">Link to this property</a>

"legal"

<a href="#">Link to this property</a>

"tabloid"

<a href="#">Link to this property</a>

"ledger"

<a href="#">Link to this property</a>

"a0"

<a href="#">Link to this property</a>

"a1"

<a href="#">Link to this property</a>

"a2"

<a href="#">Link to this property</a>

"a3"

<a href="#">Link to this property</a>

"a4"

<a href="#">Link to this property</a>

"a5"

<a href="#">Link to this property</a>

"a6"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

headerTemplate: optional string

HTML template for the print header.

<a href="#">Link to this property</a>

<details>

<summary>

height: optional stringor number

Sets the height of paper. Can be a number or string with unit.

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

landscape: optional boolean

Whether to print in landscape orientation.

<a href="#">Link to this property</a>

<details>

<summary>

margin: optional object {bottom, left, right, top }

Set the PDF margins. Useful when setting header and footer.

</summary>

<details>

<summary>

bottom: optional stringor number

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

left: optional stringor number

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

right: optional stringor number

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

top: optional stringor number

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

omitBackground: optional boolean

Hides default white background and allows generating pdfs with transparency.

<a href="#">Link to this property</a>

outline: optional boolean

Generate document outline.

<a href="#">Link to this property</a>

pageRanges: optional string

Paper ranges to print, e.g. ‘1-5, 8, 11-13’.

<a href="#">Link to this property</a>

preferCSSPageSize: optional boolean

Give CSS @page size priority over other size declarations.

<a href="#">Link to this property</a>

printBackground: optional boolean

Set to true to print background graphics.

<a href="#">Link to this property</a>

scale: optional number

Scales the rendering of the web page. Amount must be between 0.1 and 2.

maximum2

minimum0.1

<a href="#">Link to this property</a>

tagged: optional boolean

Generate tagged (accessible) PDF.

<a href="#">Link to this property</a>

timeout: optional number

Timeout in milliseconds.

<a href="#">Link to this property</a>

<details>

<summary>

width: optional stringor number

Sets the width of paper. Can be a number or string with unit.

</summary>

One of the following:

string

<a href="#">Link to this property</a>

number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

prompt: optional string

<a href="#">Link to this property</a>

rejectRequestPattern: optional array of string

Block undesired requests that match the provided regex patterns, eg. ’/^.\*.(css)’.

<a href="#">Link to this property</a>

<details>

<summary>

rejectResourceTypes: optional array of "document"or "stylesheet"or "image"or 15 more

Block undesired requests that match the provided resource types, eg. ‘image’ or ‘script’.

</summary>

One of the following:

"document"

<a href="#">Link to this property</a>

"stylesheet"

<a href="#">Link to this property</a>

"image"

<a href="#">Link to this property</a>

"media"

<a href="#">Link to this property</a>

"font"

<a href="#">Link to this property</a>

"script"

<a href="#">Link to this property</a>

"texttrack"

<a href="#">Link to this property</a>

"xhr"

<a href="#">Link to this property</a>

"fetch"

<a href="#">Link to this property</a>

"prefetch"

<a href="#">Link to this property</a>

"eventsource"

<a href="#">Link to this property</a>

"websocket"

<a href="#">Link to this property</a>

"manifest"

<a href="#">Link to this property</a>

"signedexchange"

<a href="#">Link to this property</a>

"ping"

<a href="#">Link to this property</a>

"cspviolationreport"

<a href="#">Link to this property</a>

"preflight"

<a href="#">Link to this property</a>

"other"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

response\_format: optional object {type, json\_schema }

</summary>

type: string

<a href="#">Link to this property</a>

json\_schema: optional map\[unknown]

Schema for the response format. More information here: <a href="https://developers.cloudflare.com/workers-ai/json-mode/">https://developers.cloudflare.com/workers-ai/json-mode/</a>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

root: optional string

<a href="#">Link to this property</a>

<details>

<summary>

screenshotOptions: optional object {captureBeyondViewport, clip, fromSurface, 5 more }

</summary>

captureBeyondViewport: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

clip: optional object {height, width, x, 2 more }

</summary>

height: number

<a href="#">Link to this property</a>

width: number

<a href="#">Link to this property</a>

x: number

<a href="#">Link to this property</a>

y: number

<a href="#">Link to this property</a>

scale: optional number

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

fromSurface: optional boolean

<a href="#">Link to this property</a>

fullPage: optional boolean

<a href="#">Link to this property</a>

omitBackground: optional boolean

<a href="#">Link to this property</a>

optimizeForSpeed: optional boolean

<a href="#">Link to this property</a>

quality: optional number

<a href="#">Link to this property</a>

<details>

<summary>

type: optional "png"or "jpeg"or "webp"

</summary>

One of the following:

"png"

<a href="#">Link to this property</a>

"jpeg"

<a href="#">Link to this property</a>

"webp"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

scrollPage: optional boolean

<a href="#">Link to this property</a>

selector: optional string

<a href="#">Link to this property</a>

setExtraHTTPHeaders: optional map\[string]

<a href="#">Link to this property</a>

setJavaScriptEnabled: optional boolean

<a href="#">Link to this property</a>

url: optional string

<a href="#">Link to this property</a>

userAgent: optional string

<a href="#">Link to this property</a>

<details>

<summary>

viewport: optional object {height, width, deviceScaleFactor, 3 more }

Check <a href="https://pptr.dev/api/puppeteer.page.setviewport">options</a>.

</summary>

height: number

<a href="#">Link to this property</a>

width: number

<a href="#">Link to this property</a>

deviceScaleFactor: optional number

<a href="#">Link to this property</a>

hasTouch: optional boolean

<a href="#">Link to this property</a>

isLandscape: optional boolean

<a href="#">Link to this property</a>

isMobile: optional boolean

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

visibleLinksOnly: optional boolean

<a href="#">Link to this property</a>

<details>

<summary>

waitForSelector: optional object {selector, hidden, timeout, visible }

Wait for the selector to appear in page. Check <a href="https://pptr.dev/api/puppeteer.page.waitforselector">options</a>.

</summary>

selector: string

<a href="#">Link to this property</a>

hidden: optional true

<a href="#">Link to this property</a>

timeout: optional number

maximum120000

<a href="#">Link to this property</a>

visible: optional true

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

waitForTimeout: optional number

Waits for a specified timeout before continuing.

maximum120000

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20browser_rendering.snapshot%20%3E%20(method)%20create%20%3E%20(params)%200%20%3E%20(param)%20body%20%3E%20(schema)>)

##### ReturnsExpand Collapse

<details>

<summary>

meta: object {finalUrl, headers, redirectChain, 2 more }

</summary>

finalUrl: optional string

URL that served the response, after any redirects the browser followed.

<a href="#">Link to this property</a>

headers: optional map\[string]

Origin response headers, lowercased. Repeated headers are joined with a newline. Credential and transport-only headers that do not survive rendering are omitted.

<a href="#">Link to this property</a>

<details>

<summary>

redirectChain: optional array of object {headers, status, url }

HTTP redirects followed to reach <code>finalUrl</code>, oldest first. Omitted for direct navigation and for client-side redirects such as meta refresh. An empty array means redirects occurred but their intermediate responses could not be read.

</summary>

headers: map\[string]

Redirect response headers, including <code>location</code>.

<a href="#">Link to this property</a>

status: number

HTTP status of the redirect.

<a href="#">Link to this property</a>

url: string

URL that returned the redirect.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

status: optional number

HTTP status returned by the origin.

<a href="#">Link to this property</a>

title: optional string

Page title.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20browser_rendering.snapshot%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20meta>)

success: boolean

Response status.

[Link to this property](#)%20browser_rendering.snapshot%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20success>)

<details>

<summary>

errors: optional array of object {code, message }

</summary>

code: number

Error code.

<a href="#">Link to this property</a>

message: string

Error message.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20browser_rendering.snapshot%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20errors>)

<details>

<summary>

result: optional object {accessibilityTree, content, json, 5 more }

</summary>

<details>

<summary>

accessibilityTree: optional object {role, autocomplete, checked, 23 more }

Accessibility tree node

</summary>

role: string

<a href="#">Link to this property</a>

autocomplete: optional string

<a href="#">Link to this property</a>

<details>

<summary>

checked: optional booleanor "mixed"

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

pressed: optional booleanor "mixed"

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

value: optional stringor number

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

json: optional map\[unknown]or array of unknown

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

scrape: optional array of object {results, selector }

Elements matched by the requested selectors.

</summary>

<details>

<summary>

results: array of object {attributes, html, left, 4 more }

</summary>

<details>

<summary>

attributes: array of object {name, value }

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

[Link to this property](#)%20browser_rendering.snapshot%20%3E%20(method)%20create%20%3E%20(network%20schema)%20%3E%20(property)%20result>)

### Capture multiple page formats.

HTTP

HTTPTypeScriptPythonGoTerraform

```
curl https://api.cloudflare.com/client/v4/accounts/$ACCOUNT_ID/browser-rendering/snapshot \
    -H 'Content-Type: application/json' \
    -H "Authorization: Bearer $CLOUDFLARE_API_TOKEN" \
    -d '{
          "url": "url"
        }'
```

200 example

429 example

```
{
  "meta": {
    "finalUrl": "finalUrl",
    "headers": {
      "foo": "string"
    },
    "redirectChain": [
      {
        "headers": {
          "foo": "string"
        },
        "status": 0,
        "url": "url"
      }
    ],
    "status": 0,
    "title": "title"
  },
  "success": true,
  "errors": [
    {
      "code": 0,
      "message": "message"
    }
  ],
  "result": {
    "accessibilityTree": {
      "role": "role",
      "autocomplete": "autocomplete",
      "checked": "mixed",
      "children": [
        {}
      ],
      "description": "description",
      "disabled": true,
      "expanded": true,
      "focused": true,
      "haspopup": "haspopup",
      "invalid": "invalid",
      "keyshortcuts": "keyshortcuts",
      "level": 0,
      "modal": true,
      "multiline": true,
      "multiselectable": true,
      "name": "name",
      "orientation": "orientation",
      "pressed": "mixed",
      "readonly": true,
      "required": true,
      "roledescription": "roledescription",
      "selected": true,
      "value": "string",
      "valuemax": 0,
      "valuemin": 0,
      "valuetext": "valuetext"
    },
    "content": "content",
    "json": {
      "foo": "bar"
    },
    "links": [
      "string"
    ],
    "markdown": "markdown",
    "pdf": "pdf",
    "scrape": [
      {
        "results": [
          {
            "attributes": [
              {
                "name": "name",
                "value": "value"
              }
            ],
            "html": "html",
            "left": 0,
            "top": 0,
            "height": 0,
            "text": "text",
            "width": 0
          }
        ],
        "selector": "selector"
      }
    ],
    "screenshot": "screenshot"
  }
}
```

```
{
  "errors": [
    {
      "code": 2001,
      "message": "Rate limit exceeded"
    }
  ],
  "success": false
}
```

##### Returns Examples

200 example

429 example

```
{
  "meta": {
    "finalUrl": "finalUrl",
    "headers": {
      "foo": "string"
    },
    "redirectChain": [
      {
        "headers": {
          "foo": "string"
        },
        "status": 0,
        "url": "url"
      }
    ],
    "status": 0,
    "title": "title"
  },
  "success": true,
  "errors": [
    {
      "code": 0,
      "message": "message"
    }
  ],
  "result": {
    "accessibilityTree": {
      "role": "role",
      "autocomplete": "autocomplete",
      "checked": "mixed",
      "children": [
        {}
      ],
      "description": "description",
      "disabled": true,
      "expanded": true,
      "focused": true,
      "haspopup": "haspopup",
      "invalid": "invalid",
      "keyshortcuts": "keyshortcuts",
      "level": 0,
      "modal": true,
      "multiline": true,
      "multiselectable": true,
      "name": "name",
      "orientation": "orientation",
      "pressed": "mixed",
      "readonly": true,
      "required": true,
      "roledescription": "roledescription",
      "selected": true,
      "value": "string",
      "valuemax": 0,
      "valuemin": 0,
      "valuetext": "valuetext"
    },
    "content": "content",
    "json": {
      "foo": "bar"
    },
    "links": [
      "string"
    ],
    "markdown": "markdown",
    "pdf": "pdf",
    "scrape": [
      {
        "results": [
          {
            "attributes": [
              {
                "name": "name",
                "value": "value"
              }
            ],
            "html": "html",
            "left": 0,
            "top": 0,
            "height": 0,
            "text": "text",
            "width": 0
          }
        ],
        "selector": "selector"
      }
    ],
    "screenshot": "screenshot"
  }
}
```

```
{
  "errors": [
    {
      "code": 2001,
      "message": "Rate limit exceeded"
    }
  ],
  "success": false
}
```