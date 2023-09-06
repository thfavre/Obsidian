#CPP 
# Declaration
`Sample.hpp`
```CPP:Sample.hpp
#ifndef SAMPLE_CLASS_H
# SAMPLE_CLASS_H

class Sample {

public:
	Sample(void); // Construcotr
	~Sample(void); // Destructor
};
#endif
```
`Sample.cpp`
```CPP:Sample.cpp
#include "Sample.hpp"
Sample::Sample(void) {
	std::cout << "Construcor called";
}
Sample::~Sample(void) {
	std::cout << "Destructor called";
}
```
`main.cpp`
```CPP:main.cpp
#include "Sample.hpp"
int main() {
	Sample sampleName;
}
```
When the main function is finished, all local variables are destroyed.
-> The `sampleName` local variable is destroyed with the destructor.

## Constructor
When the class is instanced, the Constructor method is called.
## Destructor
When the class instance is destroyed, the Destructor method is called.
