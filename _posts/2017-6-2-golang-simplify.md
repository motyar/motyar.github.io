---
layout: post
title: Auto Simplify your Golang code
tags: golang
---
Do you know you can simplify your Go Code using the *gofmt -s* command like this

``` 
gofmt -s file.go
```


# The simplify command

When invoked with -s gofmt will make the following source transformations where possible.



```

An array, slice, or map composite literal of the form:
	[]T{T{}, T{}}
will be simplified to:
	[]T{{}, {}}

A slice expression of the form:
	s[a:len(s)]
will be simplified to:
	s[a:]

A range of the form:
	for x, _ = range v {...}
will be simplified to:
	for x = range v {...}

A range of the form:
	for _ = range v {...}
will be simplified to:
	for range v {...}
```

[Source](https://golang.org/cmd/gofmt/#hdr-The_simplify_command) 
 

