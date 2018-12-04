# Post

## Get All Post


```shell
curl "https://community.tribe.so/api/v1/posts"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let posts = api.posts.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "_id": "5c0621864cb2b119dc174a63",
    "shortId": "Px10b",
    "lang": "en",
    "updatedAt": "2018-12-04T06:41:25.370Z",
    "createdAt": "2018-12-04T06:41:10.046Z",
    "title": "This is a test discussion.",
    "content": "<p>Here is the content of the discussion.</p>",
    "portal": "5a73b1fcc48071e4c4dc1cae",
    "publishedAt": "2018-12-04T06:41:10.031Z",
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
      "id": "5b1f99a7478dd3768d84b646"
    },
    "__v": 2,
    "referrers": [],
    "global": true,
    "downvotes": [],
    "upvotes": [],
    "comments": [],
    "rewards": [],
    "images": [],
    "links": [],
    "media": [],
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
    "posters": [
      {
        "user": "5b1f99a7478dd3768d84b646",
        "score": 1,
        "_id": "5c062192f3d2d61a37864a5c"
      }
    ],
    "followers": [],
    "score": 0,
    "counts": {
      "downvotes": 0,
      "links": 0,
      "totalUpvotes": 0,
      "upvotes": 0,
      "followers": 1,
      "users": 1,
      "edits": 0,
      "responses": 1,
      "comments": 0,
      "views": 0
    },
    "status": "published",
    "privacy": "public",
    "type": "discussion",
    "anonymous": false,
    "verified": false,
    "responses": [
      "5c062192f3d2d61a37864a5b"
    ],
    "summary": "Here is the content of the discussion.",
    "id": "5c0621864cb2b119dc174a63",
    "upvoted": false,
    "downvoted": false,
    "followed": false
  }
]
```

This endpoint retrieves all posts.

### HTTP Request

<code class="request">GET /api/v1/posts</code>

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
page | 1 | Intended page
limit | 20 | Number of items per page
sort | createdAt.desc | The field to sort on


## Get a Specific Post


```shell
curl "https://community.tribe.so/api/v1/posts/5c0621864cb2b119dc174a63"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let posts = api.posts.get('5c0621864cb2b119dc174a63');
```

> The above command returns JSON structured like this:

```json
  {
    "_id": "5c0621864cb2b119dc174a63",
    "shortId": "Px10b",
    "lang": "en",
    "updatedAt": "2018-12-04T06:41:25.370Z",
    "createdAt": "2018-12-04T06:41:10.046Z",
    "title": "This is a test discussion.",
    "content": "<p>Here is the content of the discussion.</p>",
    "portal": "5a73b1fcc48071e4c4dc1cae",
    "publishedAt": "2018-12-04T06:41:10.031Z",
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
      "id": "5b1f99a7478dd3768d84b646"
    },
    "__v": 2,
    "referrers": [],
    "global": true,
    "downvotes": [],
    "upvotes": [],
    "comments": [],
    "rewards": [],
    "images": [],
    "links": [],
    "media": [],
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
    "posters": [
      {
        "user": "5b1f99a7478dd3768d84b646",
        "score": 1,
        "_id": "5c062192f3d2d61a37864a5c"
      }
    ],
    "followers": [],
    "score": 0,
    "counts": {
      "downvotes": 0,
      "links": 0,
      "totalUpvotes": 0,
      "upvotes": 0,
      "followers": 1,
      "users": 1,
      "edits": 0,
      "responses": 1,
      "comments": 0,
      "views": 0
    },
    "status": "published",
    "privacy": "public",
    "type": "discussion",
    "anonymous": false,
    "verified": false,
    "responses": [
      "5c062192f3d2d61a37864a5b"
    ],
    "summary": "Here is the content of the discussion.",
    "id": "5c0621864cb2b119dc174a63",
    "upvoted": false,
    "downvoted": false,
    "followed": false
  }
```

This endpoint retrieves a specific post using ID.

### HTTP Request

<code class="request">GET /api/v1/posts/{id}</code>


### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the item


## Delete a Specific Post


```shell
curl "https://community.tribe.so/api/v1/posts/5c0621864cb2b119dc174a63"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.posts.delete('5c0621864cb2b119dc174a63');
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint deletes a specific post.

### HTTP Request

<code class="request">DELETE /api/v1/posts/{id}</code>


### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the post to delete




## Get Post's Responses


```shell
curl "https://community.tribe.so/api/v1/posts/5c0621864cb2b119dc174a63/responses"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.posts.responses('5c0621864cb2b119dc174a63');
```



> The above command returns JSON structured like this:

```json
[
  {
    "_id": "5c062192f3d2d61a37864a5b",
    "shortId": "PKqoR",
    "lang": "en",
    "updatedAt": "2018-12-04T06:41:22.270Z",
    "createdAt": "2018-12-04T06:41:22.270Z",
    "content": "<p>This is a test response to a discussion.</p>",
    "parent": "5c0621864cb2b119dc174a63",
    "portal": "5a73b1fcc48071e4c4dc1cae",
    "publishedAt": "2018-12-04T06:41:22.262Z",
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
      "id": "5b1f99a7478dd3768d84b646"
    },
    "__v": 0,
    "referrers": [],
    "global": true,
    "downvotes": [],
    "upvotes": [],
    "comments": [],
    "rewards": [],
    "images": [],
    "links": [],
    "media": [],
    "topics": [],
    "posters": [],
    "followers": [],
    "score": 0,
    "counts": {
      "downvotes": 0,
      "links": 0,
      "totalUpvotes": 0,
      "upvotes": 0,
      "followers": 1,
      "users": 1,
      "edits": 0,
      "responses": 0,
      "comments": 0,
      "views": 0
    },
    "status": "published",
    "privacy": "public",
    "type": "response",
    "anonymous": false,
    "verified": false,
    "responses": [],
    "summary": "This is a test response to a discussion.",
    "id": "5c062192f3d2d61a37864a5b",
    "upvoted": false,
    "downvoted": false,
    "followed": false
  }
]
```

### HTTP Request

<code class="request">GET /api/v1/posts/{id}/responses</code>


### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the question

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
page | 1 | Intended page
limit | 20 | Number of items per page
sort | createdAt.desc | The field to sort on


