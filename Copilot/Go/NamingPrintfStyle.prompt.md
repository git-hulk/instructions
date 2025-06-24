- Use standard `Printf`-style names or end with `f` so `go vet` can check format strings.
- Example:
  ```go
  func Wrapf(format string, args ...interface{}) string { return fmt.Sprintf(format, args...) }
  ```
