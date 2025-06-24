- Use non-pointer `sync.Mutex` or `sync.RWMutex` fields in structs. The zero value is valid.
- Do not embed mutexes in structs, even if unexported.
- Example:
  ```go
  type SMap struct {
    mu sync.Mutex
    data map[string]string
  }
  ```
