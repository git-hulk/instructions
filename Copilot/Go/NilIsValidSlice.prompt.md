- Return `nil` for empty slices. Use `len(s) == 0` to check for emptiness. The zero value of a slice is usable immediately.
- Example:
  ```go
  if x == "" { return nil }
  func isEmpty(s []string) bool { return len(s) == 0 }
  var nums []int
  ```
