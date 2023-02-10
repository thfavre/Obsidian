#C

## Sytax : 

```C
returnType functionName(parameter1, parameter2) // declaration
{ 
		... // definition 
		}
functionName(argument1, argument2) // call the function
```
## Concept : 
- Not possible to return more than one value from a function
- Parameters are passed by copy. (modifing a parameter will not change is value globaly)
- When a parameter is a pointer, it will modify the variable value (because we are now accecing its memory address)
- We can't define a default value for a parameter
- The function must be define before calling it (look Good Practice)

## Good Practice :
```C
int myFunction(int, int);  // Function declaration (prototype)
int main() { myFunction(1, 2); }
int myFunction(int x, int y) { return x + y }  // Function definition
```

## Main : 
`int main(int argc, char *argv[]) { ... }`
 is the same as :
`int main(){ ... }`
### argc
arguments counts, it is the number of arguments 
ex : `./a.out test1 test2` -> argc will be 3 (the first one is ALWAYS the program name)
### argv 
arguments values
ex : `./a.out test1 test2` -> `argv[0]` will be `"a.out"`, `argv[1]` will be `"test1"`,...

## Return type :
integer : int, 	floating point : float,	const char * : string,	...

## Returning void*
![[pointer#Void pointers]]

