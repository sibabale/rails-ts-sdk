# Transaction

## Example Usage

```typescript
import { Transaction } from "@rails/sdk/models";

let value: Transaction = {
  id: "4d2415c0-d4dc-4e16-85d1-4059c3bceb2e",
  accountId: "e9a78ca2-aff8-4bad-96bb-c6bed3288699",
  transactionType: "withdrawal",
  amount: "466.46",
  currency: "Libyan Dinar",
  balanceAfter: "<value>",
  status: "completed",
  createdAt: new Date("2026-09-09T21:01:30.448Z"),
  updatedAt: new Date("2026-12-15T13:59:00.087Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `accountId`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `transactionType`                                                                             | [models.TransactionType](../models/transactiontype.md)                                        | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `amount`                                                                                      | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `currency`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `balanceAfter`                                                                                | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `recipientAccountId`                                                                          | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `externalRecipientId`                                                                         | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `referenceId`                                                                                 | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `description`                                                                                 | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `status`                                                                                      | [models.TransactionStatus](../models/transactionstatus.md)                                    | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |