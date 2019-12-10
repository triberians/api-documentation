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
page | `Number` | `1` | Intended page
limit | `Number` | `20` | Number of items per page
sort | `Number` | `createdAt.desc` | The field to sort on


## Create a new User


```shell
curl "https://community.tribe.so/api/v1/users"
  -X POST
  -H "Authorization: Bearer {access_token}"
  --DATA '{data}'
```
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.users.create({
  username: "info",
  name:"Mr Support",
  email: "info@tribe.so",
  password: ...,
  confirmPassword: ...
});
```

This endpoint creates a new user.

### HTTP Request

<code class="request">POST /api/v1/users/</code>

### Request Parameters

Parameter | Type | Description | Required
--------- | ----------- | ----------- | -----------
username | `String` | Username of the user | `Yes`
name | `String` | Name of the user | `Yes`
email | `String` | Email of the user | `Yes`
password | `String` | Password of the user | `Yes`
confirmPassword | `String` | Confirm password of the user | `No`

## Invite new Users


```shell
curl "https://community.tribe.so/api/v1/user/email/invitations"
  -X POST
  -H "Authorization: Bearer {access_token}"
  --DATA '{data}'
```
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = [
  {
    name:"Mr Support",
    email: "info@tribe.so",
  },
  {
    name:"Mr Tech",
    email: "tech@tribe.so",
  },
];
let data = {
  users,
  role: 'member',
}
api.users.invite(data)
```

> The above command returns JSON structured like this:

```json
{
  "success": true,
  "count": 1
}
```

This endpoint send invitation email to people. The free plan is limited to 50 invitaions per day.

### HTTP Request

<code class="request">POST /api/v1/user/email/invitations/</code>

### Request Parameters

Parameter | Type | Description | Required
--------- | ----------- | ----------- | -----------
role | `String` | Role of the users | `Yes`
users | `Array<Object>` | List of users | `Yes`
message | `String` | Custom message for the invitation | `No`

### User Parameters
Parameter | Type | Description
--------- | ----------- | -----------
name | `String` | Name of the user
email | `String` | Email of the user

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
id | `String` | The ID of the user


## Update a Specific User


```shell
curl "https://community.tribe.so/api/v1/users/5b1f99a7478dd3768d84b646"
  -X PUT
  -H "Authorization: Bearer {access_token}"
  --DATA '{data}'
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.users.update("5b1f99a7478dd3768d84b646",{
  name:"Ms. Support"
});
```

This endpoint updates a specific user using ID.

### HTTP Request

<code class="request">PUT /api/v1/users/{id}</code>


### URL Parameters

Parameter | Type | Description
--------- | -----------  | -----------
id | `String` | The ID of the user to update

### Request Parameters

Parameter | Type | Description | Required
--------- | ----------- | ----------- | -----------
username | `String` | Username of the user | `Yes`
name | `String` | Name of the user | `Yes`
email | `String` | Email of the user | `Yes`
password | `String` | Password of the user | `Yes`
confirmPassword | `String` | Confirm password of the user | `No`
links | `Object` | List of user's social network accounts | `No`
bankAccount | `Object` | User's bank account | `No`
location | `String` | Location of the user | `No`
website | `String` | Website owned by user | `No`
gender | `String` | Gender of the user | `No`
title | `String` | Title of the user | `No`
description | `String` | A short description of user | `No`

### Bank Account Parameters
Parameter | Type | Description
--------- | ----------- | -----------
holderName | `String` | Name of the holder
accountNumber | `String` | Account number
type | `String` | Type of the account. Can be: `card`, `checking`, `saving`
routingNumber | `String` | Routing number for the bank account
bankName | `String` | Name of the bank related to account

### Links Parameters
Parameter | Type | Description
--------- | ----------- | -----------
telegram | `String` | Telegram account of the user
instagram | `String` | Instagram account of the user
twitter | `String` | Twitter account of the user
facebook | `String` | Facebook account of the user
linkedin | `String` | Twitter account of the user
homepage | `String` | The url of homepage of user

### Extra Request Parameters for Moderators
Parameter | Type | Description
--------- | ----------- | -----------
verified | `Boolean` | Is the user verified or not
status | `String` | Status of the user
badge | `Object` | User's badge | `No`

### Extra Request Parameters for Admin
Parameter | Type | Description
--------- | ----------- | -----------
role | `String` | Role of the user

### Badge Parameters
Parameter | Type | Description
--------- | ----------- | -----------
text | `Boolean` | Text of the badge
type | `String` | Type of the badge. It can be one of the followings: [`gold`, `silver`, `bronze`]

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
id | `String` | The ID of the user to delete





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
id | `String` | The ID of the user


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
id | `String` | The ID of the user




## Follow a user


```shell
curl "https://community.tribe.so/api/v1/users/5b1f99a7478dd3768d84b646/followers"
  -X POST
  -H "Authorization: Bearer {access_token}"
```
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let user = api.users.follow('5b1f99a7478dd3768d84b646');
```

This endpoint follows a user.

### HTTP Request

<code class="request">POST /api/v1/users/{id}/followers</code>


## Unfollow a user


```shell
curl "https://community.tribe.so/api/v1/users/5b1f99a7478dd3768d84b646/followers"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let user = api.users.unfollow('5b1f99a7478dd3768d84b646');
```

This endpoint unfollows a user.

### HTTP Request

<code class="request">DELETE /api/v1/users/{id}/followers</code>


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
id | `String` | The ID of the user




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

> The above command returns JSON structured like this:

```json
[
  {
    "_id": "5ddbdb3d47a56345bc4bb3d2",
    "shortId": "dAV2L",
    "lang": "en",
    "updatedAt": "2019-11-25T13:46:37.529Z",
    "createdAt": "2019-11-25T13:46:37.529Z",
    "title": "how do i embed endorsal dynamic form on tribe and can i use tags from the site like avatar, first name, second name and email?",
    "publishedAt": "2019-11-25T13:46:37.528Z",
    "portal": "5a73b1fcc48071e4c4dc1cae",
    "lastAskedAt": "2019-11-25T13:46:37.528Z",
    "user": {
      "_id": "5dd484e7b033d753be0f71a4",
      "profile": {
        "name": "andy sandford",
        "username": "andrewsandford",
        ...
      },
      "externalId": null,
      "id": "5dd484e7b033d753be0f71a4"
    },
    "__v": 0,
    "referrers": [],
    "aliases": [],
    "rewards": [],
    "hasReward": false,
    "downvotes": [],
    "upvotes": [],
    "followers": [],
    "askers": [],
    "comments": [],
    "options": [],
    "topics": [],
    "score": 0,
    "status": "published",
    "counts": {
      "pollVotes": 0,
      "asks": 1,
      "downvotes": 0,
      "upvotes": 0,
      "edits": 1,
      "comments": 0,
      "hiddenAnswers": 0,
      "answers": 0,
      "views": 0,
      "followers": 0
    },
    "type": "general",
    "privacy": "public",
    "anonymous": false,
    "verified": false,
    "locked": false,
    "id": "5ddbdb3d47a56345bc4bb3d2",
    "followed": false,
    "url": "/question/5ddbdb3d47a56345bc4bb3d2",
    "api_url": "/questions/5ddbdb3d47a56345bc4bb3d2"
  },
  ...
]
```

This endpoint retrieves a specific user's questions using ID.

### HTTP Request

<code class="request">GET /api/v1/users/{id}/questions</code>


### URL Parameters

Parameter | Type | Default | Description
--------- | ------- | ----------- | -----------
id | `String` | | The ID of the user
page | `Number` | `1` | Intended page
limit | `Number` | `20` | Number of items per page
sort | `String` | `createdAt.desc` | The field to sort on



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

> The above command returns JSON structured like this:

```json
[
  {
    "_id": "5dd7260552a5be0ba42b94a6",
    "updatedAt": "2019-11-25T12:55:10.718Z",
    "createdAt": "2019-11-22T00:04:21.631Z",
    "portal": "5a73b1fcc48071e4c4dc1cae",
    "question": {
      "_id": "5dd6f272f8730a37e88ba86c",
      ...
    },
    "user": {
      "_id": "5c7037e168356d17013df39b",
      "profile": {
        "name": "Preetish",
        "username": "preetish",
        ...
      },
      ...
    },
    "__v": 9,
    "lang": "en",
    "publishedAt": "2019-11-22T00:12:25.579Z",
    "shortId": "LOKKn",
    "downvotes": [],
    "upvotes": [
      ...
    ],
    "comments": [
      ...
    ],
    "rewards": [],
    "images": [
      ...
    ],
    "links": [
      ...
    ],
    "privacy": "public",
    "anonymous": false,
    "verified": false,
    "summary": "Sure, if you have already verified your domain via Google Analytics or Tag Manager, you can simply use that. Otherwise, you can access the community Theme (look for advanced settings tab) un...",
    "id": "5dd7260552a5be0ba42b94a6",
    ...
  },
  ...
]
```

This endpoint retrieves a specific user's answers using ID.

### HTTP Request

<code class="request">GET /api/v1/users/{id}/answers</code>


### URL Parameters

Parameter | Type | Default | Description
--------- | ------- | ----------- | -----------
id | `String` | | The ID of the user
page | `Number` | `1` | Intended page
limit | `Number` | `20` | Number of items per page
sort | `String` | `createdAt.desc` | The field to sort on

## Get User's Posts


```shell
curl "https://community.tribe.so/api/v1/users/5c7037e168356d17013df39b/posts?type=discussion"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let data = {
  type: 'discussion'
}
let users = api.users.posts('5c7037e168356d17013df39b', data);
```

> The above command returns JSON structured like this:

```json
[
  {
    "_id": "5d03f4abdb3dbb6f2c9d4ff8",
    "shortId": "yM7Zz",
    "lang": "en",
    "updatedAt": "2019-11-23T15:49:47.804Z",
    "createdAt": "2019-06-14T19:25:31.241Z",
    "title": "Common Mistakes to Avoid When Building Online Communities",
    "content": "<p>This <a href=\"https://blog.tribe.so/10-common-mistakes-to-avoid-when-building-online-communities/\"><strong>comprehensive blog</strong></a> covers the 10 most common mistakes that must be avoided when building online communities — from the lack of content seeding and internal support to poor processes and aggressive growth targets.</p><p>What are some of your key learnings from community building?</p>",
    "publishedAt": "2019-06-14T19:25:31.201Z",
    "portal": "5a73b1fcc48071e4c4dc1cae",
    "user": {
      "_id": "5c7037e168356d17013df39b",
      "profile": {
        "name": "Preetish",
        "username": "preetish",
        ...
      },
      "externalId": null,
      "id": "5c7037e168356d17013df39b"
    },
    "__v": 6,
    "referrers": [],
    "downvotes": [],
    "upvotes": [
      ...
    ],
    "comments": [],
    "rewards": [],
    "files": [],
    "images": [],
    "attachments": [],
    "topics": [
      ...
    ],
    "posters": [
      ...
    ],
    "followers": [
      ...
    ],
    "score": 0,
    "counts": {
      "downvotes": 0,
      "links": 0,
      "totalUpvotes": 0,
      "upvotes": 2,
      "followers": 0,
      "edits": 0,
      "responses": 1,
      "comments": 0,
      "views": 0
    },
    "status": "published",
    "privacy": "public",
    "kind": "article",
    "type": "discussion",
    "anonymous": false,
    "verified": false,
    "responses": [
      ...
    ],
    "summary": "This comprehensive blog covers the 10 most common mistakes that must be avoided when building online communities — from the lack of content seeding and internal support to poor processes and...",
    "id": "5d03f4abdb3dbb6f2c9d4ff8",
    "upvoted": false,
    "downvoted": false,
    "followed": false
  }
]
```

This endpoint retrieves a specific user's posts (Discussions, Blogs, Quick Post, Replies) using ID.

### HTTP Request

<code class="request">GET /api/v1/users/{id}/posts</code>


### URL Parameters

Parameter | Type | Default | Description
--------- | ------- | ----------- | -----------
id | `String` | | The ID of the user
type | `String` | | Type of posts. It can be empty (for all types) or a string of types of posts (`simple`, `discussion`, `article`, `response`) seprated by comma 
page | `Number` | `1` | Intended page
limit | `Number` | `20` | Number of items per page
sort | `String` | `createdAt.desc` | The field to sort on

## Add device token

```shell
curl "https://community.tribe.so/api/v1/user/devices"
  -H "Authorization: Bearer {access_token}"
  -X POST
  --DATA "{...}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
api.authUser().addDevice({...})
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint add device token to the authenticated user.

### HTTP Request

<code class="request">POST /api/v1/user/devices</code>

### URL Parameters

Parameter | Default | Description
--------- | --------- | -----------
id |  | The ID of user to add the device token

### Request Parameters

Parameter | Default | Description
--------- | --------- | -----------
token |  | Device token
type |  | Type of the device. It can be one of [`web` , `ios`, `android`]
name |  | Optional name for the device 

## Remove device token

```shell
curl "https://community.tribe.so/api/v1/user/devices"
  -H "Authorization: Bearer {access_token}"
  -X DELETE
  --DATA "{...}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
api.authUser().removeDevice({...})
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint remove device token from the authenticated user.

### HTTP Request

<code class="request">DELETE /api/v1/user/devices</code>

### URL Parameters

Parameter | Default | Description
--------- | --------- | -----------
id |  | The ID of user to add the device token

### Request Parameters

Parameter | Default | Description
--------- | --------- | -----------
token |  | Device token