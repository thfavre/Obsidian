# [[C]] include

Source : https://www.youtube.com/watch?v=1VwZ4aI8rUk&list=PLVQYiy6xNUxxMI_GiGGb2hxMcd3IwNYRy&index=2

## Theorie :
C'est une commande du [[preprocessor directive]] -> fait avant la [[compilation]]

<> chercher dans les directives de base du compilateur 
"" chercher dans le repertoire actuel ou repectoire fourni dans les -i

Remplacer l'endroit des include avec les fichiers mentionner
Exemple :
```C:ftc.c
int fct(void) {
	return (42);}
```
```C:main.c
#include "fct.c"
int main() {
	int i = fct();
	return (0)}
```
Ca va copier le fichier fct.c a la place du include 

## .h
c'est .header, l'endroit ou ya les prototype de functions (et rarement des fonctions) afin de partager le prototype dans plusieurs fichiers
Les [[library]] sont des include!

### Example :
```C:main
#include "fct.h"
int main(){
	int i = fct()
}
```
```C
#include "fct.h"
int fct(void) {
	return (42);
}
```
```C:fct.h
#include "fct.h"
int fct(void);
```

### Correct way of creating a .h :
![[header file]]