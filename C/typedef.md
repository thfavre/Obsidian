# [[C]] typedef

## Concept :
Allow to redefine a name for a type of varibale
(Rename exxisting types)
It is a instruction (; at the end,...), it is a keyword

## Problematic :
```
int *a, b, c; // error!
int *a, *b, *c; // correct but annoying 
```

## Sytax :
>typedef type \* name;


## Example : 
```C:test.c
typedef int * int_p

void test(){
	int_p a, b, c;  // create a int * type
}

```

## Scope :
[[scope]]
Be ===carful=== with the scope, if define at a global level, it will be accessible in all the file.
If defined in a function, at the end of the function the variables will no longer exist any more

## With [[structure]] :
![[structure#With typedef]]

## With [[enumeration]] :
![[enumeration#With typedef]]

## Old notes :
Typedef :
		Definition :
			It allows to defined new types
		Sytax :
			typedef existingtype NEWTYPE;
		Example :
			typedef int NUMBER;  // define a NUMBER type
			NUMBER one = 1;
		-> Usefull when paired with enumerated and structures types
		Paired with enumerations :
			Example :
				typedef enum week {Monday, Tuesday, Wednesday, Thursday, Friday, Saturday Sunday} WEEKDAY;
				int main() {
				   WEEKDAY day = Monday;
			   	   if (day == monday) {printf("It's monday!");}}
			Inernally each item of the enum definition is paired to an integer (Monday is 0, Thuesday 1, ...)
		Paired with structures :
			Example :
				typedef struct {
 			 	   int age;
  				   char *name;
				} PERSON;
				PERSON flavio; flavio.age = 13;
				PERSON maria = {37, "Maria"}
				