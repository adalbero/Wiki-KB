---
title: MongoDB KB
description: Tricks & Tips
published: true
date: 2020-03-28T17:41:14.804Z
tags: 
---

# Overview
MongoDB Shell is a CLI to manage MopngoDB server.

# Download
- Download **MongoDB Shell**.
  - Windows: [download](https://downloads.mongodb.org/win32/mongodb-shell-win32-x86_64-2012plus-4.2.5.zip)
  - MacOS:  `brew install mongodb/brew/mongodb-community-shell`
# Install
You can install **MongoDB Shell** in any computer. It is only one .exe file.

- Copy the `mongo.exe` from `/bin` folder in the zip file to any folder in your PATH.


# Tricks & Tips

## Connection
```shell
mongo "mongodb+srv://<host>/<database>" --username <user> --password <pass>
```


