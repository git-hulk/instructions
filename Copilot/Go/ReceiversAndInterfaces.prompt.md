- Use value receivers if the method does not modify the receiver.
- Use pointer receivers if the method modifies the receiver or to avoid copying large structs.
- Methods with value receivers can be called on both values and pointers; pointer receivers only on pointers.
- Example:
  ```go
  type S struct { data string }
  func (s S) Read() string { return s.data }
  func (s *S) Write(str string) { s.data = str }
  ```
