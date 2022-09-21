# [[C]] library
It is a [[preprocessor directive]]
\#include <...>	import file to the projet 

## Example : 
```C
#include <stdio.h>
println("Hello world");

#include <unistd.h>
write(1, "Grrr", 4);
```

## Create our own library :
- Mettre toutes nos fonctions qu'on utilise regulierement
- La possibilite de partager nos fonctions sans partager leur code source

### Procedure :
- Creer des .o a partir des .c  :
```Shell
gcc -c file1.c
```
- Creer le .a (mot lib obligatoire)
```Shell
ar rc libname.a file1.o
```

### Use :
```Shell
gcc main.c -L -lname
```

### Optimisation :
Si il y a bcp de fonctions dans la bibliotheque, gcc va aprendre bcp de temps de rechercher celle voulue..
-> creation d'un index (= un annuaire) :
```Shell
ranlib libname.a  
```

## Create with .sh file :
```sh
rm -f libft.a

find . -name "*.c" -type f -maxdepth 1 -exec gcc -Wall -Werror -Wextra -c {} \;

ar -rcs libft.a *.o

find . -name "*.o" -type f -maxdepth 1 -delete
```