
*Which part of the .go file executes at first ?*
>*function with name as *main* should be defined which will be called as package name on top of the file 😪*


*But why package name should be main not something else ?*
>*There are specific rules to be followed w.r.t package name & structure of the code!!*
- *Main function is the entry point of Go program, making it every Go program must have a main function within the main package*

*Waittttt!!! What happens if some other package name is being used instead of main? 🤯*
- *Program becomes un-executable bro !!😏*

***Okayyy funss apart 🫡 🤫 [Drains up]***

>*I'm using a package name other than main, Go compiler gets to treat my program as a part of library and not as an executable program .... (shhhhh, Go have lost it's chill mann)*
>*So, my custom package(!= main) can be imported and used by others but wouldn't produce an executable*



