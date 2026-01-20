# CreateAccountRequest

## Example Usage

```typescript
import { CreateAccountRequest } from "@rails/sdk/models";

let value: CreateAccountRequest = {
  accountType: "saving",
  userId: "851c4bea-acfe-4011-af6c-bd7a46a570da",
};
```

## Fields

| Field                                          | Type                                           | Required                                       | Description                                    |
| ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- |
| `accountType`                                  | [models.AccountType](../models/accounttype.md) | :heavy_check_mark:                             | N/A                                            |
| `organizationId`                               | *string*                                       | :heavy_minus_sign:                             | N/A                                            |
| `environment`                                  | *string*                                       | :heavy_minus_sign:                             | N/A                                            |
| `userId`                                       | *string*                                       | :heavy_check_mark:                             | N/A                                            |
| `currency`                                     | *string*                                       | :heavy_minus_sign:                             | N/A                                            |