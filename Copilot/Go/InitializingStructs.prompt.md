- Use field names when initializing structs. Omit zero-value fields unless meaningful. Use `var` for zero-value structs. Use `&T{}` for struct pointers.
- Example:
  ```go
  user := User{FirstName: "John", LastName: "Doe"}
  var user User
  sptr := &T{Name: "bar"}
  ```
