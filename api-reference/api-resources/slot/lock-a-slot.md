---
description: 'Locks the Slot for a while, making it impossible for others to book.'
---

# Lock a Slot

{% api-method method="post" host="https://api.overbooked.io" path="/slots/:slot\_id/lock" %}
{% api-method-summary %}
public.slot.lock
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
{% api-method-parameter name="lock\_until" type="string" required=true %}
The date to which the Slot is locked, in UTC in ISO 8601.
{% endapi-method-parameter %}

{% api-method-parameter name="lock\_key" type="string" required=true %}
A unique, random string used to distinguish a lock. The lock key should be passed in the request in case of an unlocking operation.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

{% code title="public.slot.lock" %}
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
    "locked_until": "2020-12-19T16:00:00.000Z",
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

const { data, error, meta, success } = await overbooked.slot.lock(
  "21b2c36b-f458-4fce-b8fe-0ca48f8dcbe0",
  {
    lock_until: new Date("2020-12-19T15:00:00.000Z"),
    lock_key: "lock_key_1234"
  }
)

console.log(data) // locked slot
```
{% endtab %}
{% endtabs %}

