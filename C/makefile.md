# [[C]] makefile
## Concept :
Fichier qui permet d'organiser la compilation avec un ensemble de règles

## Example :
```Makefile
all:
	cc -o hello main.c fct.c
coucou:
	echo salut!
	echo bonjour!
```
## Explication :
- all et coucou sont des règles
- En appelant le fichier makefill, sans argument ca va prendre la premiere regle (make)
- On peut présiser la regle qu'on veut utiliser (p.ex : make coucou)
- A la premiere erreur dans une regle, ca s'arrete 

## Example :
```Makefile
SRCS = main.c fct.c

all:
	cc -o hello ${SRCS}
```
Ca va recompiler tous les fichier srcs a chaque fois, pas opti
-> on peut juste recompiler le fichier modifié et refaire le linkage

## Example :
```Makefile
SRCS = main.c fct.c

OBJS = ${SRCS:.c=.o} 

hello:   ${OBJS}   
		cc -o hello ${OBJS}
```
Va complier les .c en .o SI besion (que si il a été modifié)
Au lieu de compiler les .c, on link les .o
