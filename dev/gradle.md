---
title: Gradle
description: 
published: true
date: 2020-12-22T07:16:32.359Z
tags: gradle, java, eclipse
editor: markdown
dateCreated: 2020-12-22T07:16:32.359Z
---

# Gradle
Your content here

## Java project

```groovy
apply plugin: 'java'
apply plugin: 'eclipse'

repositories {
    jcenter()
}

dependencies {
    implementation 'com.google.guava:guava:28.0-jre'
    testImplementation 'junit:junit:4.12'
}
```