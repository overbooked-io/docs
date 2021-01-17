---
description: >-
  Updates the specified Slot by setting the values of the parameters passed. Any
  parameters not provided will be left unchanged.
---

# Update a Slot

{% api-method method="patch" host="https://api.overbooked.io" path="/slots/:slot\_id" %}
{% api-method-summary %}
public.slot.update
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="slot\_id" type="string" required=true %}
Unique identifier for the Slot.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer `{secret_key}`
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="start\_date" type="string" required=false %}
The date at which the Slot begins, in UTC in ISO 8601.
{% endapi-method-parameter %}

{% api-method-parameter name="end\_date" type="string" required=false %}
The date at which the Slot ends, in UTC in ISO 8601.
{% endapi-method-parameter %}

{% api-method-parameter name="metadata" type="object" required=false %}
Set of key-value data that you can attach to the Slot. This can be useful for storing additional information about the object in a structured format.
{% endapi-method-parameter %}

{% api-method-parameter name="lockable" type="boolean" required=false %}
A flag indicating whether the Slot can be locked. If `lockable` equals `false` then the Slot cannot be locked via the API.
{% endapi-method-parameter %}

{% api-method-parameter name="capacity" type="integer" required=false %}
The maximum amount of active Appointments that the Slot can contain.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

{% code title="public.slot.update" %}
```javascript
{
  "data": {
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
  "meta": {},
  "success": true
}
```
{% endcode %}
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

