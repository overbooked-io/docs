---
description: The Resource is a bucket for Slots and Bookings.
---

# Resource

The Resource is not embedded in a time, so that is very flexible in usage. You control your booking availability by using Slots and their properties.

The Resource can have 2 statuses: `draft` and `published`. When the status is `draft`, it means that it's not visible publicly and none can book Bookings within it. You can easily publish it to make it available.

You can also use `metadata` property to store data that refer to any entities from your system.

| Property | Type | Description |
| :--- | :--- | :--- |
| `id` | [uuid](https://en.wikipedia.org/wiki/Universally_unique_identifier) | Unique identifier for the Resource. |
| `metadata` | [metadata](../../metadata.md) | Set of key-value data that you can attach to a Resource. This can be useful for storing additional information about the object in a structured format. |
| `name` | string | The Resource’s name, meant to be displayable publicly. |
| `status` | string | The status of the Resource is either `draft` or `published`. When the status is equal to `draft`, then [Slots](../slot/) are not available to be booked. |
| `timezone` | string | The output timezone for all timestamps in the Resource. A list of possible time zone values is maintained at the [IANA Time Zone Database](http://www.iana.org/time-zones). |
| `short_id` | string | Short representation of the property `id`. |
| `num_bookings` | integer | A number of all [Bookings](../booking/) booked on [Slots](../slot/) within the Resource. |
| `num_active_bookings` | integer | A number of active [Bookings](../booking/) \(with status `active`\) booked on [Slots](../slot/) within the Resource. |
| `num_cancelled_bookings` | integer | A number of cancelled [Bookings](../booking/) \(with status `cancelled`\) booked on [Slots](../slot/) within the Resource. |
| `num_slots` | integer | A number of all [Slots](../slot/) created within the Resource. |
| `num_available_slots` | integer | A number of all available [Slots](../slot/) \(available to book\) created within the Resource. |
| `booking_disabled_before` | integer | The number of seconds before the [Slot](../slot/) starts when the booking option is disabled. |
| `updated_at` | date | The date at which the object was last updated, in UTC in ISO 8601. |
| `created_at` | date | The date at which the object was created, in UTC in ISO 8601. |

## Example

{% code title="Resource" %}
```javascript
{
  "_object": "resource",
  "id": "e4e2af17-bc74-483e-9b17-53cbcf907ac4",
  "metadata": {},
  "name": "test_1",
  "status": "published",
  "timezone": "Europe/Warsaw",
  "short_id": "ajdCcXlwTHd",
  "num_active_bookings": 7,
  "num_bookings": 7,
  "num_available_slots": 0,
  "num_cancelled_bookings": 0,
  "num_slots": 7,
  "booking_disabled_before": 0,
  "updated_at": "2020-12-10T18:55:08.822Z",
  "created_at": "2020-12-10T18:55:08.749Z"
}
```
{% endcode %}

## Methods

* [`POST /resources`](create-a-resource.md)
* [`GET /resources`](list-resources.md)
* [`GET /resources/:resource_id`](get-a-resource.md)
* [`PATCH /resources/:resource_id`](update-a-resource.md)
* [`POST /resources/:resource_id/publish`](publish-a-resource.md)
* [`POST /resources/:resource_id/convert-draft`](convert-a-resource-to-draft.md)

