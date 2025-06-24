- Use table-driven tests for repetitive test logic. Avoid complex branching in table tests. Use `tests` for the table and `tt` for each case.
- For parallel tests, rebind loop variables inside the loop.
- Example:
  ```go
  tests := []struct{ give string; want int }{ {give: "a", want: 1}, {give: "b", want: 2} }
  for _, tt := range tests { t.Run(tt.give, func(t *testing.T) { t.Parallel(); /* ... */ }) }
  ```
