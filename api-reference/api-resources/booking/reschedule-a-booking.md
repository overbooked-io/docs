---
description: Reschedules the Booking to a different Slot.
---

# Reschedule a Booking

{% api-method method="post" host="https://api.overbooked.io" path="/bookings/:booking\_id/reschedule" %}
{% api-method-summary %}
public.booking.reschedule
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
Bearer `{public_key|secret_key}`
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="target\_slot\_id" type="string" required=true %}
The Slot's id that Booking is being rescheduled to.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

{% code title="public.booking.reschedule" %}
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
{% tab title="Javascript/Node.js" %}
```javascript
const overbooked = new Overbooked.Client({ ... })

const { data, error, meta, success } = await overbooked.booking.reschedule(
  "21b2c36b-f458-4fce-b8fe-0ca48f8dcbe0",
  {
    target_slot_id: "67b2c36a-fg12-4fce-b8fe-0ca45fadcbe0"
  }
)
 
console.log(data) // recheduled booking
```
{% endtab %}
{% endtabs %}

