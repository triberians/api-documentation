# Groups

## Create a Group

```shell
curl "https://community.tribe.so/api/v1/groups"
  -H "Authorization: Bearer {access_token}"
  -X POST
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let group = api.group.create({ ... });
```

> The above command returns JSON structured like this:

```json
{
  "__v": 0,
  "shortId": "GRmdo",
  "updatedAt": "2020-03-04T17:41:01.656Z",
  "createdAt": "2020-03-04T17:41:01.656Z",
  "slug": "a-good-car",
  "name": "A good car",
  "portal": "5b8f50eff731cf14c8b40bac",
  "user": {
    "_id": "5d41ef5c16eaa51dbfb47fbf",
    "updatedAt": "2020-03-04T17:40:58.469Z",
    "createdAt": "2019-07-31T19:43:24.999Z",
    "portal": "5b8f50eff731cf14c8b40bac",
    "email": "amir@tribe.so",
    "deviceTokens": [],
    "slack": null,
    "messenger": null,
    "telegram": null,
    "facebook": null,
    "linkedin": null,
    "google": null,
    "lastPostAt": "2020-01-08T20:56:51.142Z",
    "lastActionAt": "2020-03-02T13:57:38.331Z",
    "lastSeenAt": "2020-03-04T17:40:58.469Z",
    "notifications": {
      "email": {
        "newFollowersFrequency": "default",
        "followedUsersFrequency": "default",
        "upvotesFrequency": "default",
        "followedPostsFrequency": "default",
        "followedTopicsFrequency": "default",
        "mentionsFrequency": "default",
        "topicFollowMethod": "default",
        "autoFollow": true,
        "enabled": true
      },
      "telegram": {
        "comment_upvote": true,
        "upvote": true,
        "request_answer": true,
        "comment": true,
        "ask": true,
        "answer": true,
        "follow_question": true,
        "mention": true,
        "follow_user": true
      }
    },
    "profile": ...,
    "groups": [...],
    "devices": [],
    "externalId": null,
    "followedUsers": [],
    "followedTopics": [
      "5d769dd30494fcc995cd84d9"
    ],
    "credit": 0,
    "status": "active",
    "role": "admin",
    "emailStatus": "verified",
    "bankAccount": {
      "routingNumber": "",
      "accountNumber": ""
    },
    "id": "5d41ef5c16eaa51dbfb47fbf"
  },
  "_id": "5e5fe82d90ab955f09ca40fd",
  "pinned": [],
  "topics": [],
  "featured": {
    "posts": [],
    "topics": [],
    "users": [],
    "questions": []
  },
  "notificationsDefaults": {
    "inapp": {
      "enabled": false
    },
    "email": {
      "enabled": false
    }
  },
  "score": 0,
  "counts": {
    "members": 1,
    "posts": 0,
    "comments": 0,
    "answers": 0,
    "questions": 0
  },
  "registration": "open",
  "privacy": "public",
  "status": "active",
  "contentTypes": [],
  "type": "general",
  "verified": false,
  "summary": "",
  "id": "5e5fe82d90ab955f09ca40fd",
  "joinStatus": "none"
}
```

This endpoint creates a new group. Only for admins.

### HTTP Request

<code class="request">POST /api/v1/groups</code>

### Query Parameters

| Parameter       | Default   | Description                                                                                            |
| --------------- | --------- | ------------------------------------------------------------------------------------------------------ |
| name            |           | Name of the group to create                                                                            |
| slug            |           | Slug of the group to create                                                                            |
| color           |           | Color of the group to create                                                                           |
| type            | `general` | Type of the group to create. It can be one the followings: [`blog`, `general`, `feedback`]             |
| description     |           | Description of the group to create                                                                     |
| privacy         | `public`  | Group privacy. It can be one of the followings: [`public`, `private`, `secret`]                        |
| verified        |           | Is group verified?                                                                                     |
| picture         |           | Picture URL of the group                                                                               |
| banner          |           | Banner URL of the group                                                                                |
| registration    | `open`    | Registration of the group. It can be one of the followings: [`open`, `invitation`, `approval`, `none`] |
| featured.topics |           | Array of highlighted topics' IDs                                                                       |

## Update a Specific Group

```shell
curl "https://community.tribe.so/api/v1/groups"
  -H "Authorization: Bearer {access_token}"
  -X PUT
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let group = api.group.create({ ... });
group.update()
```

> The above command returns JSON structured like this:

```json
{
  "__v": 0,
  "shortId": "GRmdo",
  "updatedAt": "2020-03-04T17:41:01.656Z",
  "createdAt": "2020-03-04T17:41:01.656Z",
  "slug": "a-good-car",
  "name": "A good car",
  "portal": "5b8f50eff731cf14c8b40bac",
  "user": {
    "_id": "5d41ef5c16eaa51dbfb47fbf",
    "updatedAt": "2020-03-04T17:40:58.469Z",
    "createdAt": "2019-07-31T19:43:24.999Z",
    "portal": "5b8f50eff731cf14c8b40bac",
    "email": "amir@tribe.so",
    "deviceTokens": [],
    "slack": null,
    "messenger": null,
    "telegram": null,
    "facebook": null,
    "linkedin": null,
    "google": null,
    "lastPostAt": "2020-01-08T20:56:51.142Z",
    "lastActionAt": "2020-03-02T13:57:38.331Z",
    "lastSeenAt": "2020-03-04T17:40:58.469Z",
    "notifications": {
      "email": {
        "newFollowersFrequency": "default",
        "followedUsersFrequency": "default",
        "upvotesFrequency": "default",
        "followedPostsFrequency": "default",
        "followedTopicsFrequency": "default",
        "mentionsFrequency": "default",
        "topicFollowMethod": "default",
        "autoFollow": true,
        "enabled": true
      },
      "telegram": {
        "comment_upvote": true,
        "upvote": true,
        "request_answer": true,
        "comment": true,
        "ask": true,
        "answer": true,
        "follow_question": true,
        "mention": true,
        "follow_user": true
      }
    },
    "profile": ...,
    "groups": [...],
    "devices": [],
    "externalId": null,
    "followedUsers": [],
    "followedTopics": [
      "5d769dd30494fcc995cd84d9"
    ],
    "credit": 0,
    "status": "active",
    "role": "admin",
    "emailStatus": "verified",
    "bankAccount": {
      "routingNumber": "",
      "accountNumber": ""
    },
    "id": "5d41ef5c16eaa51dbfb47fbf"
  },
  "_id": "5e5fe82d90ab955f09ca40fd",
  "pinned": [],
  "topics": [],
  "featured": {
    "posts": [],
    "topics": [],
    "users": [],
    "questions": []
  },
  "notificationsDefaults": {
    "inapp": {
      "enabled": false
    },
    "email": {
      "enabled": false
    }
  },
  "score": 0,
  "counts": {
    "members": 1,
    "posts": 0,
    "comments": 0,
    "answers": 0,
    "questions": 0
  },
  "registration": "open",
  "privacy": "public",
  "status": "active",
  "contentTypes": [],
  "type": "general",
  "verified": false,
  "summary": "",
  "id": "5e5fe82d90ab955f09ca40fd",
  "joinStatus": "none"
}
```

This endpoint updates a specific group using ID

### HTTP Request

<code class="request">PUT /api/v1/groups/:id</code>

### Query Parameters

| Parameter       | Default   | Description                                                                                            |
| --------------- | --------- | ------------------------------------------------------------------------------------------------------ |
| name            |           | Name of the group to create                                                                            |
| slug            |           | Slug of the group to create                                                                            |
| color           |           | Color of the group to create                                                                           |
| type            | `general` | Type of the group to create. It can be one the followings: [`blog`, `general`, `feedback`]             |
| description     |           | Description of the group to create                                                                     |
| privacy         | `public`  | Group privacy. It can be one of the followings: [`public`, `private`, `secret`]                        |
| verified        |           | Is group verified?                                                                                     |
| picture         |           | Picture URL of the group                                                                               |
| banner          |           | Banner URL of the group                                                                                |
| registration    | `open`    | Registration of the group. It can be one of the followings: [`open`, `invitation`, `approval`, `none`] |
| featured.topics |           | Array of highlighte topics' IDs                                                                        |

## Get a Specific Group

```shell
curl "https://community.tribe.so/api/v1/groups/5dbc4c34560ef636c0f66172"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let group = api.group.get({ ... });
```

> The above command returns JSON structured like this:

```json
{
  "_id": "5dbc4c34560ef636c0f66172",
  "shortId": "KdlVm",
  "updatedAt": "2020-03-01T17:20:25.750Z",
  "createdAt": "2019-11-01T15:16:04.500Z",
  "slug": "community-owners-hub",
  "name": "Community Owners Hub",
  "description": "<p>Welcome community owners hub! </p><p>Building a community is not about the platform but rather the right strategy, plan and execution. This group is a place to learn the best community management techniques, sharing your challenges and learnings to build a successful and engaging community. </p><p>Happy community!</p>",
  "portal": "5a73b1fcc48071e4c4dc1cae",
  "user": "5b881b2a90ecbe6751123d7e",
  "__v": 5,
  "picture": "/files/groups/172/5dbc4c34560ef636c0f66172_90175.jpg",
  "banner": "/files/groups/172/5dbc4c34560ef636c0f66172_92570.jpg",
  "pinned": [
    {
      "resourceType": "posts",
      "resourceId": "5df104da7c0d09330836b2bc",
      "_id": "5df104ee83dddf38d37754cf"
    }
  ],
  "topics": [],
  "featured": {
    "posts": [],
    "topics": [
      {
        "_id": "5dbc53520494fcc995454b9f",
        "name": "Basics for Building a Community",
        "slug": "basics-for-building-a-community",
        "id": "5dbc53520494fcc995454b9f"
      },
      {
        "_id": "5dbc61380494fcc9954e6f8f",
        "name": "Share What You Have Done In Your Community",
        "slug": "share-what-you-have-done-in-your-community",
        "id": "5dbc61380494fcc9954e6f8f"
      },
      {
        "_id": "5dbc61740494fcc9954e7f9a",
        "name": "Promote Your Community",
        "slug": "promote-your-community",
        "id": "5dbc61740494fcc9954e7f9a"
      }
    ],
    "users": [],
    "questions": []
  },
  "notificationsDefaults": {
    "inapp": {
      "enabled": false
    },
    "email": {
      "enabled": false
    }
  },
  "score": 0,
  "counts": {
    "members": 82,
    "posts": 19,
    "comments": 0,
    "answers": 20,
    "questions": 3
  },
  "registration": "open",
  "privacy": "public",
  "status": "active",
  "contentTypes": [],
  "type": "general",
  "verified": false,
  "summary": "Welcome community owners hub! \n\nBuilding a community is not about the platform but rather the right strategy, plan and execution. This group is a place to learn the best community management...",
  "id": "5dbc4c34560ef636c0f66172",
  "joinStatus": "joined"
}
```

This endpoint retrieves a specific group using ID.

### HTTP Request

<code class="request">GET /api/v1/groups/:id</code>

### URL Parameters

| Parameter | Type     | Description        |
| --------- | -------- | ------------------ |
| id        | `String` | The ID of the item |

## Delete a Group

```shell
curl "https://community.tribe.so/api/v1/groups/:id"
  -H "Authorization: Bearer {access_token}"
  -X DELETE
```

```javascript
const tribe = require("tribe");

let api = tribe.authorize("{access_token}");
api.group.remove(id);
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint removes a specific group. Only for admins.

### HTTP Request

<code class="request">DELETE /api/v1/groups/:id</code>

## Get List of Members

```shell
curl "https://community.tribe.so/api/v1/groups/:id/members"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require("tribe");

let api = tribe.authorize("{access_token}");
api.group.members(id);
```

> The above command returns JSON structured like this:

```json
[
  {
    "_id": "5de208b557fd4f3748a7d815",
    "email": ...,
    "profile": {
      "counts": {
        "receivedLikes": 21,
        "replies": 5,
        "groups": 0,
        "requests": 0,
        "edits": 0,
        "questionsFollowers": 0,
        "responses": 0,
        "posts": 0,
        "questions": 1,
        "comments": 6,
        "answersWords": 123,
        "answersVotes": 0,
        "answers": 4,
        "views": 0,
        "followings": 0,
        "followers": 0
      },
      "score": 131,
      "verified": false,
      "badge": {
        "type": "silver"
      },
      "description": "",
      "title": "",
      "banner": "",
      "picture": "https://lh3.googleusercontent.com/a-/AAuE7mDKbsqrfN6UncLd_7UwTuDaR3NS8qvyi2W5wCzXzA",
      "website": "",
      "location": "",
      "gender": "",
      "name": ...,
      "username": ...
    },
    "groups": [...],
    "externalId": null,
    "role": "member",
    "id": "5de208b557fd4f3748a7d815",
    "followed": false
  },
  {
    "_id": "5e580a6856cbdb5c735d9aaa",
    "email": ...,
    "profile": {
      "counts": {
        "receivedLikes": 0,
        "replies": 0,
        "groups": 0,
        "requests": 0,
        "edits": 0,
        "questionsFollowers": 0,
        "responses": 0,
        "posts": 0,
        "questions": 1,
        "comments": 0,
        "answersWords": 0,
        "answersVotes": 0,
        "answers": 0,
        "views": 0,
        "followings": 0,
        "followers": 0
      },
      "score": 12,
      "verified": false,
      "badge": {
        "type": "silver"
      },
      "description": "",
      "title": "",
      "banner": "",
      "picture": "https://gravatar.com/avatar/7919f07546893656cb0beb7a3d4e25f3?s=200&d=retro",
      "website": "",
      "location": "",
      "gender": "",
      "name": ...,
      "username": ...,
    },
    "groups": [...],
    "externalId": null,
    "role": "member",
    "id": "5e580a6856cbdb5c735d9aaa",
    "followed": false
  }
]
```

This endpoint retreives members of a group using ID.

### HTTP Request

<code class="request">GET /api/v1/groups/:id/members</code>

| Parameter | Type     | Default                 | Description                                                                               |
| --------- | -------- | ----------------------- | ----------------------------------------------------------------------------------------- |
| page      | `Number` | `1`                     | Intended page                                                                             |
| limit     | `Number` | `20`                    | Number of items per page                                                                  |
| sort      | `String` | `groups.createdAt.desc` | The field to sort on. You can use `recent` and `oldest` as well as other sort parameters. |

## Add a Member

```shell
curl "https://community.tribe.so/api/v1/groups/:id/members"
  -H "Authorization: Bearer {access_token}"
  -X POST
  --DATA "{}"
```

```javascript
const tribe = require("tribe");

let api = tribe.authorize("{access_token}");
api.group.addMember(id, member);
```

> The above command returns JSON structured like this:

```json

```

This endpoint adds a user to a specific group. Only for admins.

### HTTP Request

<code class="request">POST /api/v1/groups/:id/members</code>

| Parameter | Default | Description           |
| --------- | ------- | --------------------- |
| user      |         | ID of the user to add |

## Remove a Member

```shell
curl "https://community.tribe.so/api/v1/groups/:id/members/:userId"
  -H "Authorization: Bearer {access_token}"
  -X DELETE
```

```javascript
const tribe = require("tribe");

let api = tribe.authorize("{access_token}");
api.group.removeMember(id, member);
```

> The above command returns JSON structured like this:

```json

```

This endpoint removes a user from a specific group. Only for admins.

### HTTP Request

<code class="request">DELETE /api/v1/groups/:id/members/:userId</code>

## Get Group's Activity Feed

```shell
curl "https://community.tribe.so/api/v1/groups/:id/feed"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require("tribe");

let api = tribe.authorize("{access_token}");
let questions = api.user.feed();
```

> The above command returns JSON structured like this:

```json
[
  {
    "_id": "topics-1",
    "type": "Topics",
    "topics": [
      ...
    ],
    "description": "You have not picked any topics yet. Please pick some to improve this page."
  },
  {
    "_id": "5c0621864cb2b119dc174a63",
    "type": "Discussion",
    "publishedAt": "2018-12-04T06:41:10.031Z",
    "post": {
      ...
    }
  },
  {
    "_id": "5bf0e89ada3be54c190b78ba",
    "type": "Answer",
    "publishedAt": "2018-11-18T04:25:42.037Z",
    "answer": {
      ...
    }
  }
]
```

This endpoint retrieves group's activity feed.

### HTTP Request

<code class="request">GET /api/v1/groups/:id/feed</code>

### URL Parameters

| Parameter | Type     | Description         |
| --------- | -------- | ------------------- |
| id        | `String` | The ID of the group |

### Query Parameters

| Parameter | Type     | Default          | Description                                                                                              |
| --------- | -------- | ---------------- | -------------------------------------------------------------------------------------------------------- |
| type      | `String` |                  | Comma separated list of types to filter on. Types can be `post`, `question`, `discussion`, and `article` |
| page      | `Number` | `1`              | Intended page                                                                                            |
| limit     | `Number` | `20`             | Number of items per page                                                                                 |
| sort      | `String` | `createdAt.desc` | The field to sort on                                                                                     |

## Add a Topic to Group

```shell
curl "https://community.tribe.so/api/v1/groups/:id/topics"
  -H "Authorization: Bearer {access_token}"
  -X DELETE
  --DATA "{...}"
```

```javascript
const tribe = require("tribe");

let api = tribe.authorize("{access_token}");
api.group.addTopic(id, topic);
```

> The above command returns JSON structured like this:

```json

```

This endpoint adds a topic to a specific group. Only for admins.

### HTTP Request

<code class="request">POST /api/v1/groups/:id/topics</code>

| Parameter | Default | Description              |
| --------- | ------- | ------------------------ |
| name      |         | Name of the topic to add |

## Get All Groups

```shell
curl "https://community.tribe.so/api/v1/groups?topicName=First%20Topic"
```

```javascript
const tribe = require("tribe");

let api = tribe.authorize("{access_token}");
api.group.get({ topicName: ["First Topic"] });
```

> The above command returns JSON structured like this:

```json
[
  {
    "_id": "5db1b9b4c014eee3fcd97402",
    "shortId": "P8Bkn",
    "updatedAt": "2019-11-04T09:46:06.068Z",
    "createdAt": "2019-10-24T14:48:20.773Z",
    "slug": "first-group",
    "name": "First group",
    "portal": "5db1aaf9d2e97764f5c4b58e",
    "user": "5d3077834d0c0c03cb892a5f",
    "__v": 67,
    "pinned": [],
    "topics": [
      {
        "_id": "5dbdb0a2fe1c5e37f16bd9f4",
        "name": "First Topic",
        "slug": "first-topic",
        "paths": [],
        "id": "5dbdb0a2fe1c5e37f16bd9f4"
      },
      {
        "_id": "5dbdb0a7fe1c5e37f16bda84",
        "name": "Second Topic",
        "slug": "second-topic",
        "paths": [],
        "id": "5dbdb0a7fe1c5e37f16bda84"
      }
    ],
    ...
  }
]
```

This endpoint retrieves all groups.

### HTTP Request

<code class="request">GET /api/v1/groups</code>

### Query Parameters

| Parameter | Type     | Default          | Description                            |
| --------- | -------- | ---------------- | -------------------------------------- |
| page      | `Number` | `1`              | Intended page                          |
| limit     | `Number` | `20`             | Number of items per page               |
| sort      | `String` | `createdAt.desc` | The field to sort on                   |
| query     | `String` | `""`             | Keywords or name of a group            |
| topicName | `String` |                  | Topics' exact names separated by comma |

## Add A User to Multiple Groups

```shell
curl "https://community.tribe.so/api/v1/users/:id/groups"
  -H "Authorization: Bearer {access_token}"
  -X POST
  --DATA "{...}"
```

```javascript
const tribe = require("tribe");

let api = tribe.authorize("{access_token}");
api.group.join(user, [""]);
```

> The above command returns JSON structured like this:

```json
{
  "_id": "5db1aafad2e97764f5c4b593",
  "profile": {
      ...
  },
  "groups": [
      {
          "group": {
              "_id": "5db1b9b4c014eee3fcd97402",
              "shortId": "P8Bkn",
              "updatedAt": "2019-11-04T09:46:06.068Z",
              "createdAt": "2019-10-24T14:48:20.773Z",
              "slug": "first-group",
              "name": "First group",
              "portal": "5db1aaf9d2e97764f5c4b58e",
              "user": "5d3077834d0c0c03cb892a5f",
              ...
          },
          "status": "joined",
          "createdAt": "2019-10-24T15:00:03.565Z",
          "role": "member",
          "_id": "5db1bc73267d8cfed33cd2f3"
      },
      {
          "_id": "5dbe1943d794c01bbdf0196f",
          "createdAt": "2019-11-03T00:03:15.702Z",
          "role": "admin",
          "status": "joined",
          "group": {
              "_id": "5dbe1943d794c01bbdf0196e",
              "shortId": "QOlqV",
              "updatedAt": "2019-11-04T13:22:09.911Z",
              "createdAt": "2019-11-03T00:03:15.664Z",
              "slug": "second-group",
              "name": "Second group",
              "portal": "5db1aaf9d2e97764f5c4b58e",
              "user": "5db1aafad2e97764f5c4b593",
              ...
          }
      },
      {
          "_id": "5dbe1a279fe204230b82f5a4",
          "createdAt": "2019-11-03T00:07:03.922Z",
          "role": "admin",
          "status": "joined",
          "group": {
              "_id": "5dbe1a279fe204230b82f5a3",
              "shortId": "y9Mk7",
              "updatedAt": "2019-11-03T01:25:34.006Z",
              "createdAt": "2019-11-03T00:07:03.898Z",
              "slug": "asd-123",
              "name": "asd 123",
              "portal": "5db1aaf9d2e97764f5c4b58e",
              "user": "5db1aafad2e97764f5c4b593",
              ...
          }
      }
  ],
  "externalId": null,
  "id": "5db1aafad2e97764f5c4b593",
  "followed": false
}
```

This endpoint join user to multiple groups. It can also be used for community admins to add a user to multiple groups.

### HTTP Request

<code class="request">POST /api/v1/users/:id/groups</code>

### URL Parameters

| Parameter | Default | Description                  |
| --------- | ------- | ---------------------------- |
| id        |         | The ID of user to join (add) |

### Request Parameters

| Parameter | Default | Description                     |
| --------- | ------- | ------------------------------- |
| groupIds  |         | List of the groups' IDs to join |

## Join Multiple Groups

```shell
curl "https://community.tribe.so/api/v1/user/groups"
  -H "Authorization: Bearer {access_token}"
  -X POST
  --DATA "{...}"
```

```javascript
const tribe = require("tribe");

let api = tribe.authorize("{access_token}");
api.group.join(["groupId"]);
```

> The above command returns JSON structured like this:

```json
{
  "_id": "5db1aafad2e97764f5c4b593",
  "profile": {
      ...
  },
  "groups": [
      {
          "group": {
              "_id": "5db1b9b4c014eee3fcd97402",
              "shortId": "P8Bkn",
              "updatedAt": "2019-11-04T09:46:06.068Z",
              "createdAt": "2019-10-24T14:48:20.773Z",
              "slug": "first-group",
              "name": "First group",
              "portal": "5db1aaf9d2e97764f5c4b58e",
              "user": "5d3077834d0c0c03cb892a5f",
              ...
          },
          "status": "joined",
          "createdAt": "2019-10-24T15:00:03.565Z",
          "role": "member",
          "_id": "5db1bc73267d8cfed33cd2f3"
      },
      {
          "_id": "5dbe1943d794c01bbdf0196f",
          "createdAt": "2019-11-03T00:03:15.702Z",
          "role": "admin",
          "status": "joined",
          "group": {
              "_id": "5dbe1943d794c01bbdf0196e",
              "shortId": "QOlqV",
              "updatedAt": "2019-11-04T13:22:09.911Z",
              "createdAt": "2019-11-03T00:03:15.664Z",
              "slug": "second-group",
              "name": "Second group",
              "portal": "5db1aaf9d2e97764f5c4b58e",
              "user": "5db1aafad2e97764f5c4b593",
              ...
          }
      },
      {
          "_id": "5dbe1a279fe204230b82f5a4",
          "createdAt": "2019-11-03T00:07:03.922Z",
          "role": "admin",
          "status": "joined",
          "group": {
              "_id": "5dbe1a279fe204230b82f5a3",
              "shortId": "y9Mk7",
              "updatedAt": "2019-11-03T01:25:34.006Z",
              "createdAt": "2019-11-03T00:07:03.898Z",
              "slug": "asd-123",
              "name": "asd 123",
              "portal": "5db1aaf9d2e97764f5c4b58e",
              "user": "5db1aafad2e97764f5c4b593",
              ...
          }
      }
  ],
  "externalId": null,
  "id": "5db1aafad2e97764f5c4b593",
  "followed": false
}
```

This endpoint joins the authenticated user to multiple groups.

### HTTP Request

<code class="request">POST /api/v1/user/groups</code>

### Request Parameters

| Parameter | Default | Description                   |
| --------- | ------- | ----------------------------- |
| groupIds  |         | List of the group IDs to join |
