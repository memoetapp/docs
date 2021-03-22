# Deck API

{% api-method method="get" host="https://memoet.com" path="/api/decks" %}
{% api-method-summary %}
Get all decks
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get all your decks.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="limit" type="number" required=false %}
Number of decks return per page.
{% endapi-method-parameter %}

{% api-method-parameter name="before" type="string" required=false %}
Before cursor from response metadata.
{% endapi-method-parameter %}

{% api-method-parameter name="after" type="string" required=false %}
After cursor from response metadata.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Decks successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "data": [
        {
            "created_at": "2021-03-20T15:53:31",
            "id": "2253519f-6454-4dfb-aa95-b3704aee195e",
            "name": "50 geography quiz",
            "public": false,
            "source_id": null,
            "updated_at": "2021-03-21T13:45:37"
        },
        {
            "created_at": "2021-03-20T15:11:05",
            "id": "61d118ca-e969-467c-a1f8-7d26d79c8738",
            "name": "50 history quiz",
            "public": true,
            "source_id": "87b3a8de-4d6d-4d3e-b724-19cb21a8d0ba",
            "updated_at": "2021-03-20T15:19:36"
        },
        {
            "created_at": "2021-03-15T13:05:16",
            "id": "56e10c98-f30f-4eea-a9ef-02a8bd94f74b",
            "name": "50 math quiz",
            "public": false,
            "source_id": null,
            "updated_at": "2021-03-20T10:38:53"
        }
    ],
    "metadata": {
        "after": "g3QAAAABZAAKdXBkYXRlZF9hdHQAAAAJZAAKX19zdHJ1Y3RfX2QAFEVsaXhpci5OYWl2ZURhdGVUaW1lZAAIY2FsZW5kYXJkABNFbGl4aXIuQ2FsZW5kYXIuSVNPZAADZGF5YRBkAARob3VyYQ1kAAttaWNyb3NlY29uZGgCYQBhAGQABm1pbnV0ZWEhZAAFbW9udGhhA2QABnNlY29uZGE7ZAAEeWVhcmIAAAfl",
        "before": null,
        "limit": 3,
        "total_count": 10
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://memoet.com" path="/api/decks" %}
{% api-method-summary %}
Creat new deck
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to create a new deck.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required=false %}
Deck name.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "data": {
        "created_at": "2021-03-21T14:02:38",
        "id": "6def445e-2b8c-488b-a9f8-0c6248bcedf5",
        "name": "50 math quiz",
        "public": false,
        "source_id": null,
        "updated_at": "2021-03-21T14:02:38"
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://memoet.com" path="/decks/:deck\_id" %}
{% api-method-summary %}
Retrieve / Update / Delete a deck
{% endapi-method-summary %}

{% api-method-description %}
Retrieve, update, delete a deck by sending GET / PUT / DELETE to above endpoint.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="deck\_id" type="string" required=false %}
ID of the deck.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=false %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}
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

