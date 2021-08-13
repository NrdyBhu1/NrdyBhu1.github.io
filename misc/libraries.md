# [<- Misc](../misc/)

## Creating libraries in C
Libraries in C are usually statically linked or dynamically linked.

### Project structure
```sh
.
|-- header.h
|-- header.c
`-- main.c
```
### Compiling static librabry
```sh
$ gcc -c header.c
$ ar rcs libheader.a header.o
$ gcc main.c -o main -L. -lheader
```

### Compiling dynamic library
```sh
$ gcc -c -fPIC header.c
$ gcc header.o -shared -o libheader.so
$ mv libheader.so /usr/lib/
$ gcc main -o main -lheader
```
