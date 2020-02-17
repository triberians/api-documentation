# Questions

## Get All Questions


```shell
curl "https://community.tribe.so/api/v1/questions"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let questions = api.questions.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "_id": "5a816275f8030b3bdd655b0d",
    "updatedAt": "2018-02-12T19:07:21.136Z",
    "createdAt": "2018-02-12T09:46:29.646Z",
    "title": "What is a perfect life?",
    "lastAskedAt": "2018-02-12T09:46:29.642Z",
    "__v": 0,
    "lastAnsweredAt": "2018-02-12T19:07:21.135Z",
    "downvotes": [],
    "upvotes": [],
    "followers": [],
    "askers": [],
    "comments": [],
    "topics": [],
    "score": 0,
    "counts": {
      "asks": 1,
      "downvotes": 0,
      "upvotes": 0,
      "edits": 2,
      "comments": 0,
      "hiddenAnswers": 0,
      "answers": 2,
      "views": 8,
      "followers": 0
    },
    "type": "general",
    "anonymous": true,
    "verified": false,
    "locked": false,
    "followed": false
  }
]
```

This endpoint retrieves all questions.

### HTTP Request

<code class="request">GET /api/v1/questions</code>

### Query Parameters

Parameter | Type | Default | Description
--------- | ------- | ----------- | -----------
page | `Number` | `1` | Intended page
limit | `Number` | `20` | Number of items per page
sort | `String` | `createdAt.desc` | The field to sort on


## Get a Specific Question


```shell
curl "https://community.tribe.so/api/v1/questions/5a816275f8030b3bdd655b0d"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let questions = api.questions.get('5a816275f8030b3bdd655b0d');
```

> The above command returns JSON structured like this:

```json
{
  "_id": "5a816275f8030b3bdd655b0d",
  "updatedAt": "2018-02-12T19:07:21.136Z",
  "createdAt": "2018-02-12T09:46:29.646Z",
  "title": "What is a perfect life?",
  "lastAskedAt": "2018-02-12T09:46:29.642Z",
  "__v": 0,
  "lastAnsweredAt": "2018-02-12T19:07:21.135Z",
  "downvotes": [],
  "upvotes": [],
  "followers": [],
  "askers": [],
  "comments": [],
  "topics": [],
  "score": 0,
  "counts": {
    "asks": 1,
    "downvotes": 0,
    "upvotes": 0,
    "edits": 2,
    "comments": 0,
    "hiddenAnswers": 0,
    "answers": 2,
    "views": 8,
    "followers": 0
  },
  "type": "general",
  "anonymous": true,
  "verified": false,
  "locked": false,
  "followed": false
}
```

This endpoint retrieves a specific question using ID.

### HTTP Request

<code class="request">GET /api/v1/questions/{id}</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the item


## Delete a Specific Question


```shell
curl "https://community.tribe.so/api/v1/questions/5a816275f8030b3bdd655b0d"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.questions.delete('5a816275f8030b3bdd655b0d');
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint deletes a specific question.

### HTTP Request

<code class="request">DELETE /api/v1/questions/{id}</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the question to delete



## Get Question's Answers


```shell
curl "https://community.tribe.so/api/v1/questions/5a816275f8030b3bdd655b0d/answers"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.questions.answers('5a816275f8030b3bdd655b0d');
```


### HTTP Request

<code class="request">GET /api/v1/questions/{id}/answers</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the question

### Query Parameters

Parameter | Type | Default | Description
--------- | ----------- | ------- | -----------
page | `Number` | `1` | Intended page
limit | `Number` | `20` | Number of items per page
sort | `Number` | `createdAt.desc` | The field to sort on




## Get Question's Experts


```shell
curl "https://community.tribe.so/api/v1/questions/5a816275f8030b3bdd655b0d/experts"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.questions.experts('5a816275f8030b3bdd655b0d');
```


### HTTP Request

<code class="request">GET /api/v1/questions/{id}/experts</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the question



## Get a Question's Recommendations


```shell
curl "https://community.tribe.so/api/v1/questions/5a816275f8030b3bdd655b0d/recommendations"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.questions.recommendations('5a816275f8030b3bdd655b0d');
```


### HTTP Request

<code class="request">GET /api/v1/questions/{id}/recommendations</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the question


## Get Similar Questions


```shell
curl "https://community.tribe.so/api/v1/questions/similars"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.questions.similars('This is a test question title');
```

This endpoint find related questions to keywords or a question title.

### HTTP Request

<code class="request">GET /api/v1/questions/similars</code>


### Query Parameters

Parameter | Type | Default | Description
--------- | ------- | ----------- | -----------
query | `String` | `""` | Keywords or title of a question




## Create a Question


```shell
curl "https://community.tribe.so/api/v1/questions"
  -X POST
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let question = api.questions.create({ title: 'What is life?', options: [ { text: 'Life is life' }, { text: 'I have no idea' } ] });
```

This endpoint creates a new question.

### HTTP Request

<code class="request">POST /api/v1/questions</code>

### Query Parameters

Parameter | Type | Description
--------- | ----------- | ----------- | -----------
title | `String` | The title of the question to create
description | `String` | The description of the question to create
anonymous | `Boolean` | Is this an anonymous question?
from | `String` | The ID of the user who has beend asked from
topics | `[String]` | The IDs of the topics related to the question
group | `String` | The ID of the group to post
options | `[{ text: String }]` (Optional) | An array of poll options in `[{ text: 'Option text' }]` format

### Extra Query Parameters for Moderators

Parameter | Type | Description
--------- | ----------- | -----------
type | `String` | The type of the question to create
locked | `Boolean` | Is the question locked?
verified | `Boolean` | Is the question verified?
status | `String` | Status of the question to create. Can be: `archived` `collapsed` `published` `unapproved` `unlisted` `featured` `scheduled`
user | `String` | The ID of the user to ask a question on behalf 


## Add Image, File or Video to a Question

This endpoint uploads a new file that can be attached to a Question.


### HTTP Request
<strong>@deprecated</strong>
<del><code class="request">POST /api/v1/questions/image</code></del>
<small>This endpoint has been deprecated and will be removed in a future version.</small>

<code class="request">POST /api/v1/uploads/questions</code>

> The above command returns JSON structured like this for Image, File or Video:

```json
{
  "uploaded": true,
  "url": "https://static.t-cdn.net/.../questions/.../file"
}
```

### Request Parameters

Parameter | Type | Description 
--------- | ----------- | -----------
upload | `File` | The image, file or video in `multipart/form-data` format.
<a href="https://docs.aws.amazon.com/mediaconvert/latest/ug/reference-codecs-containers-input.html" target="_blank">Supported video formats</a>



### For Image or File
To attach an image or a file to a question, first we need to send the file to this endpoint.
The endpoint resizes the images, scans files, and returns the url of the image or file.

You can pass an array of `url`s to the question creation end-point (`POST /api/v1/questions`).
You should pass the array in the body with `images` or `files` key.



### For Video
To attach a video to a question, first we need to send the video to this endpoint. 
The endpoint uploads to Amazon S3 and returns the url of the original video.


You can pass an array of `url`s to the question creation end-point (`POST /api/v1/questions`).
You should pass the array in the body with `videos` key.

Once the Question is created, the video is queued for processing. If the original video is in MP4 format, it will be readily available for the users to view it. In case the video is in any other format, the video's status will be set to "processing" under `videos` key.
Upon completion, the video's status is updated to "complete" and `poster`, `duration`, and `src` with different compressions will be added to the video object.



## Update a Specific Question


```shell
curl "https://community.tribe.so/api/v1/questions/5a816275f8030b3bdd655b0d"
  -X PUT
  -H "Authorization: Bearer {access_token}"
```

This endpoint updates a specific question.

### HTTP Request

<code class="request">PUT /api/v1/questions/:id</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the question to update

### Query Parameters

Parameter | Type | Description
--------- | ----------- | -----------
title | `String` | The title of the question to create
description | `String` | The description of the question to create
anonymous | `Boolean` | Is this an anonymous question?
options | `[{ text: String, _id: ID }]` (Optional) | An array of poll options in `[{ text: 'Option text', _id: "5e2...ab" }]` format. `_id` is the ID of the option passed while fetching a question object.

### Extra Query Parameters for Moderators

Parameter | Type | Description
--------- | ----------- | -----------
type | `String` | The type of the question to create
locked | `Boolean` | Is the question locked?
verified | `Boolean` | Is the question verified?
status | `String` | Status of the question to create. Can be: `archived` `collapsed` `published` `unapproved` `unlisted` `featured` `scheduled`

## Add a Comment for a Specific Question

```shell
  curl "https://community.tribe.so/api/v1/questions/5bf0e89ada3be54c190b78ba/comments"
  -X POST
  -H "Authorization: Bearer {access_token}"
  --DATA "{'body':'New comment'}"
```
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.questions.comments.create('5c0621864cb2b119dc174a63',"4sf0e89ada3be54c190b78b2", {
  body: "New Comment"
});
```

This endpoint adds a comment for a specific question.

### HTTP Request

<code class="request">POST /api/v1/questions/:id/comments</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the question to add a comment

### Request Parameters

Parameter | Type | Description
--------- | ----------- | -----------
body | `String` | The content of the comment

### Extra Request Parameters for Moderators

Parameter | Type | Description
--------- | ----------- | -----------
user | `String` | The ID of the user to comment on behalf

## Update a Specific Comment for a Specific Question

```shell
  curl "https://community.tribe.so/api/v1/questions/5bf0e89ada3be54c190b78ba/comments/4sf0e89ada3be54c190b78b2"
  -X PUT
  -H "Authorization: Bearer {access_token}"
  --DATA "{'body':'Updated comment'}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.questions.comments.update('5c0621864cb2b119dc174a63',"4sf0e89ada3be54c190b78b2",{
  body: "Updated Comment"
});
```

This endpoint updates a specific comment.

### HTTP Request

<code class="request">PUT /api/v1/questions/:questionId/comments/:id</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the comment to update
questionId | `String` | The ID of the question to add a comment

### Request Parameters

Parameter | Type | Description
--------- | ----------- | -----------
body | `String` | The content of the comment

## Remove a Specific Comment from Specific Question

```shell
  curl "https://community.tribe.so/api/v1/questions/5bf0e89ada3be54c190b78ba/comments/4sf0e89ada3be54c190b78b2"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.questions.comments.delete('5c0621864cb2b119dc174a63',"4sf0e89ada3be54c190b78b2");
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint removes a specific comment.

### HTTP Request

<code class="request">DELETE /api/v1/questions/:questionId/comments/:id</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the comment to remove
questionId | `String` | The ID of the question to remove a comment

## Get Stats of Specific User for Questions

```shell
  curl "https://community.tribe.so/api/v1/user/stats/questions/views"
  -H "Authorization: Bearer {access_token}"
```
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.user.stats('question','views')
```

> The above command returns JSON structured like this:

```json
{
  "values": {
    "2019-02-10": 0,
    "2019-02-11": 0,
    "2019-02-12": 0,
    "2019-02-13": 0,
    "2019-02-14": 0,
    "2019-02-15": 0,
    "2019-02-16": 0,
    "2019-02-17": 0,
    "2019-02-18": 0,
    "2019-02-19": 0,
    "2019-02-20": 0,
    "2019-02-21": 0,
    "2019-02-22": 0,
    "2019-02-23": 0,
    "2019-02-24": 0,
    "2019-02-25": 0,
    "2019-02-26": 0,
    "2019-02-27": 0,
    "2019-02-28": 0,
    "2019-03-01": 0,
    "2019-03-02": 0,
    "2019-03-03": 0,
    "2019-03-04": 0,
    "2019-03-05": 0,
    "2019-03-06": 0,
    "2019-03-07": 0,
    "2019-03-08": 0,
    "2019-03-09": 0,
    "2019-03-10": 0,
    "2019-03-11": 0,
    "2019-03-12": 0,
    "2019-03-13": 0
  },
  "type": "user_question_viewed",
  "timestamp": "2019-03-01"
}
```

This endpoint returns statistics of a specific user for questions.

### HTTP Request

<code class="request">GET /api/v1/user/stats/questions/:metric</code>


### Request Parameters

Parameter | Type | Description
--------- | ----------- | -----------
metric | `String` | Metric for the statistics. Can be: `views`,`votes`,`follows`


## Follow a question


```shell
curl "https://community.tribe.so/api/v1/questions/5bf0e89ada3be54c190b78ba/followers"
  -X POST
  -H "Authorization: Bearer {access_token}"
```
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let question = api.questions.follow('5bf0e89ada3be54c190b78ba');
```

This endpoint follows a question.

### HTTP Request

<code class="request">POST /api/v1/questions/{id}/followers</code>


## Unfollow a question


```shell
curl "https://community.tribe.so/api/v1/questions/5bf0e89ada3be54c190b78ba/followers"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let question = api.questions.unfollow('5bf0e89ada3be54c190b78ba');
```

This endpoint unfollows a question.

### HTTP Request

<code class="request">DELETE /api/v1/questions/{id}/followers</code>


## Reporting a Specific Question

```shell
curl "https://community.tribe.so/api/v1/questions/5a816275f8030b3bdd655b0d/reports"
  -X POST
  -H "Authorization: Bearer {access_token}"
```

This endpoint reports (flags) a specific question to admins and moderators.

### HTTP Request

<code class="request">POST /api/v1/questions/:id/reports</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the question to report

### Query Parameters

Parameter | Type | Description
--------- | ----------- | -----------
type | `String` | The type of the report. Can be `Harrasment`, `Spam`, `Insincere`, `PoorlyWritten`, `IncorrectTopics`, or `AgainstRules`
description | `String` | The optional description of the report shown to admins and moderators
