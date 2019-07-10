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
  - groups
  - errors
  - widgets.md.erb



search: true
---

# Introduction

Welcome to the Tribe API!

We have language bindings in Shell and JavaScript! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.


# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: <YourAccessToken>"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('<YourAccessToken>');
```

> Make sure to replace `<YourAccessToken>` with your API key.

Tribe uses API keys to allow access to the API. You can request a new Tribe API key by [contacting us](dev@tribe.so).

Tribe expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: <YourAccessToken>`

<aside class="notice">
You must replace <code>&lt;YourAccessToken&gt;</code> with your personal API key.
</aside>
