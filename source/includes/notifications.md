# Notification

## Get User Notification


```shell
curl "https://community.tribe.so/api/v1/notifications"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let questions = api.notifications.list();
```

> The above command returns JSON structured like this:

```json
[
  {
    "_id": "5bf2ac9b86eb922c246e77ca",
    "emailAt": "2018-11-19T12:29:15.723Z",
    "updatedAt": "2018-11-19T12:29:15.722Z",
    "createdAt": "2018-11-19T12:29:15.722Z",
    "verb": "follow_user",
    "to": "5b1f99a7478dd3768d84b646",
    "__v": 0,
    "emailSent": false,
    "read": false,
    "objects": [],
    "from": [
      {
        "_id": "5bd164051f117e0440efb07c",
        "profile": {
          "picture": "https://gravatar.com/avatar/533db9190e9912306ed3334e3dba2a56?s=200&d=retro",
          "name": "Sayle",
          "username": "sayele"
        },
        "id": "5bd164051f117e0440efb07c"
      }
    ]
  },
  {
    "_id": "5bf210a61c546252b2d79030",
    "updatedAt": "2018-11-19T01:23:50.998Z",
    "createdAt": "2018-11-19T01:23:50.998Z",
    "verb": "upvote",
    "to": "5b1f99a7478dd3768d84b646",
    "__v": 0,
    "emailSent": false,
    "read": false,
    "objects": [
      {
        ...
      }
    ],
    "from": [
      {
        "_id": "5bd9d35ad242f810e3d84ab6",
        "profile": {
          "picture": "/files/users/ab6/5bd9d35ad242f810e3d84ab6_77365.png",
          "name": "Soheil Alavi",
          "username": "soheil"
        },
        "id": "5bd9d35ad242f810e3d84ab6"
      }
    ]
  },
  {
    "_id": "5be36b573fb95035bf9085a5",
    "emailAt": "2018-11-07T22:46:47.681Z",
    "updatedAt": "2018-11-07T22:46:47.679Z",
    "createdAt": "2018-11-07T22:46:47.679Z",
    "verb": "ask",
    "to": "5b1f99a7478dd3768d84b646",
    "__v": 0,
    "emailSent": false,
    "read": false,
    "objects": [
      {
        "_id": "5be36b573fb95035bf9085a3",
        "shortId": "QrmZ6",
        "updatedAt": "2018-11-22T22:09:56.432Z",
        "createdAt": "2018-11-07T22:46:47.522Z",
        "title": "What is Tribe's Privacy Policy?",
        "publishedAt": "2018-11-07T22:46:47.519Z",
        "portal": "5a73b1fcc48071e4c4dc1cae",
        "lastAskedAt": "2018-11-07T22:46:47.519Z",
        "actor": "5b3f7fe0d5a11b6297259cab",
        "__v": 2,
        "lastAnsweredAt": "2018-11-07T22:47:16.105Z",
        "referrers": [
          {
            "type": "social",
            "source": "facebook",
            "count": 1,
            "_id": "5be36fa23fb95035bf9085a8",
            "urls": []
          }
        ],
        "rewards": [],
        "hasReward": false,
        "askers": [],
        "score": 0,
        "status": "published",
        "type": "general",
        "privacy": "public",
        "anonymous": false,
        "verified": false,
        "locked": false,
        "id": "5be36b573fb95035bf9085a3"
      }
    ],
    "from": [
      {
        "_id": "5b913111f19a473232026877",
        "profile": {
          "picture": "/files/users/877/5b913111f19a473232026877_65884.png",
          "name": "Adrian Garcia",
          "username": "adriang"
        },
        "id": "5b913111f19a473232026877"
      }
    ]
  }
]
```

This endpoint retrieves user notifications.

### HTTP Request

<code class="request">GET /api/v1/notifications</code>


### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
page | 1 | Intended page
limit | 20 | Number of items per page



## Get User Notification Summary


```shell
curl "https://community.tribe.so/api/v1/notifications/summary"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let questions = api.notifications.summary();
```

> The above command returns JSON structured like this:

```json
{
  "count": "19"
}
```

This endpoint retrieves user notifications count.

### HTTP Request

<code class="request">GET /api/v1/notifications/summary</code>




## Mark All Notifications as Read


```shell
curl "https://community.tribe.so/api/v1/notifications/summary"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let questions = api.notifications.read();
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint marks all user notifications as read.

### HTTP Request

<code class="request">POST /api/v1/notifications/read</code>


