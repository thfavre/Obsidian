# [[C]] recursivity
A function is recursive if it call itself in his body.
Otherwise a function is iterative;

## Example :
```C:ex
int mult(int a, int b)
{
	if (b == 0)
		return 0;
	if (b < 0)
		return -a + mult(a, b + 1);
	return a + mult(a, b - 1);
}
int main() {mult(4, -10)}
```
on envoie 4 et -10 a mult, -10 est pas == a 0, -10 est plus petit que 0, 
return -4 + (mult(a, -9)) ...
