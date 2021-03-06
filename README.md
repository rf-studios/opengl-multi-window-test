# Multi Window OpenGL Test

This repository is to figure out the answer to this question:

http://stackoverflow.com/questions/29617370/multiple-opengl-contexts-multiple-windows-multithreading-and-vsync

## Building

### Linux

```
clang -Werror -Wall -g -o multi-window-test main.c -lglfw
```

### OSX

```
clang -Werror -Wall -g -o multi-window-test main.c -lglfw3
```

### Windows

Use [mxe](http://mxe.cc/).

```
i686-w64-mingw32.static-gcc -std=c99 -mconsole -mwindows -o multi-window-test.exe main.c -lglfw3 -lopengl32
```

## Running

```
./multi-window-test --windows 6
```

Now watch stderr and see the fps reported should be really close to 60, not
60 / (whatever you set --windows to)
