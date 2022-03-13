# Overview

## Tutorials
### SQL
- [sql](https://github.com/go-tutorials/go-sql-tutorial)
- [gorm](https://github.com/go-tutorials/gorm-tutorial)
- [PosgreSQL](https://github.com/go-tutorials/go-posgresql-tutorial)
- [simple gorm](https://github.com/go-tutorials/go-gin-gorm-tutorial)

### NO SQL
- [cassandra](https://github.com/go-tutorials/go-cassandra-tutorial)
- [mongo](https://github.com/go-tutorials/go-sql-tutorial)
- [elasticsearch](https://github.com/go-tutorials/go-elasticsearch-tutorial)
- [firestore](https://github.com/go-tutorials/go-firestore-tutorial)
- [dynamodb](https://github.com/go-tutorials/go-dynamodb-tutorial)
### Web Frameworks
- [echo](https://github.com/go-tutorials/go-echo-sql-tutorial)
- [gin](https://github.com/go-tutorials/go-gin-sql-tutorial)

## Layer Architecture Samples
- [mongo](https://github.com/go-tutorials/go-mongo-layer-architecture-sample)
- [sql](https://github.com/go-tutorials/go-mongo-layer-architecture-sample)
- [gorm](https://github.com/go-tutorials/gorm-layer-architecture-sample)

## Modular Samples
- [mongo](https://github.com/go-tutorials/go-mongo-modular-sample)
- [sql](https://github.com/go-tutorials/go-sql-modular-sample)
- [gorm](https://github.com/go-tutorials/gorm-modular-sample)

## Road map for the beginners
### Introduction to GO
#### Overview 
- [![IMAGE ALT TEXT](http://img.youtube.com/vi/446E-r0rXHI/0.jpg)](http://www.youtube.com/watch?v=446E-r0rXHI "Introduction to GO")
#### Introduction
- [![IMAGE ALT TEXT](http://img.youtube.com/vi/75lJDVT1h0s/0.jpg)](http://www.youtube.com/watch?v=75lJDVT1h0s&list=PLzMcBGfZo4-mtY_SE3HuzQJzuj4VlUG0q&index=1&ab_channel=TechWithTim "Introduction to GO")
### Basic GO
- To learn the basic syntax, you can start at [tutorials point](https://www.tutorialspoint.com/go/index.htm)

### Exercises:
#### After finished the basic syntax, you should do these exercises
- Exercise 1: A CRUD REST API with Mux and My SQL, table users, with these fields fields id, username, email, phone, dateOfBirth, and methods GetAll, GetByID, Insert, Update, Delete (Refer to [sql](https://github.com/go-tutorials/go-sql-tutorial))
- Exercise 2: A CRUD REST API with Mux and MongoDB: collection user, with these fields id, username, email, phone, dateOfBirth, and methods: GetAll, GetByID, Insert, Update, Delete (Refer to [mongo](https://github.com/go-tutorials/go-sql-tutorial))
- Exercise 3: A CRUD REST API with Mux and gorm with My SQL: collection user, with these fields id, username, email, phone, dateOfBirth, and methods: GetAll, GetByID, Insert, Update, Delete (Refer to [gorm](https://github.com/go-tutorials/gorm-tutorial))
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
