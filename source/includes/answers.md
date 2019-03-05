# Answers

## Get All Answers


```shell
curl "https://community.tribe.so/api/v1/answers"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let answers = api.answers.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "_id": "5bf0e89ada3be54c190b78ba",
    "updatedAt": "2018-12-03T22:20:11.069Z",
    "createdAt": "2018-11-18T04:20:42.892Z",
    "draftContent": "",
    "portal": "5a73b1fcc48071e4c4dc1cae",
    "question": {
      "_id": "5bf0e860da3be54c190b78b8",
      "shortId": "5okGL",
      "updatedAt": "2018-12-03T23:26:53.588Z",
      "createdAt": "2018-11-18T04:19:44.936Z",
      "title": "Can I embed external services (YouTube, Vimeo, etc.) in my answers or posts?",
      "user": {
        "_id": "5bacc9ff630b876a1e9785f7",
        "profile": {
          "counts": {
            "requests": 0,
            "edits": 0,
            "questionsFollowers": 0,
            "questions": 8,
            "comments": 0,
            "answersWords": 615,
            "answersVotes": 0,
            "answersViews": 0,
            "answers": 3,
            "views": 0,
            "followings": 0,
            "followers": 0
          },
          "score": 13,
          "externalId": null,
          "verified": false,
          "description": "",
          "title": "",
          "picture": "/files/users/5f7/5bacc9ff630b876a1e9785f7_15302.png",
          "website": "",
          "location": "",
          "gender": "",
          "name": "Robert D",
          "username": "robertd"
        },
        "id": "5bacc9ff630b876a1e9785f7"
      },
      "publishedAt": "2018-11-18T04:19:44.933Z",
      "portal": "5a73b1fcc48071e4c4dc1cae",
      "lastAskedAt": "2018-11-18T04:19:44.933Z",
      "actor": "5b1f99a7478dd3768d84b646",
      "__v": 1,
      "lastAnsweredAt": "2018-11-18T04:25:42.040Z",
      "referrers": [],
      "rewards": [],
      "hasReward": false,
      "downvotes": [],
      "upvotes": [],
      "followers": [],
      "askers": [],
      "comments": [],
      "topics": [
        {
          "_id": "5b88264d3d9228aa7c41f692",
          "name": "Tribe",
          "user": {
            "_id": "5b881b2a90ecbe6751123d7e",
            "profile": {
              "counts": {
                "requests": 2,
                "edits": 148,
                "questionsFollowers": 0,
                "questions": 32,
                "comments": 0,
                "answersWords": 5753,
                "answersVotes": 0,
                "answersViews": 0,
                "answers": 31,
                "views": 0,
                "followings": 1,
                "followers": 2
              },
              "score": 115,
              "externalId": null,
              "verified": false,
              "description": "<p>&nbsp;</p>",
              "title": "Biomedical Engineer ",
              "picture": "/files/users/d7e/5b881b2a90ecbe6751123d7e_57697.png",
              "website": "",
              "location": "",
              "gender": "",
              "name": "Elnaz Najafi",
              "username": "elnajafi89"
            },
            "id": "5b881b2a90ecbe6751123d7e"
          },
          "picture": "/files/topics/692/5b88264d3d9228aa7c41f692_72807.png",
          "id": "5b88264d3d9228aa7c41f692"
        }
      ],
      "score": 0,
      "status": "published",
      "counts": {
        "asks": 1,
        "downvotes": 0,
        "upvotes": 0,
        "edits": 2,
        "comments": 0,
        "hiddenAnswers": 0,
        "answers": 1,
        "views": 33,
        "followers": 0
      },
      "type": "general",
      "privacy": "public",
      "anonymous": false,
      "verified": false,
      "locked": false,
      "id": "5bf0e860da3be54c190b78b8"
    },
    "user": {
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
        "description": "<p>&nbsp;</p>",
        "title": "Tribe Moderator",
        "picture": "/files/users/646/5b1f99a7478dd3768d84b646_66172.png",
        "website": "",
        "location": "",
        "gender": "male",
        "name": "Siavash Mahmoudian",
        "username": "siavash"
      },
      "id": "5b1f99a7478dd3768d84b646",
      "followed": false
    },
    "__v": 1,
    "publishedAt": "2018-11-18T04:25:42.037Z",
    "shortId": "PEVpN",
    "downvotes": [],
    "upvotes": [
      "5bc64d97a8c76d6d771ae914"
    ],
    "comments": [],
    "rewards": [],
    "images": [],
    "links": [],
    "score": 0,
    "global": true,
    "status": "published",
    "media": [],
    "counts": {
      "reasks": 0,
      "edits": 2,
      "downvotes": 0,
      "upvotes": 1,
      "comments": 0,
      "views": 34
    },
    "privacy": "public",
    "anonymous": false,
    "verified": false,
    "summary": "...",
    "id": "5bf0e89ada3be54c190b78ba",
    "upvoted": false,
    "downvoted": false,
    "intro": "..."
  }
]
```

This endpoint retrieves all answers.

### HTTP Request

<code class="request">GET /api/v1/answers</code>

### Query Parameters

Parameter | Type | Default | Description
--------- | ------- | ----------- | -----------
page | `Number` | `1` | Intended page
limit | `Number` | `20` | Number of items per page
sort | `String` | `createdAt.desc` | The field to sort on


## Get a Specific Answer


```shell
curl "https://community.tribe.so/api/v1/answers/5bf0e89ada3be54c190b78ba"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let answers = api.answers.get('5bf0e89ada3be54c190b78ba');
```

> The above command returns JSON structured like this:

```json
{
  "_id": "5bf0e89ada3be54c190b78ba",
  "updatedAt": "2018-12-03T22:20:11.069Z",
  "createdAt": "2018-11-18T04:20:42.892Z",
  "draftContent": "",
  "portal": "5a73b1fcc48071e4c4dc1cae",
  "question": {
    "_id": "5bf0e860da3be54c190b78b8",
    "shortId": "5okGL",
    "updatedAt": "2018-12-03T23:26:53.588Z",
    "createdAt": "2018-11-18T04:19:44.936Z",
    "title": "Can I embed external services (YouTube, Vimeo, etc.) in my answers or posts?",
    "user": {
      "_id": "5bacc9ff630b876a1e9785f7",
      "profile": {
        "counts": {
          "requests": 0,
          "edits": 0,
          "questionsFollowers": 0,
          "questions": 8,
          "comments": 0,
          "answersWords": 615,
          "answersVotes": 0,
          "answersViews": 0,
          "answers": 3,
          "views": 0,
          "followings": 0,
          "followers": 0
        },
        "score": 13,
        "externalId": null,
        "verified": false,
        "description": "",
        "title": "",
        "picture": "/files/users/5f7/5bacc9ff630b876a1e9785f7_15302.png",
        "website": "",
        "location": "",
        "gender": "",
        "name": "Robert D",
        "username": "robertd"
      },
      "id": "5bacc9ff630b876a1e9785f7"
    },
    "publishedAt": "2018-11-18T04:19:44.933Z",
    "portal": "5a73b1fcc48071e4c4dc1cae",
    "lastAskedAt": "2018-11-18T04:19:44.933Z",
    "actor": "5b1f99a7478dd3768d84b646",
    "__v": 1,
    "lastAnsweredAt": "2018-11-18T04:25:42.040Z",
    "referrers": [],
    "rewards": [],
    "hasReward": false,
    "downvotes": [],
    "upvotes": [],
    "followers": [],
    "askers": [],
    "comments": [],
    "topics": [
      {
        "_id": "5b88264d3d9228aa7c41f692",
        "name": "Tribe",
        "user": {
          "_id": "5b881b2a90ecbe6751123d7e",
          "profile": {
            "counts": {
              "requests": 2,
              "edits": 148,
              "questionsFollowers": 0,
              "questions": 32,
              "comments": 0,
              "answersWords": 5753,
              "answersVotes": 0,
              "answersViews": 0,
              "answers": 31,
              "views": 0,
              "followings": 1,
              "followers": 2
            },
            "score": 115,
            "externalId": null,
            "verified": false,
            "description": "<p>&nbsp;</p>",
            "title": "Biomedical Engineer ",
            "picture": "/files/users/d7e/5b881b2a90ecbe6751123d7e_57697.png",
            "website": "",
            "location": "",
            "gender": "",
            "name": "Elnaz Najafi",
            "username": "elnajafi89"
          },
          "id": "5b881b2a90ecbe6751123d7e"
        },
        "picture": "/files/topics/692/5b88264d3d9228aa7c41f692_72807.png",
        "id": "5b88264d3d9228aa7c41f692"
      }
    ],
    "score": 0,
    "status": "published",
    "counts": {
      "asks": 1,
      "downvotes": 0,
      "upvotes": 0,
      "edits": 2,
      "comments": 0,
      "hiddenAnswers": 0,
      "answers": 1,
      "views": 33,
      "followers": 0
    },
    "type": "general",
    "privacy": "public",
    "anonymous": false,
    "verified": false,
    "locked": false,
    "id": "5bf0e860da3be54c190b78b8"
  },
  "user": {
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
      "description": "<p>&nbsp;</p>",
      "title": "Tribe Moderator",
      "picture": "/files/users/646/5b1f99a7478dd3768d84b646_66172.png",
      "website": "",
      "location": "",
      "gender": "male",
      "name": "Siavash Mahmoudian",
      "username": "siavash"
    },
    "id": "5b1f99a7478dd3768d84b646",
    "followed": false
  },
  "__v": 1,
  "publishedAt": "2018-11-18T04:25:42.037Z",
  "shortId": "PEVpN",
  "downvotes": [],
  "upvotes": [
    "5bc64d97a8c76d6d771ae914"
  ],
  "comments": [],
  "rewards": [],
  "images": [],
  "links": [],
  "score": 0,
  "global": true,
  "status": "published",
  "media": [],
  "counts": {
    "reasks": 0,
    "edits": 2,
    "downvotes": 0,
    "upvotes": 1,
    "comments": 0,
    "views": 34
  },
  "privacy": "public",
  "anonymous": false,
  "verified": false,
  "summary": "...",
  "id": "5bf0e89ada3be54c190b78ba",
  "upvoted": false,
  "downvoted": false,
  "intro": "..."
}
```

This endpoint retrieves a specific answer using ID.

### HTTP Request

<code class="request">GET /api/v1/answers/{id}</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the item


<!-- 
## Get All Answers for a Specific Topic

```shell
curl "https://community.tribe.so/api/v1/topics/5c7bfc7a157c2c34f735a53e/answers"
  -H "Authorization: Bearer {access_token}"
```


This endpoint retrieves all answers for a sepcific topic using ID.

### HTTP Request

<code class="request">GET /api/v1/topics/:topicId/answers</code>

### URL Parameters

Parameter | Description
--------- | -----------
topicId | The ID of the topic -->



## Create an Answer

```shell
curl "https://community.tribe.so/api/v1/questions/5c7bfc7a157c2c34f735a53e/answers"
  -X POST
  -H "Authorization: Bearer {access_token}"
  -H 'Content-Type: application/json; charset=utf-8'
  --DATA '{"content":""<p>Very good answer!</p>","anonymous": false,"status":"published"}'
```

```javascript
  const tribe = require('tribe');

  let api = tribe.authorize('{access_token}');
  let result = api.questions.answer("5c7bfc7a157c2c34f735a53e",{conent: "Very good answer", anonymous: false, status: "published"})
```

> The above command returns JSON structured like this:

```json
  {
  "_id": "5c7c04de68b07737dec0b39e",
  "updatedAt": "2019-03-03T16:49:29.077Z",
  "createdAt": "2019-03-03T16:46:22.281Z",
  "portal": "5c7bf24f157c2c34f735a539",
  "question": {
    "_id": "5c7bfc7a157c2c34f735a53e",
    "shortId": "5ogL5",
    "lang": "en",
    "updatedAt": "2019-03-03T16:47:35.149Z",
    "createdAt": "2019-03-03T16:10:34.005Z",
    "title": "My anonymous question",
    "publishedAt": "2019-03-03T16:10:34.003Z",
    "portal": "5c7bf24f157c2c34f735a539",
    "lastAskedAt": "2019-03-03T16:10:34.003Z",
    "user": {
      "_id": "5c7bf251157c2c34f735a53a",
      "profile": {
        "counts": {
          "requests": 0,
          "edits": 1,
          "questionsFollowers": 0,
          "questions": 2,
          "comments": 0,
          "answersWords": 3,
          "answersVotes": 0,
          "answersViews": 0,
          "answers": 1,
          "views": 0,
          "followings": 0,
          "followers": 0
        },
        "score": 10,
        "verified": false,
        "description": "",
        "title": "",
        "picture": "https://gravatar.com/avatar/b7711ecd91aebb5dd1b7c153dbfd92d0?s=200&d=retro",
        "website": "",
        "location": "",
        "gender": "",
        "name": "Admin",
        "username": "admin"
      },
      "id": "5c7bf251157c2c34f735a53a"
    },
    "__v": 1,
    "lastAnsweredAt": "2019-03-03T16:47:35.149Z",
    "referrers": [],
    "rewards": [],
    "hasReward": false,
    "downvotes": [],
    "upvotes": [],
    "followers": [],
    "askers": [],
    "comments": [],
    "topics": [
      {
        "_id": "5c7bff4bc389b77bdf1f2726",
        "name": "test",
        "user": {
          "_id": "5c7bf251157c2c34f735a53a",
          "profile": {
            "counts": {
              "requests": 0,
              "edits": 1,
              "questionsFollowers": 0,
              "questions": 2,
              "comments": 0,
              "answersWords": 3,
              "answersVotes": 0,
              "answersViews": 0,
              "answers": 1,
              "views": 0,
              "followings": 0,
              "followers": 0
            },
            "score": 10,
            "verified": false,
            "description": "",
            "title": "",
            "picture": "https://gravatar.com/avatar/b7711ecd91aebb5dd1b7c153dbfd92d0?s=200&d=retro",
            "website": "",
            "location": "",
            "gender": "",
            "name": "Admin",
            "username": "admin"
          },
          "id": "5c7bf251157c2c34f735a53a"
        },
        "id": "5c7bff4bc389b77bdf1f2726"
      }
    ],
    "score": 0,
    "status": "published",
    "counts": {
      "asks": 1,
      "downvotes": 0,
      "upvotes": 0,
      "edits": 2,
      "comments": 0,
      "hiddenAnswers": 0,
      "answers": 2,
      "views": 1,
      "followers": 0
    },
    "type": "general",
    "privacy": "public",
    "anonymous": false,
    "verified": false,
    "locked": false,
    "id": "5c7bfc7a157c2c34f735a53e"
  },
  "user": {
    "_id": "5c7c00dd68b07737dec0b39a",
    "profile": {
      "counts": {
        "requests": 0,
        "edits": 2,
        "questionsFollowers": 0,
        "questions": 0,
        "comments": 0,
        "answersWords": 3,
        "answersVotes": 0,
        "answersViews": 0,
        "answers": 1,
        "views": 0,
        "followings": 0,
        "followers": 0
      },
      "score": 10,
      "verified": false,
      "description": "",
      "title": "",
      "picture": "https://gravatar.com/avatar/a6ac5b09b633aafba41b4a0cda22976e?s=200&d=retro",
      "website": "",
      "location": "",
      "gender": "",
      "name": "Amir",
      "username": "triplea1373"
    },
    "id": "5c7c00dd68b07737dec0b39a"
  },
  "__v": 0,
  "content": "<p>Very good answer!A</p>",
  "draftContent": "",
  "publishedAt": "2019-03-03T16:47:35.147Z",
  "shortId": "yJ1pQ",
  "downvotes": [],
  "upvotes": [],
  "comments": [],
  "rewards": [],
  "images": [],
  "links": [],
  "score": 0,
  "global": true,
  "status": "published",
  "media": [],
  "counts": {
    "reasks": 0,
    "edits": 3,
    "downvotes": 0,
    "upvotes": 0,
    "comments": 0,
    "views": 1
  },
  "privacy": "public",
  "anonymous": false,
  "verified": false,
  "summary": "Very good answer!A",
  "id": "5c7c04de68b07737dec0b39e",
  "upvoted": false,
  "downvoted": false
}
```

The endpoint creates an answer for a specific question.

### HTTP Request

<code class="request">POST /api/v1/questions/:questionId/answers</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
questionId | `String` | The ID of the question

### Request Parameters

Parameter | Type | Description
--------- | ----------- | -----------
content | `String` | The content of the answer
anonymous | `Boolean` | Is it an anonymous answer or not
status | `String` | Status of the answer. Should be one of the followings: `archived` `collapsed` `draft` `published` `unapproved` `unlisted` `scheduled` `new`

### Extra Request Parameters for Moderators

Parameter | Type | Description
--------- | ----------- | -----------
verified | `Boolean` | Is this answer verified or not
user | `String` | The ID of the user to create an answer on behalf


## Update a Specific Answer


```shell
curl "https://community.tribe.so/api/v1/answers/5bf0e89ada3be54c190b78ba"
  -X PUT
  -H "Authorization: Bearer {access_token}"
  -H 'Content-Type: application/json; charset=utf-8'
  --DATA '{"content":"Test answer","anonymous": false,"status":"published"}'
```

```javascript
  const tribe = require('tribe');

  let api = tribe.authorize('{access_token}');
  let result = api.answers.update("5c7bfc7a157c2c34f735a53e",{conent: "Very good answer", anonymous: false)
```

This endpoint update a specific answer.

### HTTP Request

<code class="request">PUT /api/v1/answers/{id}</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the answer to update

### Request Parameters

Parameter | Type | Description
--------- | ----------- | -----------
content | `String` | The content of the answer
anonymous | `String` | Is it an anonymous answer or not

### Extra Request Parameters for Moderators

Parameter | Type | Description
--------- | ----------- | ------
verified | `String` | Is this a verified answer or not
status | `String` | Status of the answer. Should be one of the following values: `archived` `collapsed` `draft` `published` `unapproved` `unlisted` `scheduled` `new`

## Delete a Specific Answer


```shell
curl "https://community.tribe.so/api/v1/answers/5bf0e89ada3be54c190b78ba"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.answers.delete('5bf0e89ada3be54c190b78ba');
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint deletes a specific answer.

### HTTP Request

<code class="request">DELETE /api/v1/answers/{id}</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the answer to delete

## Delete a Specific Draft Answer


```shell
curl "https://community.tribe.so/api/v1/answers/5bf0e89ada3be54c190b78ba/draft"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.answers.drafts.delete('5bf0e89ada3be54c190b78ba');
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint deletes a specific draft answer.

### HTTP Request

<code class="request">DELETE /api/v1/answers/{id}/draft</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the answer to delete


## Upvote a Specific Answer


```shell
curl "https://community.tribe.so/api/v1/answers/5bf0e89ada3be54c190b78ba/votes"
  -X POST
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.answers.upvote('5bf0e89ada3be54c190b78ba');
```
<!-- 
> The above command returns JSON structured like this:

```json
{
  "success": true
}
``` -->

This endpoint upvotes for a specific answer.

### HTTP Request

<code class="request">POST /api/v1/answers/:id/votes</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the answer to add a vote

## Remove Upvote for a Specific Answer


```shell
curl "https://community.tribe.so/api/v1/answers/5bf0e89ada3be54c190b78ba/votes"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.answers.downvote('5bf0e89ada3be54c190b78ba');
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint removes an upvote for a specific answer.

### HTTP Request

<code class="request">DELETE /api/v1/answers/:id/votes</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the answer to remove a vote

## Get List of Votes for a Specific Answer

```shell
  curl "https://community.tribe.so/api/v1/answers/5bf0e89ada3be54c190b78ba/votes"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.answers.votes.get('5bf0e89ada3be54c190b78ba');
```

> The above command returns JSON structured like this:

```json
  {
  "upvotes": [
    {
      "_id": "5bc64d97a8c76d6d771ae914",
      "profile": {
        "title": "Customer Success @Tribe",
        "picture": "https://gravatar.com/avatar/1ec94547651bb4e27ce2bdd0113f7487?s=200&d=retro",
        "name": "Mo Malayeri",
        "username": "mo11832"
      },
      "id": "5bc64d97a8c76d6d771ae914"
    },
    {
      "_id": "5b881b2a90ecbe6751123d7e",
      "profile": {
        "title": "Community Manager at Tribe",
        "picture": "/files/users/d7e/5b881b2a90ecbe6751123d7e_88402.png",
        "name": "Eli Najafi",
        "username": "elnaz"
      },
      "id": "5b881b2a90ecbe6751123d7e"
    },
    {
      "_id": "5b912f01f19a473232026862",
      "profile": {
        "title": "Marketing Manager",
        "picture": "/files/users/862/5b912f01f19a473232026862_29979.png",
        "name": "Melanie Jones",
        "username": "mike2"
      },
      "id": "5b912f01f19a473232026862"
    },
    {
      "_id": "5bacc9ff630b876a1e9785f7",
      "profile": {
        "title": "",
        "picture": "/files/users/5f7/5bacc9ff630b876a1e9785f7_15302.png",
        "name": "Robert D",
        "username": "robertd"
      },
      "id": "5bacc9ff630b876a1e9785f7"
    },
    {
      "_id": "5ba95b5c630b876a1e9785a5",
      "profile": {
        "title": "Community Manager at BHD",
        "picture": "/files/users/5a5/5ba95b5c630b876a1e9785a5_41926.png",
        "name": "Eddie Reid",
        "username": "ereid"
      },
      "id": "5ba95b5c630b876a1e9785a5"
    },
    {
      "_id": "5b8ff4190607d4174e2eb73b",
      "profile": {
        "title": "Community Moderator at Acondo",
        "picture": "/files/users/73b/5b8ff4190607d4174e2eb73b_29849.png",
        "name": "Kenneth Jensen",
        "username": "mike1"
      },
      "id": "5b8ff4190607d4174e2eb73b"
    }
  ],
  "downvotes": []
}
```

This endpoint retrieves all answers for a specific answer.

### HTTP Request

<code class="request">GET /api/v1/answers/:id/votes</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the answer to receive the votes



## Add a Comment for a Specific Answer

```shell
  curl "https://community.tribe.so/api/v1/answers/5bf0e89ada3be54c190b78ba/comments"
  -X POST
  -H "Authorization: Bearer {access_token}"
  --DATA "{'body':'New comment'}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.answers.comment('5bf0e89ada3be54c190b78ba',{ 
  body: "New comment" 
});
```

This endpoint adds a comment for a specific answer.

### HTTP Request

<code class="request">POST /api/v1/answers/:id/comments</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the answer to add a comment

### Request Parameters

Parameter | Type | Description
--------- | ----------- | -----------
body | `String` | The content of the comment

### Extra Request Parameters for Moderators

Parameter | Type | Description
--------- | ----------- | -----------
user | `String` | The ID of the user to comment on behalf

## Update a Specific Comment for a Specific Answer

```shell
  curl "https://community.tribe.so/api/v1/answers/5bf0e89ada3be54c190b78ba/comments/4sf0e89ada3be54c190b78b2"
  -X PUT
  -H "Authorization: Bearer {access_token}"
  --DATA "{'body':'Updated comment'}"
```
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.answers.comments.update('5bf0e89ada3be54c190b78ba',"4sf0e89ada3be54c190b78b2",{ 
  body: "Updated comment" 
});
```

This endpoint updates a specific comment.

### HTTP Request

<code class="request">PUT /api/v1/answers/:answerId/comments/:id</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the comment to update
answerId | `String` | The ID of the answer to add a comment

### Request Parameters

Parameter | Type | Description
--------- | ----------- | -----------
body | `String` | The content of the comment

## Remove a Specific Comment from a Specific Answer

```shell
  curl "https://community.tribe.so/api/v1/answers/5bf0e89ada3be54c190b78ba/comments/4sf0e89ada3be54c190b78b2"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.answers.comments.delete('5bf0e89ada3be54c190b78ba',"4sf0e89ada3be54c190b78b2");
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint removes a specific comment.

### HTTP Request

<code class="request">DELETE /api/v1/answers/:answerId/comments/:id</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the comment to remove
answerId | `String` | The ID of the answer to remove a comment