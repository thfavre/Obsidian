#C

Related : [[Heap, maloc, free]]

Prototype : `void *malloc(size_t size)`
Use malloc when we return a pointer from a function

```C 
int *p = malloc(sizeof(*p))
```

## malloc of struct 
```C 
typedef struct
{
	int height;
	int width;
} t_rect;

t_rect *p = malloc(sizeof(*p));
```