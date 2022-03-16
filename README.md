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
##### Exercise 1: write a function, to add 2 integer numbers
- Run here https://go.dev/tour/basics/5
##### Exercise 2: write a function, to swap 2 strings
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
#### Declare variables
Use “var” to declare 3 variables
- Run here https://go.dev/tour/basics/8 
```go
package main

import "fmt"

var c, python, java bool

func main() {
	var i int
	fmt.Println(i, c, python, java)
}
```
Use short variables declarations
- Run here https://go.dev/tour/basics/10
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
### Exercises:
#### After finished the basic syntax, you should do these exercises
- Exercise 1: A CRUD REST API with Mux and My SQL, table users, with these fields fields id, username, email, phone, dateOfBirth, and methods GetAll, GetByID, Insert, Update, Delete (Refer to [go-sql-tutorial](https://github.com/go-tutorials/go-sql-tutorial))
- Exercise 2: A CRUD REST API with Mux and MongoDB: collection user, with these fields id, username, email, phone, dateOfBirth, and methods: GetAll, GetByID, Insert, Update, Delete (Refer to [go-mongo-tutorial](https://github.com/go-tutorials/go-sql-tutorial))
- Exercise 3: A CRUD REST API with Mux and gorm with My SQL: collection user, with these fields id, username, email, phone, dateOfBirth, and methods: GetAll, GetByID, Insert, Update, Delete (Refer to [gorm-tutorial](https://github.com/go-tutorials/gorm-tutorial))
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
