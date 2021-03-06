# Using gnu ld

## reading command options from a file

use `@`, e.g:

```
$gcc ... @libGLESv2.so.rsp ...
```
will cause the linker to read command options from libGLESv2.so.rsp.

## -B, specifying where to find executables

For each subprogram to run, the driver will first try to locate the executable with the prefix specified by `-B`,
If the executable can not be found there, it will try the standard prefixes `/usr/lib/gcc/` and `/usr/local/lib/gcc/`

## specifying where to find the headers and libraries

`--sysroot`

## configure the dynamic linker

`ldconfig` can be used to configure the behavior of the dynamic linker `ld.so`.
To show the list of shared libraries theb dynamic linker will search for a give symbol, use the following
command:

	`ldconfig -p`

## debug the linking process

If you want to debug the linking process, especially you want to confirm
how the linker editor is trying to find a symbol, you can pass the following
command to `gcc` or `clang`

	gcc -Wl,--verbose
or
    clang -Wl,--verbose


or using `ld --verbose`

This will dump the default linker script in addition to the process
for finding files.


## define symbols in the linker script

Important variables in linker script:

`.` represents the current value in VM space.

Using `PROVIDE` to define symbol so we can use it in the code.

## merge multiple object files

```
ld -r a.o b.o -o c.o
```

https://stackoverflow.com/questions/2980102/combine-two-gcc-compiled-o-object-files-into-a-third-o-file
