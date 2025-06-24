- Declare format strings as `const` when used outside string literals.
- Example:
  ```go
  const msg = "unexpected values %v, %v\n"
  fmt.Printf(msg, 1, 2)
  ```
