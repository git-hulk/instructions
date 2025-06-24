- Limit each line to 80 characters. If exceeded, wrap and align for readability.
- When breaking function calls, align parameters under the opening parenthesis.
- For string concatenation, place `..` at the start of the new line.
- Example (No):
  ```lua
  return limit_conn_new("plugin-limit-conn", conf.conn, conf.burst, conf.default_conn_delay)
  return limit_conn_new("plugin-limit-conn" ..  "plugin-limit-conn" .. "plugin-limit-conn")
  ```
- Example (Yes):
  ```lua
  return limit_conn_new("plugin-limit-conn", conf.conn, conf.burst,
                       conf.default_conn_delay)
  return limit_conn_new("plugin-limit-conn" .. "plugin-limit-conn"
                       .. "plugin-limit-conn")
  ```
