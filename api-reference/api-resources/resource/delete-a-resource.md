---
description: Permanently deletes the Resource with all Slots and all Bookings within it.
---

# Delete a Resource

{% api-method method="delete" host="https://api.overbooked.io" path="/resources/:resource\_id" %}
{% api-method-summary %}
public.resource.delete
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
{% api-method-parameter name="Authentication" type="string" required=true %}
Bearer `{secret_key}`
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

{% code title="public.resource.delete" %}
```javascript
{
  "data": {},
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

const {error, meta, success } = await overbooked.resource.delete({
  resource_id: "2ab23c3ab-f458-49ce-b8fe-0ca48f8abebe0"
})
```
{% endtab %}
{% endtabs %}

