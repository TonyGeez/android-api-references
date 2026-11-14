# LinkageError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LinkageError

```
open class LinkageError : Error
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Error](../java/lang/Error.md) ||
| | | ↳ | [java.lang.LinkageError](../java/lang/LinkageError.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [BootstrapMethodError](../java/lang/BootstrapMethodError.md), [ClassCircularityError](../java/lang/ClassCircularityError.md), [ClassFormatError](../java/lang/ClassFormatError.md), [ExceptionInInitializerError](../java/lang/ExceptionInInitializerError.md), [IncompatibleClassChangeError](../java/lang/IncompatibleClassChangeError.md), [NoClassDefFoundError](../java/lang/NoClassDefFoundError.md), [UnsatisfiedLinkError](../java/lang/UnsatisfiedLinkError.md), [VerifyError](../java/lang/VerifyError.md) |-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BootstrapMethodError](../java/lang/BootstrapMethodError.md) | Thrown to indicate that an `invokedynamic` instruction or a dynamic constant failed to resolve its bootstrap method and arguments, or for `invokedynamic` instruction the bootstrap method has failed to provide a [call site](../java/lang/invoke/CallSite.md) with a [target](../java/lang/invoke/CallSite.md)) of the correct [method type](../java/lang/invoke/MethodHandle.md)), or for a dynamic constant the bootstrap method has failed to provide a constant value of the required type. | | [ClassCircularityError](../java/lang/ClassCircularityError.md) | Thrown when the Java Virtual Machine detects a circularity in the superclass hierarchy of a class being loaded. | | [ClassFormatError](../java/lang/ClassFormatError.md) | Thrown when the Java Virtual Machine attempts to read a class file and determines that the file is malformed or otherwise cannot be interpreted as a class file. | | [ExceptionInInitializerError](../java/lang/ExceptionInInitializerError.md) | Signals that an unexpected exception has occurred in a static initializer. | | [IncompatibleClassChangeError](../java/lang/IncompatibleClassChangeError.md) | Thrown when an incompatible class change has occurred to some class definition. | | [NoClassDefFoundError](../java/lang/NoClassDefFoundError.md) | Thrown if the Java Virtual Machine or a `ClassLoader` instance tries to load in the definition of a class (as part of a normal method call or as part of creating a new instance using the `new` expression) and no definition of the class could be found. | | [UnsatisfiedLinkError](../java/lang/UnsatisfiedLinkError.md) | Thrown if the Java Virtual Machine cannot find an appropriate native-language definition of a method declared `native`. | | [VerifyError](../java/lang/VerifyError.md) | Thrown when the "verifier" detects that a class file, though well formed, contains some sort of internal inconsistency or security problem. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbstractMethodError](../java/lang/AbstractMethodError.md), [GenericSignatureFormatError](../java/lang/reflect/GenericSignatureFormatError.md), [IllegalAccessError](../java/lang/IllegalAccessError.md), [InstantiationError](../java/lang/InstantiationError.md), [NoSuchFieldError](../java/lang/NoSuchFieldError.md), [NoSuchMethodError](../java/lang/NoSuchMethodError.md), [UnsupportedClassVersionError](../java/lang/UnsupportedClassVersionError.md) |-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractMethodError](../java/lang/AbstractMethodError.md) | Thrown when an application tries to call an abstract method. | | [GenericSignatureFormatError](../java/lang/reflect/GenericSignatureFormatError.md) | Thrown when a syntactically malformed signature attribute is encountered by a reflective method that needs to interpret the generic signature information for a type, method or constructor. | | [IllegalAccessError](../java/lang/IllegalAccessError.md) | Thrown if an application attempts to access or modify a field, or to call a method that it does not have access to. | | [InstantiationError](../java/lang/InstantiationError.md) | Thrown when an application tries to use the Java `new` construct to instantiate an abstract class or an interface. | | [NoSuchFieldError](../java/lang/NoSuchFieldError.md) | Thrown if an application tries to access or modify a specified field of an object, and that object no longer has that field. | | [NoSuchMethodError](../java/lang/NoSuchMethodError.md) | Thrown if an application tries to call a specified method of a class (either static or instance), and that class no longer has a definition of that method. | | [UnsupportedClassVersionError](../java/lang/UnsupportedClassVersionError.md) | Thrown when the Java Virtual Machine attempts to read a class file and determines that the major and minor version numbers in the file are not supported. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Subclasses of `LinkageError` indicate that a class has some dependency on another class; however, the latter class has incompatibly changed after the compilation of the former class.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LinkageError](../java/lang/LinkageError.md))`()` Constructs a `LinkageError` with no detail message. |
| [LinkageError](../java/lang/LinkageError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a `LinkageError` with the specified detail message. |
| [LinkageError](../java/lang/LinkageError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a `LinkageError` with the specified detail message and cause. |

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
