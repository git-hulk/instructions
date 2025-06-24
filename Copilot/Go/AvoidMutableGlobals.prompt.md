- Avoid mutable global variables. Use dependency injection instead.
- Example:
  ```go
  type signer struct { now func() time.Time }
  func newSigner() *signer { return &signer{ now: time.Now } }
  ```
