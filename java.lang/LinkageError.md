# LinkageError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LinkageError

```
open class LinkageError : Error
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Error](Error.md) ||
| | | ↳ | [java.lang.LinkageError](LinkageError.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [BootstrapMethodError](BootstrapMethodError.md), [ClassCircularityError](ClassCircularityError.md), [ClassFormatError](ClassFormatError.md), [ExceptionInInitializerError](ExceptionInInitializerError.md), [IncompatibleClassChangeError](IncompatibleClassChangeError.md), [NoClassDefFoundError](NoClassDefFoundError.md), [UnsatisfiedLinkError](UnsatisfiedLinkError.md), [VerifyError](VerifyError.md) |-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BootstrapMethodError](BootstrapMethodError.md) | Thrown to indicate that an `invokedynamic` instruction or a dynamic constant failed to resolve its bootstrap method and arguments, or for `invokedynamic` instruction the bootstrap method has failed to provide a [call site](../java.lang.invoke/CallSite.md) with a [target](../java.lang.invoke/CallSite.md)) of the correct [method type](../java.lang.invoke/MethodHandle.md)), or for a dynamic constant the bootstrap method has failed to provide a constant value of the required type. | | [ClassCircularityError](ClassCircularityError.md) | Thrown when the Java Virtual Machine detects a circularity in the superclass hierarchy of a class being loaded. | | [ClassFormatError](ClassFormatError.md) | Thrown when the Java Virtual Machine attempts to read a class file and determines that the file is malformed or otherwise cannot be interpreted as a class file. | | [ExceptionInInitializerError](ExceptionInInitializerError.md) | Signals that an unexpected exception has occurred in a static initializer. | | [IncompatibleClassChangeError](IncompatibleClassChangeError.md) | Thrown when an incompatible class change has occurred to some class definition. | | [NoClassDefFoundError](NoClassDefFoundError.md) | Thrown if the Java Virtual Machine or a `ClassLoader` instance tries to load in the definition of a class (as part of a normal method call or as part of creating a new instance using the `new` expression) and no definition of the class could be found. | | [UnsatisfiedLinkError](UnsatisfiedLinkError.md) | Thrown if the Java Virtual Machine cannot find an appropriate native-language definition of a method declared `native`. | | [VerifyError](VerifyError.md) | Thrown when the "verifier" detects that a class file, though well formed, contains some sort of internal inconsistency or security problem. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbstractMethodError](AbstractMethodError.md), [GenericSignatureFormatError](../java.lang.reflect/GenericSignatureFormatError.md), [IllegalAccessError](IllegalAccessError.md), [InstantiationError](InstantiationError.md), [NoSuchFieldError](NoSuchFieldError.md), [NoSuchMethodError](NoSuchMethodError.md), [UnsupportedClassVersionError](UnsupportedClassVersionError.md) |-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractMethodError](AbstractMethodError.md) | Thrown when an application tries to call an abstract method. | | [GenericSignatureFormatError](../java.lang.reflect/GenericSignatureFormatError.md) | Thrown when a syntactically malformed signature attribute is encountered by a reflective method that needs to interpret the generic signature information for a type, method or constructor. | | [IllegalAccessError](IllegalAccessError.md) | Thrown if an application attempts to access or modify a field, or to call a method that it does not have access to. | | [InstantiationError](InstantiationError.md) | Thrown when an application tries to use the Java `new` construct to instantiate an abstract class or an interface. | | [NoSuchFieldError](NoSuchFieldError.md) | Thrown if an application tries to access or modify a specified field of an object, and that object no longer has that field. | | [NoSuchMethodError](NoSuchMethodError.md) | Thrown if an application tries to call a specified method of a class (either static or instance), and that class no longer has a definition of that method. | | [UnsupportedClassVersionError](UnsupportedClassVersionError.md) | Thrown when the Java Virtual Machine attempts to read a class file and determines that the major and minor version numbers in the file are not supported. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Subclasses of `LinkageError` indicate that a class has some dependency on another class; however, the latter class has incompatibly changed after the compilation of the former class.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LinkageError](LinkageError.md))`()` Constructs a `LinkageError` with no detail message. |
| [LinkageError](LinkageError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a `LinkageError` with the specified detail message. |
| [LinkageError](LinkageError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a `LinkageError` with the specified detail message and cause. |

## Public constructors

### LinkageError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinkageError()
```

Constructs a `LinkageError` with no detail message. 

### LinkageError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinkageError(s: String!)
```

Constructs a `LinkageError` with the specified detail message.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message. |

### LinkageError

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinkageError(
    s: String!, 
    cause: Throwable!)
```

Constructs a `LinkageError` with the specified detail message and cause.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause, may be `null` |
