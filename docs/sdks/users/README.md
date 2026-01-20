# Users

## Overview

Users

### Available Operations

* [usersCreate](#userscreate) - Create user

## usersCreate

Create user

### Example Usage

<!-- UsageSnippet language="typescript" operationID="usersCreate" method="post" path="/api/v1/users" -->
```typescript
import { Rails } from "@rails/sdk";

const rails = new Rails({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await rails.users.usersCreate("production", {
    firstName: "Alexanne",
    lastName: "Wehner",
    email: "Myah_Veum19@yahoo.com",
    password: "TXz5lHn_rozuDSn",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { RailsCore } from "@rails/sdk/core.js";
import { usersUsersCreate } from "@rails/sdk/funcs/usersUsersCreate.js";

// Use `RailsCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const rails = new RailsCore({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await usersUsersCreate(rails, "production", {
    firstName: "Alexanne",
    lastName: "Wehner",
    email: "Myah_Veum19@yahoo.com",
    password: "TXz5lHn_rozuDSn",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("usersUsersCreate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `xEnvironment`                                                                                                                                                                 | [models.XEnvironment](../../models/xenvironment.md)                                                                                                                            | :heavy_check_mark:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `createUserRequest`                                                                                                                                                            | [models.CreateUserRequest](../../models/createuserrequest.md)                                                                                                                  | :heavy_check_mark:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.UsersCreateResponse](../../models/operations/userscreateresponse.md)\>**

### Errors

| Error Type               | Status Code              | Content Type             |
| ------------------------ | ------------------------ | ------------------------ |
| errors.ErrorT            | 400, 401, 403            | application/json         |
| errors.ErrorT            | 500                      | application/json         |
| errors.RailsDefaultError | 4XX, 5XX                 | \*/\*                    |