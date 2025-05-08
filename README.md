**Provide an example of using union and intersection types in TypeScript.**
TypeScript provides powerful ways to compose types using `union` (|) and `intersection` (&) operators. These features help you write safer and more flexible code.
## 📌 Union Types (|)
Union types allow a value to be one of many types.

```ts
function processValue(value: string | number): number {
    if (typeof value === "string") {
      return value.length;
    } else {
      return value * 2;
    }
  }
  ```

  ## 🧩 Intersection Types (&)

  Intersection types combine multiple types into one. The resulting type has all the properties of the combined types.
```ts
  type User = { name: string };
type Admin = { role: "admin" };

type AdminUser = User & Admin;

const admin: AdminUser = {
  name: "Alice",
  role: "admin"
};
```
