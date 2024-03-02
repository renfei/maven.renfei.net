[[中文](./README.md)｜[English](./README-EN.md)]

# Maven Public Proxy Repository

Maven Public Proxy Repository, acting as a proxy for various common Maven repositories, helps developers effectively solve the problem of finding some unpopular dependency packages and accelerates the compilation and construction of the program.

- [https://maven.renfei.net](https://maven.renfei.net)

## Maven Configuration Guide

Open the configuration file of Maven (usually in the `conf/settings.xml` directory of the Maven installation), and add a mirror child node in the `<mirrors></mirrors>` tag:

```xml
<mirror>
  <id>renfeimaven</id>
  <mirrorOf>*</mirrorOf>
  <name>RENFEI公共仓库</name>
  <url>https://maven.renfei.net/nexus/repository/public/</url>
</mirror>
```

## Gradle Configuration Guide

Add the following code to the build.gradle file:

```gradle
allprojects {
  repositories {
    maven {
      url 'https://maven.renfei.net/nexus/repository/public/'
    }
    mavenLocal()
    mavenCentral()
  }
}
```

## Add a new proxy repository

If you still cannot find the dependency package you need after using our public proxy repository, you can contact us to add a proxy address. We are more than happy to help you solve your problem.

Please submit an issue: [https://github.com/renfei/maven.renfei.net/issues/new](https://github.com/renfei/maven.renfei.net/issues/new?assignees=renfei&labels=feat&projects=&template=feat_repositorie_request.md&title=%E6%96%B0%E5%A2%9E%E4%BB%93%E5%BA%93%E4%BB%A3%E7%90%86%E8%AF%B7%E6%B1%82)
