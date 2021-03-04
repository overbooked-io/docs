---
description: The API returns standardized responses for better consistency.
---

# Response

## Types of responses

The response from the API may contain four fields:`data`, `meta`, `error` and `success`

{% code title="Success response JSON object" %}
```javascript
{
  "data": {...},
  "meta": {...},
  "success": true,
}
```
{% endcode %}

{% code title="Error response JSON object" %}
```javascript
{
  "error": {...},
  "success": false,
}
```
{% endcode %}

* **error -** contains error details when there is 4xx or 5xx status returned. See [Errors](errors.md#error-handling).
* **data** - contains a result of the request \(array or object\).
* **meta** - contains additional data related to the request, for example [pagination details](pagination.md).
* **success** - true/false dependent on status, 2xx - true, 4xx and 5xx - false.

{% code title="Example of response" %}
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
    "metadata": {
      "user_email": "john.doe@example.com"
    }
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

