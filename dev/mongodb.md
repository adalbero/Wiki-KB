---
title: MongoDB KB
description: Tricks & Tips
published: true
date: 2020-03-26T09:06:13.284Z
tags: 
---

# Overview
MongoDB is a non SQL database. It is document-based database.

- **Database** - A set of collections
- **Collections** - A set of documents of the same type
- **Documents** - Each document is represented as a JSON object

There is a powerfull query language based on JavaScript.

> **Version** - Information based on MongoDB 4.2.5
{.is-info}

# Products
- **MongoDB Server** - Databse as a service or command line
- **MongoDB Compass** - GUI to manage databases (included with the server)
- **MongoDB Shell** - Interactive JavaScript Interface to MongoDB (included with the server)
- **MongoDB Atlas** - Cloud MongoDB Database

# Install
- Download and install **MongoDB Enterprise Server**
- When asked to install **MongoDB Compass**, unselect the checkbox. We will install a better version  later.
- Add MongoDB bin folder to your PATH: `C:\Program Files\MongoDB\Server\4.2\bin`
- To test, open the shell without connecting to a database:
```
mongo --nodb
```
- It sould open the shell, showing the version, like this
```
MongoDB shell version v4.2.5
>
```
- All right! You are ready to go!
- For now, just exit the shell
```
> exit
```


# Topics
- MangoDB Query Language
- Mongo DB Install
- Mongo DB Java Lib

# References
- [Mongo DB *Home PAge*](https://www.mongodb.com){target="_blank"}
- [Mongo DB University *MongoDb Courses*](https://university.mongodb.com/){target="_blank"}
- [Mongo DB Java *Java Driver for MongoDB*](https://docs.mongodb.com/ecosystem/drivers/java){target="_blank"}
{.links-list}