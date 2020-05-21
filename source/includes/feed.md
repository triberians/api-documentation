# Feed

## Get User Feed

```shell
curl "https://community.tribe.so/api/v1/feed"
  -H "Authorization: Bearer {access_token}"
```

<!--
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let questions = api.user.feed();
```
-->

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

This endpoint retrieves user feed.

### HTTP Request

<code class="request">GET /api/v1/feed</code>

### Query Parameters

| Parameter | Type     | Default          | Description                                                                                              |
| --------- | -------- | ---------------- | -------------------------------------------------------------------------------------------------------- |
| type      | `String` |                  | Comma separated list of types to filter on. Types can be `post`, `question`, `discussion`, and `article` |
| page      | `Number` | `1`              | Intended page                                                                                            |
| limit     | `Number` | `20`             | Number of items per page                                                                                 |
| sort      | `String` | `createdAt.desc` | The field to sort on                                                                                     |
