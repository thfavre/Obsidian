#C 

- Inside a function we can initialize a static variable
- [[variable#Global variables]] are static by default
- ->They are initialized to 0
- It retains the value across function calls

```C
int incrementAge() {
	static int age;  // is initialized to 0 by default
	age++;
   return age; }
int main(void) {
	printf("%d\n", incrementAge()); // 1
	printf("%d\n", incrementAge()); }  //  2
```

  