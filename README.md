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

# (For users in Mainland China) 导入
注意：所托管的库的更旧的版本之前是放在`jcenter()`上的。如果嫌麻烦不导入此Maven仓库而直接导入开源库的话，也可能导入成功，只不过导入的将是**历史版本**。

由于Github Raw在中国大陆（除香港、澳门外）被屏蔽，无法直接使用上述配置中的链接访问仓库。可以使用以下方式：

* 前往其他地区使用本仓库（自行查询解决方法）

* 使用特殊的网络连接方式并且应用在Gradle上（自行查询解决方法）

* 将`raw.githubusercontent.com`替换成可以直接访问的Gihub Raw镜像服务，这里介绍一个暂时可用的服务，如果之后此服务不可用也可以自行查找其他同类服务并替换链接

[FastGit](https://fastgit.org/) 它的Github Raw镜像为`raw.fastgit.org`，可将上述链接替换成`https://raw.fastgit.org/ryuunoakaihitomi/maven-repository/master`

最后的导入代码如下：

```groovy
dependencies {
    repositories {
        maven {
            // 注意看链接发生了变化
            url 'https://raw.fastgit.org/ryuunoakaihitomi/maven-repository/master'
        }
    }
    ...
}
```

# Including libraries

* [ReToast](https://github.com/ryuunoakaihitomi/ReToast)
* [PowerAct](https://github.com/ryuunoakaihitomi/PowerAct)