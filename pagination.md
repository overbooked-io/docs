# Pagination

## Numeric-based pagination

All top-level API resources have support for bulk fetches via "list" API methods. When you call a list API method to retrieve most of these collections, they're returned to you in portions. Overbooked API utilizes numeric-based pagination via the `limit` and `page` parameters.

| Parameter | Type |  | Min | Max |
| :--- | :--- | :--- | :--- | :--- |
| limit | integer | Number of items to return per page | 1 | 50 |
| page | integer | Page number of objects to return | 1 | - |

### Example

{% api-method method="get" host="" path="" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

