# KISS Complex math for C
Have you ever got in the situation where for some
dumb reason, complex numbers are not implemented in
`<complex.h>` or `<math.h>`? 

Here is a portable implementation with structs
and what not.

## Features

- [] Complex numbers as float, double
- [] Complex math functions for float,double
 - [] Float complex math
 - [] Double complex math
- [] Library tests vs other implementations (glibc, etc)

## How to use
Compile the file `complex.c` and include `complex.h` into your project.

Use a wrapper for creating complex numbers if you want true portability
or testing this against other implementations:

```
complex make_complex(float real, float imag){
	#ifdef KISS_COMPLEX
	/*(This library's implementation)*/
	#else
	/*(Usual <complex.h> implementation)*/
	#endif
}
```
