#C 

## Concept : 
Permet de definir un nouvea utype de variable,
definir des constantes ===entières=== (ca sera focrement des ints)

Ces constantes serront valable dans tout le [[scope]].
-> pas possible de creer deux fois le meme nom d'une cosntante dans deux enums differents

## Syntax :
```C
enum name
{
	val1,
	val2,
	val3,
	val4
};
```
de base val1 va valoir 0,
val2 va valoir 1, ...

### Change values :
```C
enum name
{
	val1 = 12, // val1 vaudra 12
	val2,      // val2 vaudra 13
	val3 = 20, // val3 vaudra 20
	val4,      // val4 vaudra 21
	val5 = 12  //val5 vaudra 12
};
```

## Examples :
```C:main.c
enum name
{
	val1,
	val2,
	val3,
	val4
};

int main(){
	printf("%d", val2); // 1
}
```

```C
enum color
{ 
    RED, 
    GREEN, 
    BLUE 
};

enum color chosenColor = RED;
```
See [[enumeration#With typedef]]


## With [[typedef]] :
```C 
typedef enum 
{ 
    RED, 
    GREEN, 
    BLUE 
} color;

color chosenColor = RED;
```




## Old notes :
Enumeration :
		Definition :
			Is a data type that consists of integral constantes.
		Syntax :
			-enum flag {const1, const2, ..., constN};  // By default const1 is 0, const2 1,...
			-enum flag(const1=5, const2=0};  // change default value
		Example : 
			enum week {Monday, Tuesday, Wednesday, Thursday, Friday, Saturday Sunday};  // add } WEEKDAY to create
			int main() {
			   enum week today = Wednesday;
			   printf("Day %d",today+1);}  // Day 3