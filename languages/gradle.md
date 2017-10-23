# Gradle

## How to enforce that  all dependencies use the same version, also transitive ones

```groovy
configurations.all {
    resolutionStrategy {
        // fail eagerly on version conflict (includes transitive dependencies)
        // e.g. multiple different versions of the same dependency (group and name are equal)
        failOnVersionConflict()
    }
}
```

## How to see dependency graph

```groovy
gradle dependencies --configuration runtime
```

## add/check license headers in source files

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

## print test names

```groovy
tasks.matching {it instanceof Test}.all {
    testLogging.events = ["failed", "passed", "skipped"]
}
```

## How to specify java version for compileJava task

```bash
./gradlew -Dorg.gradle.java.home=/path_to_jdk_directory
```

