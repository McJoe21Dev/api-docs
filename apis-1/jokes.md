---
description: Just a simple jokes API for your entertainment
---

# 😀 Jokes API

Here a simple little joke endpoint that I have created for your fun and entertainment

{% swagger method="get" path="jokes/random" baseUrl="https://api.mcjoe21.com/" summary="Returns a random joke." %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="format" type="String" required="false" %}
Data format of response can be set as 

<mark style="background-color:blue;">

xml

</mark>

 or 

<mark style="background-color:yellow;">

json

</mark>
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Returns joke object" %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="jokes/daily" baseUrl="https://api.mcjoe21.com/" summary="Returns the daily joke." %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="format" type="String" required="false" %}
Data format of response can be set as 

<mark style="background-color:blue;">

xml

</mark>

 or 

<mark style="background-color:yellow;">

json

</mark>
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Returns joke object" %}

{% endswagger-response %}
{% endswagger %}

Example of what the query endpoint will return for ether of the endpoints listed above

```json
{
  "data": {
    "id": 31,
    "text": "I pin things on my board, just pointing it out"
  }
}
```
