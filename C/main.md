#C

## Return : 
### No return :
```C:main
int main(void) {} 

```
When no return added gcc will ===returns 0=== to say all went good.
### 0 return
The main method should always end witth a return 0.
### Error return
When the main return something else than 0.

### Get return value :
```Shell
echo $?
```


## Arguments :
```C
int main(int argc, char **argv, char **environ)
```
#### int argc : arguments counts
It include the file name (so when there is no arugments, args=1)
#### char **argv : arguments values
To access the values
It is a char \*\*, so it is a pointer to the start of each string of the parameters
#### **environ : 
get access to the environment of the shell with the *env* command 
Example : usefull to use the pwd command 
Almost never useful 

### Name :
We can change the argc, argv and environ name

### Example :
```Shell
gcc -Wall -Wextra -Werror main.c && ./a.out 6 hehe
```
```C
int main(int argc, char **argv) 
{
	printf("Nbr arg : %d \n", argc);
	printf("Val arg : %c, %s, %c", argv[0], argv[1], argv[2]);  
	return (0);
}
```
>Output :   3 
>				./a.out   hehe   

## Iterate argv :
Go see : https://stackoverflow.com/questions/48333430/iterate-through-argv
```c shema
      argv                       --
        +----+    +-+-+-+-+--+     |
 argv[0]|    |--->|t|e|s|t|\0|     |
        |    |    +-+-+-+-+--+     |
        +----+    +-+-+-+-+--+     |
 argv[1]|    |--->|h|a|v|e|\0|     |
        |    |    +-+-+-+-+--+     |
        +----+    +-+--+           |
 argv[2]|    |--->|a|\0|            > char array
        |    |    +-+--+           |
        +----+    +-+-+-+-+--+     |
 argv[3]|    |--->|n|i|c|e|\0|     |
        |    |    +-+-+-+-+--+     |
        +----+    +-+-+-+--+       |
 argv[4]|    |--->|d|a|y|\0|       |
        |    |    +-+-+-+--+       |
        +----+                   --
 argv[5]|NULL|
        |    |
        +----+
```

argv+0 --> will give address of first element of array.
argv+1 --> will give address of second element of array.
...
...
and so on.
argv+0 and &argv[0] are same.

```C:ex
int	main(int argc, char **argv)
{
	while (*argv)
		printf("%s", *argv++);
	return (0);
}
```

### Derefernce :
```c
*(argv+0) and argv[0] are same
```

