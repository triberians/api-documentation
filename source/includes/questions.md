# Questions

## Get All Questions


```shell
curl "https://community.tribe.so/api/v1/questions"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let questions = api.questions.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "_id": "5a816275f8030b3bdd655b0d",
    "updatedAt": "2018-02-12T19:07:21.136Z",
    "createdAt": "2018-02-12T09:46:29.646Z",
    "title": "What is a perfect life?",
    "lastAskedAt": "2018-02-12T09:46:29.642Z",
    "__v": 0,
    "lastAnsweredAt": "2018-02-12T19:07:21.135Z",
    "downvotes": [],
    "upvotes": [],
    "followers": [],
    "askers": [],
    "comments": [],
    "topics": [],
    "score": 0,
    "counts": {
      "asks": 1,
      "downvotes": 0,
      "upvotes": 0,
      "edits": 2,
      "comments": 0,
      "hiddenAnswers": 0,
      "answers": 2,
      "views": 8,
      "followers": 0
    },
    "type": "general",
    "anonymous": true,
    "verified": false,
    "locked": false,
    "followed": false
  }
]
```

This endpoint retrieves all questions.

### HTTP Request

<code class="request">GET /api/v1/questions</code>

### Query Parameters

Parameter | Type | Default | Description
--------- | ------- | ----------- | -----------
page | `Number` | `1` | Intended page
limit | `Number` | `20` | Number of items per page
sort | `String` | `createdAt.desc` | The field to sort on


## Get a Specific Question


```shell
curl "https://community.tribe.so/api/v1/questions/5a816275f8030b3bdd655b0d"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let questions = api.questions.get('5a816275f8030b3bdd655b0d');
```

> The above command returns JSON structured like this:

```json
{
  "_id": "5a816275f8030b3bdd655b0d",
  "updatedAt": "2018-02-12T19:07:21.136Z",
  "createdAt": "2018-02-12T09:46:29.646Z",
  "title": "What is a perfect life?",
  "lastAskedAt": "2018-02-12T09:46:29.642Z",
  "__v": 0,
  "lastAnsweredAt": "2018-02-12T19:07:21.135Z",
  "downvotes": [],
  "upvotes": [],
  "followers": [],
  "askers": [],
  "comments": [],
  "topics": [],
  "score": 0,
  "counts": {
    "asks": 1,
    "downvotes": 0,
    "upvotes": 0,
    "edits": 2,
    "comments": 0,
    "hiddenAnswers": 0,
    "answers": 2,
    "views": 8,
    "followers": 0
  },
  "type": "general",
  "anonymous": true,
  "verified": false,
  "locked": false,
  "followed": false
}
```

This endpoint retrieves a specific question using ID.

### HTTP Request

<code class="request">GET /api/v1/questions/{id}</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the item


## Delete a Specific Question


```shell
curl "https://community.tribe.so/api/v1/questions/5a816275f8030b3bdd655b0d"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.questions.delete('5a816275f8030b3bdd655b0d');
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint deletes a specific question.

### HTTP Request

<code class="request">DELETE /api/v1/questions/{id}</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the question to delete



## Get Question's Answers


```shell
curl "https://community.tribe.so/api/v1/questions/5a816275f8030b3bdd655b0d/answers"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.questions.answers('5a816275f8030b3bdd655b0d');
```


### HTTP Request

<code class="request">GET /api/v1/questions/{id}/answers</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the question

### Query Parameters

Parameter | Type | Default | Description
--------- | ----------- | ------- | -----------
page | `Number` | `1` | Intended page
limit | `Number` | `20` | Number of items per page
sort | `Number` | `createdAt.desc` | The field to sort on




## Get Question's Experts


```shell
curl "https://community.tribe.so/api/v1/questions/5a816275f8030b3bdd655b0d/experts"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.questions.experts('5a816275f8030b3bdd655b0d');
```


### HTTP Request

<code class="request">GET /api/v1/questions/{id}/experts</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the question



## Get a Question's Recommendations


```shell
curl "https://community.tribe.so/api/v1/questions/5a816275f8030b3bdd655b0d/recommendations"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.questions.recommendations('5a816275f8030b3bdd655b0d');
```


### HTTP Request

<code class="request">GET /api/v1/questions/{id}/recommendations</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the question


## Get Similar Questions


```shell
curl "https://community.tribe.so/api/v1/questions/similars"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.questions.similars('This is a test question title');
```

This endpoint find related questions to keywords or a question title.

### HTTP Request

<code class="request">GET /api/v1/questions/similars</code>


### Query Parameters

Parameter | Type | Default | Description
--------- | ------- | ----------- | -----------
query | `String` | `""` | Keywords or title of a question




## Create a Question


```shell
curl "https://community.tribe.so/api/v1/questions"
  -X POST
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let question = api.questions.create({ title: 'What is life?'});
```

This endpoint creates a new question.

### HTTP Request

<code class="request">POST /api/v1/questions</code>

### Query Parameters

Parameter | Type | Description
--------- | ----------- | ----------- | -----------
title | `String` | The title of the question to create
description | `String` | The description of the question to create
anonymous | `Boolean` | Is this an anonymous question?
from | `String` | The ID of the user who has beend asked from
topics | `[String]` | The IDs of the topics related to the question

### Extra Query Parameters for Moderators

Parameter | Type | Description
--------- | ----------- | -----------
type | `String` | The type of the question to create
locked | `Boolean` | Is the question locked?
verified | `Boolean` | Is the question verified?
status | `String` | Status of the question to create. Should be one of the followings: `archived` `collapsed` `published` `unapproved` `unlisted` `featured` `scheduled`
user | `String` | The ID of the user to ask a question on behalf 

## Update a Specific Question


```shell
curl "https://community.tribe.so/api/v1/questions/5a816275f8030b3bdd655b0d"
  -X PUT
  -H "Authorization: Bearer {access_token}"
```

This endpoint updates a specific question.

### HTTP Request

<code class="request">PUT /api/v1/questions/:id</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the question to update

### Query Parameters

Parameter | Type | Description
--------- | ----------- | -----------
title | `String` | The title of the question to create
description | `String` | The description of the question to create
anonymous | `Boolean` | Is this an anonymous question?

### Extra Query Parameters for Moderators

Parameter | Type | Description
--------- | ----------- | -----------
type | `String` | The type of the question to create
locked | `Boolean` | Is the question locked?
verified | `Boolean` | Is the question verified?
status | `String` | Status of the question to create. Should be one of the followings: `archived` `collapsed` `published` `unapproved` `unlisted` `featured` `scheduled`

## Add a Comment for a Specific Question

```shell
  curl "https://community.tribe.so/api/v1/questions/5bf0e89ada3be54c190b78ba/comments"
  -X POST
  -H "Authorization: Bearer {access_token}"
  --DATA "{'body':'New comment'}"
```
> The above command returns JSON structured like this:

```json
 @todo
```

This endpoint adds a comment for a specific question.

### HTTP Request

<code class="request">POST /api/v1/questions/:id/comments</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the question to add a comment

### Request Parameters

Parameter | Type | Description
--------- | ----------- | -----------
body | `String` | The content of the comment

## Update a Specific Comment for a Specific Question

```shell
  curl "https://community.tribe.so/api/v1/questions/5bf0e89ada3be54c190b78ba/comments/4sf0e89ada3be54c190b78b2"
  -X PUT
  -H "Authorization: Bearer {access_token}"
  --DATA "{'body':'Updated comment'}"
```
> The above command returns JSON structured like this:

```json
 @todo
```

This endpoint updates a specific comment.

### HTTP Request

<code class="request">PUT /api/v1/questions/:questionId/comments/:id</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the comment to update
questionId | `String` | The ID of the question to add a comment

### Request Parameters

Parameter | Type | Description
--------- | ----------- | -----------
body | `String` | The content of the comment

## Remove a Specific Comment from Specific Question

```shell
  curl "https://community.tribe.so/api/v1/questions/5bf0e89ada3be54c190b78ba/comments/4sf0e89ada3be54c190b78b2"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```
> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint removes a specific comment.

### HTTP Request

<code class="request">DELETE /api/v1/questions/:questionId/comments/:id</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the comment to remove
questionId | `String` | The ID of the question to remove a comment