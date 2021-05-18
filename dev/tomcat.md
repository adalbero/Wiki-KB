---
title: Tomcat Tips
description: 
published: true
date: 2021-05-18T16:47:46.944Z
tags: 
editor: markdown
dateCreated: 2021-05-18T16:47:46.944Z
---

# Tomcat tips

## Configure Remote Debugging

- Open (or create) file `setenv.bat` on `Tomcat/bin`
```
CATALINA_OPTS="-agentlib:jdwp=transport=dt_socket,address=8087,server=y,suspend=n"
```