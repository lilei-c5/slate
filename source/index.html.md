---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Attune's Worker's Compensation API

# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: itsasecret"
```

```javascript
$.ajax({
    url: "api_endpoint_here",
    headers: {"Authorization" : "itsasecret"},
    success: function(){
      //handle success
    }
});
```

> Make sure to replace `itsasecret` with your API key.

WorkersComp API uses API keys to allow access to the API.

WorkersComp API expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: itsasecret`

<aside class="notice">
You must replace <code>itsasecret</code> with your personal API key.
</aside>

# Health

## GET Health

```shell
curl "http://api.attune.com/workerscomp/health"
```

```javascript
$.ajax({
    url: "http://api.attune.com/workerscomp/health",
    success: function(){
      //handle success
    }
});
```

> The above command returns JSON structured like this:

```json
{"status": "ok"}
```
This endpoint retrieves the health status of the WorkersComp API server.

### HTTP Request

`GET http://api.attune.com/workerscomp/v1/health`

<aside class="success">
Useful for monitoring tools.
</aside>

# Quote (V1)

## GET Quote

```shell
curl "http://api.attune.com/workerscomp/v1/quote"
  -H "Authorization: itsasecret"
```

> The above command returns JSON structured like this:

```json
{}
```

This endpoint retrieves a quote for an insured.

### HTTP Request

`GET http://api.attune.com/workerscomp/v1/quote`

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
class_code | true | Class code of the business.
state_code | true | Code of the state.
agent_code | false | Code of the producer.

<aside class="warning">
Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.
</aside>







