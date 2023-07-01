# KBOM - Kubernetes 物料清单

![GitHub release (latest by date)](https://img.shields.io/github/v/release/ksoclabs/kbom)
![Hex.pm](https://img.shields.io/hexpm/l/apa)
[![Go Report Card](https://goreportcard.com/badge/github.com/ksoclabs/kbom)](https://goreportcard.com/report/github.com/ksoclabs/kbom)
[![FOSSA Status](https://app.fossa.com/api/projects/custom%2B37386%2Fgithub.com%2Fksoclabs%2Fkbom.svg?type=shield)](https://app.fossa.com/projects/custom%2B37386%2Fgithub.com%2Fksoclabs%2Fkbom?ref=badge_shield)
[![OpenSSF Best Practices](https://bestpractices.coreinfrastructure.org/projects/7273/badge)](https://bestpractices.coreinfrastructure.org/projects/7273)
Kubernetes物料清单（KBOM）标准提供了对整个行业广泛使用的容器编排工具的了解。

作为初稿，我们已经创建了一个大致的规范，它应该与其他物料清单（BOM）标准保持一致。

KBOM项目提供了一个初始的JSON规范，并且可以在各种云服务提供商（CSP）以及自己构建的Kubernetes上进行扩展。

## 快速开始

### 安装

```sh
brew install ksoclabs/homebrew-kbom/kbom
```

or

```sh
make build
```

### 使用

`KBOM generate`为您的Kubernetes集群生成一个KBOM文件

```sh
kbom generate [flags]
```

可选标志包括：

```plain
  -f, --format string     Format (json, yaml) (default "json")
  -h, --help              Help for generate
  -p, --out-path string   Path to write KBOM file to. Works only with --output=file (default ".")
  -o, --output string     Output (stdout, file) (default "stdout")
      --short             Short - only include metadata, nodes, images and resources counters
```

## 模型
高层对象模型可以在[这里](docs/schema.md)中找到。

## 支持的 Kubernetes 版本
我们已经用高于*v1.19*更新的所有版本测试了*kbom*，并且可以确认它与每个版本完全兼容。这意味着您可以自信地使用我们的工具，知道它已经通过彻底的测试。

## 支持的云提供商
我们已与所有主要云提供商一起测试了我们的工具，包括`Azure`、`AWS`和`Google Cloud`。 当然，可以为任何K8s集群生成“kbom”文件，但请记住，
在某些情况下不是所有元数据条目都将被设置。

## 贡献

KBOM是Apache 2.0许可的，并通过GitHub拉取请求接受贡献。详情请参阅[CONTRIBUTING](CONTRIBUTING.md)
