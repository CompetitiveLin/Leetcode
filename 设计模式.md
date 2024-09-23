# 设计模式

1. 责任链模式

```go
package main

import "fmt"

type person struct {
}

type chain interface {
	check(person)
	setNext(chain)
}

type check1 struct {
	next chain
}

func (c check1) check(p person) {
	fmt.Println("check1")
	c.next.check(p)
}

func (c check1) setNext(ch chain) {
	c.next = ch
}

type check2 struct {
	next chain
}

func (c check2) check(p person) {
	fmt.Println("check2")
}

func (c check2) setNext(ch chain) {
	c.next = ch
}

func main() {
	p := person{}

	c1 := &check1{next: check2{}}
	c1.check(p)
}

```

