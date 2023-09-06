#CPP 

# `const` values

Make a value unmodifiable,  assignation is impossible, we can only initialize the  constant to a value. 
( In C we can only have constants like that `int const PI=3;` )

In `CPP` we can initialize a `const` by a value from the constructor. (It does NOT assign)

`Sample.hpp`
```CPP
class Sample {
public:
	float const pi;
	
	void Sample(float const f);
	~Sample(void);
	
	void bar(void) const; 
};
```
`Sample.cpp`
```CPP
Sample::Sample(float const f) : pi(f) {
}

void Sample::bar(void) const {
	std::cout << "this->pi = " << this->pi;
}
```

What does this `void bar(void) const;` means?
It means that the function will never modify the current instance (= There will never be `this->` in the function)
If a member function never change a `this` value, make it `const`!
