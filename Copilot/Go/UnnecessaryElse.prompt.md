- Remove unnecessary `else` blocks when the `if` branch returns or exits.
- Example:
  ```go
  a := 10
  if b { a = 100 }
  ```
