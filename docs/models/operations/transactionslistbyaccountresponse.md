# TransactionsListByAccountResponse

## Example Usage

```typescript
import { TransactionsListByAccountResponse } from "@rails/sdk/models/operations";

let value: TransactionsListByAccountResponse = {
  headers: {
    "key": [
      "<value 1>",
      "<value 2>",
    ],
  },
  result: [
    {
      id: "fef452ef-cb61-4332-899b-d32f591c9ea9",
      accountId: "80ba8775-2288-4577-86ce-e60c5d14adc2",
      transactionType: "deposit",
      amount: "845.21",
      currency: "Saudi Riyal",
      balanceAfter: "<value>",
      status: "cancelled",
      createdAt: new Date("2024-11-25T21:34:40.940Z"),
      updatedAt: new Date("2024-09-27T17:36:36.356Z"),
    },
  ],
};
```

## Fields

| Field                                               | Type                                                | Required                                            | Description                                         |
| --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- |
| `headers`                                           | Record<string, *string*[]>                          | :heavy_check_mark:                                  | N/A                                                 |
| `result`                                            | [models.Transaction](../../models/transaction.md)[] | :heavy_check_mark:                                  | N/A                                                 |