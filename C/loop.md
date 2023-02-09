#C

## while :
```C
while(condition) { ... }
```

## do + while
```C
do { ... } while(condition);
```

## for : 
```C
for (statement 1; statement 2; statement 3) { ... }
```
Statement 1 is executed (one time) before the execution of the code block.
Statement 2 defines the condition for executing the code block.
Statement 3 is executed (every time) after the code block has been executed.
### Example :
```C
for (int i = 0; i < 5; i++) { ... }
```


## Break and Continue : 
- break : stop a loop
- continue : go to the next iteration
### Example :
```C
int my_var = 0;
while (1){
	if (my_var == 100)
		break ;
	myvar++; }
```