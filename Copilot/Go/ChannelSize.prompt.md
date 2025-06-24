- Use unbuffered channels or channels of size one. Larger sizes require strong justification.
- Example:
  ```go
  c := make(chan int, 1) // or
  c := make(chan int)    // unbuffered
  ```
