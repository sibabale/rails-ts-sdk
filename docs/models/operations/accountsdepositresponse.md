# AccountsDepositResponse

## Example Usage

```typescript
import { AccountsDepositResponse } from "@rails/sdk/models/operations";

let value: AccountsDepositResponse = {
  headers: {},
  result: {
    account: {
      id: "f1da2913-2f9a-4882-8e99-a8ba3ee4f972",
      accountNumber: "<value>",
      accountType: "checking",
      environment: "<value>",
      userId: "43d934dd-1671-4833-8e37-b56c5b6b7ad5",
      balance: "<value>",
      currency: "Euro",
      status: "suspended",
    },
    transaction: {
      id: "a88a70bb-d5d6-4c13-a076-77608f57b31b",
      accountId: "68d77b73-9cbc-4f25-91a0-be1e37e35da0",
      transactionType: "savings_withdraw",
      amount: "590.36",
      currency: "Singapore Dollar",
      balanceAfter: "<value>",
      status: "cancelled",
      createdAt: new Date("2026-06-18T02:34:52.052Z"),
      updatedAt: new Date("2026-03-25T01:26:36.799Z"),
    },
  },
};
```

## Fields

| Field                                                                       | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `headers`                                                                   | Record<string, *string*[]>                                                  | :heavy_check_mark:                                                          | N/A                                                                         |
| `result`                                                                    | [models.AccountTransactionResult](../../models/accounttransactionresult.md) | :heavy_check_mark:                                                          | N/A                                                                         |