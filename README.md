# SOFAArk 工程用例 

SOFAArk 提供了两个样例工程来演示 `Ark Plugin` 和 `Ark 包` 的使用；样例工程目录组织如下：

```
.
│
├── sample-ark-plugin 
│ 
└── sample-springboot-ark 

```

## sample-ark-plugin
该工程演示如何使用官方提供的 `Maven` 插件 `sofa-ark-plugin-maven-plugin` 来构建一个标准的 `Ark Plugin`，详细可参考 [README](./sample-ark-plugin/README.md)。

## sample-springboot-ark
该工程演示如何使用官方提供的 `Maven` 插件 `sofa-ark-maven-plugin` 将一个普通的 Spring Boot 应用打包成一个 `Ark 包`；需要注意的是，因为该工程依赖另一个用例工程 [`sample-ark-plugin`](./sample-ark-plugin/README.md) 打包出来的 `Ark Plugin`, 由于Ark Plugin必须以jar包的方式导入工程无法使用classPath方式启动，请务必提前安装该 `Ark Plugin` 至本地 maven 仓库；详细请参考 [README](./sample-springboot-ark/README.md)。

IDE 里启动是请带上如下参数：
```properties
-Dsofa.ark.embed.enable=true
```

如果需要开启类隔离功能请带上如下参数：
```properties
-Dsofa.ark.embed.enable=false
```