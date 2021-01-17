---
description: >-
  The Overbooked API uses API keys to authenticate requests. The authentication
  is performed via Bearer Token Authentication.
---

# Authentication

## API Keys

Two types of keys can be distinguished, **public key** and **secret key.** You can read about the differences between them [here](authentication.md#public-key-and-secret-key).

To undergo the authentication process, provide your API key in `Authorization` HTTP header.

```bash
-H 'Authorization: Bearer <api_key>'
```

### Example

{% tabs %}
{% tab title="cURL" %}
```bash
curl https://api.overbooked.io/resources \
  -H 'Authorization: Bearer sk_da57d6a3fc6dc1c38877c99b5623c5a7ea99d305cb0ff0d072f3fafd99dd31c8'
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
All API requests must be made over [HTTPS](http://en.wikipedia.org/wiki/HTTP_Secure). Calls made over plain HTTP will fail. API requests without authentication will also fail.
{% endhint %}

### Public key and secret key

When you create the Overbooked organization, a public key and secret key will be created for you. These are located in your [environment settings](https://dashboard.overbooked.io/settings/environments) in the Overbooked Dashboard.

![](../.gitbook/assets/screenshot-from-2020-12-08-20-14-43.png)

{% hint style="danger" %}
Your API keys carry many privileges, so be sure to keep them secure! Do not share your secret keys in publicly accessible areas such as GitHub, client-side code, and so forth.
{% endhint %}

You can distinguish API keys with prefixes. Examples:

* Public key: `pk_437543662afd2bdb6cc1bf825a3f8ed9d25a9a900faf39fba14f99a02c7edbaf`
* Secret key: `sk_ed7379a4094f2e3bee899f91fccd68e878dc72c9be62928979726d9993c7891c`

{% hint style="warning" %}
The keys have different permission levels. The public key can be easily used on **the client-side**, while the private key should be secured and used only on **the server-side**.
{% endhint %}

Each API method has its own security level. Some endpoints are publicly accessible, others are only accessible via a secret key. You can find out more by checking the description of a specific method.

