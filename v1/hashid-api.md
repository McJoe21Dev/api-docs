# 🆔 Hash ID API

### Get a user has

The Hash ID API can be employed to obtain a hash for the expedited user, facilitating swift and uncomplicated user verification. It's essential to understand that this API does not retain any of the gathered information.

{% swagger method="get" path="hashid/get" baseUrl="https://api.mcjoe21.com/v1/" summary="Gets the users hash" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}

{% endswagger-response %}
{% endswagger %}

Here's an example of what comes back from the **get** endpoint

```json
{
  "data": {
    "value": text
  }
```



### Verify user

You can also use the hash to verify the users device by using the **verify** endpoint

{% swagger method="get" path="/hashid/verify" baseUrl="https://api.mcjoe21.com/v1" summary="Verifies the users hash" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="hash" required="true" type="Hash" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}

{% endswagger-response %}
{% endswagger %}

Here's an example of what comes back from the **verify** endpoint



```json
  "data": {
    "value": hash
  }
```
