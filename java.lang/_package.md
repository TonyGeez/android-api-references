# java.lang

## Interfaces

| [Appendable](../java/lang/Appendable.md) | An object to which `char` sequences and values can be appended. |
| --- | --- |
| [AutoCloseable](../java/lang/AutoCloseable.md) | An object that may hold resources (such as file or socket handles) until it is closed. |
| [CharSequence](../java/lang/CharSequence.md) | A `CharSequence` is a readable sequence of `char` values. |
| [Cloneable](../java/lang/Cloneable.md) | A class implements the `Cloneable` interface to indicate to the `https://developer.android.com/reference/kotlin/java/lang/Object#clone()` method that it is legal for that method to make a field-for-field copy of instances of that class. |
| --- | --- |
| [Comparable](../java/lang/Comparable.md) | This interface imposes a total ordering on the objects of each class that implements it. |
| [Iterable](../java/lang/Iterable.md) | Implementing this interface allows an object to be the target of the enhanced `for` statement (sometimes called the "for-each loop" statement). |
| [Readable](../java/lang/Readable.md) | A `Readable` is a source of characters. |
| --- | --- |
| [Runnable](../java/lang/Runnable.md) | The `Runnable` interface should be implemented by any class whose instances are intended to be executed by a thread. |
| [StackFrame](../java/lang/StackWalker.StackFrame.md) | A `StackFrame` object represents a method invocation returned by `https://developer.android.com/reference/kotlin/java/lang/StackWalker`. |
| [UncaughtExceptionHandler](../java/lang/Thread.UncaughtExceptionHandler.md) | Interface for handlers invoked when a `Thread` abruptly terminates due to an uncaught exception. |
| --- | --- |

## Classes

| [Boolean](../java/lang/Boolean.md) | The Boolean class wraps a value of the primitive type `boolean` in an object. |
| --- | --- |
| [Byte](../java/lang/Byte.md) | The `Byte` class wraps a value of primitive type `byte` in an object. |
| [Character](../java/lang/Character.md) | The `Character` class is the java. |
| [Class](../java/lang/Class.md) | Instances of the class represent classes and interfaces in a running Java application. |
| --- | --- |
| [ClassLoader](../java/lang/ClassLoader.md) | A class loader is an object that is responsible for loading classes. |
| [ClassValue](../java/lang/ClassValue.md) | Lazily associate a computed value with any `Class` object. |
| [Compiler](../java/lang/Compiler.md) | Does nothing on Android. |
| --- | --- |
| [Double](../java/lang/Double.md) | The `Double` class wraps a value of the primitive type `double` in an object. |
| [Enum](../java/lang/Enum.md) | This is the common base class of all Java language enumeration classes. |
| [Float](../java/lang/Float.md) | The `Float` class wraps a value of primitive type in an object. |
| --- | --- |
| [InheritableThreadLocal](../java/lang/InheritableThreadLocal.md) | This class extends `ThreadLocal` to provide inheritance of values from parent thread to child thread: when a child thread is created, the child receives initial values for all inheritable thread-local variables for which the parent has values. |
| [Integer](../java/lang/Integer.md) | The `Integer` class wraps a value of the primitive type `int` in an object. |
| [Long](../java/lang/Long.md) | The `Long` class wraps a value of the primitive type `long` in an object. |
| --- | --- |
| [Math](../java/lang/Math.md) | The class `Math` contains methods for performing basic numeric operations such as the elementary exponential, logarithm, square root, and trigonometric functions. |
| [Number](../java/lang/Number.md) | The abstract class `Number` is the superclass of platform classes representing numeric values that are convertible to the primitive types `byte`, `double`, `float`, `int`, `long`, and `short`. |
| [Object](../java/lang/Object.md) | Class `Object` is the root of the class hierarchy. |
| --- | --- |
| [Package](../java/lang/Package.md) | `Package` objects contain version information about the implementation and specification of a Java package. |
| [Process](../java/lang/Process.md) | The `https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start()` and `https://developer.android.com/reference/kotlin/java/lang/Runtime#exec(kotlin.Array,%20kotlin.Array,%20java.io.File)` methods create a native process and return an instance of a subclass of `Process` that can be used to control the process and obtain information about it. |
| [ProcessBuilder](../java/lang/ProcessBuilder.md) | This class is used to create operating system processes. |
| --- | --- |
| [Record](../java/lang/Record.md) | This is the common base class of all Java language record classes. |
| [Runtime](../java/lang/Runtime.md) | Every Java application has a single instance of class `Runtime` that allows the application to interface with the environment in which the application is running. |
| [RuntimePermission](../java/lang/RuntimePermission.md) | Legacy security code; do not use. |
| --- | --- |
| [SecurityManager](../java/lang/SecurityManager.md) | Legacy security code; do not use. |
| [Short](../java/lang/Short.md) | The `Short` class wraps a value of primitive type `short` in an object. |
| [StackTraceElement](../java/lang/StackTraceElement.md) | An element in a stack trace, as returned by `https://developer.android.com/reference/kotlin/java/lang/Throwable#getStackTrace()`. |
| --- | --- |
| [StackWalker](../java/lang/StackWalker.md) | A stack walker. |
| [StrictMath](../java/lang/StrictMath.md) | The class contains methods for performing basic numeric operations such as the elementary exponential, logarithm, square root, and trigonometric functions. |
| [String](../java/lang/String.md) | The `String` class represents character strings. |
| --- | --- |
| [StringBuffer](../java/lang/StringBuffer.md) | A thread-safe, mutable sequence of characters. |
| [StringBuilder](../java/lang/StringBuilder.md) | A mutable sequence of characters. |
| [System](../java/lang/System.md) | The `System` class contains several useful class fields and methods. |
| --- | --- |
| [Thread](../java/lang/Thread.md) | A *thread* is a thread of execution in a program. |
| [ThreadGroup](../java/lang/ThreadGroup.md) | A thread group represents a set of threads. |
| [ThreadLocal](../java/lang/ThreadLocal.md) | This class provides thread-local variables. |
| --- | --- |
| [Throwable](../java/lang/Throwable.md) | The `Throwable` class is the superclass of all errors and exceptions in the Java language. |
| [Void](../java/lang/Void.md) | The `Void` class is an uninstantiable placeholder class to hold a reference to the `Class` object representing the Java keyword void. |

## Exceptions

| [AbstractMethodError](../java/lang/AbstractMethodError.md) | Thrown when an application tries to call an abstract method. |
| --- | --- |
| [ArithmeticException](../java/lang/ArithmeticException.md) | Thrown when an exceptional arithmetic condition has occurred. |
| [ArrayIndexOutOfBoundsException](../java/lang/ArrayIndexOutOfBoundsException.md) | Thrown to indicate that an array has been accessed with an illegal index. |
| [ArrayStoreException](../java/lang/ArrayStoreException.md) | Thrown to indicate that an attempt has been made to store the wrong type of object into an array of objects. |
| --- | --- |
| [AssertionError](../java/lang/AssertionError.md) | Thrown to indicate that an assertion has failed. |
| [BootstrapMethodError](../java/lang/BootstrapMethodError.md) | Thrown to indicate that an `invokedynamic` instruction or a dynamic constant failed to resolve its bootstrap method and arguments, or for `invokedynamic` instruction the bootstrap method has failed to provide a [call site](../java/lang/invoke/CallSite.md) with a [target](../java/lang/invoke/CallSite.md)) of the correct [method type](../java/lang/invoke/MethodHandle.md)), or for a dynamic constant the bootstrap method has failed to provide a constant value of the required type. |
| [ClassCastException](../java/lang/ClassCastException.md) | Thrown to indicate that the code has attempted to cast an object to a subclass of which it is not an instance. |
| --- | --- |
| [ClassCircularityError](../java/lang/ClassCircularityError.md) | Thrown when the Java Virtual Machine detects a circularity in the superclass hierarchy of a class being loaded. |
| [ClassFormatError](../java/lang/ClassFormatError.md) | Thrown when the Java Virtual Machine attempts to read a class file and determines that the file is malformed or otherwise cannot be interpreted as a class file. |
| [ClassNotFoundException](../java/lang/ClassNotFoundException.md) | Thrown when an application tries to load in a class through its string name using: - The `forName` method in class `Class`. - The `findSystemClass` method in class `ClassLoader` . - The `loadClass` method in class `ClassLoader`. <br /> |
| --- | --- |
| [CloneNotSupportedException](../java/lang/CloneNotSupportedException.md) | Thrown to indicate that the `clone` method in class `Object` has been called to clone an object, but that the object's class does not implement the `Cloneable` interface. |
| [EnumConstantNotPresentException](../java/lang/EnumConstantNotPresentException.md) | Thrown when an application tries to access an enum constant by name and the enum type contains no constant with the specified name. |
| [Error](../java/lang/Error.md) | An `Error` is a subclass of `Throwable` that indicates serious problems that a reasonable application should not try to catch. |
| --- | --- |
| [Exception](../java/lang/Exception.md) | The class `Exception` and its subclasses are a form of `Throwable` that indicates conditions that a reasonable application might want to catch. |
| [ExceptionInInitializerError](../java/lang/ExceptionInInitializerError.md) | Signals that an unexpected exception has occurred in a static initializer. |
| [IllegalAccessError](../java/lang/IllegalAccessError.md) | Thrown if an application attempts to access or modify a field, or to call a method that it does not have access to. |
| --- | --- |
| [IllegalAccessException](../java/lang/IllegalAccessException.md) | An IllegalAccessException is thrown when an application tries to reflectively create an instance (other than an array), set or get a field, or invoke a method, but the currently executing method does not have access to the definition of the specified class, field, method or constructor. |
| [IllegalArgumentException](../java/lang/IllegalArgumentException.md) | Thrown to indicate that a method has been passed an illegal or inappropriate argument. |
| [IllegalCallerException](../java/lang/IllegalCallerException.md) | Thrown to indicate that a method has been called by an inappropriate caller. |
| --- | --- |
| [IllegalMonitorStateException](../java/lang/IllegalMonitorStateException.md) | Thrown to indicate that a thread has attempted to wait on an object's monitor or to notify other threads waiting on an object's monitor without owning the specified monitor. |
| [IllegalStateException](../java/lang/IllegalStateException.md) | Signals that a method has been invoked at an illegal or inappropriate time. |
| [IllegalThreadStateException](../java/lang/IllegalThreadStateException.md) | Thrown to indicate that a thread is not in an appropriate state for the requested operation. |
| --- | --- |
| [IncompatibleClassChangeError](../java/lang/IncompatibleClassChangeError.md) | Thrown when an incompatible class change has occurred to some class definition. |
| [IndexOutOfBoundsException](../java/lang/IndexOutOfBoundsException.md) | Thrown to indicate that an index of some sort (such as to an array, to a string, or to a vector) is out of range. |
| [InstantiationError](../java/lang/InstantiationError.md) | Thrown when an application tries to use the Java `new` construct to instantiate an abstract class or an interface. |
| --- | --- |
| [InstantiationException](../java/lang/InstantiationException.md) | Thrown when an application tries to create an instance of a class using the `newInstance` method in class `Class`, but the specified class object cannot be instantiated. |
| [InternalError](../java/lang/InternalError.md) | Thrown to indicate some unexpected internal error has occurred in the Java Virtual Machine. |
| [InterruptedException](../java/lang/InterruptedException.md) | Thrown when a thread is waiting, sleeping, or otherwise occupied, and the thread is interrupted, either before or during the activity. |
| --- | --- |
| [LinkageError](../java/lang/LinkageError.md) | Subclasses of `LinkageError` indicate that a class has some dependency on another class; however, the latter class has incompatibly changed after the compilation of the former class. |
| [MatchException](../java/lang/MatchException.md) | Thrown to indicate an unexpected failure in pattern matching. |
| [NegativeArraySizeException](../java/lang/NegativeArraySizeException.md) | Thrown if an application tries to create an array with negative size. |
| --- | --- |
| [NoClassDefFoundError](../java/lang/NoClassDefFoundError.md) | Thrown if the Java Virtual Machine or a `ClassLoader` instance tries to load in the definition of a class (as part of a normal method call or as part of creating a new instance using the `new` expression) and no definition of the class could be found. |
| [NoSuchFieldError](../java/lang/NoSuchFieldError.md) | Thrown if an application tries to access or modify a specified field of an object, and that object no longer has that field. |
| [NoSuchFieldException](../java/lang/NoSuchFieldException.md) | Signals that the class doesn't have a field of a specified name. |
| --- | --- |
| [NoSuchMethodError](../java/lang/NoSuchMethodError.md) | Thrown if an application tries to call a specified method of a class (either static or instance), and that class no longer has a definition of that method. |
| [NoSuchMethodException](../java/lang/NoSuchMethodException.md) | Thrown when a particular method cannot be found. |
| [NullPointerException](../java/lang/NullPointerException.md) | Thrown when an application attempts to use `null` in a case where an object is required. |
| --- | --- |
| [NumberFormatException](../java/lang/NumberFormatException.md) | Thrown to indicate that the application has attempted to convert a string to one of the numeric types, but that the string does not have the appropriate format. |
| [OutOfMemoryError](../java/lang/OutOfMemoryError.md) | Thrown when the Java Virtual Machine cannot allocate an object because it is out of memory, and no more memory could be made available by the garbage collector. |
| [ReflectiveOperationException](../java/lang/ReflectiveOperationException.md) | Common superclass of exceptions thrown by reflective operations in core reflection. |
| --- | --- |
| [RuntimeException](../java/lang/RuntimeException.md) | `RuntimeException` is the superclass of those exceptions that can be thrown during the normal operation of the Java Virtual Machine. |
| [SecurityException](../java/lang/SecurityException.md) | Thrown by the security manager to indicate a security violation. |
| [StackOverflowError](../java/lang/StackOverflowError.md) | Thrown when a stack overflow occurs because an application recurses too deeply. |
| --- | --- |
| [StringIndexOutOfBoundsException](../java/lang/StringIndexOutOfBoundsException.md) | Thrown by `String` methods to indicate that an index is either negative or greater than the size of the string. |
| [ThreadDeath](../java/lang/ThreadDeath.md) | An instance of `ThreadDeath` is thrown in the victim thread when the (deprecated) `https://developer.android.com/reference/kotlin/java/lang/Thread#stop()` method is invoked. |
| [TypeNotPresentException](../java/lang/TypeNotPresentException.md) | Thrown when an application tries to access a type using a string representing the type's name, but no definition for the type with the specified name can be found. |
| --- | --- |
| [UnknownError](../java/lang/UnknownError.md) | Thrown when an unknown but serious exception has occurred in the Java Virtual Machine. |
| [UnsatisfiedLinkError](../java/lang/UnsatisfiedLinkError.md) | Thrown if the Java Virtual Machine cannot find an appropriate native-language definition of a method declared `native`. |
| [UnsupportedClassVersionError](../java/lang/UnsupportedClassVersionError.md) | Thrown when the Java Virtual Machine attempts to read a class file and determines that the major and minor version numbers in the file are not supported. |
| --- | --- |
| [UnsupportedOperationException](../java/lang/UnsupportedOperationException.md) | Thrown to indicate that the requested operation is not supported. |
| [VerifyError](../java/lang/VerifyError.md) | Thrown when the "verifier" detects that a class file, though well formed, contains some sort of internal inconsistency or security problem. |
| [VirtualMachineError](../java/lang/VirtualMachineError.md) | Thrown to indicate that the Java Virtual Machine is broken or has run out of resources necessary for it to continue operating. |
| --- | --- |
| [WrongThreadException](../java/lang/WrongThreadException.md) | Thrown to indicate that a method has been called on the wrong thread. |

## Annotations

| [Deprecated](../java/lang/Deprecated.md) | A program element annotated `@Deprecated` is one that programmers are discouraged from using. |
| --- | --- |
| [FunctionalInterface](../java/lang/FunctionalInterface.md) | An informative annotation type used to indicate that an interface type declaration is intended to be a *functional interface* as defined by the Java Language Specification. |
| [Override](../java/lang/Override.md) | Indicates that a method declaration is intended to override a method declaration in a supertype. |
| [SafeVarargs](../java/lang/SafeVarargs.md) | A programmer assertion that the body of the annotated method or constructor does not perform potentially unsafe operations on its varargs parameter. |
| --- | --- |
| [SuppressWarnings](../java/lang/SuppressWarnings.md) | Indicates that the named compiler warnings should be suppressed in the annotated element (and in all program elements contained in the annotated element). |
