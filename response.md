# Response

## Consistent response

Overbooked API returns standardized responses for better consistency. The response from the API always contains three fields: `error`,`data` and `meta`.

{% code title="Response JSON object" %}
```javascript
{
  "error": {...},
  "data": {...},
  "meta": {...},
  "success": boolean,
}
```
{% endcode %}

* **error -** contains error details when there is 4xx or 5xx status returned. See [Errors](errors.md#error-handling).
* **data** - contains a result of the request \(array or object\)
* **meta** - contains additional data related to the request, for example [pagination details](pagination.md)
* **success** - true/false dependent on status, 2xx - true, 4xx and 5xx - false

{% code title="Example of response \(PATCH /slots/:slot\_id\)" %}
```javascript
{
  "data": {
    "available": false,
    "booking_block_id": "c5034ce4-d84e-4765-95e2-af5fc70e329c",
    "capacity": 1,
    "created_at": "2020-12-01T05:06:30.729Z",
    "end_date": "2020-12-01T05:26:30.717Z",
    "id": "de9f1f1e-1436-4f90-9658-c7d5c7009c38",
    "lock_key": null,
    "lockable": true,
    "locked_until": null,
    "metadata": {
      "obj": {
        "name": "John"
      },
      "user_email": "john.doe@example.com"
    },
    "num_active_appointments": 1,
    "num_appointments": 1,
    "num_cancelled_appointments": 0,
    "start_date": "2020-12-01T05:16:30.716Z",
    "status": "active",
    "updated_at": "2020-12-08T20:38:05.030Z"
  },
  "meta": {},
  "success": true
}
```
{% endcode %}


