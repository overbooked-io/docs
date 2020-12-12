---
description: >-
  Updates the specified Booking Block by setting the values of the parameters
  passed. Any parameters not provided will be left unchanged.
---

# Update a Booking Block

{% api-method method="patch" host="https://api.overbooked.io" path="/booking-blocks/:booking\_block\_id" %}
{% api-method-summary %}
public.bookingBlock.update
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
Bearer `{secret_key}`
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="booking\_disabled\_before" type="integer" required=false %}
The number of seconds before the Slot starts when the booking option is disabled
{% endapi-method-parameter %}

{% api-method-parameter name="metadata" type="object" required=false %}
Set of key-value data that you can attach to the Booking Block
{% endapi-method-parameter %}

{% api-method-parameter name="timezone" type="string" required=false %}
The output timezone for all timestamps in the Booking Block
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=false %}
The Booking Block’s name
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

{% code title="public.bookingBlock.update" %}
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
    "timezone": "America/New_York",
    "updated_at": "2020-12-12T16:27:47.590Z"
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

