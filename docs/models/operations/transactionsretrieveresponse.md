# TransactionsRetrieveResponse

## Example Usage

```typescript
import { TransactionsRetrieveResponse } from "@rails/sdk/models/operations";

let value: TransactionsRetrieveResponse = {
  headers: {},
  result: {
    id: "a745f626-b378-4e2c-afdc-1cf9207f4c3d",
    accountId: "b536231f-cfad-46bf-a211-48228223f984",
    transactionType: "savings_withdraw",
    amount: "998.31",
    currency: "Gourde",
    balanceAfter: "<value>",
    status: "failed",
    createdAt: new Date("2026-08-12T09:20:23.009Z"),
    updatedAt: new Date("2025-12-27T10:59:19.154Z"),
  },
};
```

## Fields

| Field                                             | Type                                              | Required                                          | Description                                       |
| ------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- |
| `headers`                                         | Record<string, *string*[]>                        | :heavy_check_mark:                                | N/A                                               |
| `result`                                          | [models.Transaction](../../models/transaction.md) | :heavy_check_mark:                                | N/A                                               |