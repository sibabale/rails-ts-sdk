# Transactions

## Overview

Transactions

### Available Operations

* [transactionsListByAccount](#transactionslistbyaccount) - List account transactions
* [transactionsRetrieve](#transactionsretrieve) - Retrieve transaction

## transactionsListByAccount

List account transactions

### Example Usage

<!-- UsageSnippet language="typescript" operationID="transactionsListByAccount" method="get" path="/api/v1/accounts/{account_id}/transactions" -->
```typescript
import { Rails } from "@rails/sdk";

const rails = new Rails({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await rails.transactions.transactionsListByAccount("6d965dc4-4ff5-49ef-a250-aadae0f57792");

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { RailsCore } from "@rails/sdk/core.js";
import { transactionsTransactionsListByAccount } from "@rails/sdk/funcs/transactionsTransactionsListByAccount.js";

// Use `RailsCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const rails = new RailsCore({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await transactionsTransactionsListByAccount(rails, "6d965dc4-4ff5-49ef-a250-aadae0f57792");
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("transactionsTransactionsListByAccount failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `accountId`                                                                                                                                                                    | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `limit`                                                                                                                                                                        | *number*                                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.TransactionsListByAccountResponse](../../models/operations/transactionslistbyaccountresponse.md)\>**

### Errors

| Error Type               | Status Code              | Content Type             |
| ------------------------ | ------------------------ | ------------------------ |
| errors.ErrorT            | 400, 401, 404            | application/json         |
| errors.ErrorT            | 500                      | application/json         |
| errors.RailsDefaultError | 4XX, 5XX                 | \*/\*                    |

## transactionsRetrieve

Retrieve transaction

### Example Usage

<!-- UsageSnippet language="typescript" operationID="transactionsRetrieve" method="get" path="/api/v1/transactions/{id}" -->
```typescript
import { Rails } from "@rails/sdk";

const rails = new Rails({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await rails.transactions.transactionsRetrieve("97b6a892-f409-4197-aaf7-f4f9be5ab90f");

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { RailsCore } from "@rails/sdk/core.js";
import { transactionsTransactionsRetrieve } from "@rails/sdk/funcs/transactionsTransactionsRetrieve.js";

// Use `RailsCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const rails = new RailsCore({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await transactionsTransactionsRetrieve(rails, "97b6a892-f409-4197-aaf7-f4f9be5ab90f");
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("transactionsTransactionsRetrieve failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                                                                                                                                                                           | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.TransactionsRetrieveResponse](../../models/operations/transactionsretrieveresponse.md)\>**

### Errors

| Error Type               | Status Code              | Content Type             |
| ------------------------ | ------------------------ | ------------------------ |
| errors.ErrorT            | 400, 401, 404            | application/json         |
| errors.ErrorT            | 500                      | application/json         |
| errors.RailsDefaultError | 4XX, 5XX                 | \*/\*                    |