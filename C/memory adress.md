Memory Address & :
		-The memory address is the location where the variable is stored on the computer
		-When we assign a value to the variable, it is stored in this memory address
		-To access it, use the reference operator (&), and the result will represent where the variable is stored
		Example : 
			int myAge = 43; printf("%p", &myAge); // Outputs 0x7ffe5367e044
		-&... is called a pointer. A pointer stores the memory address of a variable as its values.