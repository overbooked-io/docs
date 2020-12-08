# Errors

Overbooked API uses [HTTP response status codes](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes) to indicate the success or failure of your API requests. If your request fails, Overbooked API returns an [error](https://stripe.com/docs/api#errors) using the appropriate status code.

In general, there are three status code ranges you can expect:

* `2xx` success status codes confirm that your request worked as expected
* `4xx` error status codes indicate an error because of the information provided \(e.g., a required parameter was omitted\)
* `5xx` error status codes are rare and indicate an error with Overbooked’s servers

Below is a list of possible error codes that can be returned, along with an additional description.

| Code | HTTP Status | Description |
| :--- | :--- | :--- |
| E001 | 500 | Unknown internal server error |
| E002 | 404 | Route not found |
| E003 | 400 | Organization not found |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |

