# Create a booking block

{% api-method method="post" host="https://api.overbooked.io" path="/booking-blocks" %}
{% api-method-summary %}
public.bookingBlock.create
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Content-Type" type="string" required=false %}
application/json
{% endapi-method-parameter %}

{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer &lt;secret\_key&gt;
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="timezone" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="metadata" type="object" required=false %}

{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```scheme
{
  "data": {
    "_object": "booking_block",
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
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



