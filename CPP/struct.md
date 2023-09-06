#CPP 

```CPP
struct Sample {
	int foo;
	
	Sample(void);
	~Sample(void);
	
	void bar (void) const; 
}
```
What is the difference ?
A `struct` has by default a ==public== scope.
A `class` has by default a ==private== scope.
