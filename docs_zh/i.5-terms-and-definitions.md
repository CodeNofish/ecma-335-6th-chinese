## I.5 Terms and definitions 术语和定义

For the purposes of this International Standard, the following definitions apply. Other terms are defined where they appear in *italic* type.

为本国际标准的目的，下列定义适用。其他术语在以*斜体*类型出现的地方定义。



**ANSI character:** A character from an implementation-defined 8-bit character set whose first 128 code points correspond exactly to those of ISO/IEC 10646.

**ANSI character:** 来自实现定义的8位字符集的字符，其前128个码位与ISO/IEC 10646的码位完全对应。



**ANSI string:** A string of ANSI characters, of which the final character has the value all-bits-zero.

**ANSI string:** 由ANSI字符组成的字符串，其最后一个字符的值为all-bits- 0。



**argument:** The expression supplied for a parameter at the point of the call to a method.

**argument:** 在调用方法时为参数提供的表达式。



**assembly:** A configured set of loadable code modules and other resources that together implement a unit of functionality.

**assembly:** 一组配置好的可加载代码模块和其他资源，它们一起实现一个功能单元



**attribute:** A characteristic of a type and/or its members that contains descriptive information. While the most common attributes are predefined, and have a specific encoding in the metadata associated with them, user-defined attributes can also be added to the metadata.

**attribute:** 类型和/或其成员包含描述性信息的特征。虽然最常见的属性是预定义的，并且在与它们关联的元数据中具有特定的编码，但用户定义的属性也可以添加到元数据中。



**behavior, implementation-specific:** Unspecified behavior, for which each implementation is required to document the choice it makes.

**behavior, implementation-specific:** 未指定的行为，每个实现都需要记录它所做的选择。



**behavior, unspecified:** Behavior, for a well-formed program construct and correct data, that depends on the implementation. The implementation is not required to document which behavior occurs.

**behavior, unspecified:** 对于格式良好的程序构造和正确的数据，行为取决于实现。实现不需要记录发生了哪些行为。



**behavior, undefined:** Behavior, such as might arise upon use of an erroneous program construct or erroneous data, for which this International Standard imposes no requirements. Undefined behavior can also be expected in cases when this International Standard omits the description of any explicit definition of behavior.

**behavior, undefined:** 本国际标准没有要求的行为，如使用错误的程序结构或错误的数据时可能出现的行为。当本国际标准省略了对行为的任何明确定义的描述时，也可能出现未定义的行为。



**boxing:** The conversion of a value having some value type, to a newly allocated instance of the reference type `System.Object`.

**boxing:** 将具有某种值类型的值转换为引用类型 `System.Object` 的新分配实例。



**Common Intermediate Language (CIL):** The instruction set understood by the VES.

**Common Intermediate Language (CIL):** VES能够理解的指令集。



**Common Language Infrastructure (CLI):** A specification for the format of executable code, and the run-time environment that can execute that code.

**Common Language Infrastructure (CLI):** 可执行代码格式的规范，以及可以执行该代码的运行时环境。



**Common Language Specification (CLS):** An agreement between language designers and framework (class library) designers. It specifies a subset of the CTS and a set of usage conventions.

**Common Language Specification (CLS):** 语言设计者和框架（类库）设计者之间的协议。它指定了CTS的一个子集和一组使用约定。



**Common Type System (CTS):** A unified type system that is shared by compilers, tools, and the CLI itself. It is the model that defines the rules the CLI follows when declaring, using, and managing types. The CTS establishes a framework that enables cross-language integration, type safety, and high performance code execution.

**Common Type System (CTS):** 由编译器、工具和CLI本身共享的统一类型系统。该模型定义了CLI在声明、使用和管理类型时遵循的规则。CTS建立了一个支持跨语言集成、类型安全和高性能代码执行的框架。



**delegate:** A reference type such that an instance of it can encapsulate one or more methods in an invocation list. Given a delegate instance and an appropriate set of arguments, one can invoke all of the methods in a delegate’s invocation list with that set of arguments.

**delegate:** A reference type such that an instance of it can encapsulate one or more methods in an invocation list. Given a delegate instance and an appropriate set of arguments, one can invoke all of the methods in a delegate’s invocation list with that set of arguments.



**event:** A member that enables an object or class to provide notifications.

**event:** 一个成员，可以为象或类提供通知。



**Execution Engine:** See **Virtual Execution System**.

**Execution Engine:** See **Virtual Execution System**.



**field:** A member that designates a typed memory location that stores some data in a program.

**field:** 可以指定在程序中存储某些数据的类型化内存位置的成员。



**garbage collection:** The process by which memory for managed data is allocated and released.

**garbage collection:** 为托管数据分配和释放内存的进程。



**generic argument:** The actual type used to instantiate a particular generic type or generic method.  For example, in `List<string>`, `string` is the generic argument corresponding to the generic parameter `T` in the generic type definition `List<T>`.

**generic argument:** 用于实例化特定泛型类型或泛型方法的实际类型。



**generic parameter:** A parameter within the definition of a generic type or generic method that acts as a place holder for a generic argument. For example, in the generic type definition `List<T>`, `T` is a generic parameter.

**generic parameter:** 泛型类型或泛型方法定义中的参数，用作泛型实参的占位符。



**generics:** The feature that allows types and methods to be defined such that they are parameterized with one or more generic parameters.

**generics:** 允许定义类型和方法的特性，以便用一个或多个泛型参数对它们进行参数化。



**library:** A repository for a set of types, which are grouped into one or more assemblies. A library can also contain modifications to types defined in other libraries. For example, a library can include additional methods, interfaces, and exceptions for types defined in other libraries.

**library:** 一组类型的存储库，这些类型被分组到一个或多个程序集中。库还可以包含对其他库中定义的类型的修改。例如，库可以包含其他库中定义的类型的附加方法、接口和异常。



**managed code:** Code that contains enough information to allow the CLI to provide a set of core services. For example, given an address for a method inside the code, the CLI must be able to locate the metadata describing that method. It must also be able to walk the stack, handle exceptions, and store and retrieve security information.

**managed code:** 包含足够信息的代码，以允许CLI提供一组核心服务。例如，给定代码中某个方法的地址，CLI必须能够定位描述该方法的元数据。它还必须能够遍历堆栈、处理异常以及存储和检索安全信息。



**managed data:** Data that is allocated and released automatically by the CLI, through a process called garbage collection.

**managed data:** 由CLI通过称为垃圾收集的进程自动分配和释放的数据。



**manifest:** That part of an assembly that specifies the following information about that assembly: its version, name, culture, and security requirements; which other files, if any, belong to that assembly, along with a cryptographic hash of each file; which of the types defined in other files of that assembly are to be exported from that assembly; and, optionally, a digital signature for the manifest itself, and the public key used to compute it.

**manifest:** 程序集中指定有关该程序集的以下信息的部分：其版本、名称、区域性和安全要求；哪些其他文件（如果有的话）属于该程序集，以及每个文件的加密散列；在该程序集的其他文件中定义的哪些类型将从该程序集导出；以及（可选的）清单本身的数字签名和用于计算它的公钥。



**member:** Any of the fields, array elements, methods, properties, and events of a type.

**member:** 类型的任何字段、数组元素、方法、属性和事件。



**metadata:** Data that describes and references the types defined by the CTS. Metadata is stored in a way that is independent of any particular programming language. Thus, metadata provides a common interchange mechanism for use between tools that manipulate programs (such as compilers and debuggers) as well as between these tools and the VES. method: A member that describes an operation that can be performed on values of an exact type.

**metadata:** 描述和引用CTS定义的类型的数据。元数据以一种独立于任何特定编程语言的方式存储。因此，元数据为操作程序的工具（如编译器和调试器）之间以及这些工具和VES之间提供了一种通用的交换机制。method：描述可对精确类型的值执行的操作的成员。



**method, generic:** A method (be it static, instance, or virtual), defined within a type, whose signature includes one or more generic parameters, not present in the type definition itself. The enclosing type itself might, or might not, be generic. For example, within the generic type `List<T>`, the generic method `S ConvertTo<S>()` is generic.

**method, generic:** 在类型中定义的方法（静态、实例或虚拟），其签名包括一个或多个泛型参数，而不是在类型定义本身中出现。封闭类型本身可能是泛型的，也可能不是。



**method, non-generic:** A method that is not generic.

**method, non-generic: **非泛型的方法。



**module:** A single file containing content that can be executed by the VES.

**module:** 包含可由VES执行的内容的单个文件。



**object:** An instance of a reference type. An object has more to it than a value. An object is self-typing; its type is explicitly stored in its representation. It has an identity that distinguishes it from all other objects, and it has slots that store other entities (which can be either objects or values). While the contents of its slots can be changed, the identity of an object never changes.

**object:** 引用类型的实例。对象不仅仅是一个值。对象是自类型化的；它的类型显式地存储在它的表示中。它有一个区别于所有其他对象的标识，并且它有存储其他实体（可以是对象或值）的槽。虽然可以更改其槽的内容，但对象的标识永远不会更改。



**parameter:** The name used in the header and body of a method to refer to an argument value supplied at the point of call.

**parameter:** 在方法的头部和主体中使用的名称，用于引用在调用点提供的参数值。



**profile:** A set of libraries, grouped together to form a consistent whole that provides a fixed level of functionality.

**profile:** 一组库，组合在一起形成一个一致的整体，提供固定级别的功能。



**property:** A member that defines a named value and the methods that access that value. A property definition defines the accessing contracts on that value. Hence, the property definition specifies which accessing methods exist and their respective method contracts.

**property:** 定义命名值和访问该值的方法的成员。属性定义定义了对该值的访问契约。因此，属性定义指定存在哪些访问方法以及它们各自的方法契约。



**signature:** The part of a contract that can be checked and automatically enforced. Signatures are formed by adding constraints to types and other signatures. A constraint is a limitation on the use of or allowed operations on a value or location.

**signature:** 合同中可被检查和自动执行的部分。签名是通过向类型和其他签名添加约束而形成的。约束是对值或位置的使用或允许的操作的限制。



**type, generic:** A type whose definition is parameterized by one or more other types; for example, `List<T>`, where `T` is a generic parameter. The CLI supports the creation and use of instances of generic types. For example, `List<int32>` or `List<string>`.

**type, generic:** 一种其定义由一个或多个其他类型参数化的类型；



**type, reference:** A type such that an instance of it contains a reference to its data. type, value: A type such that an instance of it directly contains all its data.

**type, reference:** 一种类型，它的实例包含对其数据的引用。



**unboxing:** The conversion of a value having type `System.Object`, whose run-time type is a value type, to a value type instance.

**unboxing:** 类型为`System` 的值的转换。`System.Object`，其运行时类型为值类型，转换为值类型实例。



**unmanaged code:** Code that is not managed.

**unmanaged code:** 不受管理的代码。



**unmanaged data:** Data that is not managed.

**unmanaged data:** 未管理的数据。



**value:** A simple bit pattern for something like an integer or a float. Each value has a type that describes both the storage that it occupies and the meanings of the bits in its representation, and also the operations that can be performed on that representation. Values are intended for representing the simple types and non-objects in programming languages.

**value:** 未管理的数据。整数或浮点数的简单位模式。每个值都有一个类型，该类型既描述了它所占用的存储空间，也描述了它的表示形式中比特的含义，还描述了在该表示形式上可以执行的操作。值用于表示编程语言中的简单类型和非对象。



**verification:** The checking of both CIL and its related metadata to ensure that the CIL code sequences do not permit any access to memory outside the program’s logical address space. In conjunction with the validation tests, verification ensures that the program cannot access memory or other resources to which it is not granted access.

**verification:** 检查CIL及其相关元数据，以确保CIL代码序列不允许访问程序逻辑地址空间以外的内存。与验证测试一起，验证可确保程序不能访问未授予其访问权限的内存或其他资源。



**Virtual Execution System (VES):** This system implements and enforces the CTS model. The VES is responsible for loading and running programs written for the CLI. It provides the services needed to execute managed code and data using the metadata to connect separately generated modules together at runtime. The VES is also known as the **Execution Engine**.

**Virtual Execution System (VES):** 该系统实现并实施了CTS模型。VES负责加载和运行为CLI编写的程序。它提供了执行托管代码和数据所需的服务，使用元数据在运行时将单独生成的模块连接在一起。VES也被称为“执行引擎”。
