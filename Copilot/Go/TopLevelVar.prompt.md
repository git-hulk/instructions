- Use `var` for top-level variables. Specify type only if it differs from the initializer.
- Example:
  ```go
  var _s = F()
  func F() string { return "A" }
  ```
