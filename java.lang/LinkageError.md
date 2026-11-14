# LinkageError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LinkageError

```
open class LinkageError : Error
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error) ||
| | | ↳ | [java.lang.LinkageError](https://developer.android.com/reference/kotlin/java/lang/LinkageError#) |

| Known Direct Subclasses [BootstrapMethodError](https://developer.android.com/reference/kotlin/java/lang/BootstrapMethodError), [ClassCircularityError](https://developer.android.com/reference/kotlin/java/lang/ClassCircularityError), [ClassFormatError](https://developer.android.com/reference/kotlin/java/lang/ClassFormatError), [ExceptionInInitializerError](https://developer.android.com/reference/kotlin/java/lang/ExceptionInInitializerError), [IncompatibleClassChangeError](https://developer.android.com/reference/kotlin/java/lang/IncompatibleClassChangeError), [NoClassDefFoundError](https://developer.android.com/reference/kotlin/java/lang/NoClassDefFoundError), [UnsatisfiedLinkError](https://developer.android.com/reference/kotlin/java/lang/UnsatisfiedLinkError), [VerifyError](https://developer.android.com/reference/kotlin/java/lang/VerifyError) |-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BootstrapMethodError](https://developer.android.com/reference/kotlin/java/lang/BootstrapMethodError) | Thrown to indicate that an `invokedynamic` instruction or a dynamic constant failed to resolve its bootstrap method and arguments, or for `invokedynamic` instruction the bootstrap method has failed to provide a [call site](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite) with a [target](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite#getTarget()) of the correct [method type](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle#type()), or for a dynamic constant the bootstrap method has failed to provide a constant value of the required type. | | [ClassCircularityError](https://developer.android.com/reference/kotlin/java/lang/ClassCircularityError) | Thrown when the Java Virtual Machine detects a circularity in the superclass hierarchy of a class being loaded. | | [ClassFormatError](https://developer.android.com/reference/kotlin/java/lang/ClassFormatError) | Thrown when the Java Virtual Machine attempts to read a class file and determines that the file is malformed or otherwise cannot be interpreted as a class file. | | [ExceptionInInitializerError](https://developer.android.com/reference/kotlin/java/lang/ExceptionInInitializerError) | Signals that an unexpected exception has occurred in a static initializer. | | [IncompatibleClassChangeError](https://developer.android.com/reference/kotlin/java/lang/IncompatibleClassChangeError) | Thrown when an incompatible class change has occurred to some class definition. | | [NoClassDefFoundError](https://developer.android.com/reference/kotlin/java/lang/NoClassDefFoundError) | Thrown if the Java Virtual Machine or a `ClassLoader` instance tries to load in the definition of a class (as part of a normal method call or as part of creating a new instance using the `new` expression) and no definition of the class could be found. | | [UnsatisfiedLinkError](https://developer.android.com/reference/kotlin/java/lang/UnsatisfiedLinkError) | Thrown if the Java Virtual Machine cannot find an appropriate native-language definition of a method declared `native`. | | [VerifyError](https://developer.android.com/reference/kotlin/java/lang/VerifyError) | Thrown when the "verifier" detects that a class file, though well formed, contains some sort of internal inconsistency or security problem. | |

| Known Indirect Subclasses [AbstractMethodError](https://developer.android.com/reference/kotlin/java/lang/AbstractMethodError), [GenericSignatureFormatError](https://developer.android.com/reference/kotlin/java/lang/reflect/GenericSignatureFormatError), [IllegalAccessError](https://developer.android.com/reference/kotlin/java/lang/IllegalAccessError), [InstantiationError](https://developer.android.com/reference/kotlin/java/lang/InstantiationError), [NoSuchFieldError](https://developer.android.com/reference/kotlin/java/lang/NoSuchFieldError), [NoSuchMethodError](https://developer.android.com/reference/kotlin/java/lang/NoSuchMethodError), [UnsupportedClassVersionError](https://developer.android.com/reference/kotlin/java/lang/UnsupportedClassVersionError) |-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractMethodError](https://developer.android.com/reference/kotlin/java/lang/AbstractMethodError) | Thrown when an application tries to call an abstract method. | | [GenericSignatureFormatError](https://developer.android.com/reference/kotlin/java/lang/reflect/GenericSignatureFormatError) | Thrown when a syntactically malformed signature attribute is encountered by a reflective method that needs to interpret the generic signature information for a type, method or constructor. | | [IllegalAccessError](https://developer.android.com/reference/kotlin/java/lang/IllegalAccessError) | Thrown if an application attempts to access or modify a field, or to call a method that it does not have access to. | | [InstantiationError](https://developer.android.com/reference/kotlin/java/lang/InstantiationError) | Thrown when an application tries to use the Java `new` construct to instantiate an abstract class or an interface. | | [NoSuchFieldError](https://developer.android.com/reference/kotlin/java/lang/NoSuchFieldError) | Thrown if an application tries to access or modify a specified field of an object, and that object no longer has that field. | | [NoSuchMethodError](https://developer.android.com/reference/kotlin/java/lang/NoSuchMethodError) | Thrown if an application tries to call a specified method of a class (either static or instance), and that class no longer has a definition of that method. | | [UnsupportedClassVersionError](https://developer.android.com/reference/kotlin/java/lang/UnsupportedClassVersionError) | Thrown when the Java Virtual Machine attempts to read a class file and determines that the major and minor version numbers in the file are not supported. | |

Subclasses of `LinkageError` indicate that a class has some dependency on another class; however, the latter class has incompatibly changed after the compilation of the former class.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LinkageError](https://developer.android.com/reference/kotlin/java/lang/LinkageError#LinkageError())`()` Constructs a `LinkageError` with no detail message. |
| [LinkageError](https://developer.android.com/reference/kotlin/java/lang/LinkageError#LinkageError(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a `LinkageError` with the specified detail message. |
| [LinkageError](https://developer.android.com/reference/kotlin/java/lang/LinkageError#LinkageError(kotlin.String,%20kotlin.Throwable))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a `LinkageError` with the specified detail message and cause. |

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
