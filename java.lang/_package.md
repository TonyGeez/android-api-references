# java.lang

## Interfaces

| [Appendable](https://developer.android.com/reference/kotlin/java/lang/Appendable) | An object to which `char` sequences and values can be appended. |
| [AutoCloseable](https://developer.android.com/reference/kotlin/java/lang/AutoCloseable) | An object that may hold resources (such as file or socket handles) until it is closed. |
| [CharSequence](https://developer.android.com/reference/kotlin/java/lang/CharSequence) | A `CharSequence` is a readable sequence of `char` values. |
| [Cloneable](https://developer.android.com/reference/kotlin/java/lang/Cloneable) | A class implements the `Cloneable` interface to indicate to the `https://developer.android.com/reference/kotlin/java/lang/Object#clone()` method that it is legal for that method to make a field-for-field copy of instances of that class. |
| [Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable) | This interface imposes a total ordering on the objects of each class that implements it. |
| [Iterable](https://developer.android.com/reference/kotlin/java/lang/Iterable) | Implementing this interface allows an object to be the target of the enhanced `for` statement (sometimes called the "for-each loop" statement). |
| [Readable](https://developer.android.com/reference/kotlin/java/lang/Readable) | A `Readable` is a source of characters. |
| [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable) | The `Runnable` interface should be implemented by any class whose instances are intended to be executed by a thread. |
| [StackFrame](https://developer.android.com/reference/kotlin/java/lang/StackWalker.StackFrame) | A `StackFrame` object represents a method invocation returned by `https://developer.android.com/reference/kotlin/java/lang/StackWalker`. |
| [UncaughtExceptionHandler](https://developer.android.com/reference/kotlin/java/lang/Thread.UncaughtExceptionHandler) | Interface for handlers invoked when a `Thread` abruptly terminates due to an uncaught exception. |

## Classes

| [Boolean](https://developer.android.com/reference/kotlin/java/lang/Boolean) | The Boolean class wraps a value of the primitive type `boolean` in an object. |
| [Byte](https://developer.android.com/reference/kotlin/java/lang/Byte) | The `Byte` class wraps a value of primitive type `byte` in an object. |
| [Character](https://developer.android.com/reference/kotlin/java/lang/Character) | The `Character` class is the java. |
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class) | Instances of the class represent classes and interfaces in a running Java application. |
| [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader) | A class loader is an object that is responsible for loading classes. |
| [ClassValue](https://developer.android.com/reference/kotlin/java/lang/ClassValue) | Lazily associate a computed value with any `Class` object. |
| [Compiler](https://developer.android.com/reference/kotlin/java/lang/Compiler) | Does nothing on Android. |
| [Double](https://developer.android.com/reference/kotlin/java/lang/Double) | The `Double` class wraps a value of the primitive type `double` in an object. |
| [Enum](https://developer.android.com/reference/kotlin/java/lang/Enum) | This is the common base class of all Java language enumeration classes. |
| [Float](https://developer.android.com/reference/kotlin/java/lang/Float) | The `Float` class wraps a value of primitive type in an object. |
| [InheritableThreadLocal](https://developer.android.com/reference/kotlin/java/lang/InheritableThreadLocal) | This class extends `ThreadLocal` to provide inheritance of values from parent thread to child thread: when a child thread is created, the child receives initial values for all inheritable thread-local variables for which the parent has values. |
| [Integer](https://developer.android.com/reference/kotlin/java/lang/Integer) | The `Integer` class wraps a value of the primitive type `int` in an object. |
| [Long](https://developer.android.com/reference/kotlin/java/lang/Long) | The `Long` class wraps a value of the primitive type `long` in an object. |
| [Math](https://developer.android.com/reference/kotlin/java/lang/Math) | The class `Math` contains methods for performing basic numeric operations such as the elementary exponential, logarithm, square root, and trigonometric functions. |
| [Number](https://developer.android.com/reference/kotlin/java/lang/Number) | The abstract class `Number` is the superclass of platform classes representing numeric values that are convertible to the primitive types `byte`, `double`, `float`, `int`, `long`, and `short`. |
| [Object](https://developer.android.com/reference/kotlin/java/lang/Object) | Class `Object` is the root of the class hierarchy. |
| [Package](https://developer.android.com/reference/kotlin/java/lang/Package) | `Package` objects contain version information about the implementation and specification of a Java package. |
| [Process](https://developer.android.com/reference/kotlin/java/lang/Process) | The `https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start()` and `https://developer.android.com/reference/kotlin/java/lang/Runtime#exec(kotlin.Array,%20kotlin.Array,%20java.io.File)` methods create a native process and return an instance of a subclass of `Process` that can be used to control the process and obtain information about it. |
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder) | This class is used to create operating system processes. |
| [Record](https://developer.android.com/reference/kotlin/java/lang/Record) | This is the common base class of all Java language record classes. |
| [Runtime](https://developer.android.com/reference/kotlin/java/lang/Runtime) | Every Java application has a single instance of class `Runtime` that allows the application to interface with the environment in which the application is running. |
| [RuntimePermission](https://developer.android.com/reference/kotlin/java/lang/RuntimePermission) | Legacy security code; do not use. |
| [SecurityManager](https://developer.android.com/reference/kotlin/java/lang/SecurityManager) | Legacy security code; do not use. |
| [Short](https://developer.android.com/reference/kotlin/java/lang/Short) | The `Short` class wraps a value of primitive type `short` in an object. |
| [StackTraceElement](https://developer.android.com/reference/kotlin/java/lang/StackTraceElement) | An element in a stack trace, as returned by `https://developer.android.com/reference/kotlin/java/lang/Throwable#getStackTrace()`. |
| [StackWalker](https://developer.android.com/reference/kotlin/java/lang/StackWalker) | A stack walker. |
| [StrictMath](https://developer.android.com/reference/kotlin/java/lang/StrictMath) | The class contains methods for performing basic numeric operations such as the elementary exponential, logarithm, square root, and trigonometric functions. |
| [String](https://developer.android.com/reference/kotlin/java/lang/String) | The `String` class represents character strings. |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer) | A thread-safe, mutable sequence of characters. |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder) | A mutable sequence of characters. |
| [System](https://developer.android.com/reference/kotlin/java/lang/System) | The `System` class contains several useful class fields and methods. |
| [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread) | A *thread* is a thread of execution in a program. |
| [ThreadGroup](https://developer.android.com/reference/kotlin/java/lang/ThreadGroup) | A thread group represents a set of threads. |
| [ThreadLocal](https://developer.android.com/reference/kotlin/java/lang/ThreadLocal) | This class provides thread-local variables. |
| [Throwable](https://developer.android.com/reference/kotlin/java/lang/Throwable) | The `Throwable` class is the superclass of all errors and exceptions in the Java language. |
| [Void](https://developer.android.com/reference/kotlin/java/lang/Void) | The `Void` class is an uninstantiable placeholder class to hold a reference to the `Class` object representing the Java keyword void. |

## Exceptions

| [AbstractMethodError](https://developer.android.com/reference/kotlin/java/lang/AbstractMethodError) | Thrown when an application tries to call an abstract method. |
| [ArithmeticException](https://developer.android.com/reference/kotlin/java/lang/ArithmeticException) | Thrown when an exceptional arithmetic condition has occurred. |
| [ArrayIndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException) | Thrown to indicate that an array has been accessed with an illegal index. |
| [ArrayStoreException](https://developer.android.com/reference/kotlin/java/lang/ArrayStoreException) | Thrown to indicate that an attempt has been made to store the wrong type of object into an array of objects. |
| [AssertionError](https://developer.android.com/reference/kotlin/java/lang/AssertionError) | Thrown to indicate that an assertion has failed. |
| [BootstrapMethodError](https://developer.android.com/reference/kotlin/java/lang/BootstrapMethodError) | Thrown to indicate that an `invokedynamic` instruction or a dynamic constant failed to resolve its bootstrap method and arguments, or for `invokedynamic` instruction the bootstrap method has failed to provide a [call site](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite) with a [target](https://developer.android.com/reference/kotlin/java/lang/invoke/CallSite#getTarget()) of the correct [method type](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandle#type()), or for a dynamic constant the bootstrap method has failed to provide a constant value of the required type. |
| [ClassCastException](https://developer.android.com/reference/kotlin/java/lang/ClassCastException) | Thrown to indicate that the code has attempted to cast an object to a subclass of which it is not an instance. |
| [ClassCircularityError](https://developer.android.com/reference/kotlin/java/lang/ClassCircularityError) | Thrown when the Java Virtual Machine detects a circularity in the superclass hierarchy of a class being loaded. |
| [ClassFormatError](https://developer.android.com/reference/kotlin/java/lang/ClassFormatError) | Thrown when the Java Virtual Machine attempts to read a class file and determines that the file is malformed or otherwise cannot be interpreted as a class file. |
| [ClassNotFoundException](https://developer.android.com/reference/kotlin/java/lang/ClassNotFoundException) | Thrown when an application tries to load in a class through its string name using: - The `forName` method in class `Class`. - The `findSystemClass` method in class `ClassLoader` . - The `loadClass` method in class `ClassLoader`. <br /> |
| [CloneNotSupportedException](https://developer.android.com/reference/kotlin/java/lang/CloneNotSupportedException) | Thrown to indicate that the `clone` method in class `Object` has been called to clone an object, but that the object's class does not implement the `Cloneable` interface. |
| [EnumConstantNotPresentException](https://developer.android.com/reference/kotlin/java/lang/EnumConstantNotPresentException) | Thrown when an application tries to access an enum constant by name and the enum type contains no constant with the specified name. |
| [Error](https://developer.android.com/reference/kotlin/java/lang/Error) | An `Error` is a subclass of `Throwable` that indicates serious problems that a reasonable application should not try to catch. |
| [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception) | The class `Exception` and its subclasses are a form of `Throwable` that indicates conditions that a reasonable application might want to catch. |
| [ExceptionInInitializerError](https://developer.android.com/reference/kotlin/java/lang/ExceptionInInitializerError) | Signals that an unexpected exception has occurred in a static initializer. |
| [IllegalAccessError](https://developer.android.com/reference/kotlin/java/lang/IllegalAccessError) | Thrown if an application attempts to access or modify a field, or to call a method that it does not have access to. |
| [IllegalAccessException](https://developer.android.com/reference/kotlin/java/lang/IllegalAccessException) | An IllegalAccessException is thrown when an application tries to reflectively create an instance (other than an array), set or get a field, or invoke a method, but the currently executing method does not have access to the definition of the specified class, field, method or constructor. |
| [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException) | Thrown to indicate that a method has been passed an illegal or inappropriate argument. |
| [IllegalCallerException](https://developer.android.com/reference/kotlin/java/lang/IllegalCallerException) | Thrown to indicate that a method has been called by an inappropriate caller. |
| [IllegalMonitorStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalMonitorStateException) | Thrown to indicate that a thread has attempted to wait on an object's monitor or to notify other threads waiting on an object's monitor without owning the specified monitor. |
| [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException) | Signals that a method has been invoked at an illegal or inappropriate time. |
| [IllegalThreadStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalThreadStateException) | Thrown to indicate that a thread is not in an appropriate state for the requested operation. |
| [IncompatibleClassChangeError](https://developer.android.com/reference/kotlin/java/lang/IncompatibleClassChangeError) | Thrown when an incompatible class change has occurred to some class definition. |
| [IndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/IndexOutOfBoundsException) | Thrown to indicate that an index of some sort (such as to an array, to a string, or to a vector) is out of range. |
| [InstantiationError](https://developer.android.com/reference/kotlin/java/lang/InstantiationError) | Thrown when an application tries to use the Java `new` construct to instantiate an abstract class or an interface. |
| [InstantiationException](https://developer.android.com/reference/kotlin/java/lang/InstantiationException) | Thrown when an application tries to create an instance of a class using the `newInstance` method in class `Class`, but the specified class object cannot be instantiated. |
| [InternalError](https://developer.android.com/reference/kotlin/java/lang/InternalError) | Thrown to indicate some unexpected internal error has occurred in the Java Virtual Machine. |
| [InterruptedException](https://developer.android.com/reference/kotlin/java/lang/InterruptedException) | Thrown when a thread is waiting, sleeping, or otherwise occupied, and the thread is interrupted, either before or during the activity. |
| [LinkageError](https://developer.android.com/reference/kotlin/java/lang/LinkageError) | Subclasses of `LinkageError` indicate that a class has some dependency on another class; however, the latter class has incompatibly changed after the compilation of the former class. |
| [MatchException](https://developer.android.com/reference/kotlin/java/lang/MatchException) | Thrown to indicate an unexpected failure in pattern matching. |
| [NegativeArraySizeException](https://developer.android.com/reference/kotlin/java/lang/NegativeArraySizeException) | Thrown if an application tries to create an array with negative size. |
| [NoClassDefFoundError](https://developer.android.com/reference/kotlin/java/lang/NoClassDefFoundError) | Thrown if the Java Virtual Machine or a `ClassLoader` instance tries to load in the definition of a class (as part of a normal method call or as part of creating a new instance using the `new` expression) and no definition of the class could be found. |
| [NoSuchFieldError](https://developer.android.com/reference/kotlin/java/lang/NoSuchFieldError) | Thrown if an application tries to access or modify a specified field of an object, and that object no longer has that field. |
| [NoSuchFieldException](https://developer.android.com/reference/kotlin/java/lang/NoSuchFieldException) | Signals that the class doesn't have a field of a specified name. |
| [NoSuchMethodError](https://developer.android.com/reference/kotlin/java/lang/NoSuchMethodError) | Thrown if an application tries to call a specified method of a class (either static or instance), and that class no longer has a definition of that method. |
| [NoSuchMethodException](https://developer.android.com/reference/kotlin/java/lang/NoSuchMethodException) | Thrown when a particular method cannot be found. |
| [NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException) | Thrown when an application attempts to use `null` in a case where an object is required. |
| [NumberFormatException](https://developer.android.com/reference/kotlin/java/lang/NumberFormatException) | Thrown to indicate that the application has attempted to convert a string to one of the numeric types, but that the string does not have the appropriate format. |
| [OutOfMemoryError](https://developer.android.com/reference/kotlin/java/lang/OutOfMemoryError) | Thrown when the Java Virtual Machine cannot allocate an object because it is out of memory, and no more memory could be made available by the garbage collector. |
| [ReflectiveOperationException](https://developer.android.com/reference/kotlin/java/lang/ReflectiveOperationException) | Common superclass of exceptions thrown by reflective operations in core reflection. |
| [RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException) | `RuntimeException` is the superclass of those exceptions that can be thrown during the normal operation of the Java Virtual Machine. |
| [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException) | Thrown by the security manager to indicate a security violation. |
| [StackOverflowError](https://developer.android.com/reference/kotlin/java/lang/StackOverflowError) | Thrown when a stack overflow occurs because an application recurses too deeply. |
| [StringIndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/StringIndexOutOfBoundsException) | Thrown by `String` methods to indicate that an index is either negative or greater than the size of the string. |
| [ThreadDeath](https://developer.android.com/reference/kotlin/java/lang/ThreadDeath) | An instance of `ThreadDeath` is thrown in the victim thread when the (deprecated) `https://developer.android.com/reference/kotlin/java/lang/Thread#stop()` method is invoked. |
| [TypeNotPresentException](https://developer.android.com/reference/kotlin/java/lang/TypeNotPresentException) | Thrown when an application tries to access a type using a string representing the type's name, but no definition for the type with the specified name can be found. |
| [UnknownError](https://developer.android.com/reference/kotlin/java/lang/UnknownError) | Thrown when an unknown but serious exception has occurred in the Java Virtual Machine. |
| [UnsatisfiedLinkError](https://developer.android.com/reference/kotlin/java/lang/UnsatisfiedLinkError) | Thrown if the Java Virtual Machine cannot find an appropriate native-language definition of a method declared `native`. |
| [UnsupportedClassVersionError](https://developer.android.com/reference/kotlin/java/lang/UnsupportedClassVersionError) | Thrown when the Java Virtual Machine attempts to read a class file and determines that the major and minor version numbers in the file are not supported. |
| [UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException) | Thrown to indicate that the requested operation is not supported. |
| [VerifyError](https://developer.android.com/reference/kotlin/java/lang/VerifyError) | Thrown when the "verifier" detects that a class file, though well formed, contains some sort of internal inconsistency or security problem. |
| [VirtualMachineError](https://developer.android.com/reference/kotlin/java/lang/VirtualMachineError) | Thrown to indicate that the Java Virtual Machine is broken or has run out of resources necessary for it to continue operating. |
| [WrongThreadException](https://developer.android.com/reference/kotlin/java/lang/WrongThreadException) | Thrown to indicate that a method has been called on the wrong thread. |

## Annotations

| [Deprecated](https://developer.android.com/reference/kotlin/java/lang/Deprecated) | A program element annotated `@Deprecated` is one that programmers are discouraged from using. |
| [FunctionalInterface](https://developer.android.com/reference/kotlin/java/lang/FunctionalInterface) | An informative annotation type used to indicate that an interface type declaration is intended to be a *functional interface* as defined by the Java Language Specification. |
| [Override](https://developer.android.com/reference/kotlin/java/lang/Override) | Indicates that a method declaration is intended to override a method declaration in a supertype. |
| [SafeVarargs](https://developer.android.com/reference/kotlin/java/lang/SafeVarargs) | A programmer assertion that the body of the annotated method or constructor does not perform potentially unsafe operations on its varargs parameter. |
| [SuppressWarnings](https://developer.android.com/reference/kotlin/java/lang/SuppressWarnings) | Indicates that the named compiler warnings should be suppressed in the annotated element (and in all program elements contained in the annotated element). |
