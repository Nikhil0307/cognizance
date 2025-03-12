Just like other languages GO has if, switch, for and so on 

**If else-if else statement example**
```
func main() {
    x := 7

    // if-else if-else chain
    if x > 10 {
        fmt.Println("x is greater than 10")
    } else if x > 5 {
        fmt.Println("x is greater than 5") // Output: x is greater than 5
    } else {
        fmt.Println("x is 5 or less")
    }
}
```

**Switch statement can be either with a condition and without a condition**
```
switch with a condition 

func main() {
    day := 2
    switch day {
    case 1:
        fmt.Println("Monday")
    case 2:
        fmt.Println("Tuesday") // Output: Tuesday
    default:
        fmt.Println("Another day")
    }
}

Switch without a condition 

func main() {
    x := 20    
    switch {
    case x < 10:
        fmt.Println("x is less than 10")
    case x < 20:
        fmt.Println("x is less than 20")
    default:
        fmt.Println("x is 20 or more") // Output: x is 20 or more
    }
}
```
