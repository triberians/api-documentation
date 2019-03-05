# Portal

## Get Portal Information


```shell
curl "https://community.tribe.so/api/v1/portal"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let questions = api.portal.get();
```

> The above command returns JSON structured like this:

```json
{
  "_id": "5a73b1fcc48071e4c4dc1cae",
  "updatedAt": "2018-11-30T00:46:42.809Z",
  "createdAt": "2018-02-02T02:13:32.692Z",
  "name": "Tribe",
  "domain": "community.tribe.so",
  "baseUrl": "https://community.tribe.so",
  "moderators": [],
  "admins": [],
  "__v": 9,
  "englishName": "Tribe",
  "description": "Tribe is a cloud-based community platform that plugs into your marketing stack. Integrated with your social media, it helps you amplify the vibe around your business by allowing you and your customers to create content.",
  "keywords": "",
  "longName": "Tribe, a cloud based community platform",
  "favicon": "/files/portals/cae/favicon_19357.png",
  "logo": "/files/portals/cae/logo_59518.png",
  "banner": "/files/portals/cae/banner_96419.png",
  "apps": [],
  "announcement": {
    "title": "Forums are dead. Build your tribe.",
    "picture": "/files/portals/cae/announcement_79671.png",
    "link": "https://tribe.so/#request-form",
    "enabled": true,
    "content": "<p>Tribe is a cloud-based community platform that plugs into your marketing stack. Integrated with your social media, it helps you amplify the vibe around your business by allowing you and your customers to create content.&nbsp;</p>",
    "action": "Request Demo",
    "layout": "imageSidePadded"
  },
  "template": {
    "sidebar": "",
    "head": "",
    "css": "",
    "body": "",
    "menu": {
      "height": 65
    },
    "navbar": {
      "links": [
        {
          "_id": "5bf2400486eb922c246e77c5",
          "url": "https://tribe.so/features",
          "text": "Features",
          "position": "start"
        },
        {
          "_id": "5bf2400486eb922c246e77c4",
          "url": "https://tribe.so/services",
          "text": "Services",
          "position": "start"
        },
        {
          "_id": "5bf2400486eb922c246e77c3",
          "url": "https://tribe.so/#pricing",
          "text": "Pricing",
          "position": "start"
        },
        {
          "_id": "5bf2400486eb922c246e77c2",
          "url": "https://tribe.so/app-store",
          "text": "App Store",
          "position": "start"
        }
      ],
      "enabled": true,
      "linksString": "Features | https://tribe.so/features | start\nServices | https://tribe.so/services | start\nPricing | https://tribe.so/#pricing | start\nApp Store | https://tribe.so/app-store | start"
    },
    "colors": {
      "primary": "#26c964"
    },
    "theme": "default"
  },
  "messages": {
    "motto": "Join the community of community managers!"
  },
  "featured": {
    "posts": [],
    "events": [],
    "answers": [
      "5babcf33630b876a1e9785cd"
    ],
    "topics": [
      "5b912fcb3d9228aa7c4220dc",
      "5b9002da3d9228aa7c421ec4",
      "5b912f963d9228aa7c4220db",
      "5b8ffc353d9228aa7c421eb1",
      "5b9ad5883d9228aa7c422f0c",
      "5b88264d3d9228aa7c41f692"
    ],
    "users": [],
    "questions": []
  },
  "links": {
    "twitter": "",
    "telegram": "",
    "privacy": "/question/5be36b573fb95035bf9085a3",
    "linkedin": "",
    "instagram": "",
    "faq": "",
    "facebook": ""
  },
  "currency": {
    "external": {
      "name": "CAD"
    },
    "conversionRate": 1,
    "internal": {
      "name": "Coin"
    },
    "enabled": true
  },
  "counts": {
    "unapprovedAnswers": 0,
    "unapprovedQuestions": 0,
    "comments": 0,
    "unanswered": 25,
    "topics": 30,
    "answers": 72,
    "questions": 91,
    "users": 28
  },
  "sections": [],
  "policies": {
    "cookieConsent": "enabled",
    "registration": "public",
    "content": "shareable",
    "access": "public"
  },
  "stage": "inception",
  "status": "live",
  "type": "root",
  "plan": "basic",
  "topics": [
    {
      "_id": "5b9ad5883d9228aa7c422f0c",
      "name": "Online Community",
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
      "picture": "/files/topics/f0c/5b9ad5883d9228aa7c422f0c_586.png",
      "id": "5b9ad5883d9228aa7c422f0c"
    },
    {
      "_id": "5babb4603d9228aa7c423c23",
      "name": "Tribe Services",
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
      "picture": "/files/topics/c23/5babb4603d9228aa7c423c23_22837.png",
      "id": "5babb4603d9228aa7c423c23"
    },
    {
      "_id": "5bb1abe13d9228aa7c4242ba",
      "name": "Tribe Features",
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
      "picture": "/files/topics/2ba/5bb1abe13d9228aa7c4242ba_65172.png",
      "id": "5bb1abe13d9228aa7c4242ba"
    },
    {
      "_id": "5babe5eb3d9228aa7c423c66",
      "name": "Tribe Apps",
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
      "picture": "/files/topics/c66/5babe5eb3d9228aa7c423c66_66024.png",
      "id": "5babe5eb3d9228aa7c423c66"
    }
  ],
  "aliases": [],
  "id": "5a73b1fcc48071e4c4dc1cae",
  "updateHash": "c7bc3e38df948c7342f9e6b41d817136"
}
```

This endpoint retrieves portal information.

### HTTP Request

<code class="request">GET /api/v1/portal</code>


## Create a new Portal


```shell
curl "https://community.tribe.so/api/v1/portal"
  -X POST
  -H "Authorization: Bearer {access_token}"
  --DATA '{"name": "Test Portal","domain":"test.com"}'
```

This endpoint creates a new portal.

### HTTP Request

<code class="request">POST /api/v1/portal</code>


### Request Parameters

Field | Type | Description
--------- | ----------- | -----------
name | `string` | The name of the portal
domain | `string` | The domain of the portal
subdomain | `string` | The subdomain of the portal


## Get Trending Items


```shell
curl "https://community.tribe.so/api/v1/trends"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let questions = api.portal.trends();
```

> The above command returns JSON structured like this:

```json
{
  "questions": [ ... ],
  "users": [ ... ],
  "topics": [ ... ],
  "answers": [ ... ],
  "events": [ ... ],
  "posts": [ ... ]
}
```

This endpoint retrieves portal information.

### HTTP Request

<code class="request">GET /api/v1/stats/portal</code>



## Get Portal Health Stats


```shell
curl "https://community.tribe.so/api/v1/stats/portal"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let questions = api.portal.stats();
```

> The above command returns JSON structured like this:

```json
{
  "usersActions": 220,
  "usersPosts": 132,
  "usersSeen": 359,
  "user": {
    "lastSeenAt": "a few seconds ago",
    "lastActionAt": "7 minutes ago",
    "lastPostAt": "7 minutes ago"
  }
}
```

This endpoint retrieves portal health stats.

### HTTP Request

<code class="request">GET /api/v1/stats/portal</code>


## Get Portal Leaderboard


```shell
curl "https://community.tribe.so/api/v1/stats/users/leaderboard"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let questions = api.portal.leaderboard();
```

> The above command returns JSON structured like this:

```json
[
  {
    "target": {
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
        "description": "",
        "title": "Biomedical Engineer ",
        "picture": "/files/users/d7e/5b881b2a90ecbe6751123d7e_57697.png",
        "website": "",
        "location": "",
        "gender": "",
        "name": "Elnaz Najafi",
        "username": "elnajafi89"
      },
      "id": "5b881b2a90ecbe6751123d7e",
      "followed": true
    },
    "total": 115
  },
  {
    "target": {
      "_id": "5b7625c6307b5967d06481fb",
      "profile": {
        ...
      }
    },
    "total": 10
  },
  {
    "target": {
      "_id": "5b7de7d02234e67f52e900cf",
      "profile": {
        ...
      }
    },
    "total": 10
  }
]
```

This endpoint retrieves users leaderboard in portal.

### HTTP Request

<code class="request">GET /api/v1/stats/users/leaderboard</code>

