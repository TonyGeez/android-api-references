# Error

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Error

```
open class Error : Throwable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error#) |

| Known Direct Subclasses [AnnotationFormatError](https://developer.android.com/reference/kotlin/java/lang/annotation/AnnotationFormatError), [AssertionError](https://developer.android.com/reference/kotlin/java/lang/AssertionError), [AssertionFailedError](https://developer.android.com/reference/kotlin/android/test/AssertionFailedError.html#), [CoderMalfunctionError](https://developer.android.com/reference/kotlin/java/nio/charset/CoderMalfunctionError.html#), [FactoryConfigurationError](https://developer.android.com/reference/kotlin/javax/xml/parsers/FactoryConfigurationError.html#), [IOError](https://developer.android.com/reference/kotlin/java/io/IOError.html#), [LinkageError](https://developer.android.com/reference/kotlin/java/lang/LinkageError), [ServiceConfigurationError](https://developer.android.com/reference/kotlin/java/util/ServiceConfigurationError.html#), [ThreadDeath](https://developer.android.com/reference/kotlin/java/lang/ThreadDeath), [TransformerFactoryConfigurationError](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactoryConfigurationError.html#), [VirtualMachineError](https://developer.android.com/reference/kotlin/java/lang/VirtualMachineError) |-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AnnotationFormatError](https://developer.android.com/reference/kotlin/java/lang/annotation/AnnotationFormatError) | Thrown when the annotation parser attempts to read an annotation from a class file and determines that the annotation is malformed. | | [AssertionError](https://developer.android.com/reference/kotlin/java/lang/AssertionError) | Thrown to indicate that an assertion has failed. | | [AssertionFailedError](https://developer.android.com/reference/kotlin/android/test/AssertionFailedError.html#) | Thrown when an assertion failed. | | [CoderMalfunctionError](https://developer.android.com/reference/kotlin/java/nio/charset/CoderMalfunctionError.html#) | Error thrown when the [decodeLoop](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetDecoder.html#decodeLoop(java.nio.ByteBuffer,%20java.nio.CharBuffer))method of a [CharsetDecoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetDecoder.html#), or the [encodeLoop](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder.html#encodeLoop(java.nio.CharBuffer,%20java.nio.ByteBuffer))method of a [CharsetEncoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder.html#), throws an unexpected exception. | | [FactoryConfigurationError](https://developer.android.com/reference/kotlin/javax/xml/parsers/FactoryConfigurationError.html#) | Thrown when a problem with configuration with the Parser Factories exists. | | [IOError](https://developer.android.com/reference/kotlin/java/io/IOError.html#) | Thrown when a serious I/O error has occurred. | | [LinkageError](https://developer.android.com/reference/kotlin/java/lang/LinkageError) | Subclasses of`LinkageError`indicate that a class has some dependency on another class; however, the latter class has incompatibly changed after the compilation of the former class. | | [ServiceConfigurationError](https://developer.android.com/reference/kotlin/java/util/ServiceConfigurationError.html#) | Error thrown when something goes wrong while locating, loading, or instantiating a service provider. | | [ThreadDeath](https://developer.android.com/reference/kotlin/java/lang/ThreadDeath) | An instance of`ThreadDeath`is thrown in the victim thread when the (deprecated) [Thread.stop()](https://developer.android.com/reference/kotlin/java/lang/Thread#stop())method is invoked. | | [TransformerFactoryConfigurationError](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactoryConfigurationError.html#) | Thrown when a problem with configuration with the Transformer Factories exists. | | [VirtualMachineError](https://developer.android.com/reference/kotlin/java/lang/VirtualMachineError) | Thrown to indicate that the Java Virtual Machine is broken or has run out of resources necessary for it to continue operating. | |

| Known Indirect Subclasses [AbstractMethodError](https://developer.android.com/reference/kotlin/java/lang/AbstractMethodError), [BootstrapMethodError](https://developer.android.com/reference/kotlin/java/lang/BootstrapMethodError), [ClassCircularityError](https://developer.android.com/reference/kotlin/java/lang/ClassCircularityError), [ClassFormatError](https://developer.android.com/reference/kotlin/java/lang/ClassFormatError), [ComparisonFailure](https://developer.android.com/reference/kotlin/android/test/ComparisonFailure.html#), [ExceptionInInitializerError](https://developer.android.com/reference/kotlin/java/lang/ExceptionInInitializerError), [GenericSignatureFormatError](https://developer.android.com/reference/kotlin/java/lang/reflect/GenericSignatureFormatError), [IllegalAccessError](https://developer.android.com/reference/kotlin/java/lang/IllegalAccessError), [IncompatibleClassChangeError](https://developer.android.com/reference/kotlin/java/lang/IncompatibleClassChangeError), [InstantiationError](https://developer.android.com/reference/kotlin/java/lang/InstantiationError), [InternalError](https://developer.android.com/reference/kotlin/java/lang/InternalError), [NoClassDefFoundError](https://developer.android.com/reference/kotlin/java/lang/NoClassDefFoundError), and 9 others. |-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractMethodError](https://developer.android.com/reference/kotlin/java/lang/AbstractMethodError) | Thrown when an application tries to call an abstract method. | | [BootstrapMethodError](https://developer.android.com/reference/kotlin/java/lang/BootstrapMethodError) | Thrown to indicate that an`invokedynamic`instruction or a dynamic constant failed to resolve its bootstrap method and arguments, or for`invokedynamic`instruction the bootstrap method has failed to provide a [call site](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite) with a [target](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite#getTarget())of the correct [method type](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle#type()), or for a dynamic constant the bootstrap method has failed to provide a constant value of the required type. | | [ClassCircularityError](https://developer.android.com/reference/kotlin/java/lang/ClassCircularityError) | Thrown when the Java Virtual Machine detects a circularity in the superclass hierarchy of a class being loaded. | | [ClassFormatError](https://developer.android.com/reference/kotlin/java/lang/ClassFormatError) | Thrown when the Java Virtual Machine attempts to read a class file and determines that the file is malformed or otherwise cannot be interpreted as a class file. | | [ComparisonFailure](https://developer.android.com/reference/kotlin/android/test/ComparisonFailure.html#) | Thrown when an assert equals for Strings failed. | | [ExceptionInInitializerError](https://developer.android.com/reference/kotlin/java/lang/ExceptionInInitializerError) | Signals that an unexpected exception has occurred in a static initializer. | | [GenericSignatureFormatError](https://developer.android.com/reference/kotlin/java/lang/reflect/GenericSignatureFormatError) | Thrown when a syntactically malformed signature attribute is encountered by a reflective method that needs to interpret the generic signature information for a type, method or constructor. | | [IllegalAccessError](https://developer.android.com/reference/kotlin/java/lang/IllegalAccessError) | Thrown if an application attempts to access or modify a field, or to call a method that it does not have access to. | | [IncompatibleClassChangeError](https://developer.android.com/reference/kotlin/java/lang/IncompatibleClassChangeError) | Thrown when an incompatible class change has occurred to some class definition. | | [InstantiationError](https://developer.android.com/reference/kotlin/java/lang/InstantiationError) | Thrown when an application tries to use the Java`new`construct to instantiate an abstract class or an interface. | | [InternalError](https://developer.android.com/reference/kotlin/java/lang/InternalError) | Thrown to indicate some unexpected internal error has occurred in the Java Virtual Machine. | | [NoClassDefFoundError](https://developer.android.com/reference/kotlin/java/lang/NoClassDefFoundError) | Thrown if the Java Virtual Machine or a`ClassLoader`instance tries to load in the definition of a class (as part of a normal method call or as part of creating a new instance using the`new`expression) and no definition of the class could be found. | | [NoSuchFieldError](https://developer.android.com/reference/kotlin/java/lang/NoSuchFieldError) | Thrown if an application tries to access or modify a specified field of an object, and that object no longer has that field. | | [NoSuchMethodError](https://developer.android.com/reference/kotlin/java/lang/NoSuchMethodError) | Thrown if an application tries to call a specified method of a class (either static or instance), and that class no longer has a definition of that method. | | [OutOfMemoryError](https://developer.android.com/reference/kotlin/java/lang/OutOfMemoryError) | Thrown when the Java Virtual Machine cannot allocate an object because it is out of memory, and no more memory could be made available by the garbage collector. | | [StackOverflowError](https://developer.android.com/reference/kotlin/java/lang/StackOverflowError) | Thrown when a stack overflow occurs because an application recurses too deeply. | | [UnknownError](https://developer.android.com/reference/kotlin/java/lang/UnknownError) | Thrown when an unknown but serious exception has occurred in the Java Virtual Machine. | | [UnsatisfiedLinkError](https://developer.android.com/reference/kotlin/java/lang/UnsatisfiedLinkError) | Thrown if the Java Virtual Machine cannot find an appropriate native-language definition of a method declared`native`. | | [UnsupportedClassVersionError](https://developer.android.com/reference/kotlin/java/lang/UnsupportedClassVersionError) | Thrown when the Java Virtual Machine attempts to read a class file and determines that the major and minor version numbers in the file are not supported. | | [VerifyError](https://developer.android.com/reference/kotlin/java/lang/VerifyError) | Thrown when the "verifier" detects that a class file, though well formed, contains some sort of internal inconsistency or security problem. | | [ZipError](https://developer.android.com/reference/kotlin/java/util/zip/ZipError.html#) | Signals that an unrecoverable error has occurred. | |

An`Error`is a subclass of`Throwable`that indicates serious problems that a reasonable application should not try to catch. Most such errors are abnormal conditions. The`ThreadDeath`error, though a "normal" condition, is also a subclass of`Error`because most applications should not try to catch it.

A method is not required to declare in its`throws`clause any subclasses of`Error`that might be thrown during the execution of the method but not caught, since these errors are abnormal conditions that should never occur. That is,`Error`and its subclasses are regarded as unchecked exceptions for the purposes of compile-time checking of exceptions.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Error](https://developer.android.com/reference/kotlin/java/lang/Error#Error())`()` Constructs a new error with`null`as its detail message. |
| [Error](https://developer.android.com/reference/kotlin/java/lang/Error#Error(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new error with the specified detail message. |
| [Error](https://developer.android.com/reference/kotlin/java/lang/Error#Error(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new error with the specified detail message and cause. |
| [Error](https://developer.android.com/reference/kotlin/java/lang/Error#Error(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new error with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Error](https://developer.android.com/reference/kotlin/java/lang/Error#Error(kotlin.String,%20kotlin.Throwable,%20kotlin.Boolean,%20kotlin.Boolean))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`, `enableSuppression:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `writableStackTrace:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructs a new error with the specified detail message, cause, suppression enabled or disabled, and writable stack trace enabled or disabled. |

## Public constructors

### Error

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Error()
```

Constructs a new error with`null`as its detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](https://developer.android.com/reference/kotlin/java/lang/Throwable#initCause(kotlin.Throwable)). 

### Error

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Error(message: String!)
```

Constructs a new error with the specified detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](https://developer.android.com/reference/kotlin/java/lang/Throwable#initCause(kotlin.Throwable)).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. The detail message is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getMessage())method. |

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
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getMessage())method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### Error

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Error(cause: Throwable!)
```

Constructs a new error with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). This constructor is useful for errors that are little more than wrappers for other throwables.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

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
| `writableStackTrace` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether or not the stack trace should be writable |
