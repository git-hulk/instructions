- Always use the "comma ok" idiom for type assertions to avoid panics.
- Example:
  ```go
  t, ok := i.(string)
  if !ok {
    // handle the error gracefully
  }
  ```
