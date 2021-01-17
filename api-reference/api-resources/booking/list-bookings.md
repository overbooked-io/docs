---
description: Creates new Booking object.
---

# List Bookings

{% api-method method="get" host="https://api.overbooked.io" path="/bookings" %}
{% api-method-summary %}
public.booking.list
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

{% api-method-query-parameters %}
{% api-method-parameter name="status" type="string" required=false %}
 The status of the Booking could be either `active` or `cancelled`
{% endapi-method-parameter %}

{% api-method-parameter name="slot\_id" type="string" required=false %}
The Slot's id \(uuid\)
{% endapi-method-parameter %}

{% api-method-parameter name="resource\_id" type="string" required=false %}
The Resource’s id \(uuid\)
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="integer" required=true %}
The page number of objects to return.
{% endapi-method-parameter %}

{% api-method-parameter name="limit" type="integer" required=true %}
The number of items to return per page.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

{% code title="public.booking.list" %}
```javascript
{
  "data": [
    {
      "_object": "booking",
      "resource_id": "f968320f-300e-4da4-8fbb-6c5d8d9cc93a",
      "created_at": "2020-12-10T18:55:24.555Z",
      "id": "b1ad4b5b-2e94-44aa-be51-66afb8d2da13",
      "metadata": {},
      "slot_id": "e943cb7b-d17c-4271-85d9-bd2b87008c6e",
      "status": "active",
      "updated_at": "2020-12-10T18:55:24.555Z"
    },
    {
      "_object": "booking",
      "resource_id": "f968320f-300e-4da4-8fbb-6c5d8d9cc93a",
      "created_at": "2020-12-10T18:55:24.555Z",
      "id": "e4e2af17-bc74-483e-9b17-53cbcf907ac4",
      "metadata": {},
      "slot_id": "e943cb7b-d17c-4271-85d9-bd2b87008c6e",
      "status": "active",
      "updated_at": "2020-12-10T18:55:24.555Z"
    }
  ],
  "meta": {
    "limit": 20,
    "page": 1,
    "total": 2
  },
  "success": true
}
```
{% endcode %}
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

