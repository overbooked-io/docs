---
description: Creates new Booking object.
---

# Create a Booking

{% api-method method="post" host="https://api.overbooked.io" path="/bookings" %}
{% api-method-summary %}
public.booking.create
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer `{public_key|secret_key}`
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="slot\_id" type="string" required=true %}
The Slot's id \(uuid\)
{% endapi-method-parameter %}

{% api-method-parameter name="lock\_key" type="string" required=false %}
A unique, random string used to distinguish a lock. The lock key in this given operation is used to unlock the Slot's lock.
{% endapi-method-parameter %}

{% api-method-parameter name="metadata" type="object" required=false %}
Set of key-value data that you can attach to the Booking
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

{% code title="public.booking.create" %}
```javascript
{
  "data": {
    "_object": "booking",
    "resource_id": "f968320f-300e-4da4-8fbb-6c5d8d9cc93a",
    "created_at": "2020-12-10T18:55:24.555Z",
    "id": "b1ad4b5b-2e94-44aa-be51-66afb8d2da13",
    "metadata": {},
    "slot_id": "e943cb7b-d17c-4271-85d9-bd2b87008c6e",
    "status": "active",
    "updated_at": "2020-12-10T18:55:24.555Z"
  },
  "meta": {},
  "success": true
}
```
{% endcode %}
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% tabs %}
{% tab title="JavaScript/Node.js" %}
```javascript
const overbooked = new Overbooked.Client({ ... })

const { data, error, meta, success } = await overbooked.booking.create({
    slot_id: "21ac36b-d758-4fce-b8fe-0ca7vf8dabe0"
})
    
console.log(data) // created booking
```
{% endtab %}
{% endtabs %}

