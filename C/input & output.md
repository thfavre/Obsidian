#C 

## Output / String formatting :
- "%d" || "%i" 	int
- "%u"	unsigned int
- "%ld"	long
- "%f"	float
- "%f"	double
- "%c"	char
- "%s"	strings
- "%p"	pointer		
### Example :
```C
printf("Blabla %d bla", nombreDeVies);
int myAge=43; printf("%p", &myAge);  // Outputs 0x7ffe5367e044
```

## Input :
### Syntax :
```C
#include <stdio.h>
scanf(variable_format, variabel_address)
```
```C
#include <unistd.h>
write(int fildes, const void *buf, size_t nbytes);
```

### Examples :
```C
#include <stdio.h>
int age; 
scanf("%d", &age);  
	
char name[20]; 
scanf("%s", name)  // no need of & with strings (because the string name is a pointer to the first character)
```
