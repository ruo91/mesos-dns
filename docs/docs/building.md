---
title: Building Mesos-DNS
---

##  Building Mesos-DNS

You can download Mesos-DNS from the [Mesosphere package repositories](http://mesosphere.com/downloads/). 

If you prefer to build Mesos-DNS on your own, you will need to have `go` installed on your computer using [these](https://golang.org/doc/install) instructions. Make sure that `GOROOT` environment variable is set properly and that `$GOROOT/bin` is added to `PATH` environment variable. To build Mesos-DNS:

```
go get github.com/miekg/dns
go get github.com/mesosphere/mesos-dns
cd $GOPATH/src/github.com/mesosphere/mesos-dns
go build -o mesos-dns main.go
``` 

`mesos-dns` is a statically-linked binary that can be installed anywhere. 

We have built and tested Mesos-DNS with `go` versions 1.3.3 and 1.4. Newer versions of `go` should work as well. 
