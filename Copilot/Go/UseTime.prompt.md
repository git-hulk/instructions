- Use `time.Time` for instants and `time.Duration` for periods.
- Prefer `time.Time` and `time.Duration` in APIs and external systems when possible.
- Use RFC3339 for time strings if needed.
- Example:
  ```go
  func isActive(now, start, stop time.Time) bool {
    return (start.Before(now) || start.Equal(now)) && now.Before(stop)
  }
  func poll(delay time.Duration) {
    for { time.Sleep(delay) }
  }
  ```
