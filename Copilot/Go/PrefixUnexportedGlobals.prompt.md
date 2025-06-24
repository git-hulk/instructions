- Prefix unexported top-level variables and constants with `_` (except errors).
- Example:
  ```go
  const (
    _defaultPort = 8080
    _defaultUser = "user"
  )
  ```
