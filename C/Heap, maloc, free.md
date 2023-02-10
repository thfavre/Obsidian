#C

## Heap :
partie de la mémoire basse 
aussi appelé le tas 
Contrairement a la stack on va pouvoir avoir un controle dessus
Dans la heap, on va devoir utiliser des fonctions pour demander de la memoire -> on va pour l'utiliser un peut partout dans le programme (contrairement a la stack)

## Example :
### Part 1 :
```C:main.c
int *get() {
	int *i;
	return (&i); // renvoie l'addresse qui se trouve actuellement sur la stack
}

int main(){
	int *ptr = get();
	*ptr = 12;
	printf("%d", *ptr); 
	}
```
**gcc -Wall -Wextra -Wall main.c && ./a.out :** 
Error : Tu essaie de renvoyer une addresse qui se trouve sur la stack  -> pas une tres bonne idee, normalement l'espace de memoire de i n'appartient plus a partir du moment ou on quitte get
**gcc main.c :**
Warning, mais ca marche et print 12
### Part 2 :
```C:main.c
int *get() {
	int i;
	return (&i); // renvoie l'addresse qui se trouve actuellement sur la stack
}

int *set() {
	int lol;
	lol = 78,
	return (0);}

int main(){
	int *ptr = get();
	*ptr = 12;
	printf("%d", *ptr);  // 12
	set();
	printf("%d", *ptr);  // 78
}
```
Warning, mais ca marche
en appelant get, la stack s'agrandit, et ptr recoit et ecrit 12 dans cette addresse.
En appelant set, ca réagranit la stack et au meme endroit que le i j'ai le lol avec la valuer 78, donc au meme endroit que pointe ptr

### Theory
Dans la mémoire, les addresses vont vers le haut
La stack descend 
Pas bien de retourner une addresse de la stack

## Heap : malloc
Le tas, pour demander de la mémoire au tas on utilise malloc
>void \*malloc(size_t, size); 
>size_t :
>size : taille en octet  

Renvoie un esspace en mémoire qui peut contenir n'importe quoi (void \*)

### Example :
```C
#include <stdlib.h>

int *get() {
	int *tab;
	tab = malloc(sizeof(*tab) * 9); //will allocated 9 momory "spot" (that are the size of a tab object)
	return (tab); // renvoie l'addresse qui se trouve actuellement sur la stack
}

int *set() {
	int lol;
	lol = 78,
	return (0);}

int main(){
	int *ptr = get();
	*ptr = 12;
	printf("%d", *ptr);  // 12
	set();
	printf("%d", *ptr);  // 12
}
```
Explication : J'ai demandé de la mémoire sur la heap, j'ai renvoyé cette addresse.
Que la stack aient changé ou pas, ma heap n'a pas été touché

## Healp : free
Dans la stack, la mémoire se liberait toute seul.
Dans la heap, il faut le faire nous meme.
>void free(void *ptr);

=> j'ai plus besion de cette espace, reprends le et fais en ce que tu veux

Le faire des qu'on a plus besion de cette mémoire!
===ATTENTION :=== 
```C
...

int main(){
	...
	printf("%p", ptr); // 0x7fe119c025e0
	free(ptr);
	printf("%p", ptr); // 0x7fe119c025e0
}
```
L'addresse que contient ptr NE CHANGE PAS, (free prend une copie de cette valeur d'addresse)
Mais on ne peut plus y aller (Si on retourne dans une maison qui ne nous appartient plus : probleme)
On ne devrait plus utiliser l'addresse pointé par ptr 
