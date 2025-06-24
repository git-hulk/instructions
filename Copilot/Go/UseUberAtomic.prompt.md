- Use `go.uber.org/atomic` for atomic operations instead of `sync/atomic` for type safety.
- Example:
  ```go
  type foo struct { running atomic.Bool }
  func (f *foo) start() { if f.running.Swap(true) { return } }
  func (f *foo) isRunning() bool { return f.running.Load() }
  ```
