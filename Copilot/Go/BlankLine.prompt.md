- Do not use semicolons at the end of lines.
- Do not compress multiple statements into one line; use one statement per line.
- Separate functions with two blank lines.
- Separate `if`/`elseif` branches with a blank line.
- Example (No):
  ```lua
  if a then ngx.say("hello") end
  local function foo() end
  local function bar() end
  if a == 1 then
      foo()
  elseif a== 2 then
      bar()
  end;
  ```
- Example (Yes):
  ```lua
  if a then
      ngx.say("hello")
  end

  local function foo()
  end

  local function bar()
  end

  if a == 1 then
      foo()

  elseif a== 2 then
      bar()
  end
  ```
