---
description: >-
  All top-level API resources have support for bulk fetches via "list" API
  methods. When you call a list API method to retrieve most of these
  collections, they're returned to you in portions.
---

# Pagination

## Numeric-based pagination

Overbooked API utilizes numeric-based pagination via the `limit` and `page` parameters.

### Request parameters

| Parameter | Type |  | Min | Max |
| :--- | :--- | :--- | :--- | :--- |
| limit | integer | Number of items to return per page | 1 | 50 |
| page | integer | Page number of objects to return | 1 | - |

### Response meta

| Property | Type | Description |
| :--- | :--- | :--- |
| total | integer | Number of total found objects |
| limit | integer | Number of items to return per page |
| page | integer | Page number of objects to return |

### Example

```bash
curl https://api.overbooked.io/resources?limit=20&page=1 \
    -H 'Authorization: Bearer <api_key>'
```

```javascript
{
  "data": [
    {
      "_object": "resource",
      "booking_disabled_before": 0,
      "created_at": "2020-12-10T18:55:08.749Z",
      "id": "e4e2af17-bc74-483e-9b17-53cbcf907ac4",
      "metadata": {},
      "name": "test_1",
      "num_active_bookings": 7,
      "num_bookings": 7,
      "num_available_slots": 0,
      "num_cancelled_bookings": 0,
      "num_slots": 7,
      "short_id": "ajdCcXlwTHd",
      "status": "published",
      "timezone": "Europe/Warsaw",
      "public_scheduling_enabled": false,
      "scheduling_default_rule": "allow",
      "updated_at": "2020-12-10T18:55:08.822Z"
    },
    {
      "_object": "resource",
      "booking_disabled_before": 0,
      "created_at": "2020-12-10T18:55:08.822Z",
      "id": "5b003c67-f69f-471b-9268-3896a9a3df29",
      "metadata": {},
      "name": "test_2",
      "num_active_bookings": 31,
      "num_bookings": 31,
      "num_available_slots": 31,
      "num_cancelled_bookings": 0,
      "num_slots": 62,
      "short_id": "M2I2alhJbDl",
      "status": "published",
      "timezone": "Europe/Warsaw",
      "public_scheduling_enabled": false,
      "scheduling_default_rule": "allow",
      "updated_at": "2020-12-10T18:55:08.949Z"
    }
  ],
  "meta": {
    "limit": 20,
    "page": 1,
    "total": 2
  },
  "success": true
}
```

