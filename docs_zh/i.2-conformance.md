## I.2 Conformance 一致性

A system claiming conformance to this International Standard shall implement all the normative requirements of this standard, and shall specify the profile (see [Partition IV Library &ndash; Profiles](#todo-missing-hyperlink)) that it implements. The minimal implementation is the Kernel Profile. A conforming implementation can also include additional functionality provided that functionality does not prevent running code written to rely solely on the profile as specified in this standard. For example, a conforming implementation can provide additional classes, new methods on existing classes, or a new interface on a standardized class, but it shall not add methods or properties to interfaces specified in this standard.

一个声称符合本国际标准的系统 应实现本标准的所有规范性要求，并应指定其实现的概要文件 (see [Partition IV Library &ndash; Profiles](#todo-missing-hyperlink)) 最小的实现是内核概要文件。一个符合标准的实现还可以包括额外的功能，只要这些功能不妨碍运行仅依赖本标准中指定的概要文件编写的代码。例如，一个符合标准的实现可以提供额外的类，现有类上的新方法，或标准化类上的新接口，但它不得向本标准中指定的接口添加方法或属性。



A compiler that generates Common Intermediate Language (CIL, see [Partition III](#todo-missing-hyperlink)) and claims conformance to this International Standard shall produce output files in the format specified in this standard, and the CIL it generates shall be correct CIL as specified in this standard. Such a compiler can also claim that it generates *verifiable* code, in which case, the CIL it generates shall be verifiable as specified in this standard.

生成通用中间语言 (CIL, see [Partition III](#todo-missing-hyperlink)) 并声称符合本国际标准的编译器应以本标准规定的格式生成输出文件，并且它生成的CIL应是本标准规定的正确的CIL。这样的编译器也可以声称它生成了*可验证的*代码，在这种情况下，它生成的CIL应按照本标准的规定是可验证的。
