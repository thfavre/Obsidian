# [[C]] pointer

## Concept :
A pointer have the adress of a variable
le compilateur a besion de savoir le type de variable ou se trouve le pointeur

## Creation
```C
int a;
int *ptr;  // le compilateur a besion de savoir le type de variable ou se trouve le pointeur

ptr = &a;
print("%p", ptr);  // 0x7fff5863b38, Reference : output the memory address
```

## Dereference :
- See what is at the pointer address (Access to the variable the pointer point to)
- Go see waht is at the address
- Modify the variable 
```C:ex
int myAge = 43;        // Variable declaration
int *ptr = &myAge;     // Pointer declaration

printf("%d\n", *ptr);  // Dereference : Output the value of myAge with the pointer (43)
```
```C:ex
int *ptr;
ptr = 43;
```

## Arithmetic :
- the int take 4 bytes (octets) 
- ptr + 1 go to the next ptr (so + 4 for int)
- the stack is going down
```C
int b;
int a;
int *ptr = &a;

printf("%p", ptr);  // x7fff5863b34
printf("%p", &b);  // x7fff5863b38
printf("%p", ptr + 1);  // x7fff5863b38  // it also point to b!

b = 23;
printf("%d", *(ptr + 1));
*(ptr + 1) = 77;  // b = 77;
```

## With strings :
See [[array]]
Creating a char array (=string), it will only create a pointer to the first char of the array. A char array allways end with a \\0.

## Null pointer :
```C
int *ptr;
ptr = 0;  // it is called a null pointer
```
It point to nothing, usefull to see if a pointer is used.
It is impossible to attriuate an other value than 0

## Pointer on function
For example it is possible  to make a array of functions
```C
int fct(char c)
{
	return 0;
}

int main()
{
	int (*ptr)(char); //ptr is a pointer on a fucntion that will return a int and take as parameter a char
	ptr = &fct; // it takes the address of fct
	(*ptr)('o');
}
```
We need the ( )
### Example :
```C
void	ft_foreach(int *tab, int length, void(*f)(int)) {
	int	i = 0;
	while (i < length)
		f(tab[i++]);
}

void add3AndPrint(int i) {   printf(" %d ", i + 3);   }

int main() {
	int tab[] = {1, 2, 3, 10};
	ft_foreach(tab, 4, &add3AndPrint); // print 4 5 6 14
}
```


## Old notes :
Pointers * :
		Concept :
			-A pointer is the address of a block of memory that contains a variable
			-We can use the & operator to get the value of the address in memory of a variable : 
				int age=37; printf("%p", &age);  // 0x7ffeef7dcb9c
			-We can asign the address to a variable : 
				int *address = &age;  // declaration of a pointer to an integer variable
			-We can use the pointer operator (*) to get the value of the variable the address is pointing to : 
				int age=37;
				int *address = &age;
				printf("%u", *address);  // 37 
		Arrays :
			The variable name of an array is a pointer to the first element of the array
			Example :
				int prices[3] = {5, 4, 3}; 
				printf("%u", *prices);  // 5
				printf("%u", *(prices + 1));  // 4
		SAME CONCEPT :
		Creation : 
			Example :
				int myAge = 43;          // &myAge is called a pointer 
				int *ptr = &myAge;       // A pointer variable, with the name ptr, that stores the address of myAge
				printf("%d\n", myAge);   // Output the value of myAge (43)
				printf("%p\n", &myAge);  // Output the memory address of myAge (0x7ffe5367e044)
				printf("%p\n", ptr);     // Output the memory address of myAge with the pointer (0x7ffe5367e044)
			Ex :
				test(*a);	
				// dans main :
				int a = 2;
				test(&2)
			
Dereference : 
			To get the value of the variable the pointer points, use the * operator (dereference operator)
			Example : 
				int myAge = 43;        // Variable declaration
				int *ptr = &myAge;     // Pointer declaration
				printf("%p\n", ptr);   // Reference: Output the memory address of myAge with the pointer (0x7ffe5367e044)
				printf("%d\n", *ptr);  // Dereference: Output the value of myAge with the pointer (43)
			Example : 
				int prices[3] = { 5, 4, 3 };
				printf("%u", *prices);  //5
				printf("%u", *(prices + 1));  //4
		When used in declaration (int* ptr), it creates a pointer variable
		When not used in declaration, it act as a dereference operator.