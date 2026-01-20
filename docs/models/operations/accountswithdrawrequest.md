# AccountsWithdrawRequest

## Example Usage

```typescript
import { AccountsWithdrawRequest } from "@rails/sdk/models/operations";

let value: AccountsWithdrawRequest = {
  id: "2d37f06a-36f1-4077-b2ff-052efa73848b",
  withdrawRequest: {
    amount: "559.64",
  },
};
```

## Fields

| Field                                                     | Type                                                      | Required                                                  | Description                                               |
| --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| `id`                                                      | *string*                                                  | :heavy_check_mark:                                        | N/A                                                       |
| `withdrawRequest`                                         | [models.WithdrawRequest](../../models/withdrawrequest.md) | :heavy_check_mark:                                        | N/A                                                       |