---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - javascript

toc_footers:
  - <a href='mailto:dev@tribe.so'>Request API Key</a>

includes:
  - answers
  - comments
  - feed
  - notifications
  - portal
  - posts
  - questions
  - topics
  - users
  - errors
  - widgets.md.erb


search: true
---

# Introduction

Welcome to the Tribe API!

We have language bindings in Shell and JavaScript! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.


# Authentication

Tribe supports multiple authorization methods suitable for different scenarios. 

The two most common methods are:

- JWT Access Token
- Tribe Access Token

## JWT Access Token


> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: Bearer <YourAccessToken>"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('<YourAccessToken>');
```

> Make sure to replace `<YourAccessToken>` with your JWT access token.


If your product's authentication already provides JWT access tokens, the easiest way is to use the same access token in Tribe.

To do so, you need to install the "JWT Authorization" app from Tribe app store. Tribe supports JWKS and Public Key to validate the JWT access token.

The JWT access token should include sub (The ID of user), name, iat (token issued time), and email. If the user already exists in Tribe it will perform the API request on behalf of the user. If the user does not exist, it will create the user based on the information in the JWT access token and performs the action on behalf of the new user.

Tribe expects for the JWT access token to be included in API requests to the server in a header that looks like the following:

`Authorization: Bearer <YourAccessToken>`

<aside class="notice">
You must replace <code>&lt;YourAccessToken&gt;</code> with the JWT access token.
</aside>

## Tribe Access Token

If your product does not support JWT access token or you are using Tribe as the main identity service, you need to first request for a client ID and client Secret by [contacting us](dev@tribe.so).

Then, you'll be able to generate access token and refresh token using one of the following OAuth2 methods:

> The result for both POST requests will look like this:

```
{
  "token_type": "bearer",
  "access_token": "",
  "expires_in": 31536000,
  "refresh_token": ""
}
```
> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: Bearer <YourAccessToken>"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('<YourAccessToken>');
```

> Make sure to replace `<YourAccessToken>` with the generated access token.

### 1. Password Grant Type

To get an access token for a user using their username/email and password you can use the password grant_type. This is useful when you want to authenticate user in a phone app or a custom login form, where user enters their username and password and you want to generate an access token for them.

To do so, you should send a POST request to https://YOUR_COMMUNITY_URL/api/v1/oauth/token. It should include the following payload as <code>application/x-www-form-urlencoded</code>:

Key | Value
--------- | -----------
grant_type | <code>password</code>
client_id | The client ID provided by Tribe
client_secret |  The client secret provided by Tribe
username | The username you want to authenticate with
password | The password you want to authenticate with


### 2. Tribe Custom Grant Type

Tribe also have a custom grant_type called <code>tribe:client_secret_credentials</code>. With this grant type, you will be able to get the access_token and refresh_token for any user by their email, user_id (Tribe user id), or external_id (Your product's user_id that was passed in OAuth2 authentication). 

To do so, you should send a POST request to https://YOUR_COMMUNITY_URL/api/v1/oauth/token. It should include the following payload as <code>application/x-www-form-urlencoded</code>:

Key | Value
--------- | -----------
grant_type | <code>tribe:client_secret_credentials</code>
client_id | The client ID provided by Tribe
client_secret |  The client secret provided by Tribe
email, user_id or external_id | The unique identifier of the user

By default, this grant_type is open to all IP addresses, but for security reasons, we suggest that you give us a list of IP addresses and we'll limit it to those.

Tribe expects the access token to be included in API requests to the server in a header that looks like the following:

`Authorization: Bearer <YourAccessToken>`

<aside class="notice">
You must replace <code>&lt;YourAccessToken&gt;</code> with the generated access token.
</aside>

