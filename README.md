[[中文](./README.md)｜[English](./README-EN.md)]

# Maven 公共代理仓库

Maven 公共代理仓库，代理多种常见 Maven 仓库，帮助开发者有效解决部分冷门依赖包无法找到的问题，加速程序编译构建。

- [https://maven.renfei.net](https://maven.renfei.net)

## Maven 配置指南

打开 maven 的配置文件（一般在 maven 安装目录的 `conf/settings.xml`），在 `<mirrors></mirrors>` 标签中添加 mirror 子节点:

```xml
<mirror>
  <id>renfeimaven</id>
  <mirrorOf>*</mirrorOf>
  <name>RENFEI公共仓库</name>
  <url>https://maven.renfei.net/nexus/repository/public/</url>
</mirror>
```

## Gradle 配置指南

在 build.gradle 文件中加入以下代码:

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

## 添加代理新的代理仓库

如果您使用我们的公开代理仓库，还是未能找到您所需要的依赖包，您可以联系我们添加代理地址。我们很乐意能能够解决您的问题。

请提交 issue: [https://github.com/renfei/maven.renfei.net/issues/new](https://github.com/renfei/maven.renfei.net/issues/new?assignees=renfei&labels=feat&projects=&template=feat_repositorie_request.md&title=%E6%96%B0%E5%A2%9E%E4%BB%93%E5%BA%93%E4%BB%A3%E7%90%86%E8%AF%B7%E6%B1%82)
