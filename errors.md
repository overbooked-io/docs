# Errors

## Error handling

Overbooked API uses [HTTP response status codes](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes) to indicate the success or failure of your API requests. If your request fails, Overbooked API returns an [error](https://stripe.com/docs/api#errors) using the appropriate status code.

In general, there are three status code ranges you can expect:

* `2xx` success status codes confirm that your request worked as expected
* `4xx` error status codes indicate an error because of the information provided \(e.g., a required parameter was omitted\)
* `5xx` error status codes are rare and indicate an error with Overbooked’s servers

{% code title="Example error response" %}
```scheme
{
  "error": {
    "code": "E013",
    "message": "\"metadata\" is invalid, should be an object",
    "status": 400
  }
}
```
{% endcode %}

### Error codes

Below is a list of possible error codes that can be returned, along with an additional description.

| Code | Status | Description |
| :--- | :--- | :--- |
| E001 | 500 | Unknown internal server error |
| E002 | 404 | Route not found |
| E003 | 400 | Organization not found |
| E004 | 422 | Invalid role. Should be one of \['admin', 'developer', 'viewer'\] |
| E005 | 404 | Member not found |
| E006 | 422 | Organization plan invalid, should be one of \['standard', 'enterprise'\] |
| E007 | 404 | Environment not found |
| E008 | 401 | Unauthorized, API Key invalid |
| E009 | 404 | User with given email not found |
| E010 | 422 | Given email is already in usage |
| E011 | 401 | Password invalid |
| E012 | 404 | User not found |
| E013 | 400 | Bad request |
| E014 | 401 | Not authenticated |
| E015 | 401 | Unauthorized |
| E016 | 403 | At least one user with admin role required |
| E017 | 403 | Email not confirmed |
| E018 | 403 | Organization invitation not found |
| E019 | 422 | Organization name cannot include any special characters |
| E020 | 422 | Credits top up invalid amount |
| E021 | 422 | Invalid booking block date format. Allowed: YYYY-MM-DD |
| E022 | 422 | Invalid booking block timezone, should be correct TZ database name, eg. 'America/New\_York' |
| E023 | 422 | Slot's start date should be before end date |
| E024 | 422 | Slots should not overlap |
| E025 | 404 | Slot not found |
| E026 | 403 | Tax ID should follow the standard |
| E027 | 400 | Top up status invalid |
| E028 | 400 | Top up type invalid |
| E029 | 400 | Charge status invalid |
| E030 | 400 | Charge type invalid |
| E031 | 403 | No payment method configured |
| E032 | 403 | Payment failed |
| E033 | 403 | Payment cancelled |
| E034 | 404 | Billing Account not found |
| E035 | 400 | Invoice already issued |
| E036 | 400 | Charge status invalid |
| E037 | 400 | Charge amount invalid, should be higher than 0 |
| E038 | 404 | Invoice not found |
| E039 | 404 | Billing Period with given id not found |
| E040 | 403 | Invoice not paid in full |
| E041 | 422 | Invalid Usage Action type |
| E042 | 422 | Metadata invalid. Key should have up to 100 characters long, value should have up to 5000 characters long |
| E043 | 422 | Metadata invalid key format. Only string allowed |
| E044 | 422 | Slot is not lockable |
| E045 | 422 | Slot is already locked |
| E046 | 422 | Slot capacity invalid. There are active appointments assigned to this slot |
| E047 | 400 | Slot capacity invalid |
| E048 | 404 | Appointment not found |
| E049 | 422 | Cannot book appointment, not enough slot capacity |
| E050 | 422 | Cannot book appointment, slot locked |
| E051 | 422 | Cannot book appointment, slot disabled |
| E052 | 404 | Booking Block not found |
| E053 | 403 | Environment is deactivated |
| E054 | 403 | Organization is blocked |
| E055 | 401 | Unauthorized, API Key invalid |
| E056 | 401 | Unauthorized, no API Key provided |
| E057 | 401 | Unauthorized, no access to given resource |
| E058 | 422 | The booking\_disabled\_before property should be higher than 0 |
| E059 | 403 | Slot cannot be unlocked, lock\_key invalid |
| E060 | 422 | Slot cannot be deleted due to existing appointments assigned to it |

