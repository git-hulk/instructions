- Do not use Go built-in names (e.g., `error`, `string`) for variables, fields, or types.
- Example:
  ```go
  var errorMessage string // instead of error
  type Foo struct { err error; str string }
  ```
