#CPP 

To access [[member#Member attribute |member attribute]] or [[member#member functions|member function]] : 
`Sample.hpp`
```CPP
#include "Sample.hpp"
Sample::Sample(void) {
	this->foo = 42;
	this->bar()
}

void Sample::bar(void) {
	...}
```
`this` is a pointer, so `->` to dereference it.
(All members methods have one (hidden) parameter : `this`.)