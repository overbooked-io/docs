---
description: >-
  Main objects available in Overbooked API (like Resources, Slots, Bookings)
  have an updatable metadata property, which can be used to attach custom
  key-value data.
---

# Metadata

## Updatable metadata property

Metadata is useful for storing additional, structured information on an object. As an example, you could store the user's email or corresponding unique identifier from your system on eg. an [Booking](api-resources/booking.md) object. You can utilize it in any way you want. The Overbooked API is very flexible in this regard.

### Limitations

* The metadata key should be a string with a maximum length of **100 characters**
* The metadata value could be the type of **boolean**, **string**, **integer**, **float**, or **JSON** with a maximum length of **5000 characters**

### Example

{% code title="Metadata on Booking" %}
```scheme
{
  "_object": "booking",
  "id": "4c305fb5-6673-4df3-9f97-c7597fa86ffc",
  "resource_id": "1575a50d-3dd8-4526-b721-dcfe9e3c436a",
  "metadata": {
    "user_id": 1,
    "user_email": "john.doe@example.com"
  },
  "slot_id": "80373175-ae15-4bf7-bae8-c39c74723e1d",
  "status": "active",
  "created_at": "2020-12-10T18:55:08.995Z",
  "updated_at": "2020-12-10T18:55:08.995Z"
}
```
{% endcode %}

