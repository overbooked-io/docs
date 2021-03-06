---
description: 'Creates new Slot object, that can be used to create Bookings.'
---

# Create Slot

{% api-method method="post" host="https://api.overbooked.io" path="/slots" %}
{% api-method-summary %}
public.slot.create
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
{% api-method-parameter name="resource\_id" type="string" required=true %}
The Resource’s id \(uuid\)
{% endapi-method-parameter %}

{% api-method-parameter name="start\_date" type="string" required=true %}
The date at which the Slot begins, in UTC in ISO 8601.
{% endapi-method-parameter %}

{% api-method-parameter name="end\_date" type="string" required=true %}
The date at which the Slot ends, in UTC in ISO 8601.
{% endapi-method-parameter %}

{% api-method-parameter name="capacity" type="integer" required=true %}
The maximum amount of active Bookings that the Slot can contain.
{% endapi-method-parameter %}

{% api-method-parameter name="metadata" type="object" required=false %}
Set of key-value data that you can attach to the Slot
{% endapi-method-parameter %}

{% api-method-parameter name="lockable" type="boolean" required=false %}
A flag indicating whether the Slot can be locked.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

{% code title="public.slot.create" %}
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

const { data, error, meta, success } = await overbooked.slot.create({
  resource_id: "51b4c36b-d758-4fce-b8fe-0ca78f8dcbe0",
  start_date: new Date("2020-12-19T15:00:00.000Z"),
  end_date: new Date("2020-12-19T15:30:00.000Z"),
  capacity: 1
})

console.log(data) // created slot
```
{% endtab %}
{% endtabs %}

