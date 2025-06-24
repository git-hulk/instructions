- Do not concatenate strings in a loop on hot code paths.
- Use a table to collect strings, then concatenate with `table.concat`.
- Example (No):
  ```lua
  local s = ""
  for i = 1, 100000 do
      s = s .. "a"
  end
  ```
- Example (Yes):
  ```lua
  local t = {}
  for i = 1, 100000 do
      t[i] = "a"
  end
  local s = table.concat(t, "")
  ```
