- Localize all required libraries and `ngx`.
- Example (No):
  ```lua
  local core = require("apisix.core")
  local timer_at = ngx.timer.at
  local function foo()
    local ok, err = timer_at(delay, handler)
  end
  ```
- Example (Yes):
  ```lua
  local ngx = ngx
  local require = require
  local core = require("apisix.core")
  local timer_at = ngx.timer.at
  local function foo()
    local ok, err = timer_at(delay, handler)
  end
  ```
