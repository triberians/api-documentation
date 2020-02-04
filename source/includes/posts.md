# Post

## Get All Post


```shell
curl "https://community.tribe.so/api/v1/posts"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let posts = api.posts.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "_id": "5c0621864cb2b119dc174a63",
    "shortId": "Px10b",
    "lang": "en",
    "updatedAt": "2018-12-04T06:41:25.370Z",
    "createdAt": "2018-12-04T06:41:10.046Z",
    "title": "This is a test discussion.",
    "content": "<p>Here is the content of the discussion.</p>",
    "portal": "5a73b1fcc48071e4c4dc1cae",
    "publishedAt": "2018-12-04T06:41:10.031Z",
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
    "__v": 2,
    "referrers": [],
    "global": true,
    "downvotes": [],
    "upvotes": [],
    "comments": [],
    "rewards": [],
    "images": [],
    "links": [],
    "media": [],
    "topics": [
      {
        "_id": "5b88264d3d9228aa7c41f692",
        "name": "Tribe",
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
        "picture": "/files/topics/692/5b88264d3d9228aa7c41f692_72807.png",
        "id": "5b88264d3d9228aa7c41f692"
      }
    ],
    "posters": [
      {
        "user": "5b1f99a7478dd3768d84b646",
        "score": 1,
        "_id": "5c062192f3d2d61a37864a5c"
      }
    ],
    "followers": [],
    "score": 0,
    "counts": {
      "downvotes": 0,
      "links": 0,
      "totalUpvotes": 0,
      "upvotes": 0,
      "followers": 1,
      "users": 1,
      "edits": 0,
      "responses": 1,
      "comments": 0,
      "views": 0
    },
    "status": "published",
    "privacy": "public",
    "type": "discussion",
    "anonymous": false,
    "verified": false,
    "responses": [
      "5c062192f3d2d61a37864a5b"
    ],
    "summary": "Here is the content of the discussion.",
    "id": "5c0621864cb2b119dc174a63",
    "upvoted": false,
    "downvoted": false,
    "followed": false
  }
]
```

This endpoint retrieves all posts.

### HTTP Request

<code class="request">GET /api/v1/posts</code>

### Query Parameters

Parameter | Type | Default | Description
--------- | ------- | ----------- | -----------
page | `Number` | `1` | Intended page
limit | `Number` | `20` | Number of items per page
sort | `String` | `createdAt.desc` | The field to sort on
type | `String` | | Type of posts. It can be empty (for all types) or a string of types of posts (`simple`, `discussion`, `article`) seprated by comma 


## Get a Specific Post


```shell
curl "https://community.tribe.so/api/v1/posts/5c0621864cb2b119dc174a63"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let posts = api.posts.get('5c0621864cb2b119dc174a63');
```

> The above command returns JSON structured like this:

```json
  {
    "_id": "5c0621864cb2b119dc174a63",
    "shortId": "Px10b",
    "lang": "en",
    "updatedAt": "2018-12-04T06:41:25.370Z",
    "createdAt": "2018-12-04T06:41:10.046Z",
    "title": "This is a test discussion.",
    "content": "<p>Here is the content of the discussion.</p>",
    "portal": "5a73b1fcc48071e4c4dc1cae",
    "publishedAt": "2018-12-04T06:41:10.031Z",
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
    "__v": 2,
    "referrers": [],
    "global": true,
    "downvotes": [],
    "upvotes": [],
    "comments": [],
    "rewards": [],
    "images": [],
    "links": [],
    "media": [],
    "topics": [
      {
        "_id": "5b88264d3d9228aa7c41f692",
        "name": "Tribe",
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
        "picture": "/files/topics/692/5b88264d3d9228aa7c41f692_72807.png",
        "id": "5b88264d3d9228aa7c41f692"
      }
    ],
    "posters": [
      {
        "user": "5b1f99a7478dd3768d84b646",
        "score": 1,
        "_id": "5c062192f3d2d61a37864a5c"
      }
    ],
    "followers": [],
    "score": 0,
    "counts": {
      "downvotes": 0,
      "links": 0,
      "totalUpvotes": 0,
      "upvotes": 0,
      "followers": 1,
      "users": 1,
      "edits": 0,
      "responses": 1,
      "comments": 0,
      "views": 0
    },
    "status": "published",
    "privacy": "public",
    "type": "discussion",
    "anonymous": false,
    "verified": false,
    "responses": [
      "5c062192f3d2d61a37864a5b"
    ],
    "summary": "Here is the content of the discussion.",
    "id": "5c0621864cb2b119dc174a63",
    "upvoted": false,
    "downvoted": false,
    "followed": false
  }
```

This endpoint retrieves a specific post using ID.

### HTTP Request

<code class="request">GET /api/v1/posts/{id}</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the item

## Create a new Post


```shell
curl "https://community.tribe.so/api/v1/posts"
  -X POST
  -H "Authorization: Bearer {access_token}"
  --DATA "{data}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let post = api.posts.create({ 
  title: "New Post",
  content: "New Post's content",
});
```

This endpoint creates a new post.

### HTTP Request

<code class="request">POST /api/v1/posts</code>

### Request Parameters

Parameter | Type | Description 
--------- | ----------- | -----------
title | `String` | The title of the post
content | `String` | The content of the post
type | `String` | The type of the post
images | `Array` | An array of urls pointing to the images attached to this post (Only works with simple post type)
files | `Array` | An array of urls pointing to the files attached to this post (Only works with simple post type)
parent | `String` | The ID of the parent post
replyTo | `String` | The ID of the post to reply
group | `String` | The ID of the group to post

### Extra Request Parameters for Moderators

Parameter | Type | Description
--------- | ----------- | -----------
locked | `Boolean` | Is the post locked?
verified | `Boolean` | Is the post verified?
status | `String` | The status of the post. Can be: `new` `draft` `published` `unlisted` `archived` `collapsed` `scheduled` `unapproved`
user | `String` | The ID of the user to post on behalf



## Add Image, File or Video to a Post

This endpoint uploads a new file that can be attached to a simple post or included in an article post.


### HTTP Request
<strong>@deprecated</strong>
<del><code class="request">POST /api/v1/posts/image</code></del>
<small>This endpoint has been deprecated and will be removed in a future version.</small>

<code class="request">POST /api/v1/uploads/posts</code>

> The above command returns JSON structured like this for Image, File or Video:

```json
{
  "uploaded": true,
  "url": "https://static.t-cdn.net/.../posts/.../file"
}
```

### Request Parameters

Parameter | Type | Description 
--------- | ----------- | -----------
upload | `File` | The image, file or video in `multipart/form-data` format.
<a href="https://docs.aws.amazon.com/mediaconvert/latest/ug/reference-codecs-containers-input.html" target="_blank">Supported video formats</a>



### For Image or File
To attach an image or a file to a post, first we need to send the file to this endpoint.
The endpoint resizes the images, scans files, and returns the url of the image or file.

For simple post type, you can pass an array of `url`s to the post creation end-point (`POST /api/v1/posts`).
You should pass the array in the body with `images` or `files` key.

For article post type you can add the image in the `content` of the post as an HTML tag (e.g. `<img src="{url}" />`).



### For Video
To attach a video to a post, first we need to send the video to this endpoint. 
The endpoint uploads to Amazon S3 and returns the url of the original video.


For simple post type, you can pass an array of `url`s to the post creation end-point (`POST /api/v1/posts`).
You should pass the array in the body with `files` key.

Once the Post is created, the video is queued for processing. If the original video is in MP4 format, it will be readily available for the users to view it. In case the video is in any other format, the video player will be under a "processing" state.
Upon completion, the video player gets updated with the processed video. 




## Update a Specific Post


```shell
curl "https://community.tribe.so/api/v1/posts/5c0621864cb2b119dc174a63"
  -X PUT
  -H "Authorization: Bearer {access_token}"
  --DATA "{data}"
```
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let post = api.posts.update("5c0621864cb2b119dc174a63",{ 
  title: "New Post",
  content: "New Post's content",
});
```

This endpoint updates a specific post.

### HTTP Request

<code class="request">PUT /api/v1/posts/:id</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the post to update

### Request Parameters

Parameter | Type | Description
--------- | ----------- | -----------
title | `String` | The title of the post
content | `String` | The content of the post

### Extra Request Parameters for Moderators

Parameter | Type | Description
--------- | ----------- | -----------
locked | `Boolean` | Is the post locked?
verified | `Boolean` | Is the post verified?
status | `String` | The status of the post. Can be: `new` `draft` `published` `unlisted` `archived` `collapsed` `scheduled` `unapproved`

## Delete a Specific Post


```shell
curl "https://community.tribe.so/api/v1/posts/5c0621864cb2b119dc174a63"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.posts.delete('5c0621864cb2b119dc174a63');
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint deletes a specific post.

### HTTP Request

<code class="request">DELETE /api/v1/posts/{id}</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | ----------- 
id | `String` | The ID of the post to delete




## Get Post's Responses


```shell
curl "https://community.tribe.so/api/v1/posts/5c0621864cb2b119dc174a63/responses"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
api.posts.responses('5c0621864cb2b119dc174a63');
```



> The above command returns JSON structured like this:

```json
[
  {
    "_id": "5c062192f3d2d61a37864a5b",
    "shortId": "PKqoR",
    "lang": "en",
    "updatedAt": "2018-12-04T06:41:22.270Z",
    "createdAt": "2018-12-04T06:41:22.270Z",
    "content": "<p>This is a test response to a discussion.</p>",
    "parent": "5c0621864cb2b119dc174a63",
    "portal": "5a73b1fcc48071e4c4dc1cae",
    "publishedAt": "2018-12-04T06:41:22.262Z",
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
    "__v": 0,
    "referrers": [],
    "global": true,
    "downvotes": [],
    "upvotes": [],
    "comments": [],
    "rewards": [],
    "images": [],
    "links": [],
    "media": [],
    "topics": [],
    "posters": [],
    "followers": [],
    "score": 0,
    "counts": {
      "downvotes": 0,
      "links": 0,
      "totalUpvotes": 0,
      "upvotes": 0,
      "followers": 1,
      "users": 1,
      "edits": 0,
      "responses": 0,
      "comments": 0,
      "views": 0
    },
    "status": "published",
    "privacy": "public",
    "type": "response",
    "anonymous": false,
    "verified": false,
    "responses": [],
    "summary": "This is a test response to a discussion.",
    "id": "5c062192f3d2d61a37864a5b",
    "upvoted": false,
    "downvoted": false,
    "followed": false
  }
]
```

### HTTP Request

<code class="request">GET /api/v1/posts/{id}/responses</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | ----------- 
id | `String` | The ID of the question

### Query Parameters

Parameter | Type | Default | Description
--------- | ------- | ----------- | -----------
page | `Number` | `1` | Intended page
limit | `Number` | `20` | Number of items per page
sort | `String` | `createdAt.desc` | The field to sort on

## Upvote for a Specific Post


```shell
curl "https://community.tribe.so/api/v1/posts/5c0621864cb2b119dc174a63/votes"
  -X POST
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
api.posts.upvote('5c0621864cb2b119dc174a63');
```

This endpoint upvotes a specific post.

### HTTP Request

<code class="request">POST /api/v1/posts/{id}/votes</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the post to upvote

## Remove an Upvote for a Specific Post


```shell
curl "https://community.tribe.so/api/v1/posts/5c0621864cb2b119dc174a63/votes"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
api.posts.unvote('5c0621864cb2b119dc174a63');
```



> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint removes an upvote a specific post.

### HTTP Request

<code class="request">DELETE /api/v1/posts/{id}/votes</code>


### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the post to remove an upvote


## Add a Comment for a Specific Post

```shell
  curl "https://community.tribe.so/api/v1/posts/5bf0e89ada3be54c190b78ba/comments"
  -X POST
  -H "Authorization: Bearer {access_token}"
  --DATA "{'body':'New comment'}"
```
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
api.posts.comment('5c0621864cb2b119dc174a63',{
  body: "New Comment"
});
```

This endpoint adds a comment for a specific post.

### HTTP Request

<code class="request">POST /api/v1/posts/:id/comments</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the post to add a comment

### Request Parameters

Parameter | Type | Description
--------- | ----------- | -----------
body | `String` | The content of the comment

### Extra Request Parameters for Moderators

Parameter | Type | Description
--------- | ----------- | -----------
user | `String` | The ID of the user to comment on behalf

## Update a Specific Comment for a Specific Post

```shell
  curl "https://community.tribe.so/api/v1/posts/5bf0e89ada3be54c190b78ba/comments/4sf0e89ada3be54c190b78b2"
  -X PUT
  -H "Authorization: Bearer {access_token}"
  --DATA "{'body':'Updated comment'}"
```
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
api.posts.comments.update('5c0621864cb2b119dc174a63',"4sf0e89ada3be54c190b78b2",{
  body: "New Comment"
});
```

This endpoint updates a specific comment.

### HTTP Request

<code class="request">PUT /api/v1/posts/:postId/comments/:id</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the comment to update
postId | `String` | The ID of the post to add a comment

### Request Parameters

Parameter | Type | Description
--------- | ----------- | -----------
body | `String` | The content of the comment

## Remove a Specific Comment from Specific Post

```shell
  curl "https://community.tribe.so/api/v1/posts/5bf0e89ada3be54c190b78ba/comments/4sf0e89ada3be54c190b78b2"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
api.posts.comments.delete('5c0621864cb2b119dc174a63',"4sf0e89ada3be54c190b78b2");
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint removes a specific comment.

### HTTP Request

<code class="request">DELETE /api/v1/posts/:postId/comments/:id</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the comment to remove
postId | `String` | The ID of the post to remove a comment



## Reporting a Specific Post

```shell
curl "https://community.tribe.so/api/v1/posts/5a816275f8030b3bdd655b0d/reports"
  -X POST
  -H "Authorization: Bearer {access_token}"
```

This endpoint reports (flags) a specific post to admins and moderators.

### HTTP Request

<code class="request">POST /api/v1/posts/:id/reports</code>

### URL Parameters

Parameter | Type | Description
--------- | ----------- | -----------
id | `String` | The ID of the post to report

### Query Parameters

Parameter | Type | Description
--------- | ----------- | -----------
type | `String` | The type of the report. Can be `Harrasment`, `Spam`, `PoorlyWritten`, `IncorrectTopics`, or `AgainstRules`
description | `String` | The optional description of the report shown to admins and moderators
