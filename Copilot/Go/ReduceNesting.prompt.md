- Return early to reduce code nesting. Handle error/special cases first.
- Example:
  ```go
  for _, v := range data {
    if v.F1 != 1 { log.Printf("Invalid v: %v", v); continue }
    v = process(v)
    if err := v.Call(); err != nil { return err }
    v.Send()
  }
  ```
