---
title: Code quality rules overview
ms.date: 08/27/2020
ms.topic: reference
f1_keywords:
- CA1000
- CA1001
- CA1002
- CA1003
- CA1005
- CA1008
- CA1010
- CA1012
- CS1014
- CA1016
- CA1017
- CA1018
- CA1019
- CA1021
- CA1024
- CA1027
- CA1028
- CA1029
- CA1030
- CA1031
- CA1032
- CA1033
- CA1034
- CA1036
- CA1040
- CA1041
- CA1043
- CA1044
- CA1045
- CA1046
- CA1047
- CA1050
- CA1051
- CA1052
- CA1053
- CA1054
- CA1055
- CA1056
- CA1058
- CA1060
- CA1061
- CA1062
- CA1063
- CA1064
- CA1065
- CA1066
- CA1067
- CA1068
- CA1069
- CA1070
- CA1200
- CA1303
- CA1304
- CA1305
- CA1307
- CA1308
- CA1309
- CA1310
- CA1401
- CA1417
- CA1501
- CA1502
- CA1505
- CA1506
- CA1507
- CA1508
- CA1509
- CA1700
- CA1707
- CA1708
- CA1710
- CA1711
- CA1712
- CA1713
- CA1714
- CA1715
- CA1716
- CA1717
- CA1720
- CA1721
- CA1724
- CA1725
- CA1801
- CA1802
- CA1805
- CA1806
- CA1810
- CA1812
- CA1813
- CA1814
- CA1815
- CA1816
- CA1819
- CA1820
- CA1821
- CA1822
- CA1823
- CA1824
- CA1825
- CA1826
- CA1827
- CA1828
- CA1829
- CA1830
- CA1831
- CA1832
- CA1833
- CA1834
- CA1835
- CA1836
- CA1837
- CA1838
- CA2000
- CA2002
- CA2007
- CA2008
- CA2009
- CA2011
- CA2012
- CA2013
- CA2014
- CA2015
- CA2016
- CA2100
- CA2101
- CA2109
- CA2119
- CA2153
- CA2200
- CA2201
- CA2207
- CA2208
- CA2211
- CA2213
- CA2214
- CA2215
- CA2216
- CA2217
- CA2219
- CA2225
- CA2226
- CA2227
- CA2229
- CA2231
- CA2234
- CA2235
- CA2237
- CA2241
- CA2242
- CA2243
- CA2245
- CA2246
- CA2247
- CA2248
- CA2249
- CA2300
- CA2301
- CA2302
- CA2305
- CA2310
- CA2311
- CA2312
- CA2315
- CA2321
- CA2322
- CA2326
- CA2327
- CA2328
- CA2329
- CA2330
- CA2350
- CA2351
- CA2352
- CA2353
- CA2354
- CA2355
- CA2356
- CA2361
- CA2362
- CA3001
- CA3002
- CA3003
- CA3004
- CA3005
- CA3006
- CA3007
- CA3008
- CA3009
- CA3010
- CA3011
- CA3012
- CA3061
- CA3075
- CA3076
- CA3077
- CA5347
- CA5350
- CA5351
- CA5359
- CA5360
- CA5361
- CA5362
- CA5363
- CA5364
- CA5365
- CA5366
- CA5367
- CA5368
- CA5369
- CA5370
- CA5371
- CA5372
- CA5373
- CA5374
- CA5375
- CA5376
- CA5377
- CA5378
- CA5379
- CA5380
- CA5381
- CA5382
- CA5383
- CA5384
- CA5385
- CA5386
- CA5387
- CA5388
- CA5389
- CA5390
- CA5391
- CA5392
- CA5393
- CA5394
- CA5395
- CA5397
- CA5398
- CA5399
- CA5400
- CA5401
- CA5402
- CA5403
- IL3000
- IL3001
ms.assetid: 5cb221f6-dc59-4abf-9bfa-adbd6f907f96
author: mikadumont
ms.author: midumont
manager: jillfra
ms.workload:
- dotnet
---
# Code analysis warnings for managed code by CheckId

The following table lists Code Analysis warnings for managed code by the CheckId identifier of the warning.

| CheckId | Warning | Description |
|---------| - | - |
| CA1000 | [CA1000: Do not declare static members on generic types](../code-quality/ca1000.md) | When a static member of a generic type is called, the type argument must be specified for the type. When a generic instance member that does not support inference is called, the type argument must be specified for the member. In these two cases, the syntax for specifying the type argument is different and easily confused. |
| CA1001 | [CA1001: Types that own disposable fields should be disposable](../code-quality/ca1001.md) | A class declares and implements an instance field that is a System.IDisposable type, and the class does not implement IDisposable. A class that declares an IDisposable field indirectly owns an unmanaged resource and should implement the IDisposable interface. |
| CA1002 | [CA1002: Do not expose generic lists](../code-quality/ca1002.md) | System.Collections.Generic.List<(Of \<(T>)>) is a generic collection that is designed for performance, not inheritance. Therefore, List does not contain any virtual members. The generic collections that are designed for inheritance should be exposed instead. |
| CA1003 | [CA1003: Use generic event handler instances](../code-quality/ca1003.md) |A type contains a delegate that returns void, whose signature contains two parameters (the first an object and the second a type that is assignable to EventArgs), and the containing assembly targets Microsoft .NET Framework 2.0. |
| CA1005 | [CA1005: Avoid excessive parameters on generic types](../code-quality/ca1005.md) | The more type parameters a generic type contains, the more difficult it is to know and remember what each type parameter represents. It is usually obvious with one type parameter, as in List\<T>, and in certain cases that have two type parameters, as in Dictionary\<TKey, TValue>. However, if more than two type parameters exist, the difficulty becomes too great for most users. |
| CA1008 | [CA1008: Enums should have zero value](../code-quality/ca1008.md) | The default value of an uninitialized enumeration, just as other value types, is zero. A nonflags-attributed enumeration should define a member by using the value of zero so that the default value is a valid value of the enumeration. If an enumeration that has the FlagsAttribute attribute applied defines a zero-valued member, its name should be "None" to indicate that no values have been set in the enumeration. |
| CA1010 | [CA1010: Collections should implement generic interface](../code-quality/ca1010.md) | To broaden the usability of a collection, implement one of the generic collection interfaces. Then the collection can be used to populate generic collection types. |
| CA1012 | [CA1012: Abstract types should not have constructors](../code-quality/ca1012.md) | Constructors on abstract types can be called only by derived types. Because public constructors create instances of a type, and you cannot create instances of an abstract type, an abstract type that has a public constructor is incorrectly designed. |
| CA1014 | [CA1014: Mark assemblies with CLSCompliantAttribute](../code-quality/ca1014.md) | The Common Language Specification (CLS) defines naming restrictions, data types, and rules to which assemblies must conform if they will be used across programming languages. Good design dictates that all assemblies explicitly indicate CLS compliance by using <xref:System.CLSCompliantAttribute> . If this attribute is not present on an assembly, the assembly is not compliant. |
| CA1016 | [CA1016: Mark assemblies with AssemblyVersionAttribute](../code-quality/ca1016.md) | .NET uses the version number to uniquely identify an assembly and to bind to types in strongly named assemblies. The version number is used together with version and publisher policy. By default, applications run only with the assembly version with which they were built. |
| CA1017 | [CA1017: Mark assemblies with ComVisibleAttribute](../code-quality/ca1017.md) |ComVisibleAttribute determines how COM clients access managed code. Good design dictates that assemblies explicitly indicate COM visibility. COM visibility can be set for the whole assembly and then overridden for individual types and type members. If this attribute is not present, the contents of the assembly are visible to COM clients. |
| CA1018 | [CA1018: Mark attributes with AttributeUsageAttribute](../code-quality/ca1018.md) | When you define a custom attribute, mark it by using AttributeUsageAttribute to indicate where in the source code the custom attribute can be applied. The meaning and intended usage of an attribute will determine its valid locations in code. |
| CA1019 | [CA1019: Define accessors for attribute arguments](../code-quality/ca1019.md) | Attributes can define mandatory arguments that must be specified when you apply the attribute to a target. These are also known as positional arguments because they are supplied to attribute constructors as positional parameters. For every mandatory argument, the attribute should also provide a corresponding read-only property so that the value of the argument can be retrieved at execution time. Attributes can also define optional arguments, which are also known as named arguments. These arguments are supplied to attribute constructors by name and should have a corresponding read/write property. |
| CA1021 | [CA1021: Avoid out parameters](../code-quality/ca1021.md) | Passing types by reference (using out or ref) requires experience with pointers, understanding how value types and reference types differ, and handling methods with multiple return values. Also, the difference between out and ref parameters is not widely understood. |
| CA1024 | [CA1024: Use properties where appropriate](../code-quality/ca1024.md) | A public or protected method has a name that starts with "Get", takes no parameters, and returns a value that is not an array. The method might be a good candidate to become a property. |
| CA1027 |[CA1027: Mark enums with FlagsAttribute](../code-quality/ca1027.md) | An enumeration is a value type that defines a set of related named constants. Apply FlagsAttribute to an enumeration when its named constants can be meaningfully combined. |
| CA1028 | [CA1028: Enum storage should be Int32](../code-quality/ca1028.md) | An enumeration is a value type that defines a set of related named constants. By default, the System.Int32 data type is used to store the constant value. Although you can change this underlying type, it is not required or recommended for most scenarios. |
| CA1030 | [CA1030: Use events where appropriate](../code-quality/ca1030.md) |This rule detects methods that have names that ordinarily would be used for events. If a method is called in response to a clearly defined state change, the method should be invoked by an event handler. Objects that call the method should raise events instead of calling the method directly. |
| CA1031 | [CA1031: Do not catch general exception types](../code-quality/ca1031.md) | General exceptions should not be caught. Catch a more specific exception, or rethrow the general exception as the last statement in the catch block. |
| CA1032 |[CA1032: Implement standard exception constructors](../code-quality/ca1032.md) | Failure to provide the full set of constructors can make it difficult to correctly handle exceptions. |
| CA1033 | [CA1033: Interface methods should be callable by child types](../code-quality/ca1033.md) | An unsealed externally visible type provides an explicit method implementation of a public interface and does not provide an alternative externally visible method that has the same name. |
| CA1034 | [CA1034: Nested types should not be visible](../code-quality/ca1034.md) | A nested type is a type that is declared in the scope of another type. Nested types are useful to encapsulate private implementation details of the containing type. Used for this purpose, nested types should not be externally visible. |
| CA1036 | [CA1036: Override methods on comparable types](../code-quality/ca1036.md) |A public or protected type implements the System.IComparable interface. It does not override Object.Equals nor does it overload the language-specific operator for equality, inequality, less than, or greater than. |
| CA1040 |[CA1040: Avoid empty interfaces](../code-quality/ca1040.md) | Interfaces define members that provide a behavior or usage contract. The functionality that is described by the interface can be adopted by any type, regardless of where the type appears in the inheritance hierarchy. A type implements an interface by providing implementations for the members of the interface. An empty interface does not define any members; therefore, it does not define a contract that can be implemented. |
| CA1041 | [CA1041: Provide ObsoleteAttribute message](../code-quality/ca1041.md) | A type or member is marked by using a System.ObsoleteAttribute attribute that does not have its ObsoleteAttribute.Message property specified. When a type or member that is marked by using ObsoleteAttribute is compiled, the Message property of the attribute is displayed. This gives the user information about the obsolete type or member. |
| CA1043 | [CA1043: Use integral or string argument for indexers](../code-quality/ca1043.md) | Indexers (that is, indexed properties) should use integral or string types for the index. These types are typically used for indexing data structures and they increase the usability of the library. Use of the Object type should be restricted to those cases where the specific integral or string type cannot be specified at design time. |
| CA1044 | [CA1044: Properties should not be write only](../code-quality/ca1044.md) | Although it is acceptable and often necessary to have a read-only property, the design guidelines prohibit the use of write-only properties. This is because letting a user set a value, and then preventing the user from viewing that value, does not provide any security. Also, without read access, the state of shared objects cannot be viewed, which limits their usefulness. |
| CA1045 |[CA1045: Do not pass types by reference](../code-quality/ca1045.md) | Passing types by reference (using out or ref) requires experience with pointers, understanding how value types and reference types differ, and handling methods that have multiple return values. Library architects who design for a general audience should not expect users to master working with `out` or `ref` parameters. |
| CA1046 | [CA1046: Do not overload operator equals on reference types](../code-quality/ca1046.md) | For reference types, the default implementation of the equality operator is almost always correct. By default, two references are equal only if they point to the same object. |
| CA1047 |[CA1047: Do not declare protected members in sealed types](../code-quality/ca1047.md) | Types declare protected members so that inheriting types can access or override the member. By definition, sealed types cannot be inherited, which means that protected methods on sealed types cannot be called. |
| CA1050 | [CA1050: Declare types in namespaces](../code-quality/ca1050.md) | Types are declared in namespaces to prevent name collisions and as a way to organize related types in an object hierarchy. |
| CA1051 | [CA1051: Do not declare visible instance fields](../code-quality/ca1051.md) | The primary use of a field should be as an implementation detail. Fields should be private or internal and should be exposed by using properties. |
| CA1052 | [CA1052: Static holder types should be sealed](../code-quality/ca1052.md) | A public or protected type contains only static members and is not declared by using the sealed (C# Reference) (NotInheritable) modifier. A type that is not meant to be inherited should be marked by using the sealed modifier to prevent its use as a base type. |
| CA1053 |[CA1053: Static holder types should not have constructors](../code-quality/ca1053.md) | A public or nested public type declares only static members and has a public or protected default constructor. The constructor is unnecessary because calling static members does not require an instance of the type. The string overload should call the uniform resource identifier (URI) overload by using the string argument for safety and security. |
| CA1054 | [CA1054: URI parameters should not be strings](../code-quality/ca1054.md) | If a method takes a string representation of a URI, a corresponding overload should be provided that takes an instance of the URI class, which provides these services in a safe and secure manner. |
| CA1055 | [CA1055: URI return values should not be strings](../code-quality/ca1055.md) | This rule assumes that the method returns a URI. A string representation of a URI is prone to parsing and encoding errors, and can lead to security vulnerabilities. The System.Uri class provides these services in a safe and secure manner. |
| CA1056 | [CA1056: URI properties should not be strings](../code-quality/ca1056.md) | This rule assumes that the property represents a Uniform Resource Identifier (URI). A string representation of a URI is prone to parsing and encoding errors, and can lead to security vulnerabilities. The System.Uri class provides these services in a safe and secure manner. |
| CA1058 | [CA1058: Types should not extend certain base types](../code-quality/ca1058.md) | An externally visible type extends certain base types. Use one of the alternatives. |
| CA1060 | [CA1060: Move P/Invokes to NativeMethods class](../code-quality/ca1060.md) | Platform Invocation methods, such as those that are marked by using the System.Runtime.InteropServices.DllImportAttribute attribute, or methods that are defined by using the Declare keyword in [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)], access unmanaged code. These methods should be of the NativeMethods, SafeNativeMethods, or UnsafeNativeMethods class. |
| CA1061 |[CA1061: Do not hide base class methods](../code-quality/ca1061.md) | A method in a base type is hidden by an identically named method in a derived type, when the parameter signature of the derived method differs only by types that are more weakly derived than the corresponding types in the parameter signature of the base method. |
| CA1062 | [CA1062: Validate arguments of public methods](../code-quality/ca1062.md) | All reference arguments that are passed to externally visible methods should be checked against null. |
| CA1063 | [CA1063: Implement IDisposable correctly](../code-quality/ca1063.md) | All IDisposable types should implement the Dispose pattern correctly. |
| CA1064 | [CA1064: Exceptions should be public](../code-quality/ca1064.md) | An internal exception is visible only inside its own internal scope. After the exception falls outside the internal scope, only the base exception can be used to catch the exception. If the internal exception is inherited from <xref:System.Exception>, <xref:System.SystemException>, or <xref:System.ApplicationException>, the external code will not have sufficient information to know what to do with the exception. |
| CA1065 | [CA1065: Do not raise exceptions in unexpected locations](../code-quality/ca1065.md) | A method that is not expected to throw exceptions throws an exception. |
| CA1066 | [CA1066: Implement IEquatable when overriding Equals](../code-quality/ca1066.md) | A value type overrides <xref:System.Object.Equals%2A> method, but does not implement <xref:System.IEquatable%601>. |
| CA1067 | [CA1067: Override Equals when implementing IEquatable](../code-quality/ca1067.md) | A type implements <xref:System.IEquatable%601>, but does not override <xref:System.Object.Equals%2A> method. |
| CA1068 | [CA1068: CancellationToken parameters must come last](../code-quality/ca1068.md) | A method has a CancellationToken parameter that is not the last parameter. |
| CA1069 | [CA1069: Enums should not have duplicate values](../code-quality/ca1069.md) | An enumeration has multiple members which are explicitly assigned the same constant value. |
| CA1070 | [CA1070: Do not declare event fields as virtual](../code-quality/ca1070.md) | A [field-like event](/dotnet/csharp/language-reference/language-specification/classes#field-like-events) was declared as virtual. |
| CA1200 | [CA1200: Avoid using cref tags with a prefix](../code-quality/ca1200.md) | The [cref](/dotnet/csharp/programming-guide/xmldoc/cref-attribute) attribute in an XML documentation tag means "code reference". It specifies that the inner text of the tag is a code element, such as a type, method, or property. Avoid using `cref` tags with prefixes, because it prevents the compiler from verifying references. It also prevents the Visual Studio integrated development environment (IDE) from finding and updating these symbol references during refactorings. |
| CA1303 | [CA1303: Do not pass literals as localized parameters](../code-quality/ca1303.md) | An externally visible method passes a string literal as a parameter to a .NET constructor or method, and that string should be localizable. |
| CA1304 | [CA1304: Specify CultureInfo](../code-quality/ca1304.md) | A method or constructor calls a member that has an overload that accepts a System.Globalization.CultureInfo parameter, and the method or constructor does not call the overload that takes the CultureInfo parameter. When a CultureInfo or System.IFormatProvider object is not supplied, the default value that is supplied by the overloaded member might not have the effect that you want in all locales. |
| CA1305 | [CA1305: Specify IFormatProvider](../code-quality/ca1305.md) | A method or constructor calls one or more members that have overloads that accept a System.IFormatProvider parameter, and the method or constructor does not call the overload that takes the IFormatProvider parameter. When a System.Globalization.CultureInfo or IFormatProvider object is not supplied, the default value that is supplied by the overloaded member might not have the effect that you want in all locales. |
| CA1307 | [CA1307: Specify StringComparison for clarity](../code-quality/ca1307.md) | A string comparison operation uses a method overload that does not set a StringComparison parameter. |
| CA1308 |[CA1308: Normalize strings to uppercase](../code-quality/ca1308.md) | Strings should be normalized to uppercase. A small group of characters cannot make a round trip when they are converted to lowercase. |
| CA1309 | [CA1309: Use ordinal StringComparison](../code-quality/ca1309.md) | A string comparison operation that is nonlinguistic does not set the StringComparison parameter to either Ordinal or OrdinalIgnoreCase. By explicitly setting the parameter to either StringComparison.Ordinal or StringComparison.OrdinalIgnoreCase, your code often gains speed, becomes more correct, and becomes more reliable. |
| CA1310 | [CA1310: Specify StringComparison for correctness](../code-quality/ca1310.md) | A string comparison operation uses a method overload that does not set a StringComparison parameter and uses culture-specific string comparison by default. |
| CA1401 | [CA1401: P/Invokes should not be visible](../code-quality/ca1401.md) | A public or protected method in a public type has the System.Runtime.InteropServices.DllImportAttribute attribute (also implemented by the Declare keyword in [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]). Such methods should not be exposed. |
| CA1417 | [CA1417: Do not use `OutAttribute` on string parameters for P/Invokes](../code-quality/ca1417.md) | String parameters passed by value with the `OutAttribute` can destabilize the runtime if the string is an interned string. |
| CA1501 | [CA1501: Avoid excessive inheritance](../code-quality/ca1501.md) | A type is more than four levels deep in its inheritance hierarchy. Deeply nested type hierarchies can be difficult to follow, understand, and maintain. |
| CA1502 | [CA1502: Avoid excessive complexity](../code-quality/ca1502.md) | This rule measures the number of linearly independent paths through the method, which is determined by the number and complexity of conditional branches. |
| CA1505 | [CA1505: Avoid unmaintainable code](../code-quality/ca1505.md) | A type or method has a low maintainability index value. A low maintainability index indicates that a type or method is probably difficult to maintain and would be a good candidate for redesign. |
| CA1506 | [CA1506: Avoid excessive class coupling](../code-quality/ca1506.md) | This rule measures class coupling by counting the number of unique type references that a type or method contains. |
| CA1507 | [CA1507: Use nameof in place of string](../code-quality/ca1507.md) | A string literal is used as an argument where a `nameof` expression could be used. |
| CA1508 | [CA1508: Avoid dead conditional code](../code-quality/ca1508.md) | A method has conditional code that always evaluates to `true` or `false` at runtime. This leads to dead code in the `false` branch of the condition. |
| CA1509 | [CA1509: Invalid entry in code metrics configuration file](../code-quality/ca1509.md) | Code metrics rules, such as [CA1501](ca1501.md), [CA1502](ca1502.md), [CA1505](ca1505.md) and [CA1506](ca1506.md), supplied a configuration file named `CodeMetricsConfig.txt` that has an invalid entry. |
| CA1700 | [CA1700: Do not name enum values 'Reserved'](../code-quality/ca1700.md) | This rule assumes that an enumeration member that has a name that contains "reserved" is not currently used but is a placeholder to be renamed or removed in a future version. Renaming or removing a member is a breaking change. |
| CA1707 | [CA1707: Identifiers should not contain underscores](../code-quality/ca1707.md) | By convention, identifier names do not contain the underscore (_) character. This rule checks namespaces, types, members, and parameters. |
| CA1708 | [CA1708: Identifiers should differ by more than case](../code-quality/ca1708.md) | Identifiers for namespaces, types, members, and parameters cannot differ only by case because languages that target the common language runtime are not required to be case-sensitive. |
| CA1710 | [CA1710: Identifiers should have correct suffix](../code-quality/ca1710.md) |By convention, the names of types that extend certain base types or that implement certain interfaces, or types that are derived from these types, have a suffix that is associated with the base type or interface. |
| CA1711 | [CA1711: Identifiers should not have incorrect suffix](../code-quality/ca1711.md) | By convention, only the names of types that extend certain base types or that implement certain interfaces, or types that are derived from these types, should end with specific reserved suffixes. Other type names should not use these reserved suffixes. |
| CA1712 | [CA1712: Do not prefix enum values with type name](../code-quality/ca1712.md) | Names of enumeration members are not prefixed by using the type name because development tools are expected to provide type information. |
| CA1713 | [CA1713: Events should not have before or after prefix](../code-quality/ca1713.md) | The name of an event starts with "Before" or "After". To name related events that are raised in a specific sequence, use the present or past tense to indicate the relative position in the sequence of actions. |
| CA1714 | [CA1714: Flags enums should have plural names](../code-quality/ca1714.md) | A public enumeration has the System.FlagsAttribute attribute, and its name does not end in "s". Types that are marked by using FlagsAttribute have names that are plural because the attribute indicates that more than one value can be specified. |
| CA1715 | [CA1715: Identifiers should have correct prefix](../code-quality/ca1715.md) | The name of an externally visible interface does not start with an uppercase "I". The name of a generic type parameter on an externally visible type or method does not start with an uppercase "T". |
| CA1716 | [CA1716: Identifiers should not match keywords](../code-quality/ca1716.md) | A namespace name or a type name matches a reserved keyword in a programming language. Identifiers for namespaces and types should not match keywords that are defined by languages that target the common language runtime. |
| CA1717 | [CA1717: Only FlagsAttribute enums should have plural names](../code-quality/ca1717.md) | Naming conventions dictate that a plural name for an enumeration indicates that more than one value of the enumeration can be specified at the same time. |
| CA1720 |[CA1720: Identifiers should not contain type names](../code-quality/ca1720.md) | The name of a parameter in an externally visible member contains a data type name, or the name of an externally visible member contains a language-specific data type name. |
| CA1721 | [CA1721: Property names should not match get methods](../code-quality/ca1721.md) |The name of a public or protected member starts with "Get" and otherwise matches the name of a public or protected property. "Get" methods and properties should have names that clearly distinguish their function. |
| CA1724 | [CA1724: Type Names Should Not Match Namespaces](../code-quality/ca1724.md) | Type names should not match the names of .NET namespaces. Violating this rule can reduce the usability of the library. |
| CA1725 | [CA1725: Parameter names should match base declaration](../code-quality/ca1725.md) | Consistent naming of parameters in an override hierarchy increases the usability of the method overrides. A parameter name in a derived method that differs from the name in the base declaration can cause confusion about whether the method is an override of the base method or a new overload of the method. |
| CA1801 | [CA1801: Review unused parameters](../code-quality/ca1801.md) | A method signature includes a parameter that is not used in the method body. |
| CA1802 |[CA1802: Use Literals Where Appropriate](../code-quality/ca1802.md) |A field is declared static and read-only (Shared and ReadOnly in [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]), and is initialized by using a value that is computable at compile time. Because the value that is assigned to the targeted field is computable at compile time, change the declaration to a const (Const in [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]) field so that the value is computed at compile time instead of at run time. |
| CA1805 | [CA1805: Do not initialize unnecessarily](../code-quality/ca1805.md) | The .NET runtime initializes all fields of reference types to their default values before running the constructor. In most cases, explicitly initializing a field to its default value is redundant, which adds to maintenance costs and may degrade performance (such as with increased assembly size). |
| CA1806 | [CA1806: Do not ignore method results](../code-quality/ca1806.md) | A new object is created but never used; or a method that creates and returns a new string is called and the new string is never used; or a COM or P/Invoke method returns an HRESULT or error code that is never used. |
| CA1810 | [CA1810: Initialize reference type static fields inline](../code-quality/ca1810.md) | When a type declares an explicit static constructor, the just-in-time (JIT) compiler adds a check to each static method and instance constructor of the type to make sure that the static constructor was previously called. Static constructor checks can decrease performance. |
| CA1812 | [CA1812: Avoid uninstantiated internal classes](../code-quality/ca1812.md) | An instance of an assembly-level type is not created by code in the assembly. |
| CA1813 | [CA1813: Avoid unsealed attributes](../code-quality/ca1813.md) | .NET provides methods for retrieving custom attributes. By default, these methods search the attribute inheritance hierarchy. Sealing the attribute eliminates the search through the inheritance hierarchy and can improve performance. |
| CA1814 | [CA1814: Prefer jagged arrays over multidimensional](../code-quality/ca1814.md) | A jagged array is an array whose elements are arrays. The arrays that make up the elements can be of different sizes, leading to less wasted space for some sets of data. |
| CA1815 | [CA1815: Override equals and operator equals on value types](../code-quality/ca1815.md) | For value types, the inherited implementation of Equals uses the Reflection library and compares the contents of all fields. Reflection is computationally expensive, and comparing every field for equality might be unnecessary. If you expect users to compare or sort instances, or to use instances as hash table keys, your value type should implement Equals. |
| CA1816 | [CA1816: Call GC.SuppressFinalize correctly](../code-quality/ca1816.md) | A method that is an implementation of Dispose does not call GC.SuppressFinalize; or a method that is not an implementation of Dispose calls GC.SuppressFinalize; or a method calls GC.SuppressFinalize and passes something other than this (Me in Visual Basic). |
| CA1819 | [CA1819: Properties should not return arrays](../code-quality/ca1819.md) | Arrays that are returned by properties are not write-protected, even when the property is read-only. To keep the array tamper-proof, the property must return a copy of the array. Typically, users will not understand the adverse performance implications of calling such a property. |
| CA1820 | [CA1820: Test for empty strings using string length](../code-quality/ca1820.md) | Comparing strings by using the String.Length property or the String.IsNullOrEmpty method is significantly faster than using Equals. |
| CA1821 | [CA1821: Remove empty finalizers](../code-quality/ca1821.md) | Whenever you can, avoid finalizers because of the additional performance overhead that is involved in tracking object lifetime. An empty finalizer incurs added overhead and delivers no benefit. |
| CA1822 |[CA1822: Mark members as static](../code-quality/ca1822.md) | Members that do not access instance data or call instance methods can be marked as static (Shared in [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]). After you mark the methods as static, the compiler will emit nonvirtual call sites to these members. This can give you a measurable performance gain for performance-sensitive code. |
| CA1823 | [CA1823: Avoid unused private fields](../code-quality/ca1823.md) | Private fields were detected that do not appear to be accessed in the assembly. |
| CA1824 |[CA1824: Mark assemblies with NeutralResourcesLanguageAttribute](../code-quality/ca1824.md) | The NeutralResourcesLanguage attribute informs the resource manager of the language that was used to display the resources of a neutral culture for an assembly. This improves lookup performance for the first resource that you load and can reduce your working set. |
| CA1825 |[CA1825: Avoid zero-length array allocations](../code-quality/ca1825.md) | Initializing a zero-length array leads to unnecessary memory allocation. Instead, use the statically allocated empty array instance by calling <xref:System.Array.Empty%2A?displayProperty=nameWithType>. The memory allocation is shared across all invocations of this method. |
| CA1826 |[CA1826: Use property instead of Linq Enumerable method](../code-quality/ca1826.md) | <xref:System.Linq.Enumerable> LINQ method was used on a type that supports an equivalent, more efficient property. |
| CA1827 |[CA1827: Do not use Count/LongCount when Any can be used](../code-quality/ca1827.md) | <xref:System.Linq.Enumerable.Count%2A> or <xref:System.Linq.Enumerable.LongCount%2A> method was used where <xref:System.Linq.Enumerable.Any%2A> method would be more efficient. |
| CA1828 |[CA1828: Do not use CountAsync/LongCountAsync when AnyAsync can be used](../code-quality/ca1828.md) | <xref:Microsoft.EntityFrameworkCore.EntityFrameworkQueryableExtensions.CountAsync%2A> or <xref:Microsoft.EntityFrameworkCore.EntityFrameworkQueryableExtensions.LongCountAsync%2A> method was used where <xref:Microsoft.EntityFrameworkCore.EntityFrameworkQueryableExtensions.AnyAsync%2A> method would be more efficient. |
| CA1829 |[CA1829: Use Length/Count property instead of Enumerable.Count method](../code-quality/ca1829.md) | <xref:System.Linq.Enumerable.Count%2A> LINQ method was used on a type that supports an equivalent, more efficient `Length` or `Count` property. |
| CA1830 |[CA1830: Prefer strongly-typed Append and Insert method overloads on StringBuilder](../code-quality/ca1830.md) | <xref:System.Text.StringBuilder.Append%2A> and <xref:System.Text.StringBuilder.Insert%2A> provide overloads for multiple types beyond <xref:System.String>.  When possible, prefer the strongly-typed overloads over using ToString() and the string-based overload. |
| CA1831 |[CA1831: Use AsSpan instead of Range-based indexers for string when appropriate](../code-quality/ca1831.md) | When using a range-indexer on a string and implicitly assigning the value to  ReadOnlySpan&lt;char&gt; type, the method <xref:System.String.Substring%2A?#System_String_Substring_System_Int32_System_Int32_> will be used instead of <xref:System.Span%601.Slice%2A?#System_Span_1_Slice_System_Int32_System_Int32_>, which produces a copy of requested portion of the string. |
| CA1832 |[CA1832: Use AsSpan or AsMemory instead of Range-based indexers for getting ReadOnlySpan or ReadOnlyMemory portion of an array](../code-quality/ca1832.md) | When using a range-indexer on an array and implicitly assigning the value to a <xref:System.ReadOnlySpan%601> or <xref:System.ReadOnlyMemory%601> type, the method <xref:System.Runtime.CompilerServices.RuntimeHelpers.GetSubArray%2A> will be used instead of <xref:System.Span%601.Slice%2A?#System_Span_1_Slice_System_Int32_System_Int32_>, which produces a copy of requested portion of the array. |
| CA1833 |[CA1833: Use AsSpan or AsMemory instead of Range-based indexers for getting Span or Memory portion of an array](../code-quality/ca1833.md) | When using a range-indexer on an array and implicitly assigning the value to a <xref:System.Span%601> or <xref:System.Memory%601> type, the method <xref:System.Runtime.CompilerServices.RuntimeHelpers.GetSubArray%2A> will be used instead of <xref:System.Span%601.Slice%2A?#System_Span_1_Slice_System_Int32_System_Int32_>, which produces a copy of requested portion of the array. |
| CA1834 |[CA1834: Use StringBuilder.Append(char) for single character strings](../code-quality/ca1834.md) | <xref:System.Text.StringBuilder> has an `Append` overload that takes a `char` as its argument. Prefer calling the `char` overload for performance reasons. |
| CA1835 |[CA1835: Prefer the 'Memory'-based overloads for 'ReadAsync' and 'WriteAsync'](../code-quality/ca1835.md) | 'Stream' has a 'ReadAsync' overload that takes a 'Memory&lt;Byte&gt;' as the first argument, and a 'WriteAsync' overload that takes a 'ReadOnlyMemory&lt;Byte&gt;' as the first argument. Prefer calling the memory based overloads, which are more efficient. |
| CA1836 |[CA1836: Prefer `IsEmpty` over `Count` when available](../code-quality/ca1836.md) | Prefer `IsEmpty` property that is more efficient than `Count`, `Length`, <xref:System.Linq.Enumerable.Count%60%601%28System.Collections.Generic.IEnumerable%7B%60%600%7D%29> or <xref:System.Linq.Enumerable.LongCount%60%601%28System.Collections.Generic.IEnumerable%7B%60%600%7D%29> to determine whether the object contains or not any items. |
| CA1837 | [CA1837: Use `Environment.ProcessId` instead of `Process.GetCurrentProcess().Id`](../code-quality/ca1837.md) | `Environment.ProcessId` is simpler and faster than `Process.GetCurrentProcess().Id`. |
| CA1838 | [CA1838: Avoid `StringBuilder` parameters for P/Invokes](../code-quality/ca1838.md) | Marshaling of 'StringBuilder' always creates a native buffer copy, resulting in multiple allocations for one marshaling operation. |
| CA2000 | [CA2000: Dispose objects before losing scope](../code-quality/ca2000.md) | Because an exceptional event might occur that will prevent the finalizer of an object from running, the object should be explicitly disposed before all references to it are out of scope. |
| CA2002 |[CA2002: Do not lock on objects with weak identity](../code-quality/ca2002.md) |An object is said to have a weak identity when it can be directly accessed across application domain boundaries. A thread that tries to acquire a lock on an object that has a weak identity can be blocked by a second thread in a different application domain that has a lock on the same object. |
| CA2007 | [CA2007: Do not directly await a Task](ca2007.md) | An asynchronous method [awaits](/dotnet/csharp/language-reference/keywords/await) a <xref:System.Threading.Tasks.Task> directly. When an asynchronous method awaits a <xref:System.Threading.Tasks.Task> directly, continuation occurs in the same thread that created the task. This behavior can be costly in terms of performance and can result in a deadlock on the UI thread. Consider calling <xref:System.Threading.Tasks.Task.ConfigureAwait(System.Boolean)?displayProperty=nameWithType> to signal your intention for continuation. |
| CA2008 | [CA2008: Do not create tasks without passing a TaskScheduler](ca2008.md) | A task creation or continuation operation uses a method overload that does not specify a <xref:System.Threading.Tasks.TaskScheduler> parameter. |
| CA2009 | [CA2009: Do not call ToImmutableCollection on an ImmutableCollection value](ca2009.md) | `ToImmutable` method was unnecessarily called on an immutable collection from <xref:System.Collections.Immutable> namespace. |
| CA2011 | [CA2011: Do not assign property within its setter](ca2011.md) | A property was accidentally assigned a value within its own [set accessor](/dotnet/csharp/programming-guide/classes-and-structs/using-properties#the-set-accessor). |
| CA2012 | [CA2012: Use ValueTasks correctly](ca2012.md) | ValueTasks returned from member invocations are intended to be directly awaited.  Attempts to consume a ValueTask multiple times or to directly access one's result before it's known to be completed may result in an exception or corruption.  Ignoring such a ValueTask is likely an indication of a functional bug and may degrade performance. |
| CA2013 | [CA2013: Do not use ReferenceEquals with value types](ca2013.md) | When comparing values using <xref:System.Object.ReferenceEquals%2A?displayProperty=fullName>, if objA and objB are value types, they are boxed before they are passed to the <xref:System.Object.ReferenceEquals%2A> method. This means that even if both objA and objB represent the same instance of a value type, the <xref:System.Object.ReferenceEquals%2A> method nevertheless returns false. |
| CA2014 | [CA2014: Do not use stackalloc in loops.](ca2014.md) | Stack space allocated by a stackalloc is only released at the end of the current method's invocation.  Using it in a loop can result in unbounded stack growth and eventual stack overflow conditions. |
| CA2015 | [CA2015: Do not define finalizers for types derived from MemoryManager&lt;T&gt;](ca2015.md) | Adding a finalizer to a type derived from <xref:System.Buffers.MemoryManager%601> may permit memory to be freed while it is still in use by a <xref:System.Span%601>. |
| CA2016 | [CA2016: Forward the CancellationToken parameter to methods that take one](ca2016.md) | Forward the `CancellationToken` parameter to methods that take one to ensure the operation cancellation notifications gets properly propagated, or pass in `CancellationToken.None` explicitly to indicate intentionally not propagating the token. |
| CA2100 | [CA2100: Review SQL queries for security vulnerabilities](../code-quality/ca2100.md) | A method sets the System.Data.IDbCommand.CommandText property by using a string that is built from a string argument to the method. This rule assumes that the string argument contains user input. A SQL command string that is built from user input is vulnerable to SQL injection attacks. |
| CA2101 |[CA2101: Specify marshaling for P/Invoke string arguments](../code-quality/ca2101.md) | A platform invoke member allows partially trusted callers, has a string parameter, and does not explicitly marshal the string. This can cause a potential security vulnerability. |
| CA2109 | [CA2109: Review visible event handlers](../code-quality/ca2109.md) | A public or protected event-handling method was detected. Event-handling methods should not be exposed unless absolutely necessary. |
| CA2119 | [CA2119: Seal methods that satisfy private interfaces](../code-quality/ca2119.md) | An inheritable public type provides an overridable method implementation of an internal (Friend in [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]) interface. To fix a violation of this rule, prevent the method from being overridden outside the assembly. |
| CA2153 |[CA2153: Avoid handling Corrupted State Exceptions](../code-quality/ca2153.md) | Corrupted State Exceptions (CSEs) indicate that memory corruption exists in your process. Catching these rather than allowing the process to crash can lead to security vulnerabilities if an attacker can place an exploit into the corrupted memory region. |
| CA2200 | [CA2200: Rethrow to preserve stack details](../code-quality/ca2200.md) | An exception is rethrown and the exception is explicitly specified in the throw statement. If an exception is rethrown by specifying the exception in the throw statement, the list of method calls between the original method that threw the exception and the current method is lost. |
| CA2201 | [CA2201: Do not raise reserved exception types](../code-quality/ca2201.md) | This makes the original error difficult to detect and debug. |
| CA2207 | [CA2207: Initialize value type static fields inline](../code-quality/ca2207.md) | A value type declares an explicit static constructor. To fix a violation of this rule, initialize all static data when it is declared and remove the static constructor. |
| CA2208 |[CA2208: Instantiate argument exceptions correctly](../code-quality/ca2208.md) | A call is made to the default (parameterless) constructor of an exception type that is or derives from ArgumentException, or an incorrect string argument is passed to a parameterized constructor of an exception type that is or derives from ArgumentException. |
| CA2211 |[CA2211: Non-constant fields should not be visible](../code-quality/ca2211.md) | Static fields that are neither constants nor read-only are not thread-safe. Access to such a field must be carefully controlled and requires advanced programming techniques to synchronize access to the class object. |
| CA2213 | [CA2213: Disposable fields should be disposed](../code-quality/ca2213.md) | A type that implements System.IDisposable declares fields that are of types that also implement IDisposable. The Dispose method of the field is not called by the Dispose method of the declaring type. |
| CA2214 | [CA2214: Do not call overridable methods in constructors](../code-quality/ca2214.md) | When a constructor calls a virtual method, the constructor for the instance that invokes the method may not have executed. |
| CA2215 | [CA2215: Dispose methods should call base class dispose](../code-quality/ca2215.md) | If a type inherits from a disposable type, it must call the Dispose method of the base type from its own Dispose method. |
| CA2216 |[CA2216: Disposable types should declare finalizer](../code-quality/ca2216.md) | A type that implements System.IDisposable and has fields that suggest the use of unmanaged resources does not implement a finalizer, as described by Object.Finalize. |
| CA2217 | [CA2217: Do not mark enums with FlagsAttribute](../code-quality/ca2217.md) |An externally visible enumeration is marked by using FlagsAttribute, and it has one or more values that are not powers of two or a combination of the other defined values on the enumeration. |
| CA2219 | [CA2219: Do not raise exceptions in exception clauses](../code-quality/ca2219.md) | When an exception is raised in a finally or fault clause, the new exception hides the active exception. When an exception is raised in a filter clause, the run time silently catches the exception. This makes the original error difficult to detect and debug. |
| CA2225 | [CA2225: Operator overloads have named alternates](../code-quality/ca2225.md) |An operator overload was detected, and the expected named alternative method was not found. The named alternative member provides access to the same functionality as the operator and is provided for developers who program in languages that do not support overloaded operators. |
| CA2226 | [CA2226: Operators should have symmetrical overloads](../code-quality/ca2226.md) | A type implements the equality or inequality operator and does not implement the opposite operator. |
| CA2227 |[CA2227: Collection properties should be read only](../code-quality/ca2227.md) |A writable collection property allows a user to replace the collection with a different collection. A read-only property stops the collection from being replaced but still allows the individual members to be set. |
| CA2229 | [CA2229: Implement serialization constructors](../code-quality/ca2229.md) | To fix a violation of this rule, implement the serialization constructor. For a sealed class, make the constructor private; otherwise, make it protected. |
| CA2231 | [CA2231: Overload operator equals on overriding ValueType.Equals](../code-quality/ca2231.md) | A value type overrides Object.Equals but does not implement the equality operator. |
| CA2234 | [CA2234: Pass System.Uri objects instead of strings](../code-quality/ca2234.md) | A call is made to a method that has a string parameter whose name contains "uri", "URI", "urn", "URN", "url", or "URL". The declaring type of the method contains a corresponding method overload that has a System.Uri parameter. |
| CA2235 | [CA2235: Mark all non-serializable fields](../code-quality/ca2235.md) | An instance field of a type that is not serializable is declared in a type that is serializable. |
| CA2237 | [CA2237: Mark ISerializable types with SerializableAttribute](../code-quality/ca2237.md) | To be recognized by the common language runtime as serializable, types must be marked by using the SerializableAttribute attribute even when the type uses a custom serialization routine through implementation of the ISerializable interface. |
| CA2241 | [CA2241: Provide correct arguments to formatting methods](../code-quality/ca2241.md) | The format argument that is passed to System.String.Format does not contain a format item that corresponds to each object argument, or vice versa. |
| CA2242 |[CA2242: Test for NaN correctly](../code-quality/ca2242.md) | This expression tests a value against Single.Nan or Double.Nan. Use Single.IsNan(Single) or Double.IsNan(Double) to test the value. |
| CA2243 |[CA2243: Attribute string literals should parse correctly](../code-quality/ca2243.md) | The string literal parameter of an attribute does not parse correctly for a URL, a GUID, or a version. |
| CA2244 | [CA2244: Do not duplicate indexed element initializations](../code-quality/ca2244.md) | An object initializer has more than one indexed element initializer with the same constant index. All but the last initializer are redundant. |
| CA2245 | [CA2245: Do not assign a property to itself](../code-quality/ca2245.md) | A property was accidentally assigned to itself. |
| CA2246 | [CA2246: Do not assign a symbol and its member in the same statement](../code-quality/ca2246.md) | Assigning a symbol and its member, that is, a field or a property, in the same statement is not recommended. It is not clear if the member access was intended to use the symbol's old value prior to the assignment or the new value from the assignment in this statement. |
| CA2247 | [CA2247: Argument passed to TaskCompletionSource constructor should be TaskCreationOptions enum instead of TaskContinuationOptions enum.](../code-quality/ca2247.md) | TaskCompletionSource has constructors that take TaskCreationOptions that control the underlying Task, and constructors that take object state that's stored in the task.  Accidentally passing a TaskContinuationOptions instead of a TaskCreationOptions will result in the call treating the options as state. |
| CA2248 | [CA2248: Provide correct enum argument to Enum.HasFlag](../code-quality/ca2248.md) | The enum type passed as an argument to the `HasFlag` method call is different from the calling enum type. |
| CA2249 | [CA2249: Consider using String.Contains instead of String.IndexOf](../code-quality/ca2249.md) | Calls to `string.IndexOf` where the result is used to check for the presence/absence of a substring can be replaced by `string.Contains`. |
| CA2300 | [CA2300: Do not use insecure deserializer BinaryFormatter](../code-quality/ca2300.md) | Insecure deserializers are vulnerable when deserializing untrusted data. An attacker could modify the serialized data to include unexpected types to inject objects with malicious side effects. |
| CA2301 | [CA2301: Do not call BinaryFormatter.Deserialize without first setting BinaryFormatter.Binder](../code-quality/ca2301.md) | Insecure deserializers are vulnerable when deserializing untrusted data. An attacker could modify the serialized data to include unexpected types to inject objects with malicious side effects. |
| CA2302 | [CA2302: Ensure BinaryFormatter.Binder is set before calling BinaryFormatter.Deserialize](../code-quality/ca2302.md) | Insecure deserializers are vulnerable when deserializing untrusted data. An attacker could modify the serialized data to include unexpected types to inject objects with malicious side effects. |
| CA2305 | [CA2305: Do not use insecure deserializer LosFormatter](../code-quality/ca2305.md) | Insecure deserializers are vulnerable when deserializing untrusted data. An attacker could modify the serialized data to include unexpected types to inject objects with malicious side effects. |
| CA2310 | [CA2310: Do not use insecure deserializer NetDataContractSerializer](../code-quality/ca2310.md) | Insecure deserializers are vulnerable when deserializing untrusted data. An attacker could modify the serialized data to include unexpected types to inject objects with malicious side effects. |
| CA2311 | [CA2311: Do not deserialize without first setting NetDataContractSerializer.Binder](../code-quality/ca2311.md) | Insecure deserializers are vulnerable when deserializing untrusted data. An attacker could modify the serialized data to include unexpected types to inject objects with malicious side effects. |
| CA2312 | [CA2312: Ensure NetDataContractSerializer.Binder is set before deserializing](../code-quality/ca2312.md) | Insecure deserializers are vulnerable when deserializing untrusted data. An attacker could modify the serialized data to include unexpected types to inject objects with malicious side effects. |
| CA2315 | [CA2315: Do not use insecure deserializer ObjectStateFormatter](../code-quality/ca2315.md) | Insecure deserializers are vulnerable when deserializing untrusted data. An attacker could modify the serialized data to include unexpected types to inject objects with malicious side effects. |
| CA2321 | [CA2321: Do not deserialize with JavaScriptSerializer using a SimpleTypeResolver](../code-quality/ca2321.md) | Insecure deserializers are vulnerable when deserializing untrusted data. An attacker could modify the serialized data to include unexpected types to inject objects with malicious side effects. |
| CA2322 | [CA2322: Ensure JavaScriptSerializer is not initialized with SimpleTypeResolver before deserializing](../code-quality/ca2322.md) | Insecure deserializers are vulnerable when deserializing untrusted data. An attacker could modify the serialized data to include unexpected types to inject objects with malicious side effects. |
| CA2326 | [CA2326: Do not use TypeNameHandling values other than None](../code-quality/ca2326.md) | Insecure deserializers are vulnerable when deserializing untrusted data. An attacker could modify the serialized data to include unexpected types to inject objects with malicious side effects. |
| CA2327 | [CA2327: Do not use insecure JsonSerializerSettings](../code-quality/ca2327.md) | Insecure deserializers are vulnerable when deserializing untrusted data. An attacker could modify the serialized data to include unexpected types to inject objects with malicious side effects. |
| CA2328 | [CA2328: Ensure that JsonSerializerSettings are secure](../code-quality/ca2328.md) | Insecure deserializers are vulnerable when deserializing untrusted data. An attacker could modify the serialized data to include unexpected types to inject objects with malicious side effects. |
| CA2329 | [CA2329: Do not deserialize with JsonSerializer using an insecure configuration](../code-quality/ca2329.md) | Insecure deserializers are vulnerable when deserializing untrusted data. An attacker could modify the serialized data to include unexpected types to inject objects with malicious side effects. |
| CA2330 | [CA2330: Ensure that JsonSerializer has a secure configuration when deserializing](../code-quality/ca2330.md) | Insecure deserializers are vulnerable when deserializing untrusted data. An attacker could modify the serialized data to include unexpected types to inject objects with malicious side effects. |
| CA2350 | [CA2350: Ensure DataTable.ReadXml()'s input is trusted](ca2350.md) | When deserializing a <xref:System.Data.DataTable> with untrusted input, an attacker can craft malicious input to perform a denial of service attack. There may be unknown remote code execution vulnerabilities. |
| CA2351 | [CA2351: Ensure DataSet.ReadXml()'s input is trusted](ca2351.md) | When deserializing a <xref:System.Data.DataSet> with untrusted input, an attacker can craft malicious input to perform a denial of service attack. There may be unknown remote code execution vulnerabilities. |
| CA2352 | [CA2352: Unsafe DataSet or DataTable in serializable type can be vulnerable to remote code execution attacks](ca2352.md) | A class or struct marked with <xref:System.SerializableAttribute> contains a <xref:System.Data.DataSet> or <xref:System.Data.DataTable> field or property, and doesn't have a <xref:System.CodeDom.Compiler.GeneratedCodeAttribute>. |
| CA2353 | [CA2353: Unsafe DataSet or DataTable in serializable type](ca2353.md) | A class or struct marked with an XML serialization attribute or a data contract attribute contains a <xref:System.Data.DataSet> or <xref:System.Data.DataTable> field or property. |
| CA2354 | [CA2354: Unsafe DataSet or DataTable in deserialized object graph can be vulnerable to remote code execution attack](ca2354.md) | Deserializing with an <xref:System.Runtime.Serialization.IFormatter?displayProperty=nameWithType> serialized, and the casted type's object graph can include a <xref:System.Data.DataSet> or <xref:System.Data.DataTable>. |
| CA2355 | [CA2355: Unsafe DataSet or DataTable in deserialized object graph](ca2355.md) | Deserializing when the casted or specified type's object graph can include a <xref:System.Data.DataSet> or <xref:System.Data.DataTable>. |
| CA2356 | [CA2356: Unsafe DataSet or DataTable in web deserialized object graph](ca2356.md) | A method with a <xref:System.Web.Services.WebMethodAttribute?displayProperty=nameWithType> or <xref:System.ServiceModel.OperationContractAttribute?displayProperty=nameWithType> has a parameter that may reference a <xref:System.Data.DataSet> or <xref:System.Data.DataTable>. |
| CA2361 | [CA2361: Ensure autogenerated class containing DataSet.ReadXml() is not used with untrusted data](ca2361.md) | When deserializing a <xref:System.Data.DataSet> with untrusted input, an attacker can craft malicious input to perform a denial of service attack. There may be unknown remote code execution vulnerabilities. |
| CA2362 | [CA2362: Unsafe DataSet or DataTable in autogenerated serializable type can be vulnerable to remote code execution attacks](ca2362.md) | When deserializing untrusted input with <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter> and the deserialized object graph contains a <xref:System.Data.DataSet> or <xref:System.Data.DataTable>, an attacker can craft a malicious payload to perform a remote code execution attack. |
| CA3001 | [CA3001: Review code for SQL injection vulnerabilities](../code-quality/ca3001.md) | When working with untrusted input and SQL commands, be mindful of SQL injection attacks. An SQL injection attack can execute malicious SQL commands, compromising the security and integrity of your application. |
| CA3002 | [CA3002: Review code for XSS vulnerabilities](../code-quality/ca3002.md) | When working with untrusted input from web requests, be mindful of cross-site scripting (XSS) attacks. An XSS attack injects untrusted input into raw HTML output, allowing the attacker to execute malicious scripts or maliciously modify content in your web page. |
| CA3003 | [CA3003: Review code for file path injection vulnerabilities](../code-quality/ca3003.md) | When working with untrusted input from web requests, be mindful of using user-controlled input when specifying paths to files. |
| CA3004 | [CA3004: Review code for information disclosure vulnerabilities](../code-quality/ca3004.md) | Disclosing exception information gives attackers insight into the internals of your application, which can help attackers find other vulnerabilities to exploit. |
| CA3006 | [CA3006: Review code for process command injection vulnerabilities](../code-quality/ca3006.md) | When working with untrusted input, be mindful of command injection attacks. A command injection attack can execute malicious commands on the underlying operating system, compromising the security and integrity of your server. |
| CA3007 | [CA3007: Review code for open redirect vulnerabilities](../code-quality/ca3007.md) | When working with untrusted input, be mindful of open redirect vulnerabilities. An attacker can exploit an open redirect vulnerability to use your website to give the appearance of a legitimate URL, but redirect an unsuspecting visitor to a phishing or other malicious webpage. |
| CA3008 | [CA3008: Review code for XPath injection vulnerabilities](../code-quality/ca3008.md) | When working with untrusted input, be mindful of XPath injection attacks. Constructing XPath queries using untrusted input may allow an attacker to maliciously manipulate the query to return an unintended result, and possibly disclose the contents of the queried XML. |
| CA3009 | [CA3009: Review code for XML injection vulnerabilities](../code-quality/ca3009.md) | When working with untrusted input, be mindful of XML injection attacks. |
| CA3010 | [CA3010: Review code for XAML injection vulnerabilities](../code-quality/ca3010.md) | When working with untrusted input, be mindful of XAML injection attacks. XAML is a markup language that directly represents object instantiation and execution. That means elements created in XAML can interact with system resources (for example, network access and file system IO). |
| CA3011 | [CA3011: Review code for DLL injection vulnerabilities](../code-quality/ca3011.md) | When working with untrusted input, be mindful of loading untrusted code. If your web application loads untrusted code, an attacker may be able to inject malicious DLLs into your process and execute malicious code. |
| CA3012 | [CA3012: Review code for regex injection vulnerabilities](../code-quality/ca3012.md) | When working with untrusted input, be mindful of regex injection attacks. An attacker can use regex injection to maliciously modify a regular expression, to make the regex match unintended results, or to make the regex consume excessive CPU resulting in a Denial of Service attack. |
| CA3061 | [CA3061: Do not add schema by URL](../code-quality/ca3061.md) | Do not use the unsafe overload of the Add method because it may cause dangerous external references. |
| CA3075 | [CA3075: Insecure DTD Processing](../code-quality/ca3075.md) | If you use insecure DTDProcessing instances or reference external entity sources, the parser may accept untrusted input and disclose sensitive information to attackers. |
| CA3076 | [CA3076: Insecure XSLT Script Execution](../code-quality/ca3076.md) | If you execute Extensible Stylesheet Language Transformations (XSLT) in .NET applications insecurely, the processor may resolve untrusted URI references that could disclose sensitive information to attackers, leading to Denial of Service and Cross-Site attacks. |
| CA3077 | [CA3077: Insecure Processing in API Design, XML Document and XML Text Reader](../code-quality/ca3077.md) | When designing an API derived from XMLDocument and XMLTextReader, be mindful of DtdProcessing. Using insecure DTDProcessing instances when referencing or resolving external entity sources or setting insecure values in the XML may lead to information disclosure. |
| CA3147 | [CA3147: Mark verb handlers with ValidateAntiForgeryToken](../code-quality/ca3147.md) | When designing an ASP.NET MVC controller, be mindful of cross-site request forgery attacks. A cross-site request forgery attack can send malicious requests from an authenticated user to your ASP.NET MVC controller. |
| CA5350 | [CA5350: Do Not Use Weak Cryptographic Algorithms](../code-quality/ca5350.md) | Weak encryption algorithms and hashing functions are used today for a number of reasons, but they should not be used to guarantee the confidentiality or integrity of the data they protect. This rule triggers when it finds TripleDES, SHA1, or RIPEMD160 algorithms in the code.|
| CA5351 | [CA5351 Do Not Use Broken Cryptographic Algorithms](../code-quality/ca5351.md) | Broken cryptographic algorithms are not considered secure and their use should be strongly discouraged. This rule triggers when it finds the MD5 hash algorithm or either the DES or RC2 encryption algorithms in code. |
| CA5358 | [CA5358: Do Not Use Unsafe Cipher Modes](../code-quality/ca5358.md) | Do Not Use Unsafe Cipher Modes |
| CA5359 | [CA5359 Do not disable certificate validation](../code-quality/ca5359.md) | A certificate can help authenticate the identity of the server. Clients should validate the server certificate to ensure requests are sent to the intended server. If the ServerCertificateValidationCallback always returns `true`, any certificate will pass validation. |
| CA5360 | [CA5360 Do not call dangerous methods in deserialization](../code-quality/ca5360.md) | Insecure deserialization is a vulnerability which occurs when untrusted data is used to abuse the logic of an application, inflict a Denial-of-Service (DoS) attack, or even execute arbitrary code upon it being deserialized. It's frequently possible for malicious users to abuse these deserialization features when the application is deserializing untrusted data which is under their control. Specifically, invoke dangerous methods in the process of deserialization. Successful insecure deserialization attacks could allow an attacker to carry out attacks such as DoS attacks, authentication bypasses, and remote code execution. |
| CA5361 | [CA5361: Do not disable SChannel use of strong crypto](../code-quality/ca5361.md) | Setting `Switch.System.Net.DontEnableSchUseStrongCrypto` to `true` weakens the cryptography used in outgoing Transport Layer Security (TLS) connections. Weaker cryptography can compromise the confidentiality of communication between your application and the server, making it easier for attackers to eavesdrop sensitive data. |
| CA5362 | [CA5362 Potential reference cycle in deserialized object graph](../code-quality/ca5362.md) | If deserializing untrusted data, then any code processing the deserialized object graph needs to handle reference cycles without going into infinite loops. This includes both code that's part of a deserialization callback and code that processes the object graph after deserialization completed. Otherwise, an attacker could perform a Denial-of-Service attack with malicious data containing a reference cycle. |
| CA5363 | [CA5363: Do not disable request validation](../code-quality/ca5363.md) | Request validation is a feature in ASP.NET that examines HTTP requests and determines whether they contain potentially dangerous content that can lead to injection attacks, including cross-site-scripting. |
| CA5364 | [CA5364: Do not use deprecated security protocols](../code-quality/ca5364.md) | Transport Layer Security (TLS) secures communication between computers, most commonly with Hypertext Transfer Protocol Secure (HTTPS). Older protocol versions of TLS are less secure than TLS 1.2 and TLS 1.3 and are more likely to have new vulnerabilities. Avoid older protocol versions to minimize risk. |
| CA5365 | [CA5365 Do Not Disable HTTP Header Checking](../code-quality/ca5365.md) | HTTP header checking enables encoding of the carriage return and newline characters, \r and \n, that are found in response headers. This encoding can help to avoid injection attacks that exploit an application that echoes untrusted data contained by the header. |
| CA5366 | [CA5366 Use XmlReader For DataSet Read XML](../code-quality/ca5366.md) | Using a <xref:System.Data.DataSet> to read XML with untrusted data may load dangerous external references, which should be restricted by using an <xref:System.Xml.XmlReader> with a secure resolver or with DTD processing disabled. |
| CA5367 | [CA5367 Do Not Serialize Types With Pointer Fields](../code-quality/ca5367.md) | This rule checks whether there’s a serializable class with a pointer field or property. Members that can’t be serialized can be a pointer, such as static members or fields marked with <xref:System.NonSerializedAttribute>. |
| CA5368 | [CA5368 Set ViewStateUserKey For Classes Derived From Page](../code-quality/ca5368.md) | Setting the <xref:System.Web.UI.Page.ViewStateUserKey> property can help you prevent attacks on your application by allowing you to assign an identifier to the view-state variable for individual users so that attackers cannot use the variable to generate an attack. Otherwise, there will be vulnerabilities to cross-site request forgery. |
| CA5369 | [CA5369: Use XmlReader for Deserialize](../code-quality/ca5369.md) | Processing untrusted DTD and XML schemas may enable loading dangerous external references, which should be restricted by using an XmlReader with a secure resolver or with DTD and XML inline schema processing disabled. |
| CA5370 | [CA5370: Use XmlReader for validating reader](../code-quality/ca5370.md) | Processing untrusted DTD and XML schemas may enable loading dangerous external references. This dangerous loading can be restricted by using an XmlReader with a secure resolver or with DTD and XML inline schema processing disabled. |
| CA5371 | [CA5371: Use XmlReader for schema read](../code-quality/ca5371.md) | Processing untrusted DTD and XML schemas may enable loading dangerous external references. Using an XmlReader with a secure resolver or with DTD and XML inline schema processing disabled restricts this. |
| CA5372 | [CA5372: Use XmlReader for XPathDocument](../code-quality/ca5372.md) | Processing XML from untrusted data may load dangerous external references, which can be restricted by using an XmlReader with a secure resolver or with DTD processing disabled. |
| CA5373 | [CA5373: Do not use obsolete key derivation function](../code-quality/ca5373.md) | This rule detects the invocation of weak key derivation methods <xref:System.Security.Cryptography.PasswordDeriveBytes?displayProperty=fullName> and `Rfc2898DeriveBytes.CryptDeriveKey`. <xref:System.Security.Cryptography.PasswordDeriveBytes?displayProperty=fullName> used a weak algorithm PBKDF1. |
| CA5374 | [CA5374 Do Not Use XslTransform](../code-quality/ca5374.md) | This rule checks if <xref:System.Xml.Xsl.XslTransform?displayProperty=nameWithType> is instantiated in the code. <xref:System.Xml.Xsl.XslTransform?displayProperty=nameWithType> is now obsolete and shouldn’t be used. |
| CA5375 | [CA5375 Do not use account shared access signature](../code-quality/ca5375.md) | An account SAS can delegate access to read, write, and delete operations on blob containers, tables, queues, and file shares that are not permitted with a service SAS. However, it doesn't support container-level policies and has less flexibility and control over the permissions that are granted. Once malicious users get it, your storage account will be compromised easily. |
| CA5376 | [CA5376 Use SharedAccessProtocol HttpsOnly](../code-quality/ca5376.md) | SAS is sensitive data that can't be transported in plain text on HTTP. |
| CA5377 | [CA5377 Use container level access policy](../code-quality/ca5377.md) | A container-level access policy can be modified or revoked at any time. It provides greater flexibility and control over the permissions that are granted. |
| CA5378 | [CA5378: Do not disable ServicePointManagerSecurityProtocols](../code-quality/ca5378.md) | Setting `Switch.System.ServiceModel.DisableUsingServicePointManagerSecurityProtocols` to `true` limits Windows Communication Framework's (WCF) Transport Layer Security (TLS) connections to using TLS 1.0. That version of TLS will be deprecated. |
| CA5379 | [CA5379 Do not use weak key derivation function algorithm](../code-quality/ca5379.md) | The <xref:System.Security.Cryptography.Rfc2898DeriveBytes> class defaults to using the <xref:System.Security.Cryptography.HashAlgorithmName.SHA1> algorithm. You should specify the hash algorithm to use in some overloads of the constructor with <xref:System.Security.Cryptography.HashAlgorithmName.SHA256> or higher. Note, <xref:System.Security.Cryptography.Rfc2898DeriveBytes.HashAlgorithm> property only has a `get` accessor and doesn't have a `overriden` modifier. |
| CA5380 | [CA5380: Do not add certificates to root store](../code-quality/ca5380.md) | This rule detects code that adds a certificate into the Trusted Root Certification Authorities certificate store. By default, the Trusted Root Certification Authorities certificate store is configured with a set of public CAs that has met the requirements of the Microsoft Root Certificate Program. |
| CA5381 | [CA5381: Ensure certificates are not added to root store](../code-quality/ca5381.md) | This rule detects code that potentially adds a certificate into the Trusted Root Certification Authorities certificate store. By default, the Trusted Root Certification Authorities certificate store is configured with a set of public certification authorities (CAs) that has met the requirements of the Microsoft Root Certificate Program. |
| CA5382 | [CA5382 Use secure cookies in ASP.NET Core](../code-quality/ca5382.md) | Applications available over HTTPS must use secure cookies, which indicate to the browser that the cookie should only be transmitted using Secure Sockets Layer (SSL). |
| CA5383 | [CA5383 Ensure use secure cookies in ASP.NET Core](../code-quality/ca5383.md) | Applications available over HTTPS must use secure cookies, which indicate to the browser that the cookie should only be transmitted using Secure Sockets Layer (SSL). |
| CA5384 | [CA5384 Do not use digital signature algorithm (DSA)](../code-quality/ca5384.md) | DSA is a weak asymmetric encryption algorithm. |
| CA5385 | [CA5385 Use Rivest–Shamir–Adleman (RSA) algorithm with sufficient key size](../code-quality/ca5385.md) | An RSA key smaller than 2048 bits is more vulnerable to brute force attacks. |
| CA5386 | [CA5386: Avoid hardcoding SecurityProtocolType value](../code-quality/ca5386.md) | Transport Layer Security (TLS) secures communication between computers, most commonly with Hypertext Transfer Protocol Secure (HTTPS). Protocol versions TLS 1.0 and TLS 1.1 are deprecated, while TLS 1.2 and TLS 1.3 are current. In the future, TLS 1.2 and TLS 1.3 may be deprecated. To ensure that your application remains secure, avoid hardcoding a protocol version and target at least .NET Framework v4.7.1. |
| CA5387 | [CA5387 Do not use weak key derivation function with insufficient iteration count](../code-quality/ca5387.md) | This rule checks if a cryptographic key was generated by <xref:System.Security.Cryptography.Rfc2898DeriveBytes> with an iteration count of less than 100,000. A higher iteration count can help mitigate against dictionary attacks that try to guess the generated cryptographic key. |
| CA5388 | [CA5388 Ensure sufficient iteration count when using weak key derivation function](../code-quality/ca5388.md) | This rule checks if a cryptographic key was generated by <xref:System.Security.Cryptography.Rfc2898DeriveBytes> with an iteration count that may be less than 100,000. A higher iteration count can help mitigate against dictionary attacks that try to guess the generated cryptographic key. |
| CA5389 | [CA5389: Do not add archive item's path to the target file system path](../code-quality/ca5389.md) | File path can be relative and can lead to file system access outside of the expected file system target path, leading to malicious config changes and remote code execution via lay-and-wait technique. |
| CA5390 | [CA5390 Do not hard-code encryption key](../code-quality/ca5390.md) | For a symmetric algorithm to be successful, the secret key must be known only to the sender and the receiver. When a key is hard-coded, it is easily discovered. Even with compiled binaries, it is easy for malicious users to extract it. Once the private key is compromised, the cipher text can be decrypted directly and is not protected anymore. |
| CA5391 | [CA5391 Use antiforgery tokens in ASP.NET Core MVC controllers](../code-quality/ca5391.md) | Handling a `POST`, `PUT`, `PATCH`, or `DELETE` request without validating an antiforgery token may be vulnerable to cross-site request forgery attacks. A cross-site request forgery attack can send malicious requests from an authenticated user to your ASP.NET Core MVC controller. |
| CA5392 | [CA5392 Use DefaultDllImportSearchPaths attribute for P/Invokes](../code-quality/ca5392.md) | By default, P/Invoke functions using <xref:System.Runtime.InteropServices.DllImportAttribute> probe a number of directories, including the current working directory for the library to load. This can be a security issue for certain applications, leading to DLL hijacking. |
| CA5393 | [CA5393 Do not use unsafe DllImportSearchPath value](../code-quality/ca5393.md) | There could be a malicious DLL in the default DLL search directories and assembly directories. Or, depending on where your application is run from, there could be a malicious DLL in the application's directory. |
| CA5394 | [CA5394 Do not use insecure randomness](../code-quality/ca5394.md) | Using a cryptographically weak pseudo-random number generator may allow an attacker to predict what security-sensitive value will be generated. |
| CA5395 | [CA5395 Miss HttpVerb attribute for action methods](../code-quality/ca5395.md) | All the action methods that create, edit, delete, or otherwise modify data needs to be protected with the antiforgery attribute from cross-site request forgery attacks. Performing a GET operation should be a safe operation that has no side effects and doesn't modify your persisted data. |
| CA5396 | [CA5396 Set HttpOnly to true for HttpCookie](../code-quality/ca5396.md) | As a defense in depth measure, ensure security sensitive HTTP cookies are marked as HttpOnly. This indicates web browsers should disallow scripts from accessing the cookies. Injected malicious scripts are a common way of stealing cookies. |
| CA5397 | [CA5397: Do not use deprecated SslProtocols values](../code-quality/ca5397.md) | Transport Layer Security (TLS) secures communication between computers, most commonly with Hypertext Transfer Protocol Secure (HTTPS). Older protocol versions of TLS are less secure than TLS 1.2 and TLS 1.3 and are more likely to have new vulnerabilities. Avoid older protocol versions to minimize risk. |
| CA5398 | [CA5398: Avoid hardcoded SslProtocols values](../code-quality/ca5398.md) | Transport Layer Security (TLS) secures communication between computers, most commonly with Hypertext Transfer Protocol Secure (HTTPS). Protocol versions TLS 1.0 and TLS 1.1 are deprecated, while TLS 1.2 and TLS 1.3 are current. In the future, TLS 1.2 and TLS 1.3 may be deprecated. To ensure that your application remains secure, avoid hardcoding a protocol version. |
| CA5399 | [CA5399 Definitely disable HttpClient certificate revocation list check](../code-quality/ca5399.md) | A revoked certificate isn't trusted anymore. It could be used by attackers passing some malicious data or stealing sensitive data in HTTPS communication. |
| CA5400 | [CA5400 Ensure HttpClient certificate revocation list check is not disabled](../code-quality/ca5400.md) | A revoked certificate isn't trusted anymore. It could be used by attackers passing some malicious data or stealing sensitive data in HTTPS communication. |
| CA5401 | [CA5401 Do not use CreateEncryptor with non-default IV](../code-quality/ca5401.md) | Symmetric encryption should always use a non-repeatable initialization vector to prevent dictionary attacks. |
| CA5402 | [CA5402 Use CreateEncryptor with the default IV](../code-quality/ca5402.md) | Symmetric encryption should always use a non-repeatable initialization vector to prevent dictionary attacks. |
| CA5403 | [CA5403: Do not hard-code certificate](../code-quality/ca5403.md) | The `data` or `rawData` parameter of a <xref:System.Security.Cryptography.X509Certificates.X509Certificate> or <xref:System.Security.Cryptography.X509Certificates.X509Certificate2> constructor is hard-coded. |
| IL3000 | [IL3000 Avoid accessing Assembly file path when publishing as a single file](../code-quality/il3000.md) | Avoid using accessing Assembly file path when publishing as a single file |
| IL3001 | [IL3001 Avoid accessing Assembly file path when publishing as a single-file](../code-quality/il3001.md) | Avoid accessing Assembly file path when publishing as a single-file |
