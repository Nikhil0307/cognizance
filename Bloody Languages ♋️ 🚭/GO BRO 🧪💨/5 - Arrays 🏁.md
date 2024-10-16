In GO array is a sequence of elements of specific length (just as in java)

>array can be created without initialization, where consider creating an int array of size 5 , makes all the values to the default int value of 0. example below
```
var arr [5]int // [0,0,0,0,0]
```

To set value we can use :: `array[index]= value` 

-> We can utiulize the built in len function to get the length of the array `len(arr)`

We can declare an initialize array is one line as below 
```
arr := [5]int{1,2,3,4,5}
```

With the above , we can also make the comipler itself to count the number of elements in it, iof we create as below
```
arr := [...] int{1,2,3,4,5}
```

We can create multi-dimentional array as below
```
var twoD [2][3]int
for i := 0; i < 2;i++{
	for j:=0;j<3;j++{
		twoD[i][j] = i+j
	}
}
```

