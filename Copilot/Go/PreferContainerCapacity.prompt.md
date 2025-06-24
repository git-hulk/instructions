- Provide capacity hints when creating slices and maps with `make()`.
- Example for maps:
  ```go
  files, _ := os.ReadDir("./files")
  m := make(map[string]os.DirEntry, len(files))
  for _, f := range files { m[f.Name()] = f }
  ```
- Example for slices:
  ```go
  data := make([]int, 0, size)
  for k := 0; k < size; k++ { data = append(data, k) }
  ```
