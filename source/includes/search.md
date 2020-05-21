# Search

## Global Search

```shell
curl "https://community.tribe.so/api/v1/search?query=amir"
  -H "Authorization: Bearer {access_token}"
```

<!--
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.search({ query: 'Amir' })
```
-->

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

| Parameter | Type     | Default          | Description                                                                                 |
| --------- | -------- | ---------------- | ------------------------------------------------------------------------------------------- |
| page      | `Number` | `1`              | Intended page                                                                               |
| limit     | `Number` | `20`             | Number of items per page                                                                    |
| sort      | `String` | `createdAt.desc` | The field to sort on                                                                        |
| type      | `String` | `all`            | Type of the result. It can be one of [`question` , `group`, `topic`, `post`, `user`, `all`] |
| query     | `String` |                  | Query to search                                                                             |
