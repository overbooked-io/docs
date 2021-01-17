---
description: Returns paginated list of all Resources matched by given filters.
---

# List Resources

{% api-method method="get" host="https://api.overbooked.io" path="/resources" %}
{% api-method-summary %}
public.resource.list
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
{% api-method-parameter name="name" type="string" required=false %}
The Resource’s name
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="string" required=false %}
The status of the Resource could be either `draft` or `published`
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="integer" required=true %}
Page number of objects to return
{% endapi-method-parameter %}

{% api-method-parameter name="limit" type="integer" required=true %}
Number of items to return per page
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

{% code title="public.resource.list" %}
```scheme
{
  "data": [
    {
      "_object": "resource",
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
    {
      "_object": "resource",
      "booking_disabled_before": 0,
      "created_at": "2020-12-10T18:55:08.822Z",
      "id": "5b003c67-f69f-471b-9268-3896a9a3df29",
      "metadata": {},
      "name": "test_2",
      "num_active_appointments": 31,
      "num_appointments": 31,
      "num_available_slots": 31,
      "num_cancelled_appointments": 0,
      "num_slots": 62,
      "short_id": "M2I2alhJbDl",
      "status": "published",
      "timezone": "Europe/Warsaw",
      "updated_at": "2020-12-10T18:55:08.949Z"
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

