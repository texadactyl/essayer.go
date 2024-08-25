# essayer

This repo is for trying out things with ```purego```.

**2024-08-24 12:00**

So far, it works as expected in a GitHub Actions job in ```ubuntu-latest``` and ```macos-latest``` for libzip open and close.
I need to get that working in ```windows-latest``` too.
Also, I need to try some real JVM library functions (E.g. libzip inflate and deflate).

**2024-08-24 13:30**

Purego does not support the same user-level APIs in every O/S. In fact, they require the user to employ https://pkg.go.dev/golang.org/x/sys/windows for opening a library in the Windows environment. 

go get golang.org/x/sys/windows
go build .
```
package main
    imports golang.org/x/sys/windows: build constraints exclude all Go files in /home/elkins/go/pkg/mod/golang.org/x/sys@v0.24.0/windows
```

**2024-08-25 11**

Note: Variadic library functions (variable number of arguments) are not supported.
