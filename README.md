### references

- https://cmake.org/cmake/help/v3.9/command/add_custom_command.html
- https://cmake.org/pipermail/cmake/2014-July/058130.html


### example

From within the cmake dir


```
#! make
[100%] Append contents of input to output
hello
world
!
[100%] Built target do_custom

#! make
[100%] Built target do_custom

#! echo '!!!' > ../src/c.src

#! make
[100%] Append contents of input to output
hello
world
!!!
[100%] Built target do_custom

#! make
[100%] Built target do_custom
```
