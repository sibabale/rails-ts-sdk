# Account

## Example Usage

```typescript
import { Account } from "@rails/sdk/models";

let value: Account = {
  id: "a42c386f-4eac-462c-a9ae-4ecd6b4332cb",
  accountNumber: "<value>",
  accountType: "checking",
  environment: "<value>",
  userId: "138ed376-539a-442f-940f-a346de4ede14",
  balance: "<value>",
  currency: "UAE Dirham",
  status: "active",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `accountNumber`                                                                               | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `accountType`                                                                                 | [models.AccountType](../models/accounttype.md)                                                | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `organizationId`                                                                              | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `environment`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `userId`                                                                                      | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `adminUserId`                                                                                 | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `userRole`                                                                                    | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `balance`                                                                                     | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `currency`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `status`                                                                                      | [models.AccountStatus](../models/accountstatus.md)                                            | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | N/A                                                                                           |