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
```

This endpoint creates a new group. Only for admins.

### HTTP Request

<code class="request">POST /api/v1/groups</code>

### Query Parameters


Parameter | Default | Description
--------- | --------- | -----------
name |  | Name of the group to create
slug |  | Slug of the group to create
color |  | Color of the group to create
type | `general` | Type of the group to create. It can be one the followings: [`blog`, `general`, `feedback`]
description |  | Description of the group to create
privacy | `public` | Group privacy. It can be one of the followings: [`public`, `private`, `secret`]
verified |  | Is group verified?
picture |  | Picture URL of the group
banner |  | Banner URL of the group
registration | `open` | Registration of the group. It can be one of the followings: [`open`, `invitation`, `approval`, `none`]


## Delete a Group


```shell
curl "https://community.tribe.so/api/v1/groups/:id"
  -H "Authorization: Bearer {access_token}"
  -X DELETE
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
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

## Add a Member


```shell
curl "https://community.tribe.so/api/v1/groups/:id/members"
  -H "Authorization: Bearer {access_token}"
  -X POST
  --DATA "{}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
api.group.addMember(id,member);
```

> The above command returns JSON structured like this:

```json
```

This endpoint adds a user to a specific group. Only for admins.

### HTTP Request

<code class="request">POST /api/v1/groups/:id/members</code>

Parameter | Default | Description
--------- | --------- | -----------
user |  | ID of the user to add

## Remove a Member


```shell
curl "https://community.tribe.so/api/v1/groups/:id/members/:userId"
  -H "Authorization: Bearer {access_token}"
  -X DELETE
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
api.group.removeMember(id,member);
```

> The above command returns JSON structured like this:

```json
```

This endpoint removes a user from a specific group. Only for admins.

### HTTP Request

<code class="request">DELETE /api/v1/groups/:id/members/:userId</code>

## Add a Topic to Group


```shell
curl "https://community.tribe.so/api/v1/groups/:id/topics"
  -H "Authorization: Bearer {access_token}"
  -X DELETE
  --DATA "{...}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
api.group.addTopic(id,topic);
```

> The above command returns JSON structured like this:

```json
```

This endpoint adds a topic to a specific group. Only for admins.

### HTTP Request

<code class="request">POST /api/v1/groups/:id/topics</code>

Parameter | Default | Description
--------- | --------- | -----------
name |  | Name of the topic to add

## Get All Groups

```shell
curl "https://community.tribe.so/api/v1/groups?topicName=First%20Topic"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
api.group.get({ topicName: ['First Topic'] });
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

Parameter | Type | Default | Description
--------- | ------- | ----------- | -----------
page | `Number` | `1` | Intended page
limit | `Number` | `20` | Number of items per page
sort | `String` | `createdAt.desc` | The field to sort on
query | `String` | `""` | Keywords or name of a group
topicName | `String` | | Topics' exact names separated by comma


## Add A User to Multiple Groups

```shell
curl "https://community.tribe.so/api/v1/users/:id/groups"
  -H "Authorization: Bearer {access_token}"
  -X POST
  --DATA "{...}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
api.group.join(user,['']);
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

Parameter | Default | Description
--------- | --------- | -----------
id |  | The ID of user to join (add)

### Request Parameters

Parameter | Default | Description
--------- | --------- | -----------
groupIds |  | List of the groups' IDs to join


## Join Multiple Groups

```shell
curl "https://community.tribe.so/api/v1/user/groups"
  -H "Authorization: Bearer {access_token}"
  -X POST
  --DATA "{...}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
api.group.join(['groupId']);
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

Parameter | Default | Description
--------- | --------- | -----------
groupIds |  | List of the group IDs to join