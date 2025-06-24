- Only call `os.Exit` or `log.Fatal` in `main()`. Other functions should return errors.
- Prefer a single exit point in `main()`.
- Example:
  ```go
  func main() {
    if err := run(); err != nil { log.Fatal(err) }
  }
  func run() error { /* ... */ return nil }
  ```
