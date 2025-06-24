- Use `defer` to release resources (files, locks) for better readability and reliability.
- Example:
  ```go
  p.Lock()
  defer p.Unlock()
  if p.count < 10 { return p.count }
  p.count++
  return p.count
  ```
