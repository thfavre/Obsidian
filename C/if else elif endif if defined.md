# [[C]] if else elif endif if defined
It is a [[preprocessor directive]]
## Example :
```C:main
int main()
{
#if 7 > 1
	printf("it works!"); // it works!
#endif
}
```
Print "it works!"

```C:main
int main()
{
#if 7 < 1
	printf("it works!");
#endif
}
```
Print nothing

### Combine with [[define]] :
```C:main
#define TEST 15
int main()
{
#if TEST < 10
	printf("<10!");
#elif TEST < 20
	printf("<20!");
#else 
	printf(">=20!");
#endif
}
```
Print "<20!"

## \#if defined() :
```C:main
int main()
{
#if defined(TEST)
	printf("test is defined");
#else
	printf("test is not defined");
#endif
}
```


Le code enlevé ne sera plus dans la version compilé 