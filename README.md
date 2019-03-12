### flagvar
---
https://github.com/sgreben/flagvar

```go
import "github.com/sgreben/flagvar"

import "github.com/sgreben/flagvar/enum"

var enums flagvar.EnumsCSV


package main

import (
  "flag"
  "fmt"
  "github.com/sgreben/flagvar"
)

var (
  fruit = flagvar.Enum{Choises: []string{"apple", "banana"}}
  urls flagvar.URLs
  settings flagvar.Assignmetns
)

func main() {
  flag.Var(&fruit, "fruit", fmt.Sprintf("set a fruit (%s)", fruit.Help()))
  flag.Var(&urls, "url", "add a URL")
  flag.Var(&settings, "set", fmt.Sprintf("specify a setting (%s)", settings.Help()))
  flag.Parse()
}
```

```sh
go run main.go -set abc=xyz -url https://github.com
go run main.go -set abc=xyz -url ://github.com
go run main.go -fruit kiwi
go run main.go -h
```

```
```


