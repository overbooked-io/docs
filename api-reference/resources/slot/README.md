---
description: The Slot is a period of time for which Appointments can be booked.
---

# Slot

// TODO: 

The Slot can have 2 statuses: `active` and `disabled`. When the status is `disabled`, it means that it's not visible publicly and none can book Appointments within it. You can easily change status back to `active` to make it available.

You can also use `metadata` property to store data that refer to any entities from your system.

| Property | Type | Description |
| :--- | :--- | :--- |
| `id` | [uuid](https://en.wikipedia.org/wiki/Universally_unique_identifier) | Unique identifier for the Slot. |
| `booking_block_id` | [uuid](https://en.wikipedia.org/wiki/Universally_unique_identifier) | Unique identifier for the [Booking Block](../booking-block/README.md) that Slot is assigned to. |
| `metadata` | [metadata](../../metadata.md) | Set of key-value data that you can attach to a Slot. This can be useful for storing additional information about the object in a structured format. |
| `start_date` | date | The date at which a Slot begins, in UTC in ISO 8601. |
| `end_date` | date | The date at which a Slot ends, in UTC in ISO 8601. |
| `capacity` | integer | The maximum amount of active Appointments that Slot can contain. |
| `status` | string | The status of the Slot is either `active` or `disabled`. When the status is equal to `disabled`, then no [Appointments](../appointment.md) can be booked on this Slot. |
| `lockable` | boolean | Lorem ipsum. |
| `locked_until` | date | Lorem ipsum. |
| `num_active_appointments` | integer | Lorem ipsum. |
| `num_canelled_appointments` | integer | Lorem ipsum. |
| `num_appointments` | integer | Lorem ipsum. |
| `updated_at` | date | The date at which the object was last updated, in UTC in ISO 8601. |
| `created_at` | date | The date at which the object was created, in UTC in ISO 8601. |

## Example

{% code title="Slot" %}
```javascript
{
  "_object": "slot",
  "available": true,
  "booking_block_id": "5b003c67-f69f-471b-9268-3896a9a3df29",
  "capacity": 1,
  "created_at": "2020-12-10T18:55:08.833Z",
  "end_date": "2020-12-10T19:15:08.825Z",
  "id": "93bd6b73-c45f-4c8a-bb28-58e78e80e653",
  "lockable": true,
  "locked_until": null,
  "metadata": {},
  "num_active_appointments": 0,
  "num_appointments": 0,
  "num_cancelled_appointments": 0,
  "start_date": "2020-12-10T19:05:08.825Z",
  "status": "active",
  "updated_at": "2020-12-10T18:55:08.833Z"
}
```
{% endcode %}

## Methods

* [`POST /slots`](create-a-slot.md)
* [`GET /slots`](list-slots.md)
* [`GET /slots/:slot_id`](get-a-slot.md)
* [`PATCH /slots/:slot_id`](update-a-slot.md)
* [`POST /slots/:slot_id/enable`](enable-a-slot.md)
* [`POST /slots/:slot_id/disable`](disable-a-slot.md)
* [`POST /slots/:slot_id/lock`](lock-a-slot.md)
* [`POST /slots/:slot_id/unlock`](unlock-a-slot.md)
* [`DELETE /slots/:slot_id`](delete-a-slot.md)

