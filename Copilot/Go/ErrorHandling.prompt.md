- Always check and handle errors from functions that return error information.
- When writing your own functions, return error messages as the second return value (a string).
- Example (No):
  ```lua
  local sock = ngx.socket.tcp()
  local ok = sock:connect("www.google.com", 80)
  ngx.say("successfully connected to google!")
  local function foo()
      local ok, err = func()
      if not ok then
          return false
      end
      return true
  end
  ```
- Example (Yes):
  ```lua
  local sock = ngx.socket.tcp()
  local ok, err = sock:connect("www.google.com", 80)
  if not ok then
      ngx.say("failed to connect to google: ", err)
      return
  end
  ngx.say("successfully connected to google!")

  local function foo()
      local ok, err = func()
      if not ok then
          return false, "failed to call func(): " .. err
      end
      return true
  end
  ```
