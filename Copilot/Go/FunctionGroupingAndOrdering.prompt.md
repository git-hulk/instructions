- Group functions by receiver and order them by call hierarchy. Exported functions should appear first after type/const/var definitions.
- Example:
  ```go
  type something struct{ ... }
  func newSomething() *something { return &something{} }
  func (s *something) Cost() { return calcCost(s.weights) }
  func (s *something) Stop() { ... }
  func calcCost(n []int) int { ... }
  ```
