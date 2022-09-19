# [[C]] preprocessor define
Commence avec \# c'est donc [[C/#preprocessor directive]]  -> executer avant la compilation
Sert a definir une variable puis a la remplacer
===Remplacement par text===!

cpp : permet de voir le resultat final de la precompilation

## Sytaxe :
```C
#define XX YY
```

Ca va remplacer tous les mots  XX du fichier par YY

## Examples :
```C:main
#define LOL "hehe"
int main() {
	printf(LOL); // hehe
}
```
Tous les LOL serront rempalcé par hehe


```c:main
#define LOL f("hehe")
int main() {
	printLOL; // hehe
} 
```

```c:main
#define LOL(x) "lol %d", x

int main() {
	printf(LOL(42)); // hehe 42
} 
```
cpp main.c
```C
...
	printf("hehe %d", 42);
```
### ABS :
```C
# define ABS(value) (value < 0 ? -value : value)
```

## Create from terminal :
Example to change the LOL to "grrr" -> -D...
```shell
gcc -DLOL=grr
```

### TESt
