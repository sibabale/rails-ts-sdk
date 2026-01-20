# AccountsTransferRequest

## Example Usage

```typescript
import { AccountsTransferRequest } from "@rails/sdk/models/operations";

let value: AccountsTransferRequest = {
  id: "92317f9d-9e9c-4223-9ede-f31485957cfe",
  transferRequest: {
    toAccountId: "7e82561e-7142-488f-bb2d-e726bf1da709",
    amount: "947.31",
  },
};
```

## Fields

| Field                                                     | Type                                                      | Required                                                  | Description                                               |
| --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| `id`                                                      | *string*                                                  | :heavy_check_mark:                                        | N/A                                                       |
| `transferRequest`                                         | [models.TransferRequest](../../models/transferrequest.md) | :heavy_check_mark:                                        | N/A                                                       |