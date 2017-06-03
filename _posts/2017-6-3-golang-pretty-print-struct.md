---
layout: post
title: Golang pretty print Structure!
---

Here is quick tip to pretty print go struct

```

package main

import (
	"fmt"
)

type Person struct {
	name string
	age  int
}

func main() {

	var p Person
	p.name = "Motyar"
	p.age = 120

	fmt.Printf("%+v\n", p) //With name and value
	fmt.Printf("%#v", p) //with name, value and type
	
}

```
Will output 

```
{name:Motyar age:120}
main.Person{name:"Motyar", age:120}

```

