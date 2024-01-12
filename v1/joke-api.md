---
description: Just a simple jokes API for your entertainment
---

# 😀 Joke API

Here a simple little joke endpoint that I have created for your fun and entertainment

### Random Joke

This will return a random joke from the collection.

{% swagger method="get" path="joke/random" baseUrl="https://api.mcjoe21.com/v1/" summary="Returns a random joke." %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="Returns joke object" %}

{% endswagger-response %}
{% endswagger %}

### Daily Joke

This will return the joke of the day.

{% swagger method="get" path="joke/daily" baseUrl="https://api.mcjoe21.com/v1/" summary="Returns the daily joke." %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="Returns joke object" %}

{% endswagger-response %}
{% endswagger %}

Here, we present a comprehensive example to provide a detailed insight into the type of response you can anticipate from the query endpoint, specifically for either of the endpoints outlined in the aforementioned options.

```json
{
  "status": "200",
  "data": {
    "id": number,
    "text": text
  }
}
```
