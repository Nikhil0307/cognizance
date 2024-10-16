Go String is a read-only bytes. 
In other languages, Strings are made of "characters".  *But in Go the concept of character is called as **rune*** -> `An integer that represents a unicode code point`

looping through a string we get unicode or hexa value or value based on the string formating of fmt

To get the size of the string we need to count the number of runes in the string 
consider we have string "Hello" where 'h' 'e' 'l' 'l' 'o' -> making it rune literals (Characters with single coats are known to be string literals)
To get the rune i.e characters we can make use of range function as used in the code added to end.

```
package main

  

import (
	"fmt"
	"unicode/utf8"
)

func main() {

	const s = "nikhil"
	
	fmt.Println("Len:", len(s))
	
	for i := 0; i < len(s); i++ {
		fmt.Printf("%x ", s[i]
	}
	
	fmt.Println()
	fmt.Println("Rune count:", utf8.RuneCountInString(s))
	
	for _, chars := range s {
		fmt.Printf("%c ", chars)
	}

}
```
 
 Cool!!! 😎
 