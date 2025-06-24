- Use comments or custom types for function parameters when their meaning is not obvious. Prefer custom types for booleans or enums.
- Example:
  ```go
  printInfo("foo", true /* isLocal */, true /* done */)
  ```
