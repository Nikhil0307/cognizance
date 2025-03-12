***GO structs are typed collection of fields.***
```
type person struct{
	name string
	age int
}
```

As Go is garbage collected language , we can even return a pointer to a local variable as it will be cleaned by the garbage collector only if there are no active references to it. 🗑️

***GO supports Methods defined on struct types.***
Methods can be either defined for pointers or value as receiver (input to function) type
>BUT HOW ???🤔💭
- GO automatically handles the conversion between values and pointers for method calls.

```
package main
import "fmt"

type rect struct {
    width, height int
}
func (r *rect) area() int {
    return r.width * r.height
}

func (r rect) perim() int {
    return 2*r.width + 2*r.height
}

func main() {
    r := rect{width: 10, height: 5}

    fmt.Println("area: ", r.area())
    fmt.Println("perim:", r.perim())

    rp := &r
    fmt.Println("area: ", rp.area())
    fmt.Println("perim:", rp.perim())
}
```

Added an good goofy example above 🤪

We are calling the same methods twice , once with values and once with pointers ... jeeezz theyy workk perfectly well as said above 🔥

