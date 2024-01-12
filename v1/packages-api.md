---
description: An API for getting information about packages hosted on our service
---

# 📦 Packages API

### How to get a package <a href="#get" id="get"></a>

With this endpoint, obtaining any package becomes attainable by using the package ID. All that's required is to send a request to the specified endpoint, and it will return you with the essential data about the package.

{% swagger baseUrl="https://api.mcjoe21.com/v1/" method="get" path="packages/get" summary="Gets information about a package." %}
{% swagger-description %}
Get data of a package.
{% endswagger-description %}

{% swagger-parameter in="query" name="id" type="String" required="true" %}
ID of the package
{% endswagger-parameter %}

{% swagger-parameter in="query" name="part" %}
The item key that you want returned
{% endswagger-parameter %}

{% swagger-response status="200" description=" Returns package data object" %}

{% endswagger-response %}
{% endswagger %}

Here is a demonstration illustrating the output you can expect when a request is sent to the **get** endpoint. This illustrative example serves to showcase the type of data that will be returned in response to your query.

<pre class="language-json"><code class="lang-json">{
  "data": {
    "manifest": {
      "name": text,
      "repo": url,
      "ver": number
    },
    "files": {
      text: {
        "name": text,
        "url": url,
<strong>        "hash": hash    
</strong><strong>        "size": filesize, 
</strong>        "modified": datetime
      }
    },
    "tags": array
  }
</code></pre>

### How to query package list <a href="#query" id="query"></a>

Are you unsure about the package ID for the download you're looking for? This method streamlines the identification process by utilizing keywords within the ID. Furthermore, it will provide you with an array of matching results.

{% swagger method="get" path="packages/query" baseUrl="https://api.mcjoe21.com/v1/" summary="Query packages by keyword" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="q" required="true" type="String" %}
The query string to search
{% endswagger-parameter %}

{% swagger-parameter in="query" name="tag" type="Strings List" required="false" %}
List of tags to filter results
{% endswagger-parameter %}

{% swagger-parameter in="query" name="format" type="String" required="false" %}
Data format of response can be set as

<mark style="background-color:blue;">xml</mark>

or

<mark style="background-color:yellow;">json</mark>
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Returns packages list object" %}

{% endswagger-response %}
{% endswagger %}

Here is a demonstration illustrating the output you can expect when a request is sent to the **query** endpoint. This illustrative example serves to showcase the type of data that will be returned in response to your query.

```json
{
  "data": {
    "results": array
  }
}
```
