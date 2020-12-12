---
description: Lorem ipsum
---

# Booking Block

Lorem ipsum ...

| Property | Type | Description |
| :--- | :--- | :--- |
| `id` | [uuid](https://en.wikipedia.org/wiki/Universally_unique_identifier) | Unique identifier for the object. |
| `metadata` | [metadata](../../metadata.md) | Set of key-value data that you can attach to an object. This can be useful for storing additional information about the object in a structured format. |
| `name` | string | The booking block’s name, meant to be displayable publicly. |
| `status` | string | The status of the booking block is either `draft` or `published`. When the status is equal to `draft`, then [Slots](../slot/) are not available to be booked. |
| `timezone` | string | The output timezone for all timestamps in the Booking Block. A list of possible time zone values is maintained at the [IANA Time Zone Database](http://www.iana.org/time-zones). |
| `short_id` | string | Short representation of the property `id`. |
| `num_appointments` | integer | A number of all [Appointments](../appointment/) booked on [Slots](../slot/) within the Booking Block. |
| `num_active_appointments` | integer | A number of active [Appointments](../appointment/) \(with status `active`\) booked on [Slots](../slot/) within the Booking Block. |
| `num_cancelled_appointments` | integer | A number of cancelled [Appointments](../appointment/) \(with status `cancelled`\) booked on [Slots](../slot/) within the Booking Block. |
| `num_slots` | integer | A number of all [Slots](../slot/) created within the Booking Block. |
| `num_available_slots` | integer | A number of all available [Slots](../slot/) \(available to book\) created within the Booking Block. |
| `booking_disabled_before` | integer | The number of seconds before the [Slot](../slot/) starts when the booking option is disabled. |
| `updated_at` | date | The date at which the object was last updated, in UTC in ISO 8601. |
| `created_at` | date | The date at which the object was created, in UTC in ISO 8601. |

### Example

{% code title="Booking Block" %}
```javascript
{
  "_object": "booking_block",
  "id": "e4e2af17-bc74-483e-9b17-53cbcf907ac4",
  "metadata": {},
  "name": "test_1",
  "status": "published",
  "timezone": "Europe/Warsaw",
  "short_id": "ajdCcXlwTHd",
  "num_active_appointments": 7,
  "num_appointments": 7,
  "num_available_slots": 0,
  "num_cancelled_appointments": 0,
  "num_slots": 7,
  "booking_disabled_before": 0,
  "updated_at": "2020-12-10T18:55:08.822Z",
  "created_at": "2020-12-10T18:55:08.749Z"
}
```
{% endcode %}

### Methods

* [`POST /booking-blocks`](create-a-booking-block.md)\`\`
* [`GET /booking-blocks`](object.md)
* 
