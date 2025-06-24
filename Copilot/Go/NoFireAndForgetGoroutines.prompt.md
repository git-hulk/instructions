### Don't fire-and-forget goroutines
- Always provide a way to stop and wait for goroutines. Do not leak goroutines.
- Do not start goroutines in `init()`.
- Example:
  ```go
  done := make(chan struct{})
  go func() { defer close(done); /* ... */ }()
  <-done // wait for goroutine to finish
  ```
