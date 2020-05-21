# Comments

## Update a Specific Comment

```shell
curl "https://community.tribe.so/api/v1/comments/5c0621864cb2b119dc174a63"
  -X PUT
  -H "Authorization: Bearer {access_token}"
  --DATA "{data}"
```

<!--
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let comment = api.comments.update("5c0621864cb2b119dc174a63",{
  body: "New Comment",
});
```
-->

This endpoint updates a specific comment.

### HTTP Request

<code class="request">PUT /api/v1/comments/:id</code>

### URL Parameters

| Parameter | Type     | Description                     |
| --------- | -------- | ------------------------------- |
| id        | `String` | The ID of the comment to update |

### Request Parameters

| Parameter | Type     | Description                |
| --------- | -------- | -------------------------- |
| body      | `String` | The content of the comment |

## Delete a Specific Comment

```shell
curl "https://community.tribe.so/api/v1/comments/5c0621864cb2b119dc174a63"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```

<!--
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.comments.delete('5c0621864cb2b119dc174a63');
```
-->

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint deletes a specific comment.

### HTTP Request

<code class="request">DELETE /api/v1/comments/{id}</code>

### URL Parameters

| Parameter | Type     | Description                     |
| --------- | -------- | ------------------------------- |
| id        | `String` | The ID of the comment to delete |

## Upvote for a Specific Comment

```shell
curl "https://community.tribe.so/api/v1/comments/5c0621864cb2b119dc174a63/votes"
  -X POST
  -H "Authorization: Bearer {access_token}"
```

<!--
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
api.comments.upvote('5c0621864cb2b119dc174a63');
```
-->

This endpoint upvotes a specific comment.

### HTTP Request

<code class="request">POST /api/v1/comments/{id}/votes</code>

### URL Parameters

| Parameter | Type     | Description                     |
| --------- | -------- | ------------------------------- |
| id        | `String` | The ID of the comment to upvote |

## Remove an Upvote for a Specific Comment

```shell
curl "https://community.tribe.so/api/v1/comments/5c0621864cb2b119dc174a63/votes"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```

<!--
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
api.comments.unvote('5c0621864cb2b119dc174a63');
```
-->

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint removes an upvote a specific comment.

### HTTP Request

<code class="request">DELETE /api/v1/comments/{id}/votes</code>

### URL Parameters

| Parameter | Type     | Description                               |
| --------- | -------- | ----------------------------------------- |
| id        | `String` | The ID of the comment to remove an upvote |

## Reporting a Specific Comment

```shell
curl "https://community.tribe.so/api/v1/comments/5a816275f8030b3bdd655b0d/reports"
  -X POST
  -H "Authorization: Bearer {access_token}"
```

This endpoint reports (flags) a specific comment to admins and moderators.

### HTTP Request

<code class="request">POST /api/v1/comments/:id/reports</code>

### URL Parameters

| Parameter | Type     | Description                     |
| --------- | -------- | ------------------------------- |
| id        | `String` | The ID of the comment to report |

### Query Parameters

| Parameter   | Type     | Description                                                                                                                                             |
| ----------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| type        | `String` | The type of the report. Can be `Harrasment`, `Spam`, `Plagiarism`, `JokeComment`, `OutOfDate`, `PoorlyWritten`, `FactuallyIncorrect`, or `AgainstRules` |
| description | `String` | The optional description of the report shown to admins and moderators                                                                                   |
