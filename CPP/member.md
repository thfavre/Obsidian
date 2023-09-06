#CPP 

# Member attribute
Will be used from an instance of the class 
`Sample.hpp`
```CPP
class Sample {
public:
	int foo;
};
```
`main.cpp`
```cpp
int main() {
	Sample instance;
	instance.foo = 42;
}
```
# member function
`Sample.hpp`
```CPP
class Sample {
public:
	void bar(void);
};
```
`Sample.cpp`
```CPP
void Sample::bar(void) {
	std::cout << "Member function called"
}
```
`main.cpp`
```cpp
int main() {
	Sample instance;
	instance.bar();
}
```