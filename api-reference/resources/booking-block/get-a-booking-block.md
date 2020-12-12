---
description: Lorem ipsum...
---

# Get a booking block

{% api-method method="get" host="https://api.overbooked.io" path="/booking-blocks/:booking\_block\_id" %}
{% api-method-summary %}
public.bookingBlock.get
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="booking\_block\_id" type="string" required=true %}
Unique identifier of the Booking Block
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer `{public_key|secret_key}`
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

{% code title="public.bookingBlock.get" %}
```scheme
{
  "data": {
    "_object": "booking_block",
    "booking_disabled_before": 0,
    "created_at": "2020-12-10T18:55:08.749Z",
    "id": "e4e2af17-bc74-483e-9b17-53cbcf907ac4",
    "metadata": {},
    "name": "test_1",
    "num_active_appointments": 7,
    "num_appointments": 7,
    "num_available_slots": 0,
    "num_cancelled_appointments": 0,
    "num_slots": 7,
    "short_id": "ajdCcXlwTHd",
    "status": "published",
    "timezone": "Europe/Warsaw",
    "updated_at": "2020-12-10T18:55:08.822Z"
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

