- Use `make()` for empty or programmatically populated maps. Use literals for fixed elements. Provide capacity hints if possible.
- Example:
  ```go
  m := make(map[string]int, 10)
  m := map[string]int{ "foo": 1, "bar": 2 }
  ```
