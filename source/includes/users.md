# Users

## Get All Users


```shell
curl "https://community.tribe.so/api/v1/users"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.users.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "_id": "5b1f99a7478dd3768d84b646",
    "profile": {
      "counts": {
        "requests": 2,
        "edits": 46,
        "questionsFollowers": 0,
        "questions": 2,
        "comments": 2,
        "answersWords": 1586,
        "answersVotes": 0,
        "answersViews": 0,
        "answers": 12,
        "views": 0,
        "followings": 3,
        "followers": 3
      },
      "score": 52,
      "externalId": null,
      "verified": true,
      "description": "",
      "title": "Tribe Moderator",
      "picture": "",
      "website": "",
      "location": "",
      "gender": "male",
      "name": "John Smith",
      "username": "john"
    },
    "id": "5b1f99a7478dd3768d84b646",
    "followed": false
  }
]
```

This endpoint retrieves all users.

### HTTP Request

<code class="request">GET /api/v1/users</code>

### Query Parameters

Parameter | Type | Default | Description
--------- | ------- | ----------- | -----------
page | `number` | `1` | Intended page
limit | `number` | `20` | Number of items per page
sort | `number` | `createdAt.desc` | The field to sort on


## Get a Specific User


```shell
curl "https://community.tribe.so/api/v1/users/5b1f99a7478dd3768d84b646"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.users.get('5b1f99a7478dd3768d84b646');
```

> The above command returns JSON structured like this:

```json
{
  "_id": "5b1f99a7478dd3768d84b646",
  "profile": {
    "counts": {
      "requests": 2,
      "edits": 46,
      "questionsFollowers": 0,
      "questions": 2,
      "comments": 2,
      "answersWords": 1586,
      "answersVotes": 0,
      "answersViews": 0,
      "answers": 12,
      "views": 0,
      "followings": 3,
      "followers": 3
    },
    "score": 52,
    "externalId": null,
    "verified": true,
    "description": "",
    "title": "Tribe Moderator",
    "picture": "",
    "website": "",
    "location": "",
    "gender": "male",
    "name": "John Smith",
    "username": "john"
  },
  "id": "5b1f99a7478dd3768d84b646",
  "followed": false
}
```

This endpoint retrieves a specific user using ID.

### HTTP Request

<code class="request">GET /api/v1/users/{id}</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `string` | The ID of the user


## Update a Specific User


```shell
curl "https://community.tribe.so/api/v1/users/5b1f99a7478dd3768d84b646"
  -X PUT
  -H "Authorization: Bearer {access_token}"
```

This endpoint updates a specific user using ID.

### HTTP Request

<code class="request">PUT /api/v1/users/{id}</code>


### URL Parameters

Parameter | Type | Description
--------- | -----------  | -----------
id | `string` | The ID of the user to update

### Request Parameters

Parameter | Type | Description
--------- | ----------- | -----------
name | `string` | Name of the user
@todo | @todo | @todo


## Delete a Specific User


```shell
curl "https://community.tribe.so/api/v1/users/5b1f99a7478dd3768d84b646"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.users.delete('5b1f99a7478dd3768d84b646');
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint deletes a specific user.

### HTTP Request

<code class="request">DELETE /api/v1/users/{id}</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `string` | The ID of the user to delete





## Get User's Followers


```shell
curl "https://community.tribe.so/api/v1/users/5b1f99a7478dd3768d84b646/followers"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.users.followers('5b1f99a7478dd3768d84b646');
```

> The above command returns JSON structured like this:

```json
[
  {
    "_id": "5b3f7fe0d5a11b6297259cab",
    "profile": {
      "counts": {
        "requests": 2,
        "edits": 46,
        "questionsFollowers": 0,
        "questions": 4,
        "comments": 0,
        "answersWords": 1128,
        "answersVotes": 0,
        "answersViews": 0,
        "answers": 8,
        "views": 0,
        "followings": 1,
        "followers": 2
      },
      "score": 58,
      "externalId": null,
      "verified": true,
      "description": "<p>&nbsp;</p>",
      "title": "Community Moderator at Tribe",
      "picture": "/files/users/cab/5b3f7fe0d5a11b6297259cab_57983.png",
      "website": "",
      "location": "",
      "gender": "",
      "name": "Mike Modiri",
      "username": "mike"
    },
    "id": "5b3f7fe0d5a11b6297259cab",
    "followed": false
  }
]
```

This endpoint retrieves a specific user's followers using ID.

### HTTP Request

<code class="request">GET /api/v1/users/{id}/followers</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `string` | The ID of the user


## Get User's Following


```shell
curl "https://community.tribe.so/api/v1/users/5b1f99a7478dd3768d84b646/followings"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.users.following('5b1f99a7478dd3768d84b646');
```

> The above command returns JSON structured like this:

```json
[
  {
    "_id": "5b3f7fe0d5a11b6297259cab",
    "profile": {
      "counts": {
        "requests": 2,
        "edits": 46,
        "questionsFollowers": 0,
        "questions": 4,
        "comments": 0,
        "answersWords": 1128,
        "answersVotes": 0,
        "answersViews": 0,
        "answers": 8,
        "views": 0,
        "followings": 1,
        "followers": 2
      },
      "score": 58,
      "externalId": null,
      "verified": true,
      "description": "<p>&nbsp;</p>",
      "title": "Community Moderator at Tribe",
      "picture": "/files/users/cab/5b3f7fe0d5a11b6297259cab_57983.png",
      "website": "",
      "location": "",
      "gender": "",
      "name": "Mike Modiri",
      "username": "mike"
    },
    "id": "5b3f7fe0d5a11b6297259cab",
    "followed": false
  }
]
```

This endpoint retrieves a specific user's followings using ID.

### HTTP Request

<code class="request">GET /api/v1/users/{id}/followings</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `string` | The ID of the user



## Get User's Expertise


```shell
curl "https://community.tribe.so/api/v1/users/5b1f99a7478dd3768d84b646/expertise"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.users.expertise('5b1f99a7478dd3768d84b646');
```

> The above command returns JSON structured like this:

```json
[
  {
    "topic": {
      "_id": "5b88264d3d9228aa7c41f692",
      "name": "Tribe",
      "portal": "5a73b1fcc48071e4c4dc1cae",
      "updatedAt": "2018-12-04T06:41:25.365Z",
      "__v": 8,
      "createdAt": "2018-08-30T17:15:57.884Z",
      "shortId": "5oqoy",
      "picture": "/files/topics/692/5b88264d3d9228aa7c41f692_72807.png",
      "experts": {
        "5ba95b5c630b876a1e9785a5": 1,
        "5b913111f19a473232026877": 3,
        "5b1f99a7478dd3768d84b646": 12,
        "5b3f7fe0d5a11b6297259cab": 16,
        "5b881b2a90ecbe6751123d7e": 24
      },
      "about": "<p>&nbsp;</p>",
      "counts": {
        "children": 4,
        "edits": 0,
        "posts": 1,
        "subquestions": 79,
        "questions": 55,
        "subanswers": 0,
        "answers": 0,
        "views": 0,
        "followers": 3
      },
      "paths": [
        [
          {
            "picture": "/files/topics/692/5b88264d3d9228aa7c41f692_72807.png",
            "name": "Tribe",
            "_id": "5b88264d3d9228aa7c41f692"
          }
        ]
      ],
      "id": "5b88264d3d9228aa7c41f692",
      "followed": true
    },
    "score": 12
  },
  {
    "topic": {
      ...
    },
    "score": 5
  },
  {
    "topic": {
      ...
    },
    "score": 2
  },
  {
    "topic": {
      ...
    },
    "score": 1
  }
]
```

This endpoint retrieves a specific user's expertise using ID.

### HTTP Request

<code class="request">GET /api/v1/users/{id}/expertise</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `string` | The ID of the user




## Get User's Questions


```shell
curl "https://community.tribe.so/api/v1/users/5b1f99a7478dd3768d84b646/questions"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.users.questions('5b1f99a7478dd3768d84b646');
```


### HTTP Request

<code class="request">GET /api/v1/users/{id}/questions</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `string` | The ID of the user



## Get User's Answers


```shell
curl "https://community.tribe.so/api/v1/users/5b1f99a7478dd3768d84b646/answers"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.users.answers('5b1f99a7478dd3768d84b646');
```


### HTTP Request

<code class="request">GET /api/v1/users/{id}/answers</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `string` | The ID of the user
