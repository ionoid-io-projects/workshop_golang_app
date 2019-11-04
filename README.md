# Golang

## Workspace

```shell
# export env
export GOPATH=~/workspace
# go inside the workspace directory
cd ~/workspace
```

## Hello World!
----
```go
package main

import (
 "fmt"
)

func main(){
  fmt.Println("Hello World!")
}
```

How to build your code

```bash
$ go build main.go
$ ./main
```

To execute your golang directly

```
go run main.go
```

## Variables
----
Declaration 1

```go
var a int
```

Declaration 2

```go
var a = 1
```

Declaration 3

```go
message := "hello world"
```

Declaration 4 

```go
var b, c int = 2, 3
```

## Typecasting
-----
```go
a := 1.1
b := int(a)
fmt.Println(b)
//-> 1
```

## Conditional Statements
----
```go
if num := 9; num < 0 {
 fmt.Println(num, "is negative")
} else if num < 10 {
 fmt.Println(num, "has 1 digit")
} else {
 fmt.Println(num, "has multiple digits")
}
```

## Switch Statement

```go
i := 2
switch i {
case 1:
 fmt.Println("one")
case 2:
 fmt.Println("two")
default:
 fmt.Println("none")
}
```

## Looping

```go
sum := 0
for i := 0; i < 10; i++ {
  sum += i
}
fmt.Println(sum)
```

Infinit loop
```go
for {
}
```

## Functions

```go
func add(a int, b int) int {
  c := a + b
  return c
}
func main() {
  fmt.Println(add(2, 1))
}
//=> 3
```

Return more than one value
```go
func add(a int, b int) (int, string) {
  c := a + b
  return c, "successfully added"
}
func main() {
  sum, message := add(2, 1)
  fmt.Println(message)
  fmt.Println(sum)
}
```

To learn more
https://www.freecodecamp.org/news/learning-go-from-zero-to-hero-d2a3223b3d86/

# Go for raspberry pi
Using https://github.com/stianeikeland/go-rpio it's possible to interacte with gpio pin
So refer to the documentation of the project to read more

To run your golang program inside Raspberry Pi you must compile with Raspberry Pi arch reference like following
```
env GOOS=linux GOARCH=arm GOARM=6 go build your_program.go
```
This command line will compile your program for arm6 arch which is the arch of Raspberry Pi 0

Raspberry pi 3 b use arm7 so you will need to replace environement var GOARM=6 by GOARM=7. 
```
env GOOS=linux GOARCH=arm GOARM=7 go build your_program.go
```

# Golang framework for raspberry


    connectordb - Open-Source Platform for Quantified Self & IoT.
    devices - Suite of libraries for IoT devices, experimental for x/exp/io.
    eywa - Project Eywa is essentially a connection manager that keeps track of connected devices.
    flogo - Project Flogo is an Open Source Framework for IoT Edge Apps & Integration.
    gatt - Gatt is a Go package for building Bluetooth Low Energy peripherals.
    gobot - Gobot is a framework for robotics, physical computing, and the Internet of Things.
    huego - An extensive Philips Hue client library for Go.
    iot - IoT is a simple framework for implementing a Google IoT Core device.
    mainflux - Industrial IoT Messaging and Device Management Server.
    periph - Peripherals I/O to interface with low-level board facilities.
    sensorbee - Lightweight stream processing engine for IoT.
