- Always specify field tags for struct fields that are marshaled (e.g., JSON, YAML).
- Example:
  ```go
  type Stock struct {
    Price int `json:"price"`
    Name  string `json:"name"`
  }
  ```
