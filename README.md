# My Maven Repository

# Background
Since [jcenter is shutting down](https://jfrog.com/blog/into-the-sunset-bintray-jcenter-gocenter-and-chartcenter/), I need a new public maven repository to store my library publications.
The most common choice is maven central or jitpack, but I prefer to choice a platform with more freedom.
So here it is.

# Import
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

# Including libraries

* [ReToast](https://github.com/ryuunoakaihitomi/ReToast)
* [PowerAct](https://github.com/ryuunoakaihitomi/PowerAct)
* [PdfiumAndroid](https://github.com/ryuunoakaihitomi/PdfiumAndroid)
* [AndroidPdfViewer](https://github.com/ryuunoakaihitomi/AndroidPdfViewer)
* [Android-Multi-Select-Dialog](https://github.com/ryuunoakaihitomi/Android-Multi-Select-Dialog)

# Backup libraries

* [FFmpegKit](https://github.com/arthenica/ffmpeg-kit) `Audio`