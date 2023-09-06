#CPP 

How to define if a member can be accessed by outside the class ?

`Sample.hpp`
```CPP
class Sample {
public:
	int public_foo;
	Sample(void);
	~Sample(void);

	void publicBar(void) const;

private:
	int _privat_foo;

	void _privatBar(void) const;
}
```

# Convention 
A private variable starts / ends with a `_` or starts with `m_`