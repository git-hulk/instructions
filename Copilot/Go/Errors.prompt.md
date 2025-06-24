- Use `errors.New` for static errors, `fmt.Errorf` for dynamic errors, and custom types for matchable errors.
- Wrap errors with `%w` if callers should match the underlying error.
- Prefix exported error variables with `Err`, unexported with `err`. Suffix custom error types with `Error`.
- Handle errors only once; do not log and return the same error.
- Example:
  ```go
  var ErrCouldNotOpen = errors.New("could not open")
  type NotFoundError struct { File string }
  func (e *NotFoundError) Error() string { return fmt.Sprintf("file %q not found", e.File) }
  ```
