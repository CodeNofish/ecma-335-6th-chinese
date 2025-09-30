## I.6 Overview of the Common Language Infrastructure

The Common Language Infrastructure (CLI) provides a specification for executable code and the execution environment (the Virtual Execution System) in which it runs. Executable code is presented to the VES as modules. A module is a single file containing executable content in the format specified in [Partition II](ii.6-assemblies-manifests-and-modules.md).

公共语言基础结构（CLI）为可执行代码及其运行的执行环境（虚拟执行系统）提供了规范。可执行代码以模块的形式呈现给VES。模块是一个包含可执行内容的文件，其格式在  [Partition II](ii.6-assemblies-manifests-and-modules.md) 中定义.



> _The remainder of this clause and its subclauses contain only informative text._

> 本条款及其子条款的其余部分仅包含资料性文本。



At the center of the CLI is a unified type system, the Common Type System that is shared by compilers, tools, and the CLI itself. It is the model that defines the rules the CLI follows when declaring, using, and managing types. The CTS establishes a framework that enables crosslanguage integration, type safety, and high performance code execution. This clause describes the architecture of the CLI by describing the CTS.

CLI的中心是一个统一的类型系统，即由编译器、工具和CLI本身共享的公共类型系统。该模型定义了CLI在声明、使用和管理类型时遵循的规则。CTS建立了一个支持跨语言集成、类型安全和高性能代码执行的框架。本节通过描述CTS来介绍CLI的体系结构。



The following four areas are covered in this clause:

本条款包括以下四个方面：



 * **The Common Type System (CTS)** &ndash; The CTS provides a rich type system that supports the types and operations found in many programming languages. The CTS is intended to support the complete implementation of a wide range of programming languages. See §[I.8](i.8-common-type-system.md)
 * **The Common Type System (CTS)** &ndash; CTS提供了一个丰富的类型系统，支持许多编程语言中的类型和操作。CTS旨在支持各种编程语言的完整实现。See §[I.8](i.8-common-type-system.md)



 * **Metadata** &ndash; The CLI uses metadata to describe and reference the types defined by the CTS. Metadata is stored (that is, persisted) in a way that is independent of any particular programming language. Thus, metadata provides a common interchange mechanism for use between tools (such as compilers and debuggers) that manipulate programs, as well as between these tools and the VES. See §[I.9](i.9-metadata.md).
 * **Metadata** &ndash; CLI使用元数据来描述和引用CTS定义的类型。元数据以一种独立于任何特定编程语言的方式存储（即持久化）。因此，元数据为操作程序的工具（如编译器和调试器）之间以及这些工具和VES之间提供了一种通用的交换机制。See §[I.9](i.9-metadata.md).



 * **The Common Language Specification (CLS)** &ndash; The CLS is an agreement between language designers and framework (that is, class library) designers.  It specifies a subset of the CTS and a set of usage conventions.  Languages provide their users the greatest ability to access frameworks by implementing at least those parts of the CTS that are part of the CLS. Similarly, frameworks will be most widely used if their publicly exported aspects (e.g., classes, interfaces, methods, and fields) use only types that are part of the CLS and that adhere to the CLS conventions. See §[I.10](i.10-name-and-type-rules-for-the-common-language-specification.md).
 * **The Common Language Specification (CLS)** &ndash; CLS是语言设计者和框架（即类库）设计者之间的协议。它指定了CTS的一个子集和一组使用约定。语言通过实现至少属于CLS的CTS部分，为其用户提供了访问框架的最大能力。类似地，如果框架的公开导出方面（例如，类、接口、方法和字段）只使用属于CLS的一部分并遵守CLS约定的类型，那么框架将得到最广泛的使用。 See §[I.10](i.10-name-and-type-rules-for-the-common-language-specification.md).



 * **The Virtual Execution System (VES)** &ndash; The VES implements and enforces the CTS model. The VES is responsible for loading and running programs written for the CLI. It provides the services needed to execute managed code and data, using the metadata to connect separately generated modules together at runtime (late binding). See §[I.12](i.12-virtual-execution-system.md).
 * **The Virtual Execution System (VES)** &ndash; VES实现并执行CTS模型。VES负责加载和运行为CLI编写的程序。它提供执行托管代码和数据所需的服务，使用元数据在运行时将单独生成的模块连接在一起（后期绑定）。See §[I.12](i.12-virtual-execution-system.md).



Together, these aspects of the CLI form a unifying infrastructure for designing, developing, deploying, and executing distributed components and applications. The appropriate subset of the CTS is available from each programming language that targets the CLI. Language-based tools communicate with each other and with the VES using metadata to define and reference the types used to construct the application. The VES uses the metadata to create instances of the types as needed and to provide data type information to other parts of the infrastructure (such as remoting services, assembly downloading, and security).

CLI的这些方面共同构成了一个统一的基础设施，用于设计、开发、部署和执行分布式组件和应用程序。针对CLI的每种编程语言都有CTS的适当子集。基于语言的工具彼此通信，并使用元数据与VES通信，以定义和引用用于构造应用程序的类型。VES使用元数据根据需要创建类型的实例，并向基础设施的其他部分（如远程服务、程序集下载和安全性）提供数据类型信息。
