#CPP

## References :
[CPlusPlus](https://cplusplus.com/reference/)
[Elearing 42](https://elearning.intra.42.fr/notions/piscine-c-d00-c-basics/subnotions)


# Basics
- ## [[namespaces]]
- ## [[stdio streams]]
- ## [[class and instance]]
- ## [[member]]
- ## [[CPP/this]]
- ## [[list initialization]]
- ## [[const]]
- ## [[visibility]]
- ## [[struct]]
- ## [[accessor]]
- ## [[CPP/this]]
- ## [[CPP/this]]

# From exo :
## new / delete:
`new` is an operator used to dynamically allocate memory for a new object at runtime. It returns a pointer to the allocated memory, which can then be used to access the object.
```CPP
data_type *pointer_variable;
pointer_variable = new data_type;
delete pointer_variable;
```
And for arrays :
```CPP
data_type pointer_variable[number_of_elements];
pointer_variable = new data_type[number_of_elements];
delete[] pointer_variable;
```

## References : 
`std::string *stringPTR = &string;`
It is just an alias for a variable.
References are often used as function parameters, where they can be used to pass variables by reference instead of by value. For example:
```CPP
void addOne(int& num) { num += 1; }
```
