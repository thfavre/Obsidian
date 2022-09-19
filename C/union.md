# [[C]] union

## Concept :
Pareil que struc mais on va utiliser le meme espace memoire pour toutes les variables!
->stocke au meme endroit en mémoire mais le lit de maniere differente
### Similitary with [[structure]] :
#### Use :
Utiliser ===exactement=== comme le struct (c.f  [[union#Example with typedef]])

#### Same sytax :
##### Struct :
```C
struct name
{
	type n1;
	type n2;
} name2;

```
##### Union :
```C
union name
{
	type n1;
	type n2;
} name2;

```

### Difference with [[structure]] :
#### Size :
##### Struct :
Struct assemblait ensmble les differents types (par ex. avec un struc utilistant 2 ints et un int \*,  ca fera 4+4+8=16bytes)
##### Union :
Va reserver un espace pour le plus grand et ensuite on va d


## Example with [[typedef]]:
```C 
typedef union test
{
	int i;
	char c[4];
	gloat f;
} ttttest;

	int main(){
	ttttest p;
	p.i = 12
	printf("%d", p.i); //12
	p.f = 1.4
	printf("%d", p.i); //nbr random (car c'est desormais la valeur du float qui est en mémoire)
	printf("%f", p.f); //1.4
	
	printf("%d", sizeof(f)); // 4 (taille du plus grand type)
	}
```
Ca utilise le meme espace memoire pour toutes les variables!


## Size :
Taille du plus grand type de l'union
