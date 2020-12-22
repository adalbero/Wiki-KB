---
title: Gradle
description: 
published: true
date: 2020-12-22T13:51:27.428Z
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

sourceCompatibility = 1.8
targetCompatibility = 1.8
```

## Java with sub-projects

```
/Eclipse
|-- .metadata
`-- /Root
    |-- /lib
    |   `-- /dfc
    |       `-- dfc.jar
    |-- /ProjectA
    |   `-- build.gradle
    |-- /ProjectB
    |   `-- build.gradle
    |-- build.gradle
    `-- settings.gradle
```
    
`/Root/build.gradle`
```groovy
apply plugin: 'java'
apply plugin: 'eclipse'

project.ext.libsDfc = { -> fileTree(dir: 'lib/dfc', include '**/*.jar'); }
repositories {
  jcenter()
}

dependencies {
  implementation 'com.google.guava:guava:28.0-jre'
  testImplementation 'junit:junit:4.12'
}

subprojects {
  repositories {
      jcenter()
  }

  dependencies {
  }

  sourceCompatibility = 1.8
  targetCompatibility = 1.8
}
```

`/Root/settings.gradle`
```groovy
rootProject.name = 'Root'

include 'ProjectA', 'ProjectB'
```

`/ProjectA/build.gradle`
```groovy
dependencies {
	compile libsDfc()
}
```
`/ProjectB/build.gradle`
```groovy
dependencies {
  compile project(':ProjectA')
}
```
