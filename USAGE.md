<!-- Start SDK Example Usage [usage] -->
```typescript
import { Rails } from "@rails/sdk";

const rails = new Rails({
  apiKeyAuth: process.env["RAILS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await rails.users.usersCreate("production", {
    firstName: "Alexanne",
    lastName: "Wehner",
    email: "Myah_Veum19@yahoo.com",
    password: "TXz5lHn_rozuDSn",
  });

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->