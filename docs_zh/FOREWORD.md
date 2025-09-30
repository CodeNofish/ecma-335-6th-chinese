## Foreword

This sixth edition cancels and replaces the fifth edition which has been technically revised

第六版规范取消并替代了经过技术修订的第五版。



This Standard is fully aligned with ISO/IEC 23271:2012.

该标准完全符合 ISO/IEC 23271:2012.



The following features have been added, extended or clarified in the Standard:

本标准添加、扩展、澄清了以下特性：



 * The presentation of the rules for assignment compatibility (§[I.8.7](i.8.7-assignment-compatibility.md), §[III.1.8.1.2.3](iii.1.8.1.2.3-verification-type-compatibility.md)) has been extensively revised to a more precise and clearer relation-based format.

 * 赋值相容规则的表示 (§[I.8.7](i.8.7-assignment-compatibility.md), §[III.1.8.1.2.3](iii.1.8.1.2.3-verification-type-compatibility.md)) 。已广泛修订为更精确和更清楚的基于关系的格式。



 * The presentation of the verification rules for many IL instructions has been revised to be more precise and clearer by building upon the revisions to the presentation of assignment compatibility.

 * 在对赋值兼容性表示的修订基础上，对许多IL指令的验证规则的表示进行了修订，使其更加精确和清晰。



 * The presentation of delegate signature compatibility has been revised along the same lines as assignment compatibility.

 * 委托签名兼容性的表示已按照与赋值兼容性相同的方式进行了修订。



 * The verification rules for the IL `newobj` instruction have been extended to cover general delegate creation.

 * IL `newobj` 指令的验证规则已扩展到涵盖一般委托创建。



 * The dispatch rules for variance (§[II.12.2](ii.12.2-implementing-virtual-methods-on-interfaces.md)) have been extended to define resolutions for the ambiguities that can arise.
 * 对变种的分派规则 (§[II.12.2](ii.12.2-implementing-virtual-methods-on-interfaces.md)) 进行了扩展，以定义可能出现的歧义的解决方案。



 * Type forwarders have been added to support the relocation of types between libraries (§[II.6.8](ii.6.8-type-forwarders.md))
 * 添加了类型转发器以支持库之间类型的重新定位 (§[II.6.8](ii.6.8-type-forwarders.md))



The following changes of behavior have been made to the Standard:

本标准对以下行为进行了修改：



 * The semantics of variance has been redefined making it a core feature of the CLI. In the previous edition of the Standard variance could be ignored by languages not wishing to support it (§[I.1.8](#todo-missing-hyperlink)); as exact type matches always took precedence over *matches-by-variance*. In this edition the dispatch rules for interfaces (§[II.12.2](ii.12.2-implementing-virtual-methods-on-interfaces.md)) allow a *match-by-variance* to take precedence over an exact match, so all language implementation targeting the CLI must be aware of the behavior even if it is not supported in the language (§[I.1.8](#todo-missing-hyperlink)).
 * 变种的语义已经被重新定义，使其成为CLI的核心特性。在先前版本的标准中，不希望支持它的语言可以忽略它 (§[I.1.8](#todo-missing-hyperlink))；因为精确类型匹配总是优先于*按变种匹配*。在这个版本中，接口的调度规则(§[II.12.2](ii.12.2-implementing-virtual-methods-on-interfaces.md)) 允许*按变体匹配*优先于精确匹配，因此所有针对CLI的语言实现都必须意识到这种行为，即使它在语言中不被支持(§[I.1.8](#todo-missing-hyperlink)).



 * Additional requirements on ilasm to metadata conversion. The left-to-right order of interfaces listed in a type header (§[II.10.2](ii.10.2-body-of-a-type-definition.md)) must now be preserved as a top-to-bottom order in the _InterfaceImpl_ table (§[II.22.23](ii.22.23-interfaceimpl-0x09.md)); and the top-to-bottom of method definitions (§[II.10.2](ii.10.2-body-of-a-type-definition.md), §[II.25](ii.25-file-format-extensions-to-pe.md)) must now be preserved as a top-to-bottom order in the _MethodDef_ table (§[II.22.26](ii.22.26-methoddef-0x06.md)). Both these additional requirements are required to support the revised variance semantics.
 * 数据到元数据转换的附加要求。在类型头中列出的接口从左到右的顺序 (§[II.10.2](ii.10.2-body-of-a-type-definition.md)) 现在必须在_InterfaceImpl_表中保留从上到下的顺序 (§[II.22.23](ii.22.23-interfaceimpl-0x09.md))；以及从上到下的方法定义 (§[II.10.2](ii.10.2-body-of-a-type-definition.md), §[II.25](ii.25-file-format-extensions-to-pe.md)) 现在必须在_MethodDef_ 表 (§[II.22.26](ii.22.26-methoddef-0x06.md)). 这两个额外的需求都需要支持修改后的变体语义.



 * `System.Math` and `System.Double` have been modified to better conform to IEEE (see [Partition IV](#todo-missing-hyperlink) and IEC 60559:1989)
 * `System.Math` 和`System.Double` 已经被修改以更好的符合 IEEE (see [Partition IV](#todo-missing-hyperlink) and IEC 60559:1989)



The following types have been added to the Standard or have been significantly updated (* represents an update).

以下类型已被添加到标准中或已进行了重大更新（*表示更新）。



| Type                                                         | Library                |
| ------------------------------------------------------------ | ---------------------- |
| `System.Action`                                              | BCL                    |
| ``System.Action`1<-T>``* &hellip; ``System.Action`8<-T1..-T8>`` | BCL                    |
| ``System.Comparison`1<-T>``*                                 | BCL                    |
| ``System.Converter`2<-T,+U>``*                               | BCL                    |
| ``System.IComparable`1<-T>``*                                | BCL                    |
| ``System.Predicate`1<-T>``*                                  | BCL                    |
| ``System.Collections.Generic.IComparer`1<-T>``*              | BCL                    |
| ``System.Collections.Generic.IEnumerable`1<+T>``*            | BCL                    |
| ``System.Collections.Generic.IEqualityComparer`1<-T>``*      | BCL                    |
| `System.Guid`                                                | BCL                    |
| `System.MulticastDelegate`                                   | BCL                    |
| `System.Reflection.CallingConventions`                       | Runtime Infrastructure |
| `System.Runtime.InteropServices.GuidAttribute`               | Runtime Infrastructure |
| ``System.Func`1<+TResult>…System.Func`9<-T1..-T8, +TResult>`` | BCL                    |
| ``System.Collections.Generic.Comparer`1<T>``                 | BCL                    |
| ``System.Collections.Generic.EqualityComparer`1<T>``         | BCL                    |
| ``System.Collections.Generic.ISet`1<T>``                     | BCL                    |
| ``System.Collections.Generic.LinkedList`1<T>``               | BCL                    |
| ``System.Collections.Generic.LinkedList`1<T>.Enumerator``    | BCL                    |
| ``System.Collections.Generic.LinkedListNode`1<T>``           | BCL                    |
| ``System.Collections.Generic.Queue`1<T>``                    | BCL                    |
| ``System.Collections.Generic.Stack`1<T>``                    | BCL                    |
| ``System.Collections.Generic.Stack`1<T>.Enumerator``         | BCL                    |
| `System.Collections.Stack`                                   | BCL                    |
| `System.DBNull`                                              | BCL                    |
| `System.Runtime.InteropServices.Marshal`                     | Runtime Infrastructure |
| `System.Runtime.InteropServices.SafeBuffer`                  | Runtime Infrastructure |
| `System.Runtime.InteropServices.SafeHandle`                  | Runtime Infrastructure |
| `System.Threading.AutoResetEvent`                            | BCL                    |
| `System.Threading.EventWaitHandle`                           | BCL                    |
| `System.Threading.ManualResetEvent`                          | BCL                    |
| `System.WeakReference`                                       | BCL                    |
| `System.Runtime.CompilerServices.TypeForwardedToAttribute`   | BCL                    |
| `System.Runtime.CompilerServices.TypeForwardedFromAttribute` | BCL                    |
| `System.Threading.EventResetMode`                            | BCL                    |
| `System.Runtime.InteropServices.DllAttribute`*               | Runtime Infrastructure |
| `System.Math`*                                               | BCL                    |



One type, `INullableValue`, has been removed from the Standard. `INullableValue` is incompatible with the semantics of boxing as defined in the previous edition of the Standard. The references to it were included in error from an earlier draft and no implementations are known to have ever included it. 

类型 `INullableValue` 已从标准中删除。`INullableValue` 与前一版标准中定义的装箱语义不兼容。对它的引用包含在早期草案的错误中，并且已知没有实现曾经包含过它。



Technical Report 89 (TR89), which was submitted during the third edition of this Ecma standard, will no longer be part of the submission. TR89 specified a collection of generic types, to help enhance inter-language interoperability, under consideration for inclusion in a future version of the standard. That consideration has now occurred and TR89 has fulfilled its role. A selection of the types covered in TR89 has been introduced into this edition of the standard. An archive version of TR89 will continue to be available from Ecma.

技术报告89 （TR89），在本Ecma标准第三版期间提交的，将不再是提交的一部分。TR89指定了一组泛型类型，以帮助加强语言间的互操作性，现正考虑纳入标准的未来版本。这种考虑现在已经发生，TR89已经履行了它的作用。在TR89中涵盖的类型的选择已被引入到这个版本的标准中。Ecma将继续提供TR89的存档版本。



The following companies and organizations have participated in the development of this standard, and their contributions are gratefully acknowledged: Eiffel Software, Kahu Research, Microsoft Corporation, Novell Corporation, Twin Roots. For previous editions, the following companies and organizations are also acknowledged: Borland, Fujitsu Software Corporation, Hewlett-Packard, Intel Corporation, IBM Corporation, IT University of Copenhagen, Jagger Software Ltd., Monash University, Netscape, Phone.Com, Plum Hall, and Sun Microsystems.

以下公司和组织参与了本标准的开发，并对他们的贡献表示感谢：Eiffel Software、Kahu Research、Microsoft Corporation、Novell Corporation、Twin Roots。对于以前的版本，以下公司和组织也被承认：Borland，富士通软件公司，惠普，英特尔公司，IBM公司，哥本哈根IT大学，Jagger软件有限公司，莫纳什大学，网景，Phone.Com， Plum Hall和Sun Microsystems。