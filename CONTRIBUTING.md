# 贡献

KBOM遵循[Apache 2.0 许可证](https://github.com/ksoclabs/kbom/blob/main/LICENSE)，
并接受通过GitHub拉取请求的贡献。本文档概述了一些规范，以便更容易地接受您的贡献。


我们非常欢迎对问题和文档的改进，同时也欢迎对代码的改进。

## 来源证书
通过对该项目的贡献，您同意遵守《开发者来源证书》（DCO）。该文件由Linux内核社区创建，是一个简单的声明，作为贡献者，您有法律权利进行贡献。

我们要求所有提交的代码都要进行签名。通过在提交中加入您的签名，您证明您编写了补丁或者按照[DCO](DCO)的规定有权贡献这些材料。


签名方式: `Firstname Lastname <firstname.lastname@example.com>`

签名必须包含您的真实姓名 （抱歉，不能假名或匿名贡献） 如果您的`user.name`和`user.email`在您的Git配置中配置，
您可以使用`git commit -s`自动签署提交。

## 讨论
讨论想法和规格：[GitHub Discussions](https://github.com/ksoclabs/kbom/discussions)

## 如何在本地环境中运行KBOM生成器

先决条件

* go >= 1.20
* kind
* golangci-lint

I初始化项目:

```bash
make initialise
```

要生成您的第一个KBOM文件，我们需要访问一个Kubernetes集群。 如果您没有任何集群，您可以使用`Kind`创建一个本地集群。

使用kind创建集群（选做）:

```bash
kind create cluster --name kbom-test
```

构建 `kbom` 二进制文件:

```bash
make build
```

生成你的第一个`kbom`文件：

```bash
./kbom generate
```

## 验收政策

这些事情将使PR更有可能被接受：
* 良好描述的需求
* 新代码的测试
* 旧代码的测试！
* 新代码和测试遵循旧代码和测试中的约定
* 良好的提交消息（见下文）
* 所有代码必须遵守 [Go代码审查评论](https://github.com/golang/go/wiki/CodeReviewComments)
* 命名应遵守 [What's in a name](https://talks.golang.org/2014/names.slide#1)
* 代码必须在Linux和Darwin上通过普通的`go build`构建
* 代码应具有适当的测试覆盖率，并且写的测试用例可以成功运行`go test`

一般来说，一旦一个维护者认可了PR，我们将合并PR。 对于实质性的变化，可能会有更多的人参与其中，而你可能会 被要求重新提交PR或将更改分成多个PR。
