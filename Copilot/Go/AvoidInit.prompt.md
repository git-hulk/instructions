- Avoid `init()` functions. Prefer explicit initialization in `main()` or constructors.
- If unavoidable, ensure `init()` is deterministic, does not depend on global state, and avoids I/O.
- Example:
  ```go
  var _defaultFoo = defaultFoo()
  func defaultFoo() Foo { return Foo{ /* ... */ } }
  ```
