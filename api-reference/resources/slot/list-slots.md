---
description: Returns paginated list of all Slots matched by given filters.
---

# List Slots

{% api-method method="get" host="https://api.overbooked.io" path="/slots" %}
{% api-method-summary %}
public.slot.list
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
{% api-method-parameter name="limit" type="integer" required=true %}
The number of items to return per page.
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="integer" required=true %}
The page number of objects to return.
{% endapi-method-parameter %}

{% api-method-parameter name="available" type="boolean" required=false %}
A flag indicating whether the Slot is available for booking.
{% endapi-method-parameter %}

{% api-method-parameter name="start\_date" type="string" required=false %}
The date at which the Slot begins, in UTC in ISO 8601.
{% endapi-method-parameter %}

{% api-method-parameter name="end\_date" type="string" required=false %}
The date at which the Slot ends, in UTC in ISO 8601.
{% endapi-method-parameter %}

{% api-method-parameter name="booking\_block\_id" type="string" required=false %}
The Resource’s id \(uuid\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

{% code title="public.slot.list" %}
```javascript
{
  "data": [
    {
      "_object": "slot",
      "available": true,
      "resource_id": "5b003c67-f69f-471b-9268-3896a9a3df29",
      "capacity": 1,
      "created_at": "2020-12-19T15:44:22.854Z",
      "end_date": "2020-10-21T22:50:00+02:00",
      "id": "3751095a-b4ef-41a3-98a3-b8a0eecfc332",
      "lockable": true,
      "locked_until": null,
      "metadata": {},
      "num_active_appointments": 0,
      "num_appointments": 0,
      "num_cancelled_appointments": 0,
      "start_date": "2020-10-21T22:30:00+02:00",
      "status": "active",
      "updated_at": "2020-12-19T15:44:22.854Z"
    },
    {
      "_object": "slot",
      "available": true,
      "resource_id": "1575a50d-3dd8-4526-b721-dcfe9e3c436a",
      "capacity": 1,
      "created_at": "2020-12-10T18:55:08.958Z",
      "end_date": "2020-12-10T19:15:08.952Z",
      "id": "2e2b9f26-7a6f-41cd-82f8-32e84cf7b7a7",
      "lockable": true,
      "locked_until": null,
      "metadata": {},
      "num_active_appointments": 0,
      "num_appointments": 0,
      "num_cancelled_appointments": 0,
      "start_date": "2020-12-10T19:05:08.952Z",
      "status": "active",
      "updated_at": "2020-12-10T18:55:08.958Z"
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

