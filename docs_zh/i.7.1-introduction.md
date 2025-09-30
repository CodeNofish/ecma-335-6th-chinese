## I.7.1 Introduction

The CLS is a set of rules intended to promote language interoperability. These rules shall be followed in order to conform to the CLS. They are described in greater detail in subsequent clauses and are summarized in §[I.11](i.11-collected-common-language-specification-rules.md). CLS conformance is a characteristic of types that are generated for execution on a CLI implementation. Such types must conform to the CLI standard, in addition to the CLS rules. These additional rules apply only to types that are visible in assemblies other than those in which they are defined, and to the members that are accessible outside the assembly; that is, those that have an accessibility of **public**, **family** (but not on sealed types), or **family-or-assembly** (but not on sealed types).

CLS是一组旨在促进语言互操作性的规则。为了符合CLS，应遵守这些规则。它们将在后面的条款中作更详细的描述，并在  §[I.11](i.11-collected-common-language-specification-rules.md)  中作了总结。CLS一致性是为在CLI实现上执行而生成的类型的特征。除了CLS规则外，这些类型还必须符合CLI标准。这些附加规则仅适用于在程序集中可见的类型，以及可在程序集中外部访问的成员；也就是说，那些可访问性为**public**、**family**（但不包括密封类型）或**family-or-assembly**（但不包括密封类型）的对象。



_[Note:_ A library consisting of CLS-compliant code is herein referred to as a *framework*. Compilers that generate code for the CLI can be designed to make use of such libraries, but not to be able to produce or extend such library code. These compilers are referred to as *consumers*. Compilers that are designed to both produce and extend frameworks are referred to as *extenders*. In the description of each CLS rule, additional informative text is provided to assist the reader in understanding the rule's implication for each of these situations. _end note]_

注：由兼容cls的代码组成的库在这里被称为“框架”。为CLI生成代码的编译器可以设计为使用这些库，但不能生成或扩展这些库代码。这些编译器被称为“消费者”。设计用于生成和扩展框架的编译器被称为“扩展器”。在每个CLS规则的描述中，提供了额外的信息文本，以帮助读者理解规则对每种情况的含义。_end注)_
