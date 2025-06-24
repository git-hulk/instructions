- Place embedded types at the top of the struct, separated by an empty line. Only embed when it provides clear benefit.
- Do not embed mutexes. Do not embed types that expose implementation details or break zero-value usefulness.
- Example:
  ```go
  type Client struct {
    http.Client
    version int
  }
  ```
