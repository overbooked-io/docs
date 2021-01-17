---
description: >-
  Creates new Resource object, that can be used to create Slots and
  Appointments within it.
---

# Create a Resource

{% api-method method="post" host="https://api.overbooked.io" path="/resources" %}
{% api-method-summary %}
public.resource.create
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer `{secret_key}`
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required=true %}
The Resource’s name, meant to be displayable publicly
{% endapi-method-parameter %}

{% api-method-parameter name="timezone" type="string" required=true %}
The output timezone for all timestamps in the Resource
{% endapi-method-parameter %}

{% api-method-parameter name="metadata" type="object" required=false %}
Set of key-value data that you can attach to the object
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

{% code title="public.resource.create" %}
```scheme
{
  "data": {
    "_object": "resource",
    "booking_disabled_before": 0,
    "created_at": "2020-12-12T14:53:39.931Z",
    "id": "e185732d-8db3-4d71-ac2e-7fce4afe2e95",
    "metadata": {
      "foo": "bar"
    },
    "name": "test",
    "num_active_appointments": 0,
    "num_appointments": 0,
    "num_available_slots": 0,
    "num_cancelled_appointments": 0,
    "num_slots": 0,
    "short_id": "aG91djROSzM",
    "status": "draft",
    "timezone": "America/New_York",
    "updated_at": "2020-12-12T14:53:39.931Z"
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



