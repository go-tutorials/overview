# Overview

## Training
### Introduction to GO
#### Overview 
[![IMAGE ALT TEXT](http://img.youtube.com/vi/446E-r0rXHI/0.jpg)](http://www.youtube.com/watch?v=446E-r0rXHI "Introduction to GO")
#### Introduction
[![IMAGE ALT TEXT](http://img.youtube.com/vi/75lJDVT1h0s/0.jpg)](http://www.youtube.com/watch?v=75lJDVT1h0s&list=PLzMcBGfZo4-mtY_SE3HuzQJzuj4VlUG0q&index=1&ab_channel=TechWithTim "Introduction to GO")
### Basic GO
- To learn the basic syntax, you can start at https://go.dev/tour
#### Hello world
- Every Go program is made up of packages
- Start running in package main
  - Run here https://go.dev/tour/welcome/1
  - In this sample, use “fmt” package to print a string to console
```go
package main

import "fmt"

func main() {
    fmt.Println("Hello, world")
}
```

#### Function
Support to return multiple values
- Exercise 1: write a function, to add 2 integer numbers
  - Run here https://go.dev/tour/basics/5
- Exercise 2: write a function, to swap 2 strings
  - Run here https://go.dev/tour/basics/6

<table><thead><tr><td>

[Return 1 value](https://go.dev/tour/basics/5)
</td><td>

[Return 2 values](https://go.dev/tour/basics/6)
</td></tr></thead><tbody><tr><td>

```go
package main

import "fmt"

func add(x, y int) int {
  return x + y
}

func main() {
  fmt.Println(add(42, 13))
}
```
</td>
<td>

```go
package main

import "fmt"

func swap(x, y string) (string, string) {
  return y, x
}

func main() {
  a, b := swap("hello", "world")
  fmt.Println(a, b)
}
```

</td></tr></tbody></table>

#### Variables
Declare variables
- Exercise 1: Use “var” to declare 3 variables
  - Run here https://go.dev/tour/basics/8 
- Exercise 2: Use short variables declarations
  - Run here https://go.dev/tour/basics/10

<table><thead><tr><td>

[Use var](https://go.dev/tour/basics/8)
</td><td>

[Use short variables declarations](https://go.dev/tour/basics/10)
</td></tr></thead><tbody><tr><td>

```go
package main

import "fmt"

var c, python, java bool

func main() {
  var i int
  fmt.Println(i, c, python, java)
}
```
</td>
<td>

```go
package main

import "fmt"

func main() {
  var i, j int = 1, 2
  k := 3
  c, python, java := true, false, "no!"

  fmt.Println(i, j, k, c, python, java)
}
```
</td></tr></tbody></table>

#### Convert type
- Use expression T(v) to convert some number
  - Run here https://go.dev/tour/basics/13 

```go
package main

import (
    "fmt"
    "math"
)

func main() {
    var x, y int = 3, 4
    var f float64 = math.Sqrt(float64(x*x + y*y))
    var z uint = uint(f)
    fmt.Println(x, y, z)
}
```
#### Loop
Declare variables
- Exercise 1: Total from 1 to 10
  - Run here https://go.dev/tour/flowcontrol/1 
- Exercise 2: Total from 1 to 10, with "while" loop logic
  - Run here https://go.dev/tour/flowcontrol/3

<table><thead><tr><td>

[For loop](https://go.dev/tour/flowcontrol/1)
</td><td>

[while is spelled for in Go](https://go.dev/tour/flowcontrol/3)
</td></tr></thead><tbody><tr><td>

```go
package main

import "fmt"

func main() {
  sum := 0
  for i := 0; i < 10; i++ {
    sum += i
  }
  fmt.Println(sum)
}
```
</td>
<td>

```go
package main

import "fmt"

func main() {
  sum := 1
  for sum < 1000 {
    sum += sum
  }
  fmt.Println(sum)
}
```
</td></tr></tbody></table>

#### Defer
A defer statement defers the execution of a function until the surrounding function return
- Exercise: Print “hello world” with defer
  - Run here https://go.dev/tour/flowcontrol/12

```go
package main

import "fmt"

func main() {
    defer fmt.Println("world")

    fmt.Println("hello")
}
```

#### Pointer
Struct fields can be accessed through a struct pointer
- Exercise: Access a struct with a struct pointer
  - Run here https://go.dev/tour/moretypes/4

```go
package main

import "fmt"

type Vertex struct {
    X int
    Y int
}

func main() {
    v := Vertex{1, 2}
    p := &v
    p.X = 1e9
    fmt.Println(v)
}
```

#### Array
Arrays cannot be resized
- Exercise: Create arrays with string & int
  - Run here https://go.dev/tour/moretypes/6

```go
package main

import "fmt"

func main() {
    var a [2]string
    a[0] = "Hello"
    a[1] = "World"
    fmt.Println(a[0], a[1])
    fmt.Println(a)

    primes := [6]int{2, 3, 5, 7, 11, 13}
    fmt.Println(primes)
}
```

#### Slice
A dynamically-sized
- Exercise 1: Create a slice from an array
  - Run here https://go.dev/tour/moretypes/7
- Exercise 2: Create a slice from an array
  - Run here https://go.dev/tour/moretypes/13

<table><thead><tr><td>

[Print 1 slice](https://go.dev/tour/moretypes/7)
</td><td>

[Print 4 slices](https://go.dev/tour/moretypes/13)
</td></tr></thead><tbody><tr><td>

```go
package main

import "fmt"

func main() {
  primes := [6]int{2, 3, 5, 7, 11, 13}

  var s []int = primes[1:4]
  fmt.Println(s, primes)
}
```
</td>
<td>

```go
package main

import "fmt"

func main() {
  a := make([]int, 5)
  printSlice("a", a)

  b := make([]int, 0, 5)
  printSlice("b", b)

  c := b[:2]
  printSlice("c", c)

  d := c[2:5]
  printSlice("d", d)
}

func printSlice(s string, x []int) {
  fmt.Printf("%s len=%d cap=%d %v\n",
    s, len(x), cap(x), x)
}
```
</td></tr></tbody></table>

#### Range
The range form of the for loop iterates over a slice or map
- Exercise: Loop a slice and print 2 powers
  - Run here https://go.dev/tour/moretypes/16

```go
package main

import "fmt"

var pow = []int{1, 2, 4, 8, 16, 32, 64, 128}

func main() {
    for i, v := range pow {
        fmt.Printf("2**%d = %d\n", i, v)
    }
}
```

#### Method
Method is a function of struct
- Exercise: Create a method, with struct receiver
  - Run here https://go.dev/tour/methods/1

```go
package main

import (
    "fmt"
    "math"
)

type Vertex struct {
    X, Y float64
}

func (v Vertex) Abs() float64 {
    return math.Sqrt(v.X*v.X + v.Y*v.Y)
}

func main() {
    v := Vertex{3, 4}
    fmt.Println(v.Abs())
}
```

#### Interface
An interface type is defined as a set of method signatures
- Exercise: Create a method, with struct receiver
  - Run here https://go.dev/tour/methods/9

```go
package main

import (
    "fmt"
    "math"
)

type Abser interface {
    Abs() float64
}

func main() {
    var a Abser
    f := MyFloat(-math.Sqrt2)
    v := Vertex{3, 4}

    a = f    // a MyFloat implements Abser
    a = &v // a *Vertex implements Abser

    // In the following line, v is a Vertex (not *Vertex)
    // and does NOT implement Abser.
    a = v

    fmt.Println(a.Abs())
}

type MyFloat float64

func (f MyFloat) Abs() float64 {
    if f < 0 {
        return float64(-f)
    }
    return float64(f)
}

type Vertex struct {
    X, Y float64
}

func (v *Vertex) Abs() float64 {
    return math.Sqrt(v.X*v.X + v.Y*v.Y)
}
```

### Exercises:
After finished the basic syntax, you should do these exercises
#### Exercise 1
- Create a CRUD REST API with [mux](https://github.com/gorilla/mux) and My SQL, table users, with these fields fields id, username, email, phone, dateOfBirth, and methods GetAll, GetByID, Insert, Update, Delete (Refer to [go-sql-tutorial](https://github.com/go-tutorials/go-sql-tutorial))
- Objectives:
  - Understand how to query data from RMS database, using "database/sql" package
  - Can insert, update, delete data
  - Understand how to use Mux to receive an http request, and return an http response
#### Exercise 2
- Create a CRUD REST API with [gin](https://github.com/gin-gonic/gin) and [MongoDB](https://go.mongodb.org/mongo-driver): collection user, with these fields id, username, email, phone, dateOfBirth, and methods: GetAll, GetByID, Insert, Update, Delete (Refer to [go-mongo-tutorial](https://github.com/go-tutorials/go-sql-tutorial) and [go-gin-sql-tutorial](https://github.com/go-tutorials/go-gin-sql-tutorial))
- Objectives:
  - Understand how to query data from Mongo
  - Can insert, update, delete data
  - Understand how to use [gin](https://github.com/gin-gonic/gin) to receive an http request, and return an http response
#### Exercise 3
- Create a CRUD REST API with [echo](https://github.com/labstack/echo) and [gorm](https://gorm.io) with My SQL: collection user, with these fields id, username, email, phone, dateOfBirth, and methods: GetAll, GetByID, Insert, Update, Delete (Refer to [gorm-tutorial](https://github.com/go-tutorials/gorm-tutorial) and [go-echo-sql-tutorial](https://github.com/go-tutorials/go-echo-sql-tutorial))
  - Understand how to query data from RMS database, using [gorm](https://gorm.io)
  - Can insert, update, delete data
  - Understand how to use [echo](https://github.com/labstack/echo) to receive an http request, and return an http response
#### Script to create database for Exercise 1 and Exercise 3
```sql
-- script to create database for exercise 1, exercise 3
create table if not exists users (
  id varchar(40) not null,
  username varchar(120),
  email varchar(120),
  phone varchar(45),
  date_of_birth date,
  primary key (id)
);

insert into users (id, username, email, phone, date_of_birth) values ('ironman', 'tony.stark', 'tony.stark@gmail.com', '0987654321', '1963-03-25');
insert into users (id, username, email, phone, date_of_birth) values ('spiderman', 'peter.parker', 'peter.parker@gmail.com', '0987654321', '1962-08-25');
insert into users (id, username, email, phone, date_of_birth) values ('wolverine', 'james.howlett', 'james.howlett@gmail.com', '0987654321', '1974-11-16');
```

## Real project samples
### Layer Architecture Samples
- To build a REST API to support
  - search, get by ID, create, update, delete
  - support "patch" method, using [core-go/service](https://github.com/core-go/service)
  - support "search" method, using [core-go/search](https://github.com/core-go/search)
- Apply 3 tier architecture: handler, service (business logic) and repository
  - Each layer is put in a separated package
- Some standard features
  - config: load config from yaml files
  - [health check](https://github.com/core-go/health): to check health of SQL 
  - [logging](https://github.com/core-go/log): can use [logrus](https://github.com/sirupsen/logrus) or [zap](https://github.com/uber-go/zap) to log, support to switch between [logrus](https://github.com/sirupsen/logrus) or [zap](https://github.com/uber-go/zap)
  - log tracing by at the [middleware](https://github.com/core-go/log/tree/main/middleware) the http request and http response
#### [go-sql-layer-architecture-sample](https://github.com/source-code-template/go-sql-layer-architecture-sample)
- A micro service with [mux](https://github.com/gorilla/mux) and SQL
- At SQL layer, support "patch", using [core-go/sql](https://github.com/core-go/sql)

#### [go-mongo-layer-architecture-sample](https://github.com/source-code-template/go-mongo-layer-architecture-sample)
- A micro service with [mux](https://github.com/gorilla/mux) and [MongoDB](https://go.mongodb.org/mongo-driver)
- At mongo layer, support "patch", using [core-go/mongo](https://github.com/core-go/mongo)

### Modular Samples
- To build a REST API to support
  - search, get by ID, create, update, delete
  - support "patch" method, using [core-go/service](https://github.com/core-go/service)
  - support "search" method, using [core-go/search](https://github.com/core-go/search)
- 3 layers are put into the same package (handler, service (business logic) and repository)
- Some standard features
  - config: load config from yaml files
  - [health check](https://github.com/core-go/health): to check health of SQL 
  - [logging](https://github.com/core-go/log): can use [logrus](https://github.com/sirupsen/logrus) or [zap](https://github.com/uber-go/zap) to log, support to switch between [logrus](https://github.com/sirupsen/logrus) or [zap](https://github.com/uber-go/zap)
  - log tracing by at the [middleware](https://github.com/core-go/log/tree/main/middleware) the http request and http response 
#### [go-sql-modular-sample](https://github.com/source-code-template/go-sql-modular-sample)
- A micro service with [mux](https://github.com/gorilla/mux) and SQL
- At SQL layer, support "patch", using [core-go/sql](https://github.com/core-go/sql)

#### [go-mongo-modular-sample](https://github.com/source-code-template/go-mongo-modular-sample)
- A micro service with [mux](https://github.com/gorilla/mux) and [MongoDB](https://go.mongodb.org/mongo-driver)
- At mongo layer, support "patch", using [core-go/mongo](https://github.com/core-go/mongo)

### Message Queue Samples
#### [go-subscription](https://github.com/project-samples/go-subscription)
- Consume a message from queue, then write the message to database (SQL, Mongo, Casandra, Dynamodb, Firestore, Elasticsearch)
- Use [core-go/mq](https://github.com/core-go/mq)
- Support these message queues:
  - Amazon Simple Queue Service (SQS) at [sqs](https://github.com/core-go/mq/tree/main/sqs)
  - Google Cloud Pub/Sub at [pubsub](https://github.com/core-go/mq/tree/main/pubsub)
  - Kafka: at [segmentio/kafka-go](https://github.com/core-go/mq/tree/main/kafka), [Shopify/sarama](https://github.com/core-go/mq/tree/main/sarama) and [confluent](https://github.com/core-go/mq/tree/main/confluent)
  - NATS at [nats](https://github.com/core-go/mq/tree/main/nats)
  - Active MQ at [amq](https://github.com/core-go/mq/tree/main/amq)
  - RabbitMQ at [rabbitmq](https://github.com/core-go/mq/tree/main/rabbitmq)
  - IBM MQ at [ibm-mq](https://github.com/core-go/mq/tree/main/ibm-mq)
- Support these databases
  - SQL
  - Mongo
  - Casandra
  - Dynamodb
  - Firestore
  - Elasticsearch

#### [go-batch-subscription](https://github.com/project-samples/go-batch-subscription)
- Consume a message from queue one by one
- After the configured interval time (for example, 5 seconds) or reach the batch size (for example, reach 1000 messages), write all messages (1000 messages) to database (SQL, Mongo, Casandra, Dynamodb, Firestore, Elasticsearch)
#### [go-admin](https://github.com/project-samples/go-admin)
User and role management, with these features:
- Authentication
  - Log in by LDAP
  - After logged in, get all privileges based on roles of that user
- Separate the "read" and "write" permissions for 1 role, using bitwise. For example:
  - 001 (1 in decimal) is "read" permission
  - 010 (2 in decimal) is "write" permission
  - 100 (4 in decimal) is "delete" permission
  - "read" and "write" permission will be "001 | 010 = 011" (011 is 3 in decimal)
- Some standard features
  - config: load config from yaml files
  - [health check](https://github.com/core-go/health): to check health of SQL 
  - [logging](https://github.com/core-go/log): can use [logrus](https://github.com/sirupsen/logrus) or [zap](https://github.com/uber-go/zap) to log, support to switch between [logrus](https://github.com/sirupsen/logrus) or [zap](https://github.com/uber-go/zap)
  - log tracing by at the [middleware](https://github.com/core-go/log/tree/main/middleware) the http request and http response

## Tutorials
### SQL
- [go-sql-tutorial](https://github.com/go-tutorials/go-sql-tutorial)
- [gorm-tutorial](https://github.com/go-tutorials/gorm-tutorial)
- [go-posgresql-tutorial](https://github.com/go-tutorials/go-posgresql-tutorial)
- [go-gin-gorm-tutorial](https://github.com/go-tutorials/go-gin-gorm-tutorial)

### NO SQL
- [go-cassandra-tutorial](https://github.com/go-tutorials/go-cassandra-tutorial)
- [go-mongo-tutorial](https://github.com/go-tutorials/go-mongo-tutorial)
- [go-elasticsearch-tutorial](https://github.com/go-tutorials/go-elasticsearch-tutorial)
- [go-firestore-tutorial](https://github.com/go-tutorials/go-firestore-tutorial)
- [go-dynamodb-tutorial](https://github.com/go-tutorials/go-dynamodb-tutorial)
### Web Frameworks
- [go-echo-sql-tutorial](https://github.com/go-tutorials/go-echo-sql-tutorial)
- [go-gin-sql-tutorial](https://github.com/go-tutorials/go-gin-sql-tutorial)

## Layer Architecture Samples
- [go-mongo-layer-architecture-sample](https://github.com/go-tutorials/go-mongo-layer-architecture-sample)
- [go-sql-layer-architecture-sample](https://github.com/go-tutorials/go-sql-layer-architecture-sample)
- [gorm-layer-architecture-sample](https://github.com/go-tutorials/gorm-layer-architecture-sample)

## Modular Samples
- [go-mongo-modular-sample](https://github.com/go-tutorials/go-mongo-modular-sample)
- [go-sql-modular-sample](https://github.com/go-tutorials/go-sql-modular-sample)
- [gorm-modular-sample](https://github.com/go-tutorials/gorm-modular-sample)
