- Use `table.new` to pre-allocate tables when possible.
- Do not use `nil` in arrays; use `ngx.null` for null values.
- Example (No):
  ```lua
  local t = {}
  for i = 1, 100 do
    t[i] = i
  end
  local t = {1, 2, nil, 3}
  ```
- Example (Yes):
  ```lua
  local new_tab = require "table.new"
  local t = new_tab(100, 0)
  for i = 1, 100 do
    t[i] = i
  end
  local t = {1, 2, ngx.null, 3}
  ```
