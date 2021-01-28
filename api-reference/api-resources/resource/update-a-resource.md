---
description: >-
  Updates the specified Resource by setting the values of the parameters passed.
  Any parameters not provided will be left unchanged.
---

# Update a Resource

{% api-method method="patch" host="https://api.overbooked.io" path="/resources/:resource\_id" %}
{% api-method-summary %}
public.resource.update
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="resource\_id" type="string" required=true %}
Unique identifier of the Resource
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
Set of key-value data that you can attach to the Resource
{% endapi-method-parameter %}

{% api-method-parameter name="timezone" type="string" required=false %}
The output timezone for all timestamps in the Resource
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=false %}
The Resource’s name
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

{% code title="public.resource.update" %}
```scheme
{
  "data": {
    "_object": "resource",
    "booking_disabled_before": 0,
    "created_at": "2020-12-10T18:55:08.749Z",
    "id": "e4e2af17-bc74-483e-9b17-53cbcf907ac4",
    "metadata": {},
    "name": "test_1",
    "num_active_bookings": 7,
    "num_bookings": 7,
    "num_available_slots": 0,
    "num_cancelled_bookings": 0,
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

{% tabs %}
{% tab title="Javascript/Node.js" %}
```javascript
const overbooked = new Overbooked.Client({ ... })

const { data, error, meta, success } = await overbooked.resource.update({
  resource_id: "2ab23c3ab-f458-49ce-b8fe-0ca48f8abebe0"
})

console.log(data) // updated reasource
```
{% endtab %}
{% endtabs %}

