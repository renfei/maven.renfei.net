---
name: 新增仓库代理请求
about: 新增仓库代理请求
title: '新增仓库代理请求'
labels: 'feat'
assignees: 'renfei'
---

## 已经搜索过确实找不到?

您是否已经执行过搜索，确实找不到依赖的包信息？

搜索地址为 ：[https://maven.renfei.net/nexus/#browse/search](https://maven.renfei.net/nexus/#browse/search)

- [x] 是的，我已经搜索过

## 请提供 Maven 坐标信息

请提供您依赖的包坐标，包含：`groupId`、`artifactId`、`version` 信息，请修改下方的坐标信息：
```xml
<dependency>
    <groupId>junit</groupId>
    <artifactId>junit</artifactId>
    <version>4.13.2</version>
</dependency>
```

## 您是否知道提供此包的官方仓库或官方网址？

如果您知道此包的官方仓库地址、官方网址，请一起提供给我。不知道也没关系，我会为您进行搜索。

## 是否为私有包？

一般情况下，我不会提供私有包的代理，但某些情况下可以为您增加私有包的代理，您需要满足以下条件：

- [x] 包为可公开不涉密的内容，一旦发布整个互联网可以公开访问
- [x] `groupId` 为域名格式，并且使用对应的域名后缀邮箱向我发送邮件，确定允许我进行代理
  > 例如：
  > `groupId = net.renfei` ; 然后使用 `renfei.net` 后缀的邮箱比如 `example@renfei.net` 向我发送邮件
  > 确定允许我进行代理，提供仓库地址，或者您没有自建仓库，也可以在邮件中在附件中直接提供 Jar 包。
