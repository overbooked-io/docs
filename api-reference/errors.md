---
description: >-
  The API uses HTTP response status codes to indicate the success or failure of
  your API requests. If your request fails, Overbooked API returns an error
  using the appropriate status code.
---

# Errors

## Error codes

In general, there are three status code ranges you can expect:

* `2xx` success status codes confirm that your request worked as expected
* `4xx` error status codes indicate an error because of the information provided \(e.g., a required parameter was omitted\)
* `5xx` error status codes are rare and indicate an error with Overbooked’s servers

Below is a list of possible error codes that can be returned, along with an additional description.

| Code | Status | Description |
| :--- | :--- | :--- |
| E001 | 500 | Unknown internal server error |
| E002 | 404 | Route not found |
| E003 | 400 | Organization not found |
| E007 | 404 | Environment not found |
| E008 | 401 | Unauthorized, API Key invalid |
| E009 | 404 | User with given email not found |
| E013 | 400 | Bad request |
| E014 | 401 | Not authenticated |
| E015 | 401 | Unauthorized |
| E021 | 422 | Invalid Resource date format. Allowed: YYYY-MM-DD |
| E022 | 422 | Invalid Resource timezone, should be correct TZ database name, eg. 'America/New\_York' |
| E023 | 422 | Slot's start date should be before end date |
| E024 | 422 | Slots should not overlap |
| E025 | 404 | Slot not found |
| E042 | 422 | Metadata invalid. Key should have up to 100 characters long, value should have up to 5000 characters long |
| E043 | 422 | Metadata invalid key format. Only string allowed |
| E044 | 422 | Slot is not lockable |
| E045 | 422 | Slot is already locked |
| E046 | 422 | Slot capacity invalid. There are active Bookings assigned to this Slot |
| E047 | 400 | Slot capacity invalid |
| E048 | 404 | Booking not found |
| E049 | 422 | Cannot create a Booking, not enough Slot capacity |
| E050 | 422 | Cannot create a Booking, a Slot locked |
| E051 | 422 | Cannot create a Booking, a Slot disabled |
| E052 | 404 | Resource not found |
| E053 | 403 | Environment is deactivated |
| E054 | 403 | Organization is blocked |
| E055 | 401 | Unauthorized, API Key invalid |
| E056 | 401 | Unauthorized, no API Key provided |
| E057 | 401 | Unauthorized, no access to given Resource |
| E058 | 422 | The booking\_disabled\_before property should be higher than 0 |
| E059 | 403 | Slot cannot be unlocked, lock\_key invalid |
| E060 | 422 | Slot cannot be deleted due to existing Bookings assigned to it |
| E061 | 422 | Cannot create a Booking, a Resource is not published |
| E062 | 429 | API rate-limit reached |
| E066 | 422 | Resource public\_scheduling\_enabled should be boolean |

