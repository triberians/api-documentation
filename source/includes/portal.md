# Portal

## Get Portal Information


```shell
curl "https://community.tribe.so/api/v1/portal"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let portals = api.portal.get();
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

## Get Portal Health Stats


```shell
curl "https://community.tribe.so/api/v1/stats/portal"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let stats = api.portal.stats();
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
let leaderboard = api.portal.leaderboard();
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


## Update the Portal


```shell
curl "https://community.tribe.so/api/v1/portal"
  -X PUT
  -H "Authorization: Bearer {access_token}"
  --DATA '{"name": "Test Portal","domain":"test.com"}'
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let portal = api.portal.update({ 
  name: "Test Portal",
  domain: "test.com"
});
```

This endpoint updates the portal.

### HTTP Request

<code class="request">PUT /api/v1/portal</code>

### Request Parameters

Parameter | Type | Description | Required
--------- | ----------- | ----------- | -----------
name | `String` | The name of the portal | `Yes`
domain | `String` | The domain of the portal | `Yes`
subdomain | `String` | The subdomain of the portal | `No`
announcement | `Object` | The announcement visible to all users on the homepage. | `No`
banner | `String` | The path to the banner image. This image is used as the default og:image. | `No`
description | `String` | Description of the portal | `No`
email | `String` | Email of the portal | `No`
englishName | `String` | Name of the portal in English | `No`
favicon | `String` | Icon of the portal | `No`
keywords | `Array<String>` | Keywords related to the portal | `No`
links | `Object` | Community links used in the sidebar and emails. | `No`
logo | `String` | Logo of the portal | `No`
longName | `String` | The full name of the community. This is being used as the title of community home. | `No`
messages | `String` | Custom messages for the community. | `No`
policies | `Object` | Policies of community. | `No`
stage | `String` | Define the stage of the community. Can be: `inception``establishment``maturity``mitosis`. | `No`
template | `Object` | Template of the portal | `No`

### Announcement Parameters
Parameter | Type | Description
--------- | ----------- | -----------
action | `String` | The action button text
content | `String` | Content of the announcement
enabled | `String` | Is announcement enabled?
layout | `String` | The layout of the announcement. Can be: `imageTop``imageSide``imageSidePadded``imageBackground``imageTopBackground``darkImageBackground`
link | `String` | Link related to the announcement
picture | `String` | Url to the picture of the announcement
title | `String` | Title of the announcement


### Links Parameters
Parameter | Type | Description
--------- | ----------- | -----------
bug | `String` | Name of the holder
facebook | `String` | Facebook handle of the portal
faq | `String` | FAQ url of the portal
feature | `String` | Request for feature url.
homepage | `String` | Homepage of the portal
instagram | `String` | Instagram handle of the portal
linkedin | `String` | Linkedin handle of the portal
privacy | `String` | Url to portal's privacy policy
telegram | `String` | Telegram handle of the portal
terms | `String` | Url to portal's terms and condition
twitter | `String` | Twitter handle of the portal

### Messages Parameters
Parameter | Type | Description
--------- | ----------- | -----------
askRules | `String` | Rules of asking questions
motto | `String` | Motto of the portal
questionIntro | `String` | Introduction for questions
signupRules | `String` | Rules of signing up
topicIntro | `String` | Introduction for topics
userIntro | `String` |Introduction for users

### Template Parameters
Parameter | Type | Description
--------- | ----------- | -----------
body | `String` | Body tag of the template
colors.default | `String` | Default Color
colors.defaultLink | `String` | Default link
colors.link | `String` | Color of links
colors.menuLink | `String` | Color of menu
colors.primary | `String` | Primary Color
colors.secondary | `String` | Secondary Color
css | `String` | Custom CSS appended to the end of the code as style tag.
menu.background | `String` | Background Color of menu
menu.border | `Number` | Border size of the menu
menu.height | `Number` | Border height of the menu
navbar.background | `String` | Background Color of the navigation bar
navbar.border | `Number` | Border size of the navigation bar
navbar.color | `String` | Color of the navigation bar
navbar.enabled | `Boolean` | Is navigation bar enabled?
navbar.height | `Number` | Height the navigation bar
navbar.links | `Array<String>` | Links of the navigation bar
navbar.linksString | `String` | Links of the navigation bar in String format.
sidebar | `String` | The HTML code used inside the sidebar box.

### Policies Parameters
Parameter | Type | Description
--------- | ----------- | -----------
access | `String` | Access privacy of the community. Can be: `public`, `private`.
cookieConsent | `String` | Display cookie consent? Can be: `enabled`, `disabled`.
email | `String` | Defines the types of emails to be sent from the community. Can be: `important`, `disabled`, `enabled`.
registration | `String` | The registration policy of the community. Can be: `public`, `approval`, `invitation`.

## Install an App

```shell
curl "https://community.tribe.so/api/v1/apps/5c7ff860c389b77bdf1f272b/settings"
  -X POST
  -H "Authorization: Bearer {access_token}"
  -H 'Content-Type: application/json; charset=utf-8'
```

```javascript
  const tribe = require('tribe');

  let api = tribe.authorize('{access_token}');
  let result = api.admin.apps.install('5c7ff860c389b77bdf1f272b')
```

> The above command returns JSON structured like this:

```json
{
  "_id": "5c7bf24f157c2c34f735a539",
  "updatedAt": "2019-03-13T14:11:32.761Z",
  "createdAt": "2019-03-03T15:27:11.190Z",
  "name": "Tribe",
  "baseUrl": "https://community.tribe.so",
  "description": "",
  "domain": "tribe.so",
  "__v": 7,
  "apps": [
    {
      "app": {
        "_id": "5c8635bac389b77bdf1f2732",
        "slug": "moderation",
        "updatedAt": "2019-03-13T14:10:03.311Z",
        "name": "Moderation",
        "shortDescription": "Let admins create a minimum reptation.",
        "picture": "https://tribe.so/assets/images/appstore/jwt-sso.png",
        "__v": 0,
        "createdAt": "2019-03-11T10:17:25.732Z",
        "settings": {
          "user": [],
          "portal": [
            {
              "type": "checkbox",
              "name": "enabled",
              "_id": "5c890f3b1ff360189a3d038e",
              "private": false,
              "values": []
            },
            {
              "type": "number",
              "name": "minimumReputation",
              "_id": "5c890f3b1ff360189a3d038d",
              "private": true,
              "values": []
            }
          ]
        },
        "components": {
          "settings": "Moderation"
        },
        "permissions": [],
        "active": true,
        "premium": false,
        "followers": [],
        "counts": {
          "followers": 0,
          "installs": 0
        },
        "screenshots": [],
        "categories": [
          "Functionality"
        ],
        "author": {
          "link": "https://tribe.so",
          "name": "Tribe Technologies, Inc"
        },
        "type": "native",
        "id": "5c8635bac389b77bdf1f2732"
      },
      "slug": "moderation",
      "settings": {
        "minimumReputation": "8",
        "_id": "5c8635bac389b77bdf1f2732",
        "enabled": true
      },
      "_id": "5c864854f6e41f201083bf60",
      "enabled": false
    },
    {
      "app": {
        "_id": "5c7bf24fc389b77bdf1f271f",
        "name": "Welcome Email",
        "updatedAt": "2019-03-13T14:10:03.304Z",
        "shortDescription": "Send an automatic customized welcome email to new users.",
        "slug": "welcome-email",
        "picture": "https://tribe.so/assets/images/appstore/welcome-email.png",
        "__v": 0,
        "createdAt": "2019-03-03T15:27:07.020Z",
        "settings": {
          "user": [],
          "portal": [
            {
              "type": "checkbox",
              "name": "enabled",
              "_id": "5c890f3b1ff360189a3d0378",
              "private": false,
              "values": []
            },
            {
              "type": "text",
              "name": "fromEmail",
              "_id": "5c890f3b1ff360189a3d0377",
              "private": true,
              "values": []
            },
            {
              "type": "text",
              "name": "fromName",
              "_id": "5c890f3b1ff360189a3d0376",
              "private": true,
              "values": []
            },
            {
              "type": "text",
              "name": "subject",
              "_id": "5c890f3b1ff360189a3d0375",
              "private": true,
              "values": []
            },
            {
              "type": "text",
              "name": "message",
              "_id": "5c890f3b1ff360189a3d0374",
              "private": true,
              "values": []
            }
          ]
        },
        "components": {
          "settings": "WelcomeEmail"
        },
        "permissions": [],
        "active": true,
        "premium": false,
        "followers": [],
        "counts": {
          "followers": 0,
          "installs": 0
        },
        "screenshots": [],
        "categories": [
          "Functionality"
        ],
        "author": {
          "link": "https://tribe.so",
          "name": "Tribe Technologies, Inc"
        },
        "type": "native",
        "id": "5c7bf24fc389b77bdf1f271f"
      },
      "slug": "welcome-email",
      "settings": {
        "_id": "5c7bf24fc389b77bdf1f271f"
      },
      "_id": "5c864865f6e41f201083bf61",
      "enabled": false
    },
    {
      "app": {
        "_id": "5c7ff860c389b77bdf1f272b",
        "name": "SendGrid",
        "updatedAt": "2019-03-13T14:10:03.305Z",
        "shortDescription": "Send emails from your SendGrid account resulting in better email delivery.",
        "slug": "sendgrid",
        "picture": "https://tribe.so/assets/images/appstore/sendgrid.png",
        "__v": 0,
        "createdAt": "2019-03-06T16:42:05.969Z",
        "settings": {
          "user": [],
          "portal": [
            {
              "type": "checkbox",
              "name": "enabled",
              "_id": "5c890f3b1ff360189a3d037b",
              "private": false,
              "values": []
            },
            {
              "type": "text",
              "name": "username",
              "_id": "5c890f3b1ff360189a3d037a",
              "private": true,
              "values": []
            },
            {
              "type": "text",
              "name": "password",
              "_id": "5c890f3b1ff360189a3d0379",
              "private": true,
              "values": []
            }
          ]
        },
        "components": {
          "settings": "SendGrid"
        },
        "permissions": [],
        "active": true,
        "premium": false,
        "followers": [],
        "counts": {
          "followers": 0,
          "installs": 0
        },
        "screenshots": [],
        "categories": [
          "Functionality"
        ],
        "author": {
          "link": "https://tribe.so",
          "name": "Tribe Technologies, Inc"
        },
        "type": "native",
        "id": "5c7ff860c389b77bdf1f272b"
      },
      "slug": "sendgrid",
      "settings": {
        "_id": "5c7ff860c389b77bdf1f272b"
      },
      "_id": "5c890f941ff360189a3d038f",
      "enabled": false
    }
  ],
  "secrets": {
    "ssoKey": "1f4f219a4b525ddfaba64a54f997e226353726720b477c7c"
  },
  "announcement": {
    "layout": "imageSide"
  },
  "template": {
    "navbar": {
      "links": [],
      "enabled": false,
      "linksString": ""
    },
    "theme": "default"
  },
  "featured": {
    "posts": [],
    "events": [],
    "answers": [],
    "topics": [],
    "users": [],
    "questions": []
  },
  "currency": {
    "conversionRate": 100,
    "enabled": false
  },
  "counts": {
    "unapprovedAnswers": 0,
    "unapprovedQuestions": 0,
    "comments": 0,
    "unanswered": 0,
    "topics": 0,
    "answers": 0,
    "questions": 0,
    "users": 0
  },
  "sections": [],
  "policies": {
    "email": "enabled",
    "cookieConsent": "disabled",
    "registration": "public",
    "content": "shareable",
    "access": "public"
  },
  "stage": "inception",
  "status": "live",
  "type": "general",
  "plan": "basic",
  "topics": [],
  "aliases": [],
  "corsWhitelist": [],
  "id": "5c7bf24f157c2c34f735a539",
  "updateHash": "1473a306957af1b78b580c0d4cf896ff"
}
```

The endpoint installs an app in the portal.

### HTTP Request

<code class="request">POST /api/v1/apps/:id/settings</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of app to install

## Uninstall an App

```shell
curl "https://community.tribe.so/api/v1/apps/5c7ff860c389b77bdf1f272b/settings"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
  -H 'Content-Type: application/json; charset=utf-8'
```

```javascript
  const tribe = require('tribe');

  let api = tribe.authorize('{access_token}');
  let result = api.admin.apps.uninstall('5c7ff860c389b77bdf1f272b')
```

> The above command returns JSON structured like this:

```json
{
  "_id": "5c7bf24f157c2c34f735a539",
  "updatedAt": "2019-03-13T14:15:04.709Z",
  "createdAt": "2019-03-03T15:27:11.190Z",
  "name": "Tribe",
  "baseUrl": "https://community.tribe.so",
  "description": "",
  "domain": "tribe.so",
  "__v": 8,
  "apps": [
    {
      "app": {
        "_id": "5c8635bac389b77bdf1f2732",
        "slug": "moderation",
        "updatedAt": "2019-03-13T14:10:03.311Z",
        "name": "Moderation",
        "shortDescription": "Let admins create a minimum reptation.",
        "picture": "https://tribe.so/assets/images/appstore/jwt-sso.png",
        "__v": 0,
        "createdAt": "2019-03-11T10:17:25.732Z",
        "settings": {
          "user": [],
          "portal": [
            {
              "type": "checkbox",
              "name": "enabled",
              "_id": "5c890f3b1ff360189a3d038e",
              "private": false,
              "values": []
            },
            {
              "type": "number",
              "name": "minimumReputation",
              "_id": "5c890f3b1ff360189a3d038d",
              "private": true,
              "values": []
            }
          ]
        },
        "components": {
          "settings": "Moderation"
        },
        "permissions": [],
        "active": true,
        "premium": false,
        "followers": [],
        "counts": {
          "followers": 0,
          "installs": 0
        },
        "screenshots": [],
        "categories": [
          "Functionality"
        ],
        "author": {
          "link": "https://tribe.so",
          "name": "Tribe Technologies, Inc"
        },
        "type": "native",
        "id": "5c8635bac389b77bdf1f2732"
      },
      "slug": "moderation",
      "settings": {
        "enabled": true,
        "_id": "5c8635bac389b77bdf1f2732",
        "minimumReputation": "8"
      },
      "_id": "5c864854f6e41f201083bf60",
      "enabled": false
    },
    {
      "app": {
        "_id": "5c7bf24fc389b77bdf1f271f",
        "name": "Welcome Email",
        "updatedAt": "2019-03-13T14:10:03.304Z",
        "shortDescription": "Send an automatic customized welcome email to new users.",
        "slug": "welcome-email",
        "picture": "https://tribe.so/assets/images/appstore/welcome-email.png",
        "__v": 0,
        "createdAt": "2019-03-03T15:27:07.020Z",
        "settings": {
          "user": [],
          "portal": [
            {
              "type": "checkbox",
              "name": "enabled",
              "_id": "5c890f3b1ff360189a3d0378",
              "private": false,
              "values": []
            },
            {
              "type": "text",
              "name": "fromEmail",
              "_id": "5c890f3b1ff360189a3d0377",
              "private": true,
              "values": []
            },
            {
              "type": "text",
              "name": "fromName",
              "_id": "5c890f3b1ff360189a3d0376",
              "private": true,
              "values": []
            },
            {
              "type": "text",
              "name": "subject",
              "_id": "5c890f3b1ff360189a3d0375",
              "private": true,
              "values": []
            },
            {
              "type": "text",
              "name": "message",
              "_id": "5c890f3b1ff360189a3d0374",
              "private": true,
              "values": []
            }
          ]
        },
        "components": {
          "settings": "WelcomeEmail"
        },
        "permissions": [],
        "active": true,
        "premium": false,
        "followers": [],
        "counts": {
          "followers": 0,
          "installs": 0
        },
        "screenshots": [],
        "categories": [
          "Functionality"
        ],
        "author": {
          "link": "https://tribe.so",
          "name": "Tribe Technologies, Inc"
        },
        "type": "native",
        "id": "5c7bf24fc389b77bdf1f271f"
      },
      "slug": "welcome-email",
      "settings": {
        "_id": "5c7bf24fc389b77bdf1f271f"
      },
      "_id": "5c864865f6e41f201083bf61",
      "enabled": false
    }
  ],
  "secrets": {
    "ssoKey": "1f4f219a4b525ddfaba64a54f997e226353726720b477c7c"
  },
  "announcement": {
    "layout": "imageSide"
  },
  "template": {
    "navbar": {
      "links": [],
      "enabled": false,
      "linksString": ""
    },
    "theme": "default"
  },
  "featured": {
    "posts": [],
    "events": [],
    "answers": [],
    "topics": [],
    "users": [],
    "questions": []
  },
  "currency": {
    "conversionRate": 100,
    "enabled": false
  },
  "counts": {
    "unapprovedAnswers": 0,
    "unapprovedQuestions": 0,
    "comments": 0,
    "unanswered": 0,
    "topics": 0,
    "answers": 0,
    "questions": 0,
    "users": 0
  },
  "sections": [],
  "policies": {
    "email": "enabled",
    "cookieConsent": "disabled",
    "registration": "public",
    "content": "shareable",
    "access": "public"
  },
  "stage": "inception",
  "status": "live",
  "type": "general",
  "plan": "basic",
  "topics": [],
  "aliases": [],
  "corsWhitelist": [],
  "id": "5c7bf24f157c2c34f735a539",
  "updateHash": "3fa36c8343b45caeb47b31c8c59a082b"
}
```

The endpoint uninstalls an app in the portal.

### HTTP Request

<code class="request">DELETE /api/v1/apps/:id/settings</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of app to uninstall