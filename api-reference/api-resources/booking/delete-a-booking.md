---
description: Permanently deletes the Booking.
---

# Delete a Booking

{% api-method method="delete" host="https://api.overbooked.io" path="/bookings/:booking\_id" %}
{% api-method-summary %}
public.booking.delete
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="booking\_id" type="string" required=true %}
Unique identifier of the Booking
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer `{secret_key}`
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

{% code title="public.booking.delete" %}
```javascript
{
  "data": {},
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
{% tab title="Javascript/Node.js" %}
```javascript
const overbooked = new Overbooked.Client({ ... })

const {error, meta, success } = await overbooked.slot.delete({
  booking_id: "21b2c36b-f458-4fce-b8fe-0ca48f8dcbe0"
})
```
{% endtab %}
{% endtabs %}

