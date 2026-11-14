# Error

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Error

```
open class Error : Throwable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||
| | ↳ | [java.lang.Error](../java/lang/Error.md) |

| Known Direct Subclasses [AnnotationFormatError](../java/lang/annotation/AnnotationFormatError.md), [AssertionError](../java/lang/AssertionError.md), [AssertionFailedError](../android/test/AssertionFailedError.md), [CoderMalfunctionError](../java/nio/charset/CoderMalfunctionError.md), [FactoryConfigurationError](../javax/xml/parsers/FactoryConfigurationError.md), [IOError](../java/io/IOError.md), [LinkageError](../java/lang/LinkageError.md), [ServiceConfigurationError](../java/util/ServiceConfigurationError.md), [ThreadDeath](../java/lang/ThreadDeath.md), [TransformerFactoryConfigurationError](../javax/xml/transform/TransformerFactoryConfigurationError.md), [VirtualMachineError](../java/lang/VirtualMachineError.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AnnotationFormatError](../java/lang/annotation/AnnotationFormatError.md) | Thrown when the annotation parser attempts to read an annotation from a class file and determines that the annotation is malformed. | | [AssertionError](../java/lang/AssertionError.md) | Thrown to indicate that an assertion has failed. | | [AssertionFailedError](../android/test/AssertionFailedError.md) | Thrown when an assertion failed. | | [CoderMalfunctionError](../java/nio/charset/CoderMalfunctionError.md) | Error thrown when the [decodeLoop](../java/nio/charset/CharsetDecoder.md))method of a [CharsetDecoder](../java/nio/charset/CharsetDecoder.md), or the [encodeLoop](../java/nio/charset/CharsetEncoder.md))method of a [CharsetEncoder](../java/nio/charset/CharsetEncoder.md), throws an unexpected exception. | | [FactoryConfigurationError](../javax/xml/parsers/FactoryConfigurationError.md) | Thrown when a problem with configuration with the Parser Factories exists. | | [IOError](../java/io/IOError.md) | Thrown when a serious I/O error has occurred. | | [LinkageError](../java/lang/LinkageError.md) | Subclasses of`LinkageError`indicate that a class has some dependency on another class; however, the latter class has incompatibly changed after the compilation of the former class. | | [ServiceConfigurationError](../java/util/ServiceConfigurationError.md) | Error thrown when something goes wrong while locating, loading, or instantiating a service provider. | | [ThreadDeath](../java/lang/ThreadDeath.md) | An instance of`ThreadDeath`is thrown in the victim thread when the (deprecated) [Thread.stop()](../java/lang/Thread.md))method is invoked. | | [TransformerFactoryConfigurationError](../javax/xml/transform/TransformerFactoryConfigurationError.md) | Thrown when a problem with configuration with the Transformer Factories exists. | | [VirtualMachineError](../java/lang/VirtualMachineError.md) | Thrown to indicate that the Java Virtual Machine is broken or has run out of resources necessary for it to continue operating. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbstractMethodError](../java/lang/AbstractMethodError.md), [BootstrapMethodError](../java/lang/BootstrapMethodError.md), [ClassCircularityError](../java/lang/ClassCircularityError.md), [ClassFormatError](../java/lang/ClassFormatError.md), [ComparisonFailure](../android/test/ComparisonFailure.md), [ExceptionInInitializerError](../java/lang/ExceptionInInitializerError.md), [GenericSignatureFormatError](../java/lang/reflect/GenericSignatureFormatError.md), [IllegalAccessError](../java/lang/IllegalAccessError.md), [IncompatibleClassChangeError](../java/lang/IncompatibleClassChangeError.md), [InstantiationError](../java/lang/InstantiationError.md), [InternalError](../java/lang/InternalError.md), [NoClassDefFoundError](../java/lang/NoClassDefFoundError.md), and 9 others. |-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractMethodError](../java/lang/AbstractMethodError.md) | Thrown when an application tries to call an abstract method. | | [BootstrapMethodError](../java/lang/BootstrapMethodError.md) | Thrown to indicate that an`invokedynamic`instruction or a dynamic constant failed to resolve its bootstrap method and arguments, or for`invokedynamic`instruction the bootstrap method has failed to provide a [call site](../java/lang/invoke/CallSite.md) with a [target](../java/lang/invoke/CallSite.md))of the correct [method type](../java/lang/invoke/MethodHandle.md)), or for a dynamic constant the bootstrap method has failed to provide a constant value of the required type. | | [ClassCircularityError](../java/lang/ClassCircularityError.md) | Thrown when the Java Virtual Machine detects a circularity in the superclass hierarchy of a class being loaded. | | [ClassFormatError](../java/lang/ClassFormatError.md) | Thrown when the Java Virtual Machine attempts to read a class file and determines that the file is malformed or otherwise cannot be interpreted as a class file. | | [ComparisonFailure](../android/test/ComparisonFailure.md) | Thrown when an assert equals for Strings failed. | | [ExceptionInInitializerError](../java/lang/ExceptionInInitializerError.md) | Signals that an unexpected exception has occurred in a static initializer. | | [GenericSignatureFormatError](../java/lang/reflect/GenericSignatureFormatError.md) | Thrown when a syntactically malformed signature attribute is encountered by a reflective method that needs to interpret the generic signature information for a type, method or constructor. | | [IllegalAccessError](../java/lang/IllegalAccessError.md) | Thrown if an application attempts to access or modify a field, or to call a method that it does not have access to. | | [IncompatibleClassChangeError](../java/lang/IncompatibleClassChangeError.md) | Thrown when an incompatible class change has occurred to some class definition. | | [InstantiationError](../java/lang/InstantiationError.md) | Thrown when an application tries to use the Java`new`construct to instantiate an abstract class or an interface. | | [InternalError](../java/lang/InternalError.md) | Thrown to indicate some unexpected internal error has occurred in the Java Virtual Machine. | | [NoClassDefFoundError](../java/lang/NoClassDefFoundError.md) | Thrown if the Java Virtual Machine or a`ClassLoader`instance tries to load in the definition of a class (as part of a normal method call or as part of creating a new instance using the`new`expression) and no definition of the class could be found. | | [NoSuchFieldError](../java/lang/NoSuchFieldError.md) | Thrown if an application tries to access or modify a specified field of an object, and that object no longer has that field. | | [NoSuchMethodError](../java/lang/NoSuchMethodError.md) | Thrown if an application tries to call a specified method of a class (either static or instance), and that class no longer has a definition of that method. | | [OutOfMemoryError](../java/lang/OutOfMemoryError.md) | Thrown when the Java Virtual Machine cannot allocate an object because it is out of memory, and no more memory could be made available by the garbage collector. | | [StackOverflowError](../java/lang/StackOverflowError.md) | Thrown when a stack overflow occurs because an application recurses too deeply. | | [UnknownError](../java/lang/UnknownError.md) | Thrown when an unknown but serious exception has occurred in the Java Virtual Machine. | | [UnsatisfiedLinkError](../java/lang/UnsatisfiedLinkError.md) | Thrown if the Java Virtual Machine cannot find an appropriate native-language definition of a method declared`native`. | | [UnsupportedClassVersionError](../java/lang/UnsupportedClassVersionError.md) | Thrown when the Java Virtual Machine attempts to read a class file and determines that the major and minor version numbers in the file are not supported. | | [VerifyError](../java/lang/VerifyError.md) | Thrown when the "verifier" detects that a class file, though well formed, contains some sort of internal inconsistency or security problem. | | [ZipError](../java/util/zip/ZipError.md) | Signals that an unrecoverable error has occurred. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An`Error`is a subclass of`Throwable`that indicates serious problems that a reasonable application should not try to catch. Most such errors are abnormal conditions. The`ThreadDeath`error, though a "normal" condition, is also a subclass of`Error`because most applications should not try to catch it.

A method is not required to declare in its`throws`clause any subclasses of`Error`that might be thrown during the execution of the method but not caught, since these errors are abnormal conditions that should never occur. That is,`Error`and its subclasses are regarded as unchecked exceptions for the purposes of compile-time checking of exceptions.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Error](../java/lang/Error.md))`()` Constructs a new error with`null`as its detail message. |
| [Error](../java/lang/Error.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new error with the specified detail message. |
| [Error](../java/lang/Error.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new error with the specified detail message and cause. |
| [Error](../java/lang/Error.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new error with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Error](../java/lang/Error.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`, `enableSuppression:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `writableStackTrace:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructs a new error with the specified detail message, cause, suppression enabled or disabled, and writable stack trace enabled or disabled. |

## Public constructors

### Error

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Error()
```

Constructs a new error with`null`as its detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](../java/lang/Throwable.md)). 

### Error

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Error(message: String!)
```

Constructs a new error with the specified detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](../java/lang/Throwable.md)).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. The detail message is saved for later retrieval by the [getMessage()](../java/lang/Throwable.md))method. |

### Error

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Error(
    message: String!, 
    cause: Throwable!)
```

Constructs a new error with the specified detail message and cause.

Note that the detail message associated with`cause`is*not*automatically incorporated in this error's detail message.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](../java/lang/Throwable.md))method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java/lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### Error

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Error(cause: Throwable!)
```

Constructs a new error with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). This constructor is useful for errors that are little more than wrappers for other throwables.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java/lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

## Protected constructors

### Error

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Error(
    message: String!, 
    cause: Throwable!, 
    enableSuppression: Boolean, 
    writableStackTrace: Boolean)
```

Constructs a new error with the specified detail message, cause, suppression enabled or disabled, and writable stack trace enabled or disabled.

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause. (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
| `enableSuppression` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether or not suppression is enabled or disabled |
| --- | --- |
| `writableStackTrace` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether or not the stack trace should be writable |
