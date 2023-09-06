#CPP 

Group functions, symbols that have a link together inside a group named "namespace".

```CPP
int gl_var = 1;
int f(void) { retrun 2; }

namespace Foo { // create a scope called Foo
	int gl_var = 3;
	int f(void) { retrun 4; }
}

namespace Bar { // create a new namespace, the values are not shared with otehrs namespaces
	int gl_var = 5;
	int f(void) { retrun 6; }
}

namespace Muf = Bar; // alias to the namespace Bar

int main(void) {
	printf("%d", gl_var); // 1
	printf("%d", f()); // 2
	
	printf("%d", Foo::gl_var); // 3
	printf("%d", Foo::f()); // 4
	
	printf("%d", Bar::gl_var); // 5
	printf("%d", Bar::f()); // 6
	
	printf("%d", Muf::gl_var); // 5
	printf("%d", Muf::f()); // 6

	printf("%d", ::gl_var); // 1 Will use the global variable. Exactly the same as without the "::" 
	printf("%d", ::f()); // 2 (Do not do that, it is overkill)
}
```

## scope resolution operator `::`
It is used to specify the scope of a function or a variable in a namespace or a class.

