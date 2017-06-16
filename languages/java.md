# Java

## Libraries to check out

* [JDBI is a SQL convenience library](http://www.jdbi.org/)
* [HikariCP, a solid high-performance JDBC connection pool](https://github.com/brettwooldridge/HikariCP)

## Javadoc

How to link to methods or classes

```
{@link package.class#member label}
```

## UNIX TOOLS TO TROUBLESHOOT JAVA

### jps – java process information

```
jps
```
It lists all java-processes.

[Documentation](http://docs.oracle.com/javase/7/docs/technotes/tools/share/jps.html)

### lsof – List of open files

```
lsof -p <pid>
```

Given the process id, it shows every file that is opened by that process.

### jstack

```
jstack <pid>
```
It dumps out all threads and what they are doing

## Testing

### How to test that an exception is thrown

[expected exception in test](https://monkeyisland.pl/2010/07/26/expected-exception-in-tests/)

## Gradle

### How to enforce that  all dependencies use the same version, also transitive ones

```groovy
configurations.all {
    resolutionStrategy {
        // fail eagerly on version conflict (includes transitive dependencies)
        // e.g. multiple different versions of the same dependency (group and name are equal)
        failOnVersionConflict()
    }
}
```

### How to see dependency graph

```groovy
gradle dependencies --configuration runtime
```

### add/check license headers in source files

[link](https://github.com/hierynomus/license-gradle-plugin)

```groovy
buildscript {
    repositories {
        mavenCentral()
        maven {
            url "https://plugins.gradle.org/m2/"
        }
    }
    dependencies {
        classpath "gradle.plugin.nl.javadude.gradle.plugins:license-gradle-plugin:0.13.1"
    }
}

apply plugin: "com.github.hierynomus.license"

license {
    mapping('java', 'SLASHSTAR_STYLE')
}
```

### Use LinkedHashMap instead of HashMap

[link](https://publicobject.com/2016/02/08/linkedhashmap-is-always-better-than-hashmap/)