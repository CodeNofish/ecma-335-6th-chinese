## I.1 Scope

This International Standard defines the Common Language Infrastructure (CLI) in which applications written in multiple high-level languages can be executed in different system environments without the need to rewrite those applications to take into consideration the unique characteristics of those environments. This International Standard consists of the following parts:

本国际标准定义了公共语言基础结构（CLI），其中用多种高级语言编写的应用程序 可以在不同的系统环境中执行，而无需根据这些环境的独特特征重写这些应用程序。本国际标准由以下部分组成：



 * **Partition I: Concepts and Architecture** &ndash; Describes the overall architecture of the CLI, and provides the normative description of the Common Type System (CTS), the Virtual Execution System (VES), and the Common Language Specification (CLS). It also provides an informative description of the metadata.
 * **分区1：概念和体系结构**，描述CLI的总体体系结构，对CTS （Common Type System）、VES （Virtual Execution System）和CLS （Common Language Specification）进行规范描述。它还提供了元数据的信息描述。



 * **Partition II: Metadata Definition and Semantics** &ndash; Provides the normative description of the metadata: its physical layout (as a file format), its logical contents (as a set of tables and their relationships), and its semantics (as seen from a hypothetical assembler, *ilasm*).
 * **分区II：元数据定义和语义** ，提供元数据的规范描述：它的物理布局（例如文件格式），它的逻辑内容（例如一组表及其关系），以及它的语义（如 假设汇编器*ilasm* ）。



 * **Partition III: CIL Instruction Set** &ndash; Describes the Common Intermediate Language (CIL) instruction set.
 * **分区III: CIL指令集**，描述公共中间语言（CIL）指令集



 * **Partition IV: Profiles and Libraries** &ndash; Provides an overview of the CLI Libraries, and a specification of their factoring into Profiles and Libraries. A companion file, `CLILibrary.xml`, considered to be part of this Partition, but distributed in XML format, provides details of each class, value type, and interface in the CLI Libraries.
 * **分区IV：配置文件和库** ，提供CLI库的概述，以及一个规范 可以把它们分解为配置文件和库。一个配套文件`CLILibrary.xml` 被认为是这个分区的一部分，但以XML格式分发，它提供了CLI库中每个类、值类型和接口的详细信息。



 * **Partition V: Debug Interchange Format** &ndash; Describes a standard way to interchange debugging information between CLI producers and consumers.
 * **分区V：调试交换格式** ，描述在CLI生产者和消费者之间交换调试信息的标准方法。



 * **Partition VI: Annexes** &ndash; Contains some sample programs written in CIL Assembly Language (ILAsm), information about a particular implementation of an assembler, a machine-readable description of the CIL instruction set which can be used to derive parts of the grammar used by this assembler as well as other tools that manipulate CIL, a set of guidelines used in the design of the libraries of [Partition IV](#todo-missing-hyperlink), and portability considerations.
 * **分区VI：附件** ，包含一些用CIL汇编语言（ILAsm）编写的示例程序，关于汇编器的特定实现的信息，CIL指令集的机器可读描述，可用于派生该汇编器使用的部分语法以及操作CIL的其他工具，一组用于指导库设计的方针，以及可移植性考虑。

