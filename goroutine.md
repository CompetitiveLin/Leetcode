# Goroutine

1. 两个协程轮流打印 `1, 2`

```go
package main

import (
	"fmt"
	"sync"
)

var wg sync.WaitGroup

func main() {
	wg.Add(2)
	ch1 := make(chan int)
	go func() {
		defer wg.Done()
		for i := 0; i < 10; i++ {
			ch1 <- i
			if i%2 == 0 {
				fmt.Println("1: ", i)
			}
		}
	}()
	go func() {
		defer wg.Done()
		for i := 0; i < 10; i++ {
			<-ch1
			if i%2 == 1 {
				fmt.Println("2: ", i)
			}
		}
	}()
	wg.Wait()
}
```

2. 三个协程轮流打印 `1, 2, 3`

```go
package main

import (
	"fmt"
	"sync"
)

func main() {
	var wg sync.WaitGroup
	wg.Add(2)
	ch1 := make(chan int)
	ch2 := make(chan int)
	go func() {
		defer wg.Done()
		for i := 0; i < 100; i++ {
			<-ch1
			<-ch2
			if i%3 == 0 {
				fmt.Println(1, ": ", i)
			}
		}
	}()
	go func() {
		defer wg.Done()
		for i := 0; i < 100; i++ {
			ch1 <- 1
			if i%3 == 1 {
				fmt.Println(2, ": ", i)
			}
		}
	}()
	go func() {
		defer wg.Done()
		for i := 0; i < 100; i++ {
			ch2 <- 1
			if i%3 == 2 {
				fmt.Println(3, ": ", i)
			}
		}
	}()
	wg.Wait()
}
```

3. 生产者消费者模型

```go
package main

import (
	"fmt"
	"sync"
)

var wg sync.WaitGroup
var lock sync.Mutex

func main() {
	ch := make(chan int, 100)
	producer(ch)
	cnt := 3
	wg.Add(cnt)
	for i := 0; i < cnt; i++ {
		go consumer(i, ch)
	}
	wg.Wait()
}

func producer(ch chan int) {
	defer close(ch)
	for i := 0; i < 10; i++ {
		fmt.Println("producer: ", i)
		ch <- i
	}
}

func consumer(i int, ch chan int) {
	for {
		if v, ok := <-ch; ok {
			fmt.Println("consumer ", i, ":", v)
		} else {
			break
		}
	}
	wg.Done()
}
```



## 手写协程池

```go
package main

import (
	"fmt"
	"time"
)

type Task struct {
	f func()
}

func (t *Task) Execute() {
	t.f()
}

type Pool struct {
	tasks chan *Task
	entry chan *Task
	nums  int
}

func (p *Pool) Work(id int) {
	for task := range p.tasks {
		task.Execute()
		fmt.Println("excute id: ", id)
		time.Sleep(2 * time.Second)
	}
}

func (p *Pool) Run() {
	for i := 1; i <= p.nums; i++ {
		go p.Work(i)
	}
	for task := range p.entry {
		p.tasks <- task
	}
}

func main() {
	task := &Task{f: func() {
		fmt.Println("Execute!", time.Now())
	}}
	p := &Pool{nums: 3, entry: make(chan *Task), tasks: make(chan *Task)}
	go func() {
		for {
			p.entry <- task
		}
	}()
	p.Run()
}
```

