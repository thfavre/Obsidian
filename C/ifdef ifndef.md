#C 

It is a [[preprocessor directive]]
## \#ifdef :
pour savoir si ca a ete define
pareil que if defined ([[if else elif endif if defined]])

## \#ifndef
pur savoir si ca n'a pas ete define

## Usecase :
Add the -DDEBUG to the gcc to add the needed debug code

## Example :
```C:main.c
int main()
{
#ifndef TEST1
	printf("test is defined");
#else
	printf("test is not defined");
#endif
}
```

## Protect .h :
### Problematic : 
Si un .h inclu un autre .h etc., il y a un risque d'avoir l'import 2 fois -> erreur 
(ou par exemple si mon .h est aussi appelé dans plusieurs autres library...)
```C:main.c
#include fct.h
#include fct.h
```
-> error
### Solution :
Dans le .h :
```C:fct.h
#ifndef __FCT_H__
#define __FCT_H__

int gl_pouet = 12;

#endif
```
Comme ca, si \#include "fct.h" est appelé deux fois, ce code va etre inclu deux fois mais au deuxieme \#include, au \#ifndef, \_\_FCT\_H\_\_ serra deja define -> le int sera donc pas redefin
touch 