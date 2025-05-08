**TypeScript improves code quality and project maintainability in several key ways:**

TypeScript significantly enhances code quality and project maintainability by introducing static typing to JavaScript. With TypeScript, many common errors—such as passing the wrong type of data to a function—are caught at compile time rather than at **runtime**, reducing the chance of bugs making it into production.
* TypeScript catches errors at compile time, not run time.
* Better Code Completion and IntelliSense (Auto-completion,Method suggestions,Parameter hints)
* TypeScript understands your code structure. When renaming or moving **functions**, **variables**, or **files**


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
