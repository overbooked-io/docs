---
description: Reverts the status from published to draft.
---

# Convert a Resource to draft

{% api-method method="post" host="https://api.overbooked.io" path="/resources/:resource\_id/convert-draft" %}
{% api-method-summary %}
public.resource.convertToDraft
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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

{% code title="public.resource.convertToDraft" %}
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
    "status": "draft",
    "timezone": "America/New_York",
    "public_scheduling_enabled": false,
    "scheduling_default_rule": "allow",
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

const { data, error, meta, success } = await overbooked.resource.convertToDraft(
  "2ab23c3ab-f458-49ce-b8fe-0ca48f8abebe0"
)

console.log(data) // converted to draft reasource
```
{% endtab %}
{% endtabs %}

