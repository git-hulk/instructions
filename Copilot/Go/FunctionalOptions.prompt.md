- Use the functional options pattern for optional arguments in constructors and APIs. Prefer interface-based options for flexibility and testability.
- Example:
  ```go
  type Option interface { apply(*options) }
  func WithCache(c bool) Option { return cacheOption(c) }
  func Open(addr string, opts ...Option) (*Connection, error) { /* ... */ }
  ```
