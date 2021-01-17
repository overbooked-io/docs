---
description: 'Creates new Booking object.'
---
# Create Booking

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
{% api-method-parameter name="resource\_id" type="string" required=true %}
The Resource's id \(uuid\)
{% endapi-method-parameter %}
{% api-method-parameter name="slots\[\]\[start\_date\]" type="string" required=true %}
The date at which the Slot begins, in UTC in ISO 8601.
{% endapi-method-parameter %}
{% api-method-parameter name="slots\[\]\[end\_date\]" type="string" required=true %}
The date at which the Slot ends, in UTC in ISO 8601.
{% endapi-method-parameter %}
{% api-method-parameter name="slots\[\]\[capacity\]" type="integer" required=true %}
The maximum amount of active Bookings that the Slot can contain.
{% endapi-method-parameter %}
{% api-method-parameter name="slots\[\]\[metadata\]" type="object" required=false %}
Set of key-value data that you can attach to the Slot
{% endapi-method-parameter %}
{% api-method-parameter name="slots\[\]\[lockable\]" type="boolean" required=false %}
A flag indicating whether the Slot can be locked.
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