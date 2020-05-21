# Virtual Currency

## Add Credit to User

```shell
curl "https://community.tribe.so/api/v1/users/:id/credit"
  -H "Authorization: Bearer {access_token}"
  -X POST
```

<!--
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
api.currency.add(id,amount);
```
-->

> The above command returns JSON structured like this:

```json

```

This endpoint adds credits to a specific user. It does not reduce credits from the giver and is only for admins.

### HTTP Request

<code class="request">POST /api/v1/users/:id/credit</code>

### Query Parameters

| Parameter | Default  | Description                                                |
| --------- | -------- | ---------------------------------------------------------- |
| type      | `credit` | Type of the request. For adding credit it must be `credit` |
| amount    |          | Amount of the credit to add                                |

## Withdraw Credit from User

```shell
curl "https://community.tribe.so/api/v1/users/:id/credit"
  -H "Authorization: Bearer {access_token}"
  -X POST
```

<!--
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
api.currency.withdraw(id,amount);
```
-->

> The above command returns JSON structured like this:

```json

```

This endpoint withdraws credits from a specific user. Only for admins.

### HTTP Request

<code class="request">POST /api/v1/users/:id/credit</code>

### Query Parameters

| Parameter | Default    | Description                                                       |
| --------- | ---------- | ----------------------------------------------------------------- |
| type      | `withdraw` | Type of the request. For withdrawing credit it must be `withdraw` |
| amount    |            | Amount of the credit to withdraw                                  |

## Deposit Credit from User

```shell
curl "https://community.tribe.so/api/v1/users/:id/credit"
  -H "Authorization: Bearer {access_token}"
  -X POST
```

<!--
```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
api.currency.deposit(id,amount);
```
-->

> The above command returns JSON structured like this:

```json

```

This endpoint deposits credits to a specific user.

### HTTP Request

<code class="request">POST /api/v1/users/:id/credit</code>

### Query Parameters

| Parameter | Default   | Description                                                      |
| --------- | --------- | ---------------------------------------------------------------- |
| type      | `deposit` | Type of the request. For withdrawing credit it must be `deposit` |
| amount    |           | Amount of the credit to deposit                                  |
