#CPP 

`a1(p1)` initialize `a1` to a value `p1`, It does NOT assign the value p1 to a1.

`Sample.hpp`
```CPP
class Sample {
public:
	char a1;
	int a2;
	
	Sample(char p1, int p2);
	~Sample(void);
}
```
`Sample.cpp`
```CPP
#incloude "Sample.hpp"
Sample::Sample(char p1, int p2) : a1(p1), a2(p2) {
	std::cout << "this->a1 = " << this->a1;
	std::cout << "this->a2 = " << this->a2;
}
```
`main.cpp`
```CPP
#include "Sample.hpp"
int main() {
	Sample isntance('a', 42);
}
```

