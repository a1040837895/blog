---
title: golang并发编程
description: golang并发编程
date: 2020-06-08T06:00:20+06:00
menu:
  sidebar:
    name: golang并发编程
    identifier: golang-concurrency
    parent: golang
    weight: 2
---

```go
func main() {
    wg := &sync.waitGroup{}
    wg.Add(1)
    go func(){
        defer wg.Done()
        //... doSomething
    }()
    wg.Wait()
}

```