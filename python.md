# Python

These are a list of python features you MUST know
* print(string): prints a string to stdout
* x = value: Assigns a value to a variable
	* Note no declaration required
	* x = 1; x= "string" is valid python since variables are dynamically typed
		* Dynamic typing means the type of a variable may change during the exceution of a program
* [1, 2, 3]: Python lists (arrays)
	* Lists are heterogenous, i.e. they can have elements of different types, such as [1, "two", 0x3]
* for element in set: The python for loop is deisgned to iterate over a set of elements
	* these sets are often lists
	* to iterate over numbers, use range(start, end, step)
		* range(x) == range(0,x,1) and range(x,y) == range(x,y,1)
* input(message): Prints a message to stdout and then retreives an input from stdin
	* Usually use like so: x = input("message"), with command line as stdin and stdout
* int(), str(): Functions like these cast their arguments to the appropriate type
	* eg int("3") == 3, str(3) == "3"
* #: The hash symbol is the python comment symbol
	* Anything on a line after a hash is discarded by the interpreter

These are some useful features you SHOULD know
* x += y: The same as saying x = x + y
* " and ': There is no difference between " and ', unlike some other languages
* x[index]: See this [link](https://www.tutorialspoint.com/numpy/numpy_indexing_and_slicing.htm) for more on python indexing and slicing (its very useful)

These are some advanced features you MIGHT know
* eval(expression): Takes a string and uses the python interpreter to evaluate the expression
	* e.g. eval("sum([3,5,6])") returns 14

