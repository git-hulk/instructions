- Always use local variables, not globals.
- Use `snake_case` for variable names.
- Use ALL_CAPS for constants.
- Example (No):
  ```lua
  i = 1
  local IndexArr = 1
  local max_int = 65535
  ```
- Example (Yes):
  ```lua
  local i = 1
  local index_arr = 1
  local MAX_INT = 65535
  ```
