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