- Convert strings to byte slices once and reuse the result.
- Example:
  ```go
  data := []byte("Hello world")
  for i := 0; i < n; i++ { w.Write(data) }
  ```
