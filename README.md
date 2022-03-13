# Overview

## Training
### Introduction to GO
#### Overview 
[![IMAGE ALT TEXT](http://img.youtube.com/vi/446E-r0rXHI/0.jpg)](http://www.youtube.com/watch?v=446E-r0rXHI "Introduction to GO")
#### Introduction
[![IMAGE ALT TEXT](http://img.youtube.com/vi/75lJDVT1h0s/0.jpg)](http://www.youtube.com/watch?v=75lJDVT1h0s&list=PLzMcBGfZo4-mtY_SE3HuzQJzuj4VlUG0q&index=1&ab_channel=TechWithTim "Introduction to GO")
### Basic GO
- To learn the basic syntax, you can start at [tutorials point](https://www.tutorialspoint.com/go/index.htm)

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
