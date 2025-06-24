- Minimize the scope of variables and constants. Prefer short-lived variables. Only make constants global if used in multiple places or as part of a contract.
- Example:
  ```go
  if err := os.WriteFile(name, data, 0644); err != nil { return err }
  ```
