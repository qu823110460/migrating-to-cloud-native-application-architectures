# 组织变革

在本节中，我们将探讨采用云原生应用程序架构的组织在创建团队时需要进行的变革。这个重组背后的理论是著名的康威定律。我们的解决方案是在长周期的产品开发中，创建一个包含了各方面专业员工的团队，而不是将他们分离在单一的团队中，例如测试人员。

## 业务能力团队

设计系统的组织，最终产生的设计等同于组织之内、之间的沟通结构。

—Melvyn Conway

我们已经讨论了“从孤岛到DevOps”将IT组织成专门的信息孤岛的做法。我们很自然地创造了这些孤岛，并把个体放到与这些孤岛一致的团队中。但是当我们需要构建一个新的软件的时候会怎么样？

一个很常见的做法是成立一个项目团队。该团队向项目经理汇报，然后项目经理与各种孤岛合作，为项目所需的各个专业领域寻求“资源”。正如康威定律所言，这些团队将很自然地在系统中构筑起各种孤岛，我们最终得到的是联合各种孤岛相对应的孤立模块的架构：

- 数据访问层
- 服务层
- Web MVC层
- 消息层
- 等等

这些层次中的每一层都跨越了多个业务能力领域，使得在其之上的创新和部署独立于其他业务能力的新功能变的非常困难。

寻求迁移到将业务能力分离的微服务等云原生架构的公司经常采用Thoughtworks称之为的“逆康威定律”。他们没有建立一个与其组织结构图相匹配的架构，而是决定了他们想要的架构，并重组组织以匹配该架构。如果你这样做的话，根据康威定律，您所期望的架构终将出现。

因此，作为转向DevOps文化的一部分，我们组织了跨职能、业务能力的团队，开发的是产品而不再是项目。开发产品需要长期的付出，直到它们不再为企业提供价值为止。（直到你的代码不再运行在生产上为止！）构建、测试、交付和运营提供业务能力的服务所需的所有角色都存在于一个团队中，该团队不会向组织的其他部分交接代码。这些团队通常被组织为“双比萨队”，意思是如果不能用两个比萨饼喂饱，那就意味着团队规模太大了。

那么剩下的就是确定要创建的团队。如果我们遵循逆康威定律，我们将从组织的领域模型开始，并寻求可以封装在有限环境中的业务能力。一旦我们确定了这些能力，我们就可以创建为这些业务能力的整个生命周期负责的团队。 业务能力团队掌握其应用程序从开发到运营的整个生命周期。

## 平台运营团队

业务能力团队需要依赖于我们前面提到的”自助敏捷基础架构“。

事实上，我们可以这样来描述一种特殊的业务能力——开发、部署和运营业务的能力。这种能力应该是平台运营团队所具有的。

平台运营团队运营自助敏捷基础架构平台，并交付给业务能力团队使用。该团队通常包括传统的系统、网络和存储管理员角色。如果公司正在运营云平台，该团队也将拥有管理数据中心的团队或与他们紧密合作，并了解提供基础架构平台所需的硬件能力。

IT运营传统上通过各种基于单据的系统与客户进行互动。由于基于平台操作流来运行自助服务平台，因此必须提供不同形式的交互方式。正如业务能力团队之间通过定义好的API协议相互协作一样，平台运营团队也为该平台提供了API协议。业务能力团队不再需要排队申请应用环境和数据服务，而是采用更精简的方式构建按需申请环境和服务的自动化发布管道。