# Topics

## Get All Topics


```shell
curl "https://community.tribe.so/api/v1/topics"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let topics = api.topics.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "_id": "5b88264d3d9228aa7c41f692",
    "name": "Tribe",
    "portal": "5a73b1fcc48071e4c4dc1cae",
    "updatedAt": "2018-11-29T06:16:08.223Z",
    "__v": 8,
    "createdAt": "2018-08-30T17:15:57.884Z",
    "aliases": [],
    "children": [
      "5bb1abe13d9228aa7c4242ba",
      "5babb4603d9228aa7c423c23",
      "5bbf7b083d9228aa7c427450",
      "5babe5eb3d9228aa7c423c66"
    ],
    "counts": {
      "questions": 55,
      "followers": 3,
      "subquestions": 79,
      "children": 4
    },
    "definitions": [],
    "paths": [
      [
        {
          "_id": "5b88264d3d9228aa7c41f692",
          "name": "Tribe",
          "picture": "/files/topics/692/5b88264d3d9228aa7c41f692_72807.png"
        }
      ]
    ],
    "shortId": "5oqoy",
    "user": "5b881b2a90ecbe6751123d7e",
    "picture": "/files/topics/692/5b88264d3d9228aa7c41f692_72807.png",
    "experts": {
      "5b881b2a90ecbe6751123d7e": 24,
      "5b3f7fe0d5a11b6297259cab": 16,
      "5b1f99a7478dd3768d84b646": 12,
      "5b913111f19a473232026877": 3,
      "5ba95b5c630b876a1e9785a5": 1
    },
    "about": "",
    "followed": true
  }
]
```

This endpoint retrieves all topics.

### HTTP Request

<code class="request">GET /api/v1/topics</code>

### Query Parameters

Parameter | Type | Default | Description
--------- | ------- | ----------- | -----------
page | `Number` | `1` | Intended page
limit | `Number` | `20` | Number of items per page
sort | `String` | `createdAt.desc` | The field to sort on


## Get a Specific Topic


```shell
curl "https://community.tribe.so/api/v1/topics/5b88264d3d9228aa7c41f692"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let topics = api.topics.get('5b88264d3d9228aa7c41f692');
```

> The above command returns JSON structured like this:

```json
{
  "_id": "5b88264d3d9228aa7c41f692",
  "name": "Tribe",
  "portal": "5a73b1fcc48071e4c4dc1cae",
  "updatedAt": "2018-11-29T06:16:08.223Z",
  "__v": 8,
  "createdAt": "2018-08-30T17:15:57.884Z",
  "aliases": [],
  "children": [
    "5bb1abe13d9228aa7c4242ba",
    "5babb4603d9228aa7c423c23",
    "5bbf7b083d9228aa7c427450",
    "5babe5eb3d9228aa7c423c66"
  ],
  "counts": {
    "questions": 55,
    "followers": 3,
    "subquestions": 79,
    "children": 4
  },
  "definitions": [],
  "paths": [
    [
      {
        "_id": "5b88264d3d9228aa7c41f692",
        "name": "Tribe",
        "picture": "/files/topics/692/5b88264d3d9228aa7c41f692_72807.png"
      }
    ]
  ],
  "shortId": "5oqoy",
  "user": "5b881b2a90ecbe6751123d7e",
  "picture": "/files/topics/692/5b88264d3d9228aa7c41f692_72807.png",
  "experts": {
    "5b881b2a90ecbe6751123d7e": 24,
    "5b3f7fe0d5a11b6297259cab": 16,
    "5b1f99a7478dd3768d84b646": 12,
    "5b913111f19a473232026877": 3,
    "5ba95b5c630b876a1e9785a5": 1
  },
  "about": "",
  "followed": true
}
```

This endpoint retrieves a specific topic using ID.

### HTTP Request

<code class="request">GET /api/v1/topics/{id}</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the item




## Create a Topic


```shell
curl "https://community.tribe.so/api/v1/topics"
  -X POST
  -H "Authorization: Bearer {access_token}"
  -H 'Content-Type: application/json; charset=utf-8' \
  --DATA '{"name":"Test Topic"}'
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.topics.create({name: 'Test Topic'});
```

> The above command returns JSON structured like this:

```json
{
  "_id": "5b88264d3d9228aa7c41f693",
  "name": "Test Topic",
  "portal": "5a73b1fcc48071e4c4dc1cae",
  "updatedAt": "2018-11-29T06:16:08.223Z",
  "__v": 8,
  "createdAt": "2018-08-30T17:15:57.884Z",
  "aliases": [],
  "children": [],
  "counts": {
    "questions": 0,
    "followers": 0,
    "subquestions": 0,
    "children": 0
  },
  "definitions": [],
  "paths": [],
  "shortId": "5oqoy",
  "user": "5b881b2a90ecbe6751123d7e",
  "experts": {},
  "about": "",
  "followed": false
}
```

This endpoint creates a new topic.

### HTTP Request

<code class="request">POST /api/v1/topics</code>


### Request Parameters

Parameter | Type | Default | Description
--------- | ------- | ----------- | -----------
name | `String` | `null` | The name of the Topic
about | `String` | `null` | The description of the Topic
picture | `String` | `null` | Url to a picture for this Topic
definitions | `[String]` | `[]` | The different types assigned with the Topic. It can be an array of following: <code>['Concept', 'Location', 'Localizable','Activity', 'QuestionType', 'Category', 'Event', 'Person', 'AcademicField', 'Job', 'Person', 'Company', 'School', 'Product', 'Adult']</code>
aliases | `[String]` | `[]` | An array of Aliases for this Topic. Aliases help users search the Topic with different keywords.
externalId | `String` | `null` | The unique ID of the Topic in an external platform. This is useful when creating a Topic for an external entity.

## Update a Specific Topic


```shell
curl "https://community.tribe.so/api/v1/topics/5b88264d3d9228aa7c41f692"
  -X PUT
  -H "Authorization: Bearer {access_token}"
  -H 'Content-Type: application/json; charset=utf-8' \
  --DATA '{data}'
```

This endpoint updates a specific topic.

### HTTP Request

<code class="request">PUT /api/v1/topics/:id</code>

### URL Parameters

Parameter | Type | Default
--------- | ------- | -------
id | `String` | The ID of the topic to update

### Request Parameters

Parameter | Type | Default | Description
--------- | ------- | ----------- | -----------
name | `String` | `null` | The name of the Topic
about | `String` | `null` | The description of the Topic
definitions | `[String]` | `[]` | The different types assigned with the Topic. It can be an array of following: <code>['Concept', 'Location', 'Localizable','Activity', 'QuestionType', 'Category', 'Event', 'Person', 'AcademicField', 'Job', 'Person', 'Company', 'School', 'Product', 'Adult']</code>
aliases | `[String]` | `[]` | An array of Aliases for this Topic. Aliases help users search the Topic with different keywords.

### Extra Request Parameters

Parameter | Type | Default | Description
--------- | ------- | -----------  | -----------
picture | `String` | `null` | Url to a picture for this Topic
externalId | `String` | `null` | The unique ID of the Topic in an external platform. This is useful when creating a Topic for an external entity.

## Delete a Specific Topic


```shell
curl "https://community.tribe.so/api/v1/topics/5b88264d3d9228aa7c41f692"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.topics.delete('5b88264d3d9228aa7c41f692');
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint deletes a specific topic.

### HTTP Request

<code class="request">DELETE /api/v1/topics/{id}</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the topic to delete



## Get Topic's Questions


```shell
curl "https://community.tribe.so/api/v1/topics/5b88264d3d9228aa7c41f692/questions"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.topics.questions('5b88264d3d9228aa7c41f692');
```


### HTTP Request

<code class="request">GET /api/v1/topics/{id}/questions</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the topic




## Get Topic's Experts


```shell
curl "https://community.tribe.so/api/v1/topics/5b88264d3d9228aa7c41f692/experts"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.topics.experts('5b88264d3d9228aa7c41f692');
```


### HTTP Request

<code class="request">GET /api/v1/topics/{id}/experts</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the topic