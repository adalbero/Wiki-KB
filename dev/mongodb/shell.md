---
title: MongoDB KB
description: Tricks & Tips
published: true
date: 2020-03-26T17:10:37.279Z
tags: 
---

# Overview
MongoDB Shell is a CLI to manage MopngoDB server.

# Download
- Download **MongoDB Shell**. [Ver 4.2.5](https://downloads.mongodb.org/win32/mongodb-shell-win32-x86_64-2012plus-4.2.5.zip)

# Install
You can install **MongoDB Shell** in any computer. It is only one .exe file.

- Copy the `mongo.exe` from `/bin` folder in the zip file to any folder in your PATH.


# Tricks & Tips

## Connection
```shell
mongo "mongodb+srv://<host>/<database>" --username <user> --password <pass>
```


