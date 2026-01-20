# AccountsUpdateStatusResponse

## Example Usage

```typescript
import { AccountsUpdateStatusResponse } from "@rails/sdk/models/operations";

let value: AccountsUpdateStatusResponse = {
  headers: {
    "key": [
      "<value 1>",
    ],
    "key1": [
      "<value 1>",
      "<value 2>",
    ],
  },
  result: {
    id: "87dd9143-6965-45e1-afad-cb3dcd7f76e8",
    accountNumber: "<value>",
    accountType: "saving",
    environment: "<value>",
    userId: "444287a6-442c-48ba-b02e-70114fd561f5",
    balance: "<value>",
    currency: "Somoni",
    status: "active",
  },
};
```

## Fields

| Field                                     | Type                                      | Required                                  | Description                               |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| `headers`                                 | Record<string, *string*[]>                | :heavy_check_mark:                        | N/A                                       |
| `result`                                  | [models.Account](../../models/account.md) | :heavy_check_mark:                        | N/A                                       |