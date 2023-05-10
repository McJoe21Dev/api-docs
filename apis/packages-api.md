---
description: An API for download packages I host on my website
---

# 📦 Packages API

### How to get a package <a href="#get" id="get"></a>

You can get any package if you know its id and just send request this to endpoint and it will give you the data of what you need to do the things you want with the API.

{% swagger baseUrl="https://api.mcjoe21.com/" method="get" path="packages/get" summary="Gets information about a package." %}
{% swagger-description %}
Get data of a package.
{% endswagger-description %}

{% swagger-parameter in="query" name="id" type="String" required="true" %}
ID of the package
{% endswagger-parameter %}

{% swagger-parameter in="query" name="format" type="String" required="false" %}
Data format of response can be set as

<mark style="background-color:blue;">xml</mark>

or

<mark style="background-color:yellow;">json</mark>
{% endswagger-parameter %}

{% swagger-response status="200" description=" Returns package data object" %}

{% endswagger-response %}
{% endswagger %}

Example of what the get endpoint will return for the "**mqo-game"** package.

```json
{
  "data": {
    "manifest": {
      "name": "MQO Game",
      "repo": "https://github.com/mqo-game/math-quiz-game"
    },
    "ver": "0.4",
    "prev": [],
    "tags": [
      "zip",
      "html",
      "game",
      "github"
    ],
    "file": {
      "name": "mqo-game_v0.4.zip",
      "url": "https://dl.mcjoe21.com/mqo-game/mqo-game_v0.4.zip",
      "modified": "2022-04-01 21:01:20",
      "size": "118.86 KB",
      "hash": "147d8bc5777e1f993701e8fa469605e9"
    }
  }
```

### How to query package list <a href="#query" id="query"></a>

Don't know the ID of the package you want to download? Then this will make it easy to find it out by the keyword in the ID.

{% swagger method="get" path="packages/get" baseUrl="https://api.mcjoe21.com/" summary="Query packages by keyword" %}
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

Example of what the query endpoint will return for the "**game"** query.

```json
{
  "data": [
    "mqo-game",
    "mqo-game-beta"
  ]
}
```
