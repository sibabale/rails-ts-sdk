# UsersCreateResponse

## Example Usage

```typescript
import { UsersCreateResponse } from "@rails/sdk/models/operations";

let value: UsersCreateResponse = {
  headers: {
    "key": [
      "<value 1>",
    ],
  },
  result: {
    userId: "b4b7a8d1-372a-4020-85dc-f4ce9cb0e757",
    status: "<value>",
  },
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `headers`                                                       | Record<string, *string*[]>                                      | :heavy_check_mark:                                              | N/A                                                             |
| `result`                                                        | [models.CreateUserResponse](../../models/createuserresponse.md) | :heavy_check_mark:                                              | N/A                                                             |