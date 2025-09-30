## I.6.2 Relationship to managed metadata-driven execution 与元数据驱动的执行的关系

Metadata describes code by describing the types that the code defines and the types that it references externally. The compiler produces the metadata when the code is produced. Enough information is stored in the metadata to:

元数据通过描述代码定义的类型及其外部引用的类型来描述代码。编译器在生成代码时生成元数据。元数据中存储了足够的信息，以便：



 * **Manage code execution** &ndash; not just load and execute, but also memory management and execution state inspection.
 * **Manage code execution** &ndash; 不仅仅是加载和执行，还有内存管理和执行状态检查。



 * **Administer the code** &ndash; Installation, resolution, and other services.

 * **Administer the code** &ndash; 安装、解析和其他服务。



 * **Reference types in the code** &ndash; Importing into other languages and tools as well as scripting and automation support. The CTS assumes that the execution environment is metadata-driven. Using metadata allows the CLI to support:

 * **Reference types in the code** &ndash; 导入到其他语言和工具，以及脚本和自动化支持。CTS假设执行环境是元数据驱动的。使用元数据允许CLI支持：



 * **Multiple execution models** &ndash; The metadata allows the execution environment to deal with a mixture of interpreted, JIT-compiled, native, and legacy code, and still present uniform services to tools like debuggers and profilers, consistent exception handling and unwinding, reliable code access security, and efficient memory management.
 * **Multiple execution models** &ndash; 元数据允许执行环境处理解释代码、jit编译代码、本机代码和遗留代码的混合，并且仍然向调试器和分析器等工具提供统一的服务、一致的异常处理和解卷、可靠的代码访问安全性和高效的内存管理。



 * **Auto support for services** &ndash; Since the metadata is available at execution time, the execution environment and the base libraries can automatically supply support for reflection, automation, serialization, remote objects, and inter-operability with existing unmanaged native code with little or no effort on the part of the programmer.
 * **Auto support for services** &ndash; 由于元数据在执行时可用，因此执行环境和基本库可以自动提供对反射、自动化、序列化、远程对象以及与现有非托管本机代码的互操作性的支持，而程序员只需付出很少或根本不需要付出努力。



 * **Better optimization** &ndash; Using metadata references instead of physical offsets, layouts, and sizes allows the CLI to optimize the physical layouts of members and dispatch tables. In addition, this allows the generated code to be optimized to match the particular CPU or environment.
 * **Better optimization** &ndash; 使用元数据引用而不是物理偏移量、布局和大小，CLI可以优化成员和调度表的物理布局。此外，这允许优化生成的代码以匹配特定的CPU或环境。



 * **Reduced binding brittleness** &ndash; Using metadata references reduces version-to-version brittleness by replacing compile-time object layout with load-time layout and binding by name.
 * **Reduced binding brittleness** &ndash; 使用元数据引用通过用加载时布局和按名称绑定取代编译时对象布局，减少了版本间的脆弱性。



 * **Flexible deployment resolution** &ndash; Since we can have metadata for both the reference and the definition of a type, more robust and flexible deployment and resolution mechanisms are possible. Resolution means that by looking in the appropriate set of places it is possible to find the implementation that best satisfies these requirements for use in this context. There are five elements of information in the foregoing: requirements and context are made available via metadata; where to look, how to find an implementation, and how to decide the best match all come from application packaging and deployment.
 * **Flexible deployment resolution** &ndash; 由于我们可以同时拥有类型的引用和定义的元数据，因此可以实现更健壮、更灵活的部署和解析机制。解析意味着通过查找适当的位置集，可以找到最能满足在此上下文中使用的这些需求的实现。上述信息有五个要素：需求和上下文通过元数据提供；在哪里查找、如何找到实现以及如何决定最佳匹配都来自于应用程序打包和部署。
