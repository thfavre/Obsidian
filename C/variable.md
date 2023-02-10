#C 

## Types Size :
### Integer variable:
#### signed char : 
-128 to 127 // char j = 127; j = j + 10; // j will be a random value (because it is a signed type)
unsigned char : 0 to 255  //
##### unsigned char
j = 255; j = j + 10; // j will = 9, (because it is an unsigned type)

#### int :
-32'767 to 32'767
##### unsigned int : 
0 to 65'535

#### long :
-2'147'483'647 to 2'147'483'647
##### unsigned long : 
0 to 4'294'967'295


## Declaration : 
===There is no default value  !===
```C
int foo;
int foo1, foo2, foo3;
int foo1 = 1, foo2 = 2;
```

## Scope :
### Local variables :
- It is a variable defined inside a function
-> Will only be accessible in the function, when the function ends they stop their existence (=freed (=cleared from memory (some exceptions))) because they are declared on the stack (unless we explicitly allocate them on the heap using pointers (we have to manage memory ourself))

### Global variables :
-It is a variable defined outside a function
-> Will be accessible from any function of the program 
-> Can be read and update by any function
-Are static by default -> initialized to 0

## ![[static variable]]
## Constant :
If there is no need to motify the variable -> [[constant|constants]]












