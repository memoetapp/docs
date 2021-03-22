# Note API

{% api-method method="get" host="https://memoet.com" path="/api/decks/:deck\_id/notes" %}
{% api-method-summary %}
Get all notes in a deck
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get all notes in a deck.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="deck\_id" type="string" required=true %}
ID of the deck.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="limit" type="string" required=false %}
Number of notes per page.
{% endapi-method-parameter %}

{% api-method-parameter name="before" type="string" required=false %}
Before cursor of current page.
{% endapi-method-parameter %}

{% api-method-parameter name="after" type="string" required=false %}
After cursor of current page.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "data": [
        {
            "id": "6f397ed6-e5d0-43af-9265-d2b14b8a9a7c",
            "title": "Which city is the capital of the United States of America? Which city is the capital of the United States of America? "
        }
    ],
    "metadata": {
        "after": null,
        "before": null,
        "limit": 1,
        "total_count": 3
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://memoet.com" path="/api/decks/:deck\_id/notes" %}
{% api-method-summary %}
Create new notes
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to create new notes for a deck.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="deck\_id" type="string" required=true %}
ID of the deck to add notes to.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="note" type="object" required=false %}
See example below.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Note successfully created.
{% endapi-method-response-example-description %}

```
{}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find the deck.
{% endapi-method-response-example-description %}

```
{}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Body content example:

```text
{
  "note": {
    "title": "Greenland is a part of which kingdom?",
    "content": "[Source](https://opentdb.com)",
    "type": "multiple_choice",
    "options": [
      {
        "content": "Sweden",
        "correct": false
      },
      {
        "content": "Denmark",
        "correct": true
      },
      {
        "content": "United Kingdom",
        "correct": false
      },
      {
        "content": "Norway",
        "correct": false
      }
    ]
  }
}
```

{% api-method method="get" host="https://memoet.com" path="/api/decks/:deck\_id/notes/:note\_id" %}
{% api-method-summary %}
Retrieve / Update / Delete a note in deck
{% endapi-method-summary %}

{% api-method-description %}
Retrieve, update, delete a note by sending GET, PUT, DELETE request to endpoint above.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="note\_id" type="string" required=true %}
ID of the note.
{% endapi-method-parameter %}

{% api-method-parameter name="deck\_id" type="string" required=true %}
ID of the deck.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
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

