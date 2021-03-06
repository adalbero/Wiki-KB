---
title: Gradle
description: 
published: true
date: 2021-01-05T14:41:32.784Z
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

project.ext.libsDfc = { -> fileTree(dir: 'lib/dfc', include '**/*.jar'); }

subprojects {
	apply plugin: 'java'
	apply plugin: 'eclipse'
  
  repositories {
      jcenter()
  }

  dependencies {
	  implementation 'com.google.guava:guava:28.0-jre'
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
version "1.0.0"

dependencies {
	compile libsDfc()
}
```
`/ProjectB/build.gradle`
```groovy
version "1.0.0"

dependencies {
  compile project(':ProjectA')
}
```

### Task `dist`
* Copy all generated `jar` files to a `/dist` folder
* Make `build` depends on `dist`
```groovy
subprojects {
  ...
  
	task dist(type: Copy) {
  	from("$buildDir/libs")
    into("../dist")
  }
   
  build.dependsOn dist
   
}

```

### Gradle + JUnit 4
```groovy
dependencies {
	testImplementation ('junit:junit:4.12') {
		exclude group: 'org.hamcrest'
	}
	testImplementation 'org.hamcrest:hamcrest-library:1.3'
}
```

### Include sub-project Jar

```groovy
configurations {
  extraLibs
}

dependencies {
  extraLibs project (path: ':SubProject', configuration: 'archives')
}

jar {
  from configurations.extraLibs.collect { it.isDirectory() ? it : zipTree(it) }
}
```
