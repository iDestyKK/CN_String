#CN\_String
A C library that makes Null-Terminated strings less of a pain in the arse.

CN\_String is a library which helps users handle strings in a more "object-oriented" way in C. Chances are that you have been spoiled by std::string in C++. Getting string length in C is **NOT** constant time, meanwhile it is in C++. Also concatenation isn't as trivial in C as opposed to C++. This library supplies functions for enhanced string handling. You can concatenate and insert into CN\_Strings, and it supports C-Strings as well. This library is similar to CN\_Vec as in it handles dynamic memory management on its own, but it guarantees that its data will contain an empty string at least as opposed to a NULL pointer.

Example
```C
#include <stdio.h>
#include <stdlib.h>

#include "cn_string.h"

main() {
	//Starting with a blank string
	CN_STRING str = cn_string_init();
	cn_string_insert_from_cstr(str, "This is a test.", 0);
	printf("%s\n", cn_string_str(str));
	cn_string_free(str);
	
	//Starting with initial string
	CN_STRING str_i = cn_string_from_cstr("This is also a test.");
	printf("%s\n", cn_string_str(str_i));
	cn_string_free(str_i);
}
```

Output:
```
This is a test.
This is also a test.
```

Full documentation at: <a href = "http://web.eecs.utk.edu/~ssmit285/lib/cn_string/index.html">http://web.eecs.utk.edu/~ssmit285/lib/cn_string/index.html</a></br>The documentation has details and examples of every single function in the library, as well as a guide.
