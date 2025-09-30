## I.6.1 Relationship to type safety 与类型安全的关系

Type safety is usually discussed in terms of what it does (e.g., guaranteeing encapsulation between different objects) or in terms of what it prevents (e.g., memory corruption by writing where one shouldn't). However, from the point of view of the CTS, type safety guarantees that:

类型安全通常是根据它所做的事情（例如，保证不同对象之间的封装）或根据它所防止的事情（例如，在不应该写的地方写内存损坏）来讨论的。然而，从CTS的角度来看，类型安全保证：



 * **References are what they say they are** &ndash; Every reference is typed, the object or value referenced also has a type, and these types are assignment compatible (see §[I.8.7](i.8.7-assignment-compatibility.md)).
 * 每个引用都是有类型的，被引用的对象或值也有一个类型，这些类型是赋值兼容的 (see §[I.8.7](i.8.7-assignment-compatibility.md)).



 * **Identities are who they say they are** &ndash; There is no way to corrupt or spoof an object, and, by implication, a user or security domain. Access to an object is through accessible functions and fields. An object can still be designed in such a way that security is compromised. However, a local analysis of the class, its methods, and the things it uses, as opposed to a global analysis of all uses of a class, is sufficient to assess the vulnerabilities.
 * **Identities are who they say they are** &ndash; 没有办法破坏或欺骗对象，也就是说，无法破坏或欺骗用户或安全域。通过可访问的函数和字段来访问对象。对象仍然可以被设计成危及安全性的方式。但是，与对类的所有使用进行全局分析相反，对类、类的方法和类使用的东西进行局部分析就足以评估漏洞。



 * **Only appropriate operations can be invoked** &ndash; The reference type defines the accessible functions and fields. This includes limiting visibility based on where the reference is (e.g., protected fields only visible in derived classes).
 * **Only appropriate operations can be invoked** &ndash; 引用类型定义了可访问的函数和字段。这包括根据引用的位置限制可见性（例如，受保护的字段仅在派生类中可见）。



The CTS promotes type safety (e.g., everything is typed). Type safety can optionally be enforced. The hard problem is determining if an implementation conforms to a type-safe declaration. Since the declarations are carried along as metadata with the compiled form of the program, a compiler from the Common Intermediate Language (CIL) to native code (see §[I.8.8](i.8.8-type-safety-and-verification.md)) can type-check the implementations.

CTS提高了类型安全性（例如，所有东西都是类型的）。可以选择性地强制类型安全。困难的问题是确定实现是否符合类型安全声明。由于声明作为元数据与程序的编译形式一起携带，因此从公共中间语言（CIL）到本机代码的编译器(see §[I.8.8](i.8.8-type-safety-and-verification.md))。可以对实现进行类型检查。
