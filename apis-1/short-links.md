---
description: Create easy custom short links.
---

# 🔗 Short Links API

### Creation a Link

An API for creation quick short links for free for any needs you want.

{% swagger method="get" path="links/new" baseUrl="https://api.mcjoe21.com/" summary="Creates a new short link" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="url" required="true" type="URL" %}
The url of the redirect page 
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Returns short link object" %}

{% endswagger-response %}
{% endswagger %}
