---
title: Override Codes
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Zero Trust](https://developers.cloudflare.com/api/resources/zero_trust)

[Devices](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Override Codes

##### [Get override codes (deprecated)](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/override_codes/methods/list)

Deprecated

GET/accounts/{account\_id}/devices/{device\_id}/override\_codes

##### [Get override codes](https://developers.cloudflare.com/api/resources/zero_trust/subresources/devices/subresources/override_codes/methods/get)

GET/accounts/{account\_id}/devices/registrations/{registration\_id}/override\_codes

##### ModelsExpand Collapse

<details>

<summary>

OverrideCodeListResponse object {disable\_for\_time }

</summary>

<details>

<summary>

disable\_for\_time: optional object {"1", "12", "24", 2 more }

</summary>

"1": optional string

Override code that is valid for 1 hour.

<a href="#">Link to this property</a>

"12": optional string

Override code that is valid for 12 hour2.

<a href="#">Link to this property</a>

"24": optional string

Override code that is valid for 24 hour.2.

<a href="#">Link to this property</a>

"3": optional string

Override code that is valid for 3 hours.

<a href="#">Link to this property</a>

"6": optional string

Override code that is valid for 6 hours.

<a href="#">Link to this property</a>

</details>

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.override_codes%20%3E%20(model)%20override_code_list_response%20%3E%20(schema)>)

<details>

<summary>

OverrideCodeGetResponse object {disable\_for\_time }

</summary>

disable\_for\_time: optional map\[string]

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20zero_trust.devices.override_codes%20%3E%20(model)%20override_code_get_response%20%3E%20(schema)>)