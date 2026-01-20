# TransferResult

## Example Usage

```typescript
import { TransferResult } from "@rails/sdk/models";

let value: TransferResult = {
  fromAccount: {
    id: "c025648a-f46c-4193-8dcb-4a2ba4749abe",
    accountNumber: "<value>",
    accountType: "checking",
    environment: "<value>",
    userId: "9a13a108-62b9-422a-8cdd-100131821937",
    balance: "<value>",
    currency: "Serbian Dinar",
    status: "closed",
  },
  toAccount: {
    id: "7e0226de-b119-46e4-a05d-fbdf07982c85",
    accountNumber: "<value>",
    accountType: "checking",
    environment: "<value>",
    userId: "23800d3a-332f-41b3-9938-dc7c1169b5c5",
    balance: "<value>",
    currency: "UAE Dirham",
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
};
```

## Fields

| Field                                          | Type                                           | Required                                       | Description                                    |
| ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- |
| `fromAccount`                                  | [models.Account](../models/account.md)         | :heavy_check_mark:                             | N/A                                            |
| `toAccount`                                    | [models.Account](../models/account.md)         | :heavy_check_mark:                             | N/A                                            |
| `transaction`                                  | [models.Transaction](../models/transaction.md) | :heavy_check_mark:                             | N/A                                            |