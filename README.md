# rails

Developer-friendly & type-safe Typescript SDK specifically catered to leverage *rails* API.

<div align="left">
    <a href="https://www.speakeasy.com/?utm_source=rails&utm_campaign=typescript"><img src="https://custom-icon-badges.demolab.com/badge/-Built%20By%20Speakeasy-212015?style=for-the-badge&logoColor=FBE331&logo=speakeasy&labelColor=545454" /></a>
    <a href="https://opensource.org/licenses/MIT">
        <img src="https://img.shields.io/badge/License-MIT-blue.svg" style="width: 100px; height: 28px;" />
    </a>
</div>


<br /><br />
> [!IMPORTANT]
> This SDK is not yet ready for production use. To complete setup please follow the steps outlined in your [workspace](https://app.speakeasy.com/org/rails/poc). Delete this section before > publishing to a package manager.

<!-- Start Summary [summary] -->
## Summary

Rails API: Rails public API for founders
<!-- End Summary [summary] -->

<!-- Start Table of Contents [toc] -->
## Table of Contents
<!-- $toc-max-depth=2 -->
* [rails](#rails)
  * [SDK Installation](#sdk-installation)
  * [Requirements](#requirements)
  * [SDK Example Usage](#sdk-example-usage)
  * [Authentication](#authentication)
  * [Available Resources and Operations](#available-resources-and-operations)
  * [Standalone functions](#standalone-functions)
  * [Retries](#retries)
  * [Error Handling](#error-handling)
  * [Server Selection](#server-selection)
  * [Custom HTTP Client](#custom-http-client)
  * [Debugging](#debugging)
* [Development](#development)
  * [Maturity](#maturity)
  * [Contributions](#contributions)

<!-- End Table of Contents [toc] -->

<!-- Start SDK Installation [installation] -->
## SDK Installation

The SDK can be installed with either [npm](https://www.npmjs.com/), [pnpm](https://pnpm.io/), [bun](https://bun.sh/) or [yarn](https://classic.yarnpkg.com/en/) package managers.

### NPM

```bash
npm add @rails/sdk
```

### PNPM

```bash
pnpm add @rails/sdk
```

### Bun

```bash
bun add @rails/sdk
```

### Yarn

```bash
yarn add @rails/sdk
```

> [!NOTE]
> This package is published with CommonJS and ES Modules (ESM) support.
<!-- End SDK Installation [installation] -->

<!-- Start Requirements [requirements] -->
## Requirements

For supported JavaScript runtimes, please consult [RUNTIMES.md](RUNTIMES.md).
<!-- End Requirements [requirements] -->

<!-- Start SDK Example Usage [usage] -->
## SDK Example Usage

### Example

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
<!-- End SDK Example Usage [usage] -->


<!-- Start Authentication [security] -->
## Authentication

### Per-Client Security Schemes

This SDK supports the following security scheme globally:

| Name         | Type   | Scheme  | Environment Variable |
| ------------ | ------ | ------- | -------------------- |
| `apiKeyAuth` | apiKey | API key | `RAILS_API_KEY_AUTH` |

To authenticate with the API the `apiKeyAuth` parameter must be set when initializing the SDK client instance. For example:
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
<!-- End Authentication [security] -->

<!-- Start Available Resources and Operations [operations] -->
## Available Resources and Operations

<details open>
<summary>Available methods</summary>

### [Accounts](docs/sdks/accounts/README.md)

* [accountsCreate](docs/sdks/accounts/README.md#accountscreate) - Create account
* [accountsList](docs/sdks/accounts/README.md#accountslist) - List accounts
* [accountsRetrieve](docs/sdks/accounts/README.md#accountsretrieve) - Retrieve account
* [accountsUpdateStatus](docs/sdks/accounts/README.md#accountsupdatestatus) - Update account status
* [accountsClose](docs/sdks/accounts/README.md#accountsclose) - Close account
* [accountsDeposit](docs/sdks/accounts/README.md#accountsdeposit) - Deposit into account
* [accountsWithdraw](docs/sdks/accounts/README.md#accountswithdraw) - Withdraw from account
* [accountsTransfer](docs/sdks/accounts/README.md#accountstransfer) - Transfer between accounts

### [Transactions](docs/sdks/transactions/README.md)

* [transactionsListByAccount](docs/sdks/transactions/README.md#transactionslistbyaccount) - List account transactions
* [transactionsRetrieve](docs/sdks/transactions/README.md#transactionsretrieve) - Retrieve transaction

### [Users](docs/sdks/users/README.md)

* [usersCreate](docs/sdks/users/README.md#userscreate) - Create user

</details>
<!-- End Available Resources and Operations [operations] -->

<!-- Start Standalone functions [standalone-funcs] -->
## Standalone functions

All the methods listed above are available as standalone functions. These
functions are ideal for use in applications running in the browser, serverless
runtimes or other environments where application bundle size is a primary
concern. When using a bundler to build your application, all unused
functionality will be either excluded from the final bundle or tree-shaken away.

To read more about standalone functions, check [FUNCTIONS.md](./FUNCTIONS.md).

<details>

<summary>Available standalone functions</summary>

- [`accountsAccountsClose`](docs/sdks/accounts/README.md#accountsclose) - Close account
- [`accountsAccountsCreate`](docs/sdks/accounts/README.md#accountscreate) - Create account
- [`accountsAccountsDeposit`](docs/sdks/accounts/README.md#accountsdeposit) - Deposit into account
- [`accountsAccountsList`](docs/sdks/accounts/README.md#accountslist) - List accounts
- [`accountsAccountsRetrieve`](docs/sdks/accounts/README.md#accountsretrieve) - Retrieve account
- [`accountsAccountsTransfer`](docs/sdks/accounts/README.md#accountstransfer) - Transfer between accounts
- [`accountsAccountsUpdateStatus`](docs/sdks/accounts/README.md#accountsupdatestatus) - Update account status
- [`accountsAccountsWithdraw`](docs/sdks/accounts/README.md#accountswithdraw) - Withdraw from account
- [`transactionsTransactionsListByAccount`](docs/sdks/transactions/README.md#transactionslistbyaccount) - List account transactions
- [`transactionsTransactionsRetrieve`](docs/sdks/transactions/README.md#transactionsretrieve) - Retrieve transaction
- [`usersUsersCreate`](docs/sdks/users/README.md#userscreate) - Create user

</details>
<!-- End Standalone functions [standalone-funcs] -->


<!-- Start Retries [retries] -->
## Retries

Some of the endpoints in this SDK support retries.  If you use the SDK without any configuration, it will fall back to the default retry strategy provided by the API.  However, the default retry strategy can be overridden on a per-operation basis, or across the entire SDK.

To change the default retry strategy for a single API call, simply provide a retryConfig object to the call:
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
  }, {
    retries: {
      strategy: "backoff",
      backoff: {
        initialInterval: 1,
        maxInterval: 50,
        exponent: 1.1,
        maxElapsedTime: 100,
      },
      retryConnectionErrors: false,
    },
  });

  console.log(result);
}

run();

```

If you'd like to override the default retry strategy for all operations that support retries, you can provide a retryConfig at SDK initialization:
```typescript
import { Rails } from "@rails/sdk";

const rails = new Rails({
  retryConfig: {
    strategy: "backoff",
    backoff: {
      initialInterval: 1,
      maxInterval: 50,
      exponent: 1.1,
      maxElapsedTime: 100,
    },
    retryConnectionErrors: false,
  },
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
<!-- End Retries [retries] -->

<!-- Start Error Handling [errors] -->
## Error Handling

[`RailsError`](./src/models/errors/railserror.ts) is the base class for all HTTP error responses. It has the following properties:

| Property            | Type       | Description                                                                             |
| ------------------- | ---------- | --------------------------------------------------------------------------------------- |
| `error.message`     | `string`   | Error message                                                                           |
| `error.statusCode`  | `number`   | HTTP response status code eg `404`                                                      |
| `error.headers`     | `Headers`  | HTTP response headers                                                                   |
| `error.body`        | `string`   | HTTP body. Can be empty string if no body is returned.                                  |
| `error.rawResponse` | `Response` | Raw HTTP response                                                                       |
| `error.data$`       |            | Optional. Some errors may contain structured data. [See Error Classes](#error-classes). |

### Example
```typescript
import { Rails } from "@rails/sdk";
import * as errors from "@rails/sdk/models/errors";

const rails = new Rails({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  try {
    const result = await rails.users.usersCreate("production", {
      firstName: "Alexanne",
      lastName: "Wehner",
      email: "Myah_Veum19@yahoo.com",
      password: "TXz5lHn_rozuDSn",
    });

    console.log(result);
  } catch (error) {
    // The base class for HTTP error responses
    if (error instanceof errors.RailsError) {
      console.log(error.message);
      console.log(error.statusCode);
      console.log(error.body);
      console.log(error.headers);

      // Depending on the method different errors may be thrown
      if (error instanceof errors.ErrorT) {
        console.log(error.data$.status); // string
        console.log(error.data$.code); // string
        console.log(error.data$.message); // string
      }
    }
  }
}

run();

```

### Error Classes
**Primary errors:**
* [`RailsError`](./src/models/errors/railserror.ts): The base class for HTTP error responses.
  * [`ErrorT`](./src/models/errors/errort.ts): Error.

<details><summary>Less common errors (6)</summary>

<br />

**Network errors:**
* [`ConnectionError`](./src/models/errors/httpclienterrors.ts): HTTP client was unable to make a request to a server.
* [`RequestTimeoutError`](./src/models/errors/httpclienterrors.ts): HTTP request timed out due to an AbortSignal signal.
* [`RequestAbortedError`](./src/models/errors/httpclienterrors.ts): HTTP request was aborted by the client.
* [`InvalidRequestError`](./src/models/errors/httpclienterrors.ts): Any input used to create a request is invalid.
* [`UnexpectedClientError`](./src/models/errors/httpclienterrors.ts): Unrecognised or unexpected error.


**Inherit from [`RailsError`](./src/models/errors/railserror.ts)**:
* [`ResponseValidationError`](./src/models/errors/responsevalidationerror.ts): Type mismatch between the data returned from the server and the structure expected by the SDK. See `error.rawValue` for the raw value and `error.pretty()` for a nicely formatted multi-line string.

</details>
<!-- End Error Handling [errors] -->

<!-- Start Server Selection [server] -->
## Server Selection

### Override Server URL Per-Client

The default server can be overridden globally by passing a URL to the `serverURL: string` optional parameter when initializing the SDK client instance. For example:
```typescript
import { Rails } from "@rails/sdk";

const rails = new Rails({
  serverURL: "https://api.rails.com",
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
<!-- End Server Selection [server] -->

<!-- Start Custom HTTP Client [http-client] -->
## Custom HTTP Client

The TypeScript SDK makes API calls using an `HTTPClient` that wraps the native
[Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API). This
client is a thin wrapper around `fetch` and provides the ability to attach hooks
around the request lifecycle that can be used to modify the request or handle
errors and response.

The `HTTPClient` constructor takes an optional `fetcher` argument that can be
used to integrate a third-party HTTP client or when writing tests to mock out
the HTTP client and feed in fixtures.

The following example shows how to use the `"beforeRequest"` hook to to add a
custom header and a timeout to requests and how to use the `"requestError"` hook
to log errors:

```typescript
import { Rails } from "@rails/sdk";
import { HTTPClient } from "@rails/sdk/lib/http";

const httpClient = new HTTPClient({
  // fetcher takes a function that has the same signature as native `fetch`.
  fetcher: (request) => {
    return fetch(request);
  }
});

httpClient.addHook("beforeRequest", (request) => {
  const nextRequest = new Request(request, {
    signal: request.signal || AbortSignal.timeout(5000)
  });

  nextRequest.headers.set("x-custom-header", "custom value");

  return nextRequest;
});

httpClient.addHook("requestError", (error, request) => {
  console.group("Request Error");
  console.log("Reason:", `${error}`);
  console.log("Endpoint:", `${request.method} ${request.url}`);
  console.groupEnd();
});

const sdk = new Rails({ httpClient: httpClient });
```
<!-- End Custom HTTP Client [http-client] -->

<!-- Start Debugging [debug] -->
## Debugging

You can setup your SDK to emit debug logs for SDK requests and responses.

You can pass a logger that matches `console`'s interface as an SDK option.

> [!WARNING]
> Beware that debug logging will reveal secrets, like API tokens in headers, in log messages printed to a console or files. It's recommended to use this feature only during local development and not in production.

```typescript
import { Rails } from "@rails/sdk";

const sdk = new Rails({ debugLogger: console });
```

You can also enable a default debug logger by setting an environment variable `RAILS_DEBUG` to true.
<!-- End Debugging [debug] -->

<!-- Placeholder for Future Speakeasy SDK Sections -->

# Development

## Maturity

This SDK is in beta, and there may be breaking changes between versions without a major version update. Therefore, we recommend pinning usage
to a specific package version. This way, you can install the same version each time without breaking changes unless you are intentionally
looking for the latest version.

## Contributions

While we value open-source contributions to this SDK, this library is generated programmatically. Any manual changes added to internal files will be overwritten on the next generation. 
We look forward to hearing your feedback. Feel free to open a PR or an issue with a proof of concept and we'll do our best to include it in a future release. 

### SDK Created by [Speakeasy](https://www.speakeasy.com/?utm_source=rails&utm_campaign=typescript)
