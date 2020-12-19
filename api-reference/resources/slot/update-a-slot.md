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

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer `{secret_key}`
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="metadata" type="object" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="lockable" type="boolean" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="capacity" type="integer" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="end\_date" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="start\_date" type="string" required=false %}

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
    "booking_block_id": "5b003c67-f69f-471b-9268-3896a9a3df29",
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

