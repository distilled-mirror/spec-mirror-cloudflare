---
title: Payload Logging
---

[Skip to content](#_top)

[API Reference](https://developers.cloudflare.com/api)

[Firewall](https://developers.cloudflare.com/api/resources/firewall)

Copy Markdown

Open in **Claude**Open in **ChatGPT**Open in **Cursor**

---

**Copy Markdown****View as Markdown**

# Payload Logging

##### [Get the payload logging key](https://developers.cloudflare.com/api/resources/firewall/subresources/payload_logging/methods/get)

GET/{accounts\_or\_zones}/{account\_or\_zone\_id}/firewall/payload\_logging/key

##### [Set the payload logging key](https://developers.cloudflare.com/api/resources/firewall/subresources/payload_logging/methods/update)

PUT/{accounts\_or\_zones}/{account\_or\_zone\_id}/firewall/payload\_logging/key

##### [Delete the payload logging key](https://developers.cloudflare.com/api/resources/firewall/subresources/payload_logging/methods/delete)

DELETE/{accounts\_or\_zones}/{account\_or\_zone\_id}/firewall/payload\_logging/key

##### ModelsExpand Collapse

<details>

<summary>

PayloadLoggingKey object {public\_key }

</summary>

public\_key: string

Defines the X25519 public key, as standard base64 of exactly 32 bytes, that encrypts matched payloads. Cloudflare stores only the public key; keep the private key to decrypt logged payloads.

maxLength44

minLength44

<a href="#">Link to this property</a>

</details>

[Link to this property](#)%20firewall.payload_logging%20%3E%20(model)%20payload_logging_key%20%3E%20(schema)>)