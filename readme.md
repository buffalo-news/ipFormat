[![GoDoc](https://godoc.org/github.com/buffalo-news/ipFormat?status.svg)](https://godoc.org/github.com/buffalo-news/ipFormat)

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
	ip1, _ := ipFormat.New("192.168.0.2/24")
	ip2, _ := ipFormat.New("192.168.0.6")

	ip1, _ = ip1.ToV6()
	ip2, _ = ip2.ToV6()

	fmt.Println(ip1.Address)
	fmt.Println(ip1.CIDR)
	fmt.Println(ip2.Address)
}
```