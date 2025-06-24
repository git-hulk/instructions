- Copy slices and maps when receiving or returning them to avoid unintended sharing.
  - Example for receiving: 
    ```go
    func (d *Driver) SetTrips(trips []Trip) {
      d.trips = make([]Trip, len(trips))
      copy(d.trips, trips)
    }
    ```
  - Example for returning:
    ```go
    func (s *Stats) Snapshot() map[string]int {
      s.mu.Lock()
      defer s.mu.Unlock()
      result := make(map[string]int, len(s.counters))
      for k, v := range s.counters { result[k] = v }
      return result
    }
    ```
