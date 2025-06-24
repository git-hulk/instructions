- Do not embed types in public structs. Use explicit fields and delegate methods instead.
- Example:
  ```go
  type ConcreteList struct { list *AbstractList }
  func (l *ConcreteList) Add(e Entity) { l.list.Add(e) }
  ```
