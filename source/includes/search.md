# Search

## Global Search


```shell
curl "https://community.tribe.so/api/v1/search?query=amir"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.search({ query: 'Amir' })
```

> The above command returns JSON structured like this:

```json
{
  "items": [
    {
      "role": "member",
      "profile": {
        "username": "amirtyz",
        "name": "Amir T",
        "gender": "",
        "location": "",
        "website": "",
        "picture": "https://gravatar.com/avatar/90bff30e822fcae0f56d13ce9e4a28e5?s=200&d=retro",
        "banner": "",
        "title": "",
        "description": "",
        "badge": {},
        "verified": false,
        "score": 10,
        "counts": {
          "followers": 0,
          "followings": 0,
          "views": 0,
          "answers": 0,
          "answersVotes": 0,
          "answersWords": 0,
          "comments": 0,
          "questions": 0,
          "posts": 0,
          "responses": 0,
          "questionsFollowers": 0,
          "edits": 0,
          "requests": 0,
          "groups": 0,
          "replies": 0,
          "receivedLikes": 0
        }
      },
      "notifications": {
        "telegram": {
          "follow_user": false,
          "mention": false,
          "follow_question": false,
          "answer": false,
          "ask": false,
          "comment": false,
          "request_answer": false,
          "upvote": false,
          "comment_upvote": false
        },
        "email": {
          "enabled": true,
          "autoFollow": true,
          "topicFollowMethod": "default",
          "mentionsFrequency": "daily",
          "followedTopicsFrequency": "never",
          "followedPostsFrequency": "daily",
          "upvotesFrequency": "daily",
          "followedUsersFrequency": "default",
          "newFollowersFrequency": "daily"
        }
      },
      "lastSeenAt": "2019-12-05T00:12:10.907Z",
      "lastActionAt": "2019-12-05T00:12:10.929Z",
      "lastPostAt": null,
      "portal": "5a73b1fcc48071e4c4dc1cae",
      "_id": "5de84a9c53e2404848b1b0fb",
      "_type": "user"
    },
    {
      "role": "member",
      "profile": {
        "username": "triplea1373",
        "name": "Amir Ahangari",
        "gender": "",
        "location": "",
        "website": "",
        "picture": "https://gravatar.com/avatar/a6ac5b09b633aafba41b4a0cda22976e?s=200&d=retro",
        "banner": "",
        "title": "",
        "description": "",
        "badge": {},
        "verified": false,
        "score": 10,
        "counts": {
          "followers": 0,
          "followings": 0,
          "views": 0,
          "answers": 0,
          "answersVotes": 0,
          "answersWords": 0,
          "comments": 0,
          "questions": 0,
          "posts": 0,
          "responses": 0,
          "questionsFollowers": 0,
          "edits": 0,
          "requests": 0,
          "groups": 0,
          "replies": 0,
          "receivedLikes": 0
        }
      },
      "notifications": {
        "telegram": {
          "follow_user": true,
          "mention": true,
          "follow_question": true,
          "answer": true,
          "ask": true,
          "comment": true,
          "request_answer": true,
          "upvote": true,
          "comment_upvote": true
        },
        "email": {
          "enabled": true,
          "autoFollow": true,
          "topicFollowMethod": "default",
          "mentionsFrequency": "default",
          "followedTopicsFrequency": "default",
          "followedPostsFrequency": "default",
          "upvotesFrequency": "default",
          "followedUsersFrequency": "default",
          "newFollowersFrequency": "default"
        }
      },
      "lastSeenAt": "2019-03-28T17:02:15.034Z",
      "lastActionAt": null,
      "lastPostAt": null,
      "portal": "5a73b1fcc48071e4c4dc1cae",
      "_id": "5c890abdf1d2414b5034dc3a",
      "_type": "user"
    },
    {
      "role": "admin",
      "profile": {
        "username": "amir",
        "name": "Amir Ahangari",
        "gender": "",
        "location": "",
        "website": "",
        "picture": "/files/users/a3e/5cf06ec07575275814411a3e_7824.png",
        "banner": "",
        "title": "Fullstack Developer at Tribe",
        "description": "",
        "badge": {
          "text": "Tribe Team"
        },
        "verified": true,
        "score": 30,
        "counts": {
          "followers": 4,
          "followings": 7,
          "views": 0,
          "answers": 3,
          "answersVotes": 0,
          "answersWords": 75,
          "comments": 2,
          "questions": 0,
          "posts": 0,
          "responses": 0,
          "questionsFollowers": 0,
          "edits": 8,
          "requests": 1,
          "groups": 0,
          "replies": 0,
          "receivedLikes": 0
        }
      },
      "notifications": {
        "telegram": {
          "follow_user": true,
          "mention": true,
          "follow_question": true,
          "answer": true,
          "ask": true,
          "comment": true,
          "request_answer": true,
          "upvote": true,
          "comment_upvote": true
        },
        "email": {
          "enabled": true,
          "autoFollow": true,
          "topicFollowMethod": "default",
          "mentionsFrequency": "default",
          "followedTopicsFrequency": "default",
          "followedPostsFrequency": "default",
          "upvotesFrequency": "default",
          "followedUsersFrequency": "default",
          "newFollowersFrequency": "default"
        }
      },
      "lastSeenAt": "2019-12-09T21:38:35.192Z",
      "lastActionAt": "2019-12-09T21:38:18.333Z",
      "lastPostAt": "2019-12-09T21:38:18.333Z",
      "portal": "5a73b1fcc48071e4c4dc1cae",
      "_id": "5cf06ec07575275814411a3e",
      "_type": "user"
    }
  ],
  "count": 3
}
```

This endpoint retrieves search results.

### HTTP Request

<code class="request">GET /api/v1/search</code>


### Query Parameters

Parameter | Type | Default | Description
--------- | ------- | ----------- | -----------
page | `Number` | `1` | Intended page
limit | `Number` | `20` | Number of items per page
sort | `String` | `createdAt.desc` | The field to sort on
type | `String` | `all` | `createdAt.desc` | Type of the result. It can be one of [`question` , `group`, `topic`, `post`, `user`, `all`]
query | `String` | | Query to search

## Search Questions


```shell
curl "https://community.tribe.so/api/v1/search/questions"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.search({ type: 'question', query: 'Tribe' })
```

> The above command returns JSON structured like this:

```json
[
  {
    "shortId": "QrZOL",
    "user": {
      "_id": "5ba95b5c630b876a1e9785a5",
      "profile": {
        "picture": "/files/users/5a5/5ba95b5c630b876a1e9785a5_41926.png",
        "location": "",
        "gender": "",
        "name": "Eddie Reid",
        "username": "ereid"
      },
      "id": "5ba95b5c630b876a1e9785a5"
    },
    "actor": "5b1f99a7478dd3768d84b646",
    "title": "What are the best resources you've seen around community management?",
    "lang": "en",
    "locked": false,
    "verified": false,
    "anonymous": false,
    "publishedAt": "2019-05-15T20:10:42.725Z",
    "group": {
      "_id": "5cc9d23e5ead3e4539b29849",
      "slug": "community-managers",
      "name": "Community Managers",
      "description": "<p>&nbsp;</p>",
      "picture": "/files/groups/849/5cc9d23e5ead3e4539b29849_55645.jpg",
      "banner": "/files/groups/849/5cc9d23e5ead3e4539b29849_23029.jpg",
      "topics": [],
      "privacy": "public",
      "type": "general",
      "summary": "",
      "id": "5cc9d23e5ead3e4539b29849"
    },
    "privacy": "public",
    "type": "general",
    "counts": {
      "followers": 1,
      "views": 7,
      "answers": 0,
      "hiddenAnswers": 0,
      "comments": 0,
      "edits": 1,
      "upvotes": 0,
      "downvotes": 0,
      "asks": 1
    },
    "lastAskedAt": "2019-05-15T20:10:42.725Z",
    "status": "published",
    "score": 0,
    "topics": [],
    "comments": [],
    "askers": [],
    "followers": [
      "5cd1d318dc7fef4b3cba31c1"
    ],
    "upvotes": [],
    "downvotes": [],
    "portal": "5a73b1fcc48071e4c4dc1cae",
    "hasReward": false,
    "aliases": [],
    "updatedAt": "2019-06-10T06:38:45.419Z",
    "createdAt": "2019-05-15T20:10:42.727Z",
    "_id": "5cdc7242f2d994091caa5e76"
  },
  ...
]

```

This endpoint retrieves question search results.

### HTTP Request

<code class="request">GET /api/v1/search/questions</code>


### Query Parameters

Parameter | Type | Default | Description
--------- | ------- | ----------- | -----------
page | `Number` | `1` | Intended page
limit | `Number` | `20` | Number of items per page
sort | `String` | `createdAt.desc` | The field to sort on
query | `String` | | Query to search

<!-- ## Search Users


```shell
curl "https://community.tribe.so/api/v1/search/users"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.search({ type: 'user', query: 'Tribe' })
```

> The above command returns JSON structured like this:

```json


```

This endpoint retrieves question search results.

### HTTP Request

<code class="request">GET /api/v1/search/users</code>


### Query Parameters

Parameter | Type | Default | Description
--------- | ------- | ----------- | -----------
page | `Number` | `1` | Intended page
limit | `Number` | `20` | Number of items per page
sort | `String` | `createdAt.desc` | The field to sort on
query | `String` | | Query to search -->