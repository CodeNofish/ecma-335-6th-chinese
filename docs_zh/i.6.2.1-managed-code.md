## I.6.2.1 Managed code 托管代码

**Managed code** is code that provides enough information to allow the CLI to provide a set of core services, including

**托管代码** 是提供足够信息的代码，允许CLI提供一组核心服务，包括



 * Given an address inside the code for a method, locate the metadata describing the method
 * 给定方法代码中的地址，定位描述该方法的元数据



 * Walk the stack
 * 遍历堆栈



 * Handle exceptions

 * 处理异常



 * Store and retrieve security information
 * 存储和检索安全信息



 This standard specifies a particular instruction set, the CIL (see [Partition III](#todo-missing-hyperlink)), and a file format (see [Partition II](#todo-missing-hyperlink)) for storing and transmitting managed code.

这个标准指定了一个特定的指令集，CIL（参见[Partition III](#todo-missing-hyperlink)）和一个文件格式（参见[Partition II](#todo-missing-hyperlink)），用于存储和传输托管代码。
