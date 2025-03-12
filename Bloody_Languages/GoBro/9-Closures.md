***Closures can also be said as anonymous functions, where anonymous functions are useful when we need to define a function inline without having to name it.***

```
package main
import "fmt"

func intSeq() func() int {
    i := 0
    return func() int {
        i++
        return i
    }
}

func main() {
    nextInt := intSeq()
    fmt.Println(nextInt())
    fmt.Println(nextInt())
    fmt.Println(nextInt())
    newInts := intSeq()
    fmt.Println(newInts())
}

# outputs
1
2
3
1
```