The **`for`** loop is the only loop construct in Go, but it can be used in various ways. 🤑

**Basic for loop**

```
func main() { 
    for i := 0; i < 5; i++ {
        fmt.Println(i) // Output: 0 1 2 3 4
    }
}
```

**For loop as a *WHILE loop***

```
func main() {
    x := 0
    for x < 5 {
        fmt.Println(x) // Output: 0 1 2 3 4
        x++
    }
}
```

**Infinte loop**

```
for { 
	fmt.Println("Running infinitely...") 
	break // Break used to prevent infinite execution 
}
```

**for loop with range**

```
func main() {    
    nums := []int{10, 20, 30}
    for index, value := range nums {
        fmt.Printf("Index: %d, Value: %d\n", index, value)
        // Output:
        // Index: 0, Value: 10
        // Index: 1, Value: 20
        // Index: 2, Value: 30
    }
}
```
