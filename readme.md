# Golang ip Formatting functions

All methods are fairly self explanatory, and reading the godoc page should
explain everything. If something isn't clear, open an issue or submit
a pull request.

## Example

First, ensure the library is installed and up to date by running
`go get -u github.com/buffalo-news/ipFormat`.

```go
package main

import (
	"fmt"

	"github.com/buffalo-news/ipFormat"
)

func main() {
	ip1 := ipFormat.New("192.168.0.2/24")
    ip2 := ipFormat.New("192.168.0.6")

    ip1 = ip1.ToV6()
    ip2 = ip2.ToV6()
    
    fmt.PrintLn(ip1.Address)
    fmt.PrintLn(ip1.CIDR)
    fmt.PrintLn(ip2.Address)
}
```