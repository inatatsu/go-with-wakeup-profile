# go-with-wakeup-profile

A fork of [the Go programming language](https://github.com/golang/go). This repository adds a new feature to generate additional performance profiling data.

Link to the original [README](README-ORIGINAL.md).


## how to build

1. Build a container to build a golang

Select a golang version (1.9 or 1.10) to build by choosing a branch

```
$ docker build -t go-wakeup git@github.com:IBM/go-with-wakeup-profile#wakeup-profile.go1.10
```

2. Run the container
```
$ docker run --rm go-wakeup > go-1.10-wakeup.tar.gz
```

3. Make sure you get a golang with wakeup profile

```
$ tar -zxvf go-1.10-wakeup.tar.gz
$ ./go/bin/go version
go version go1.10.2-wakeup linux/{$ARCH}
```