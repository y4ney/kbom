## KBOM Schema

以下部分描述了KBOM的高级对象模型。

集群细节

实例
- Name
- Hostname
- CloudType
- Creation Timestamp
- Capacity
- OS Version
- Kernel Version
- Architecture
- CRI Version
- Kubelet Version
- Kube Proxy Version

镜像
- Name
- Digest

Kube对象
- Kind
- Api Version
- Count
- Details

这种整体结构提供了一个由社区扩展的基本规格。 该标准的意图是可扩展，以支持整个行业的各种用例。
