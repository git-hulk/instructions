- Start enums at 1 (not 0) unless zero is a meaningful default.
- Example:
  ```go
  type Operation int
  const (
    Add Operation = iota + 1
    Subtract
    Multiply
  )
  ```
