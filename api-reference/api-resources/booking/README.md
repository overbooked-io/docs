---
description: An arrangement placed on a particular Slot.
---

# Booking

The Booking can be utilized as any entity you need in your application. This can be a hotel room, flight, or maybe an appointment. It's up to you.  
  
The Booking has two possible statuses: `active` and `cancelled`. When the Booking is `cancelled`, it frees up the Slot, so that other Bookings can be created on it.  
  
You can also use [`metadata`](../../metadata.md) property to store data that refer to any entities from your system.

| Property | Type | Description |
| :--- | :--- | :--- |
| `id` | [uuid](https://en.wikipedia.org/wiki/Universally_unique_identifier) | Unique identifier for the Booking. |
| `resource_id` | [uuid](https://en.wikipedia.org/wiki/Universally_unique_identifier) | Unique identifier for the [Resource](../resource/) that Booking is assigned to. |
| `slot_id` | [uuid](https://en.wikipedia.org/wiki/Universally_unique_identifier) | Unique identifier for the [Slot](../slot/) that Booking is assigned to. |
| `metadata` | [metadata](../../metadata.md) | Set of key-value data that you can attach to the Booking. This can be useful for storing additional information about the object in a structured format. |
| `status` | string | The status of the Booking is either `active` or `cancelled`. |
| `updated_at` | date | The date at which the Booking was last updated, in UTC in ISO 8601. |
| `created_at` | date | The date at which the Booking was created, in UTC in ISO 8601. |

## Example

{% code title="Booking" %}
```javascript
{
  "_object": "booking",
  "resource_id": "f968320f-300e-4da4-8fbb-6c5d8d9cc93a",
  "created_at": "2020-12-10T18:55:24.555Z",
  "id": "b1ad4b5b-2e94-44aa-be51-66afb8d2da13",
  "metadata": {},
  "slot_id": "e943cb7b-d17c-4271-85d9-bd2b87008c6e",
  "status": "active",
  "updated_at": "2020-12-10T18:55:24.555Z"
}
```
{% endcode %}

## Methods

* [`POST /bookings`](create-a-booking.md)
* [`GET /bookings`](list-bookings.md)
* [`GET /bookings/:booking_id`](get-a-booking.md)
* [`PATCH /bookings/:booking_id`](update-a-booking.md)
* [`POST /bookings/:booking_id/enable`](enable-a-booking.md)
* [`POST /bookings/:booking_id/cancel`](cancel-a-booking.md)
* [`POST /bookings/:booking_id/reschedule`](reschedule-a-booking.md)
* [`DELETE /bookings/:booking_id`](delete-a-booking.md)

