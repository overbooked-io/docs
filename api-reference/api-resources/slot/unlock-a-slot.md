---
description: Unlocks the Slot making it available to book by others.
---

# Unlock a Slot

{% api-method method="post" host="https://api.overbooked.io" path="/slots/:slot\_id/unlock" %}
{% api-method-summary %}
public.slot.unlock
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
Bearer `{public_key|secret_key}`
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="lock\_key" type="string" required=true %}
A unique, random string used to distinguish a lock, provided during locking operation.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

{% code title="public.slot.unlock" %}
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
    "num_active_bookings": 0,
    "num_bookings": 0,
    "num_cancelled_bookings": 0,
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

{% tabs %}
{% tab title="Javascript/Node.js" %}
```javascript
const overbooked = new Overbooked.Client({ ... })

const { data, error, meta, success } = await overbooked.slot.unlock(
  "21b2c36b-f458-4fce-b8fe-0ca48f8dcbe0",
  {
    lock_key: "lock_key_4321"
  }
)

console.log(data) // unlocked slot
```
{% endtab %}
{% endtabs %}

