---
description: The Slot is a period of time for which Bookings can be booked.
---

# Slot

The Slot is a bucket for Bookings, embedded in time. It has the `start_date` and the `end_date`. It has a maximum `capacity` which defines how many [Bookings](../booking/) can be booked in a given Slot, and can have 2 statuses: `active` and `disabled`. It can be also extended via `metadata` property to store data that refer to any entities from your system.

| Property | Type | Description |
| :--- | :--- | :--- |
| `id` | [uuid](https://en.wikipedia.org/wiki/Universally_unique_identifier) | Unique identifier for the Slot. |
| `resource_id` | [uuid](https://en.wikipedia.org/wiki/Universally_unique_identifier) | Unique identifier for the [Resource](../resource/) that Slot is assigned to. |
| `available` | boolean | A flag indicating whether the Slot is available for booking. |
| `metadata` | [metadata](../../metadata.md) | Set of key-value data that you can attach to the Slot. This can be useful for storing additional information about the object in a structured format. |
| `start_date` | date | The date at which the Slot begins, in UTC in ISO 8601. |
| `end_date` | date | The date at which the Slot ends, in UTC in ISO 8601. |
| `capacity` | integer | The maximum amount of active Bookings that the Slot can contain. |
| `status` | string | The status of the Slot is either `active` or `disabled`. When the status is equal to `disabled`, then no [Bookings](../booking/) can be booked on this Slot. |
| `lockable` | boolean | A flag indicating whether the Slot can be locked. If `lockable` equals `false` then the Slot cannot be locked via the API. |
| `locked_until` | date | The date to which the Slot is locked, in UTC in ISO 8601. |
| `num_bookings` | integer | The number of all [Bookings](../booking/) booked on the Slot. |
| `num_canelled_bookings` | integer | The number of all cancelled [Bookings](../booking/) booked on the Slot. |
| `num_active_bookings` | integer | The number of all active [Bookings](../booking/) booked on the Slot. |
| `updated_at` | date | The date at which the Slot was last updated, in UTC in ISO 8601. |
| `created_at` | date | The date at which the Slot was created, in UTC in ISO 8601. |

## Example

{% code title="Slot" %}
```javascript
{
  "_object": "slot",
  "available": true,
  "resource_id": "5b003c67-f69f-471b-9268-3896a9a3df29",
  "capacity": 1,
  "created_at": "2020-12-10T18:55:08.833Z",
  "end_date": "2020-12-10T19:15:08.825Z",
  "id": "93bd6b73-c45f-4c8a-bb28-58e78e80e653",
  "lockable": true,
  "locked_until": null,
  "metadata": {},
  "num_active_bookings": 0,
  "num_bookings": 0,
  "num_cancelled_bookings": 0,
  "start_date": "2020-12-10T19:05:08.825Z",
  "status": "active",
  "updated_at": "2020-12-10T18:55:08.833Z"
}
```
{% endcode %}

## Methods

* [`POST /slots`](add-slots.md)
* [`GET /slots`](list-slots.md)
* [`GET /slots/:slot_id`](get-a-slot.md)
* [`PATCH /slots/:slot_id`](update-a-slot.md)
* [`POST /slots/:slot_id/enable`](enable-a-slot.md)
* [`POST /slots/:slot_id/disable`](disable-a-slot.md)
* [`POST /slots/:slot_id/lock`](lock-a-slot.md)
* [`POST /slots/:slot_id/unlock`](unlock-a-slot.md)
* [`DELETE /slots/:slot_id`](delete-a-slot.md)

