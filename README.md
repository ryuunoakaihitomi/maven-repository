# My Maven Repository

# ⚠ TIME TO MIGRATE TO [GITHUB PACKAGES](https://github.com/features/packages).

This git repository used to store artifacts will no longer be available. The lastest version of artifacts are removed to remind users to read this README.md again.

# Usage

** 💡 Remember to replace `<library name>` and `<import statement>` to the correct value according to the documentation of the library you want to import.**

(If you think you are using a relatively new Android Studio, you can just read the next section)

Import the library in app(module-level) build.gradle:

```groovy
dependencies {
    repositories {
        // 👇
        maven {
            url 'https://maven.pkg.github.com/ryuunoakaihitomi/<library name>'
            credentials {
                username = 'ryuunoakaihitomi'
                password = 'ghp_extQ2D8b8NztcmmUyMzngcthP2VYJm0cEGS\u0020'
            }
        }
    }
    <import statement> // 👈
    // ...
}
```

### For Android studio Arctic Fox 2020.3.1+

If you encountered this error,
> Build was configured to prefer settings repositories over project repositories but repository 'maven' was added by build file 'app\build.gradle'

you have to perform it in two steps...

① Import the maven repository in settings.gradle:

```groovy
dependencyResolutionManagement {
    repositories {
        // ...
        // 👇
        maven {
            url 'https://maven.pkg.github.com/ryuunoakaihitomi/<library name>'
            credentials {
                username = 'ryuunoakaihitomi'
                password = 'ghp_extQ2D8b8NztcmmUyMzngcthP2VYJm0cEGS\u0020'
            }
        }
    }
}
```

② Import the library in app(module-level) build.gradle

```groovy
dependencies {
    // ...
    <import statement> // 👈
}
```

# Including libraries

* [ReToast](https://github.com/ryuunoakaihitomi/ReToast)
* [PowerAct](https://github.com/ryuunoakaihitomi/PowerAct)

# Legacy Usage

This was the previous usage of this repository, which is now deprecated.

```groovy

dependencies {
    repositories {
        maven {
            url 'https://raw.githubusercontent.com/ryuunoakaihitomi/maven-repository/master'
        }
    }
    ...
}

```
