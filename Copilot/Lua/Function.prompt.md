- Use `snake_case` for function names.
- Return as early as possible in functions.
- Example (No):
  ```lua
  local function testNginx() end
  local function check(age, name)
    local ret = true
    if age < 20 then
        ret = false
    end
    if name == "a" then
        ret = false
    end
    return ret
  end
  ```
- Example (Yes):
  ```lua
  local function test_nginx() end
  local function check(age, name)
    if age < 20 then
      return false
    end
    return name == "a" 
  end
  ```
