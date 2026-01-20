# Accounts

## Overview

Accounts

### Available Operations

* [accountsCreate](#accountscreate) - Create account
* [accountsList](#accountslist) - List accounts
* [accountsRetrieve](#accountsretrieve) - Retrieve account
* [accountsUpdateStatus](#accountsupdatestatus) - Update account status
* [accountsClose](#accountsclose) - Close account
* [accountsDeposit](#accountsdeposit) - Deposit into account
* [accountsWithdraw](#accountswithdraw) - Withdraw from account
* [accountsTransfer](#accountstransfer) - Transfer between accounts

## accountsCreate

Create account

### Example Usage

<!-- UsageSnippet language="typescript" operationID="accountsCreate" method="post" path="/api/v1/accounts" -->
```typescript
import { Rails } from "@rails/sdk";

const rails = new Rails({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await rails.accounts.accountsCreate({
    accountType: "saving",
    userId: "795523de-24bc-4177-824a-bee4de92a0bd",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { RailsCore } from "@rails/sdk/core.js";
import { accountsAccountsCreate } from "@rails/sdk/funcs/accountsAccountsCreate.js";

// Use `RailsCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const rails = new RailsCore({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await accountsAccountsCreate(rails, {
    accountType: "saving",
    userId: "795523de-24bc-4177-824a-bee4de92a0bd",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("accountsAccountsCreate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.CreateAccountRequest](../../models/createaccountrequest.md)                                                                                                            | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.AccountsCreateResponse](../../models/operations/accountscreateresponse.md)\>**

### Errors

| Error Type               | Status Code              | Content Type             |
| ------------------------ | ------------------------ | ------------------------ |
| errors.ErrorT            | 400, 401                 | application/json         |
| errors.ErrorT            | 500                      | application/json         |
| errors.RailsDefaultError | 4XX, 5XX                 | \*/\*                    |

## accountsList

List accounts

### Example Usage

<!-- UsageSnippet language="typescript" operationID="accountsList" method="get" path="/api/v1/accounts" -->
```typescript
import { Rails } from "@rails/sdk";

const rails = new Rails({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await rails.accounts.accountsList("11082ddf-06b2-4844-a796-77324356047b");

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { RailsCore } from "@rails/sdk/core.js";
import { accountsAccountsList } from "@rails/sdk/funcs/accountsAccountsList.js";

// Use `RailsCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const rails = new RailsCore({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await accountsAccountsList(rails, "11082ddf-06b2-4844-a796-77324356047b");
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("accountsAccountsList failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `userId`                                                                                                                                                                       | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.AccountsListResponse](../../models/operations/accountslistresponse.md)\>**

### Errors

| Error Type               | Status Code              | Content Type             |
| ------------------------ | ------------------------ | ------------------------ |
| errors.ErrorT            | 400, 401                 | application/json         |
| errors.ErrorT            | 500                      | application/json         |
| errors.RailsDefaultError | 4XX, 5XX                 | \*/\*                    |

## accountsRetrieve

Retrieve account

### Example Usage

<!-- UsageSnippet language="typescript" operationID="accountsRetrieve" method="get" path="/api/v1/accounts/{id}" -->
```typescript
import { Rails } from "@rails/sdk";

const rails = new Rails({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await rails.accounts.accountsRetrieve("33f03b55-3149-49b1-b0da-8002068f6dc4");

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { RailsCore } from "@rails/sdk/core.js";
import { accountsAccountsRetrieve } from "@rails/sdk/funcs/accountsAccountsRetrieve.js";

// Use `RailsCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const rails = new RailsCore({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await accountsAccountsRetrieve(rails, "33f03b55-3149-49b1-b0da-8002068f6dc4");
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("accountsAccountsRetrieve failed:", res.error);
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

**Promise\<[operations.AccountsRetrieveResponse](../../models/operations/accountsretrieveresponse.md)\>**

### Errors

| Error Type               | Status Code              | Content Type             |
| ------------------------ | ------------------------ | ------------------------ |
| errors.ErrorT            | 400, 401, 404            | application/json         |
| errors.ErrorT            | 500                      | application/json         |
| errors.RailsDefaultError | 4XX, 5XX                 | \*/\*                    |

## accountsUpdateStatus

Update account status

### Example Usage

<!-- UsageSnippet language="typescript" operationID="accountsUpdateStatus" method="patch" path="/api/v1/accounts/{id}" -->
```typescript
import { Rails } from "@rails/sdk";

const rails = new Rails({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await rails.accounts.accountsUpdateStatus("79189c96-0fe5-479d-bcc8-0e2052b74662", {});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { RailsCore } from "@rails/sdk/core.js";
import { accountsAccountsUpdateStatus } from "@rails/sdk/funcs/accountsAccountsUpdateStatus.js";

// Use `RailsCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const rails = new RailsCore({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await accountsAccountsUpdateStatus(rails, "79189c96-0fe5-479d-bcc8-0e2052b74662", {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("accountsAccountsUpdateStatus failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                                                                                                                                                                           | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `updateAccountRequest`                                                                                                                                                         | [models.UpdateAccountRequest](../../models/updateaccountrequest.md)                                                                                                            | :heavy_check_mark:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.AccountsUpdateStatusResponse](../../models/operations/accountsupdatestatusresponse.md)\>**

### Errors

| Error Type               | Status Code              | Content Type             |
| ------------------------ | ------------------------ | ------------------------ |
| errors.ErrorT            | 400, 401, 404            | application/json         |
| errors.ErrorT            | 500                      | application/json         |
| errors.RailsDefaultError | 4XX, 5XX                 | \*/\*                    |

## accountsClose

Close account

### Example Usage

<!-- UsageSnippet language="typescript" operationID="accountsClose" method="delete" path="/api/v1/accounts/{id}" -->
```typescript
import { Rails } from "@rails/sdk";

const rails = new Rails({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await rails.accounts.accountsClose("663552dd-c955-459e-9809-a0b0cd848370");

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { RailsCore } from "@rails/sdk/core.js";
import { accountsAccountsClose } from "@rails/sdk/funcs/accountsAccountsClose.js";

// Use `RailsCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const rails = new RailsCore({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await accountsAccountsClose(rails, "663552dd-c955-459e-9809-a0b0cd848370");
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("accountsAccountsClose failed:", res.error);
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

**Promise\<[operations.AccountsCloseResponse](../../models/operations/accountscloseresponse.md)\>**

### Errors

| Error Type               | Status Code              | Content Type             |
| ------------------------ | ------------------------ | ------------------------ |
| errors.ErrorT            | 400, 401, 404            | application/json         |
| errors.ErrorT            | 500                      | application/json         |
| errors.RailsDefaultError | 4XX, 5XX                 | \*/\*                    |

## accountsDeposit

Deposit into account

### Example Usage

<!-- UsageSnippet language="typescript" operationID="accountsDeposit" method="post" path="/api/v1/accounts/{id}/deposit" -->
```typescript
import { Rails } from "@rails/sdk";

const rails = new Rails({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await rails.accounts.accountsDeposit("bd87bf62-7b45-4b98-a31c-44ea759b76e3", {
    amount: "676.67",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { RailsCore } from "@rails/sdk/core.js";
import { accountsAccountsDeposit } from "@rails/sdk/funcs/accountsAccountsDeposit.js";

// Use `RailsCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const rails = new RailsCore({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await accountsAccountsDeposit(rails, "bd87bf62-7b45-4b98-a31c-44ea759b76e3", {
    amount: "676.67",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("accountsAccountsDeposit failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                                                                                                                                                                           | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `depositRequest`                                                                                                                                                               | [models.DepositRequest](../../models/depositrequest.md)                                                                                                                        | :heavy_check_mark:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.AccountsDepositResponse](../../models/operations/accountsdepositresponse.md)\>**

### Errors

| Error Type               | Status Code              | Content Type             |
| ------------------------ | ------------------------ | ------------------------ |
| errors.ErrorT            | 400, 401, 404            | application/json         |
| errors.ErrorT            | 500                      | application/json         |
| errors.RailsDefaultError | 4XX, 5XX                 | \*/\*                    |

## accountsWithdraw

Withdraw from account

### Example Usage

<!-- UsageSnippet language="typescript" operationID="accountsWithdraw" method="post" path="/api/v1/accounts/{id}/withdraw" -->
```typescript
import { Rails } from "@rails/sdk";

const rails = new Rails({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await rails.accounts.accountsWithdraw("0c311ee2-14ab-4f73-8c3d-054e4cba3cad", {
    amount: "817.38",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { RailsCore } from "@rails/sdk/core.js";
import { accountsAccountsWithdraw } from "@rails/sdk/funcs/accountsAccountsWithdraw.js";

// Use `RailsCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const rails = new RailsCore({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await accountsAccountsWithdraw(rails, "0c311ee2-14ab-4f73-8c3d-054e4cba3cad", {
    amount: "817.38",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("accountsAccountsWithdraw failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                                                                                                                                                                           | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `withdrawRequest`                                                                                                                                                              | [models.WithdrawRequest](../../models/withdrawrequest.md)                                                                                                                      | :heavy_check_mark:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.AccountsWithdrawResponse](../../models/operations/accountswithdrawresponse.md)\>**

### Errors

| Error Type               | Status Code              | Content Type             |
| ------------------------ | ------------------------ | ------------------------ |
| errors.ErrorT            | 400, 401, 404            | application/json         |
| errors.ErrorT            | 500                      | application/json         |
| errors.RailsDefaultError | 4XX, 5XX                 | \*/\*                    |

## accountsTransfer

Transfer between accounts

### Example Usage

<!-- UsageSnippet language="typescript" operationID="accountsTransfer" method="post" path="/api/v1/accounts/{id}/transfer" -->
```typescript
import { Rails } from "@rails/sdk";

const rails = new Rails({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await rails.accounts.accountsTransfer("3a11a7c2-36f0-4955-ba89-218fe4574452", {
    toAccountId: "13fa99b9-fece-4f6b-b269-d108af4eefa9",
    amount: "26.42",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { RailsCore } from "@rails/sdk/core.js";
import { accountsAccountsTransfer } from "@rails/sdk/funcs/accountsAccountsTransfer.js";

// Use `RailsCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const rails = new RailsCore({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await accountsAccountsTransfer(rails, "3a11a7c2-36f0-4955-ba89-218fe4574452", {
    toAccountId: "13fa99b9-fece-4f6b-b269-d108af4eefa9",
    amount: "26.42",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("accountsAccountsTransfer failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                                                                                                                                                                           | *string*                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `transferRequest`                                                                                                                                                              | [models.TransferRequest](../../models/transferrequest.md)                                                                                                                      | :heavy_check_mark:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.AccountsTransferResponse](../../models/operations/accountstransferresponse.md)\>**

### Errors

| Error Type               | Status Code              | Content Type             |
| ------------------------ | ------------------------ | ------------------------ |
| errors.ErrorT            | 400, 401, 404            | application/json         |
| errors.ErrorT            | 500                      | application/json         |
| errors.RailsDefaultError | 4XX, 5XX                 | \*/\*                    |