# [[C]] condition
## if, else if, else :
```C
if (condition) 
{
 ... 
} else if (condition2) 
{
 ...
} else 
{
 ... 
 }
```

## Ternary Operator : 
```C
variable = (condition) ? expressionTrue : expressionFalse;
```
### Example :
```C
int time = 20; (time < 18) ? printf("Good day.") : printf("Good evening.");
```

## Switch :
```C
switch (condition) 
{
  case 0:
	break;  // break to avoid the "cascade" effect
  case 1:
	break;
  default: // handle all the other cases
	break; 
}
```


