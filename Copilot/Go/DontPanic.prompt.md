- Avoid panics in production code. Return errors instead. Only panic for truly unrecoverable situations.
- In tests, use `t.Fatal` or `t.FailNow` instead of panics.
- Example:
  ```go
  func run(args []string) error {
    if len(args) == 0 { return errors.New("an argument is required") }
    return nil
  }
  ```
