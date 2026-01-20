# UsersCreateRequest

## Example Usage

```typescript
import { UsersCreateRequest } from "@rails/sdk/models/operations";

let value: UsersCreateRequest = {
  xEnvironment: "production",
  createUserRequest: {
    firstName: "Valerie",
    lastName: "Kling-Dibbert",
    email: "Alyson_Ledner@gmail.com",
    password: "CyqxLWEHjyJH8Zn",
  },
};
```

## Fields

| Field                                                         | Type                                                          | Required                                                      | Description                                                   |
| ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- |
| `xEnvironment`                                                | [models.XEnvironment](../../models/xenvironment.md)           | :heavy_check_mark:                                            | N/A                                                           |
| `createUserRequest`                                           | [models.CreateUserRequest](../../models/createuserrequest.md) | :heavy_check_mark:                                            | N/A                                                           |