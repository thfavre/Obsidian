# [[C]] array
Suject linked to [[pointer]]

## Concept :
```C
int tab[3]  // demande au programme d'allouer 3 int  sur la stack
```
tab est un pointeur sur int possedant l'adresse du premier int

```C
int tab[3];
tab[0] = 42;
printf("%d", *tab);  // 42
```

```C
int tab[3];
tab[1] = 777;
printf("%d", *(tab+1));  // 777
```
```C
tab[1] == *(tab + 1)
tab[n] == *(tab +n)
```



## String
 ![[string]]

## Old notes :
Arrays : 
		Concept :
			-The size of an array can not change after his creation
			-Every value should be of the same type
			-The variable name of an array is a pointer to the first element of the array
		Creation : 
			-int myNumbers[] = {25, 50, 75, 100}
			-int myNumber[4]; myNumber[0] = 1; ...
		Loop through an array :
			int myNumbers[] = {25, 50, 75, 100};
			for (int i = 0; i < 4; i++) { printf("%d\n", myNumbers[i]); }
		Strings : 
			Example :
				char greetings[] = "Hello World!";
				greetings[0] = 'J';
				printf("%s", greetings); // Outputs Jello World!
				printf("%lu", sizeof(greetings));   // Outputs 13 (the \0 count!)
			Example : 
				char greetings[] = {'H', 'e', 'l', 'l', 'o', ' ', 'W', 'o', 'r', 'l', 'd', '!', '\0'};
				//  The \0 is known as the "null termininating character", and must be included when creating strings using this method. It tells C that this is the end of the string.
				printf("%lu", sizeof(greetings));   // Outputs 13 (the \0 count!)
			Library : 
				#include <string.h>
					-strcpy()	-strcat()	-strcmp()
					-strncmp()	-strlen()	...