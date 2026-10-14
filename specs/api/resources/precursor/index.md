---
title: Precursor
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Precursor

##### [Get Zone Precursor Config](https://developers.cloudflare.com/api/resources/precursor/methods/get)

GET/zones/{zone\_id}/precursor

##### [Update Zone Precursor Config](https://developers.cloudflare.com/api/resources/precursor/methods/update)

PUT/zones/{zone\_id}/precursor

##### ModelsExpand Collapse

<details>

<summary>

PrecursorConfig object {mode, rules, show\_interstitial }

</summary>

<details>

<summary>

mode: optional "off"or "monitor"or "arm"

Controls Precursor detection for the zone. <code>off</code> disables detection, <code>monitor</code> records detections without affecting bot scores, and <code>arm</code> allows detections to affect bot scores.

</summary>

One of the following:

"off"

<a href="#">Link to this property</a>

"monitor"

<a href="#">Link to this property</a>

"arm"

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

<details>

<summary>

rules: optional array of object {expression, show\_interstitial, id, 2 more }

The ordered list of Precursor rules for the zone.

</summary>

expression: string

The filter expression that determines which requests the rule matches.

maxLength4000

<a href="#">Link to this property</a>

show\_interstitial: boolean

Whether Precursor shows an interstitial when it takes action on a request.

<a href="#">Link to this property</a>

id: optional string

The read-only identifier that Cloudflare assigns to the rule.

<a href="#">Link to this property</a>

description: optional string

An informative description of the rule.

<a href="#">Link to this property</a>

enabled: optional boolean

Whether the rule is active.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

show\_interstitial: optional boolean

Whether Precursor shows an interstitial when it takes action on a request.

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20precursor%20%3E%20(model)%20precursor_config%20%3E%20(schema)>)