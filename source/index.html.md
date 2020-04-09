---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

This is developers documentation about used APIs in Project 'GON'. Will be used for enhanced communication between front-back teams. Should contain all backend API calls with description of usage (if not obvious), request and response parameters, errors, and examples. Good luck! :)



# API

## Level up unit

###CloudCode script key
UNIT_UPGRADE

### Request Parameters

Parameter | Value Type | Description
--------- | ------- | -----------
unitId | int | Unit unique id

### Response Parameters

* unitId : (Dictionary/<int, Dictionary/<string, object/>/>) | keys
    * type : (string) | unit type name
	* level : (int) | unit level
	* rarity : (int) | unit rarity

> JSON response example

```json
"3": {
"type": "Cleopatra",
"rarity": 1,
"level": 2
}
```


<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

## Delete a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.delete(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.delete(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -X DELETE
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete
