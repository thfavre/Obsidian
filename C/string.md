# [[C]] string

## Concept :
==A string is a group of octet that end with  \\0===
The size of a string is nb letters + 1

```C
char *str;  // pointer on a char
str = "test";

printf("%c %s", *str, str);  // t test
```

Vu qu'on met entre ", on le met dans les constantes (zone en memoire non inscriptibe)

>string are immutable!  Can't be chanegd with pointers
>Error if tried : zsh: bus error  

```C
char str[] = "test"  // tableau statique qui prend la taille quand on l'assigne (doit etre sur la meme ligne)
```
>ONLY in this case it can be changed with pointer

## Looping a string :
### Way nb 1
```C
char str[] = "test"
while (*str) {
	str++;  // on décale le pointeur vers la lettre suivante
...}

```
The end of a string is 0, so it will stop!
### Way nb 2
```C
char str[] = "test"
int n = 0;
while (*(str+n)) {
	n++;
...}
```
### Way nb 2
```C
char str[] = "test"
int n = 0;
while (str[n]) {
	n++;
...}
