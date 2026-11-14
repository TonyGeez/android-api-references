# Throwable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Throwable

```
open class Throwable : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.lang.Throwable](https://developer.android.com/reference/kotlin/java/lang/Throwable#) |

The`Throwable`class is the superclass of all errors and exceptions in the Java language. Only objects that are instances of this class (or one of its subclasses) are thrown by the Java Virtual Machine or can be thrown by the Java`throw`statement. Similarly, only this class or one of its subclasses can be the argument type in a`catch`clause. For the purposes of compile-time checking of exceptions,`Throwable`and any subclass of`Throwable`that is not also a subclass of either [RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException) or [Error](https://developer.android.com/reference/kotlin/java/lang/Error) are regarded as checked exceptions.

Instances of two subclasses, [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error) and [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception), are conventionally used to indicate that exceptional situations have occurred. Typically, these instances are freshly created in the context of the exceptional situation so as to include relevant information (such as stack trace data).

A throwable contains a snapshot of the execution stack of its thread at the time it was created. It can also contain a message string that gives more information about the error. Over time, a throwable can [suppress](https://developer.android.com/reference/kotlin/java/lang/Throwable#addSuppressed(kotlin.Throwable))other throwables from being propagated. Finally, the throwable can also contain a*cause* : another throwable that caused this throwable to be constructed. The recording of this causal information is referred to as the*chained exception*facility, as the cause can, itself, have a cause, and so on, leading to a "chain" of exceptions, each caused by another.

One reason that a throwable may have a cause is that the class that throws it is built atop a lower layered abstraction, and an operation on the upper layer fails due to a failure in the lower layer. It would be bad design to let the throwable thrown by the lower layer propagate outward, as it is generally unrelated to the abstraction provided by the upper layer. Further, doing so would tie the API of the upper layer to the details of its implementation, assuming the lower layer's exception was a checked exception. Throwing a "wrapped exception" (i.e., an exception containing a cause) allows the upper layer to communicate the details of the failure to its caller without incurring either of these shortcomings. It preserves the flexibility to change the implementation of the upper layer without changing its API (in particular, the set of exceptions thrown by its methods).

A second reason that a throwable may have a cause is that the method that throws it must conform to a general-purpose interface that does not permit the method to throw the cause directly. For example, suppose a persistent collection conforms to the [Collection](https://developer.android.com/reference/kotlin/java/util/Collection.html#) interface, and that its persistence is implemented atop`java.io`. Suppose the internals of the`add`method can throw an [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#). The implementation can communicate the details of the`IOException`to its caller while conforming to the`Collection`interface by wrapping the`IOException`in an appropriate unchecked exception. (The specification for the persistent collection should indicate that it is capable of throwing such exceptions.)

A cause can be associated with a throwable in two ways: via a constructor that takes the cause as an argument, or via the [initCause(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable#initCause(kotlin.Throwable))method. New throwable classes that wish to allow causes to be associated with them should provide constructors that take a cause and delegate (perhaps indirectly) to one of the`Throwable`constructors that takes a cause. Because the`initCause`method is public, it allows a cause to be associated with any throwable, even a "legacy throwable" whose implementation predates the addition of the exception chaining mechanism to`Throwable`.

By convention, class`Throwable`and its subclasses have two constructors, one that takes no arguments and one that takes a`String`argument that can be used to produce a detail message. Further, those subclasses that might likely have a cause associated with them should have two more constructors, one that takes a`Throwable`(the cause), and one that takes a`String`(the detail message) and a`Throwable`(the cause).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Throwable](https://developer.android.com/reference/kotlin/java/lang/Throwable#Throwable())`()` Constructs a new throwable with`null`as its detail message. |
| [Throwable](https://developer.android.com/reference/kotlin/java/lang/Throwable#Throwable(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Constructs a new throwable with the specified detail message. |
| [Throwable](https://developer.android.com/reference/kotlin/java/lang/Throwable#Throwable(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Constructs a new throwable with the specified detail message and cause. |
| [Throwable](https://developer.android.com/reference/kotlin/java/lang/Throwable#Throwable(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Constructs a new throwable with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Throwable](https://developer.android.com/reference/kotlin/java/lang/Throwable#Throwable(kotlin.String,%20kotlin.Throwable,%20kotlin.Boolean,%20kotlin.Boolean))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`, `enableSuppression:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `writableStackTrace:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructs a new throwable with the specified detail message, cause, [suppression](https://developer.android.com/reference/kotlin/java/lang/Throwable#addSuppressed(kotlin.Throwable))enabled or disabled, and writable stack trace enabled or disabled. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addSuppressed](https://developer.android.com/reference/kotlin/java/lang/Throwable#addSuppressed(kotlin.Throwable))`(`exception:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`)` Appends the specified exception to the exceptions that were suppressed in order to deliver this exception. |
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | [fillInStackTrace](https://developer.android.com/reference/kotlin/java/lang/Throwable#fillInStackTrace())`()` Fills in the execution stack trace. |
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | [getCause](https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause())`()` Returns the cause of this throwable or`null`if the cause is nonexistent or unknown. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getLocalizedMessage](https://developer.android.com/reference/kotlin/java/lang/Throwable#getLocalizedMessage())`()` Creates a localized description of this throwable. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getMessage](https://developer.android.com/reference/kotlin/java/lang/Throwable#getMessage())`()` Returns the detail message string of this throwable. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [StackTraceElement](https://developer.android.com/reference/kotlin/java/lang/StackTraceElement)!\> | [getStackTrace](https://developer.android.com/reference/kotlin/java/lang/Throwable#getStackTrace())`()` Provides programmatic access to the stack trace information printed by [printStackTrace()](https://developer.android.com/reference/kotlin/java/lang/Throwable#printStackTrace()). |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!\> | [getSuppressed](https://developer.android.com/reference/kotlin/java/lang/Throwable#getSuppressed())`()` Returns an array containing all of the exceptions that were suppressed, typically by the`try`-with-resources statement, in order to deliver this exception. |
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | [initCause](https://developer.android.com/reference/kotlin/java/lang/Throwable#initCause(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Initializes the*cause*of this throwable to the specified value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](https://developer.android.com/reference/kotlin/java/lang/Throwable#printStackTrace())`()` Prints this throwable and its backtrace to the standard error stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](https://developer.android.com/reference/kotlin/java/lang/Throwable#printStackTrace(java.io.PrintStream))`(`s:` ` [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream.html#)`)` Prints this throwable and its backtrace to the specified print stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printStackTrace](https://developer.android.com/reference/kotlin/java/lang/Throwable#printStackTrace(java.io.PrintWriter))`(`s:` ` [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)`)` Prints this throwable and its backtrace to the specified print writer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStackTrace](https://developer.android.com/reference/kotlin/java/lang/Throwable#setStackTrace(kotlin.Array))`(`stackTrace:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [StackTraceElement](https://developer.android.com/reference/kotlin/java/lang/StackTraceElement)!>`)` Sets the stack trace elements that will be returned by [getStackTrace()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getStackTrace())and printed by [printStackTrace()](https://developer.android.com/reference/kotlin/java/lang/Throwable#printStackTrace())and related methods. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/lang/Throwable#toString())`()` Returns a short description of this throwable. |

## Public constructors

### Throwable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Throwable()
```

Constructs a new throwable with`null`as its detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](https://developer.android.com/reference/kotlin/java/lang/Throwable#initCause(kotlin.Throwable)).

The [fillInStackTrace()](https://developer.android.com/reference/kotlin/java/lang/Throwable#fillInStackTrace())method is called to initialize the stack trace data in the newly created throwable. 

### Throwable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Throwable(message: String?)
```

Constructs a new throwable with the specified detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](https://developer.android.com/reference/kotlin/java/lang/Throwable#initCause(kotlin.Throwable)).

The [fillInStackTrace()](https://developer.android.com/reference/kotlin/java/lang/Throwable#fillInStackTrace())method is called to initialize the stack trace data in the newly created throwable.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the detail message. The detail message is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getMessage())method. |

### Throwable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Throwable(
    message: String?, 
    cause: Throwable?)
```

Constructs a new throwable with the specified detail message and cause.

Note that the detail message associated with`cause`is*not*automatically incorporated in this throwable's detail message.

The [fillInStackTrace()](https://developer.android.com/reference/kotlin/java/lang/Throwable#fillInStackTrace())method is called to initialize the stack trace data in the newly created throwable.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the detail message (which is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getMessage())method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### Throwable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Throwable(cause: Throwable?)
```

Constructs a new throwable with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). This constructor is useful for throwables that are little more than wrappers for other throwables (for example, ).

The [fillInStackTrace()](https://developer.android.com/reference/kotlin/java/lang/Throwable#fillInStackTrace())method is called to initialize the stack trace data in the newly created throwable.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

## Protected constructors

### Throwable

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Throwable(
    message: String?, 
    cause: Throwable?, 
    enableSuppression: Boolean, 
    writableStackTrace: Boolean)
```

Constructs a new throwable with the specified detail message, cause, [suppression](https://developer.android.com/reference/kotlin/java/lang/Throwable#addSuppressed(kotlin.Throwable))enabled or disabled, and writable stack trace enabled or disabled. If suppression is disabled, [getSuppressed](https://developer.android.com/reference/kotlin/java/lang/Throwable#getSuppressed())for this object will return a zero-length array and calls to [addSuppressed](https://developer.android.com/reference/kotlin/java/lang/Throwable#addSuppressed(kotlin.Throwable))that would otherwise append an exception to the suppressed list will have no effect. If the writable stack trace is false, this constructor will not call [fillInStackTrace()](https://developer.android.com/reference/kotlin/java/lang/Throwable#fillInStackTrace()), a`null`will be written to the`stackTrace`field, and subsequent calls to`fillInStackTrace`and[setStackTrace(java.lang.StackTraceElement[])](https://developer.android.com/reference/kotlin/java/lang/Throwable#setStackTrace(kotlin.Array))will not set the stack trace. If the writable stack trace is false, [getStackTrace](https://developer.android.com/reference/kotlin/java/lang/Throwable#getStackTrace())will return a zero length array.

Note that the other constructors of`Throwable`treat suppression as being enabled and the stack trace as being writable. Subclasses of`Throwable`should document any conditions under which suppression is disabled and document conditions under which the stack trace is not writable. Disabling of suppression should only occur in exceptional circumstances where special requirements exist, such as a virtual machine reusing exception objects under low-memory situations. Circumstances where a given exception object is repeatedly caught and rethrown, such as to implement control flow between two sub-systems, is another situation where immutable throwable objects would be appropriate.

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the detail message. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:the cause. (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
| `enableSuppression` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether or not suppression is enabled or disabled |
| `writableStackTrace` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether or not the stack trace should be writable |

**See Also**

- [java.lang.OutOfMemoryError](https://developer.android.com/reference/kotlin/java/lang/OutOfMemoryError)
- [java.lang.NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException)
- [java.lang.ArithmeticException](https://developer.android.com/reference/kotlin/java/lang/ArithmeticException)

## Public methods

### addSuppressed

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addSuppressed(exception: Throwable): Unit
```

Appends the specified exception to the exceptions that were suppressed in order to deliver this exception. This method is thread-safe and typically called (automatically and implicitly) by the`try`-with-resources statement.

The suppression behavior is enabled*unless* disabled [via](https://developer.android.com/reference/kotlin/java/lang/Throwable#Throwable(kotlin.String,%20kotlin.Throwable,%20kotlin.Boolean,%20kotlin.Boolean)). When suppression is disabled, this method does nothing other than to validate its argument.

Note that when one exception [causes](https://developer.android.com/reference/kotlin/java/lang/Throwable#initCause(kotlin.Throwable))another exception, the first exception is usually caught and then the second exception is thrown in response. In other words, there is a causal connection between the two exceptions. In contrast, there are situations where two independent exceptions can be thrown in sibling code blocks, in particular in the`try`block of a`try`-with-resources statement and the compiler-generated`finally`block which closes the resource. In these situations, only one of the thrown exceptions can be propagated. In the`try`-with-resources statement, when there are two such exceptions, the exception originating from the`try`block is propagated and the exception from the`finally`block is added to the list of exceptions suppressed by the exception from the`try`block. As an exception unwinds the stack, it can accumulate multiple suppressed exceptions.

An exception may have suppressed exceptions while also being caused by another exception. Whether or not an exception has a cause is semantically known at the time of its creation, unlike whether or not an exception will suppress other exceptions which is typically only determined after an exception is thrown.

Note that programmer written code is also able to take advantage of calling this method in situations where there are multiple sibling exceptions and only one can be propagated.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html):the exception to be added to the list of suppressed exceptions |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`exception`is this throwable; a throwable cannot suppress itself. |
| `java.lang.NullPointerException` | if`exception`is`null` |

### fillInStackTrace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun fillInStackTrace(): Throwable
```

Fills in the execution stack trace. This method records within this`Throwable`object information about the current state of the stack frames for the current thread.

If the stack trace of this`Throwable` [writable](https://developer.android.com/reference/kotlin/java/lang/Throwable#Throwable(kotlin.String,%20kotlin.Throwable,%20kotlin.Boolean,%20kotlin.Boolean)), calling this method has no effect.

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | a reference to this`Throwable`instance. |

**See Also**

- [java.lang.Throwable#printStackTrace()](https://developer.android.com/reference/kotlin/java/lang/Throwable#printStackTrace()) 

### getCause

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCause(): Throwable?
```

Returns the cause of this throwable or`null`if the cause is nonexistent or unknown. (The cause is the throwable that caused this throwable to get thrown.)

This implementation returns the cause that was supplied via one of the constructors requiring a`Throwable`, or that was set after creation with the [initCause(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable#initCause(kotlin.Throwable))method. While it is typically unnecessary to override this method, a subclass can override it to return a cause set by some other means. This is appropriate for a "legacy chained throwable" that predates the addition of chained exceptions to`Throwable`. Note that it is*not* necessary to override any of the`PrintStackTrace`methods, all of which invoke the`getCause`method to determine the cause of a throwable.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | the cause of this throwable or`null`if the cause is nonexistent or unknown. |

### getLocalizedMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalizedMessage(): String?
```

Creates a localized description of this throwable. Subclasses may override this method in order to produce a locale-specific message. For subclasses that do not override this method, the default implementation returns the same result as`getMessage()`.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The localized description of this throwable. |

### getMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMessage(): String?
```

Returns the detail message string of this throwable.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the detail message string of this`Throwable`instance (which may be`null`). |

### getStackTrace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStackTrace(): Array<StackTraceElement!>
```

Provides programmatic access to the stack trace information printed by [printStackTrace()](https://developer.android.com/reference/kotlin/java/lang/Throwable#printStackTrace()). Returns an array of stack trace elements, each representing one stack frame. The zeroth element of the array (assuming the array's length is non-zero) represents the top of the stack, which is the last method invocation in the sequence. Typically, this is the point at which this throwable was created and thrown. The last element of the array (assuming the array's length is non-zero) represents the bottom of the stack, which is the first method invocation in the sequence.

Some virtual machines may, under some circumstances, omit one or more stack frames from the stack trace. In the extreme case, a virtual machine that has no stack trace information concerning this throwable is permitted to return a zero-length array from this method. Generally speaking, the array returned by this method will contain one element for every frame that would be printed by`printStackTrace`. Writes to the returned array do not affect future calls to this method.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [StackTraceElement](https://developer.android.com/reference/kotlin/java/lang/StackTraceElement)!> | an array of stack trace elements representing the stack trace pertaining to this throwable. |

### getSuppressed

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSuppressed(): Array<Throwable!>
```

Returns an array containing all of the exceptions that were suppressed, typically by the`try`-with-resources statement, in order to deliver this exception. If no exceptions were suppressed or [suppression is](https://developer.android.com/reference/kotlin/java/lang/Throwable#Throwable(kotlin.String,%20kotlin.Throwable,%20kotlin.Boolean,%20kotlin.Boolean)), an empty array is returned. This method is thread-safe. Writes to the returned array do not affect future calls to this method.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!> | an array containing all of the exceptions that were suppressed to deliver this exception. |

### initCause

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun initCause(cause: Throwable?): Throwable
```

Initializes the*cause*of this throwable to the specified value. (The cause is the throwable that caused this throwable to get thrown.)

This method can be called at most once. It is generally called from within the constructor, or immediately after creating the throwable. If this throwable was created with [Throwable(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable#Throwable(kotlin.Throwable))or [Throwable(java.lang.String,java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable#Throwable(kotlin.String,%20kotlin.Throwable)), this method cannot be called even once.

An example of using this method on a legacy throwable type without other support for setting the cause is: 

```kotlin
try {
      lowLevelOp();
  } catch (LowLevelException le) {
      throw (HighLevelException)
            new HighLevelException().initCause(le); // Legacy constructor
  }
  
```

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | a reference to this`Throwable`instance. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`cause`is this throwable. (A throwable cannot be its own cause.) |
| `java.lang.IllegalStateException` | if this throwable was created with [Throwable(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable#Throwable(kotlin.Throwable))or [Throwable(java.lang.String,java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable#Throwable(kotlin.String,%20kotlin.Throwable)), or this method has already been called on this throwable. |

### printStackTrace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun printStackTrace(): Unit
```

Prints this throwable and its backtrace to the standard error stream. This method prints a stack trace for this`Throwable`object on the error output stream that is the value of the field`System.err`. The first line of output contains the result of the [toString()](https://developer.android.com/reference/kotlin/java/lang/Throwable#toString())method for this object. Remaining lines represent data previously recorded by the method [fillInStackTrace()](https://developer.android.com/reference/kotlin/java/lang/Throwable#fillInStackTrace()). The format of this information depends on the implementation, but the following example may be regarded as typical: 

```kotlin
java.lang.NullPointerException
          at MyClass.mash(MyClass.java:9)
          at MyClass.crunch(MyClass.java:6)
          at MyClass.main(MyClass.java:3)
  
```
This example was produced by running the program: 

```kotlin
class MyClass {
      public static void main(String[] args) {
          crunch(null);
      }
      static void crunch(int[] a) {
          mash(a);
      }
      static void mash(int[] b) {
          System.out.println(b[0]);
      }
  }
  
```
The backtrace for a throwable with an initialized, non-null cause should generally include the backtrace for the cause. The format of this information depends on the implementation, but the following example may be regarded as typical: 

```kotlin
HighLevelException: MidLevelException: LowLevelException
          at Junk.a(Junk.java:13)
          at Junk.main(Junk.java:4)
  Caused by: MidLevelException: LowLevelException
          at Junk.c(Junk.java:23)
          at Junk.b(Junk.java:17)
          at Junk.a(Junk.java:11)
          ... 1 more
  Caused by: LowLevelException
          at Junk.e(Junk.java:30)
          at Junk.d(Junk.java:27)
          at Junk.c(Junk.java:21)
          ... 3 more
  
```
Note the presence of lines containing the characters`"..."`. These lines indicate that the remainder of the stack trace for this exception matches the indicated number of frames from the bottom of the stack trace of the exception that was caused by this exception (the "enclosing" exception). This shorthand can greatly reduce the length of the output in the common case where a wrapped exception is thrown from same method as the "causative exception" is caught. The above example was produced by running the program: 

```kotlin
public class Junk {
      public static void main(String args[]) {
          try {
              a();
          } catch(HighLevelException e) {
              e.printStackTrace();
          }
      }
      static void a() throws HighLevelException {
          try {
              b();
          } catch(MidLevelException e) {
              throw new HighLevelException(e);
          }
      }
      static void b() throws MidLevelException {
          c();
      }
      static void c() throws MidLevelException {
          try {
              d();
          } catch(LowLevelException e) {
              throw new MidLevelException(e);
          }
      }
      static void d() throws LowLevelException {
         e();
      }
      static void e() throws LowLevelException {
          throw new LowLevelException();
      }
  }
 
  class HighLevelException extends Exception {
      HighLevelException(Throwable cause) { super(cause); }
  }
 
  class MidLevelException extends Exception {
      MidLevelException(Throwable cause)  { super(cause); }
  }
 
  class LowLevelException extends Exception {
  }
  
```
As of release 7, the platform supports the notion of*suppressed exceptions* (in conjunction with the`try`-with-resources statement). Any exceptions that were suppressed in order to deliver an exception are printed out beneath the stack trace. The format of this information depends on the implementation, but the following example may be regarded as typical: 

```kotlin
Exception in thread "main" java.lang.Exception: Something happened
   at Foo.bar(Foo.java:10)
   at Foo.main(Foo.java:5)
   Suppressed: Resource$CloseFailException: Resource ID = 0
           at Resource.close(Resource.java:26)
           at Foo.bar(Foo.java:9)
           ... 1 more
  
```
Note that the "... n more" notation is used on suppressed exceptions just as it is used on causes. Unlike causes, suppressed exceptions are indented beyond their "containing exceptions."

<br />

An exception can have both a cause and one or more suppressed exceptions: 

```kotlin
Exception in thread "main" java.lang.Exception: Main block
   at Foo3.main(Foo3.java:7)
   Suppressed: Resource$CloseFailException: Resource ID = 2
           at Resource.close(Resource.java:26)
           at Foo3.main(Foo3.java:5)
   Suppressed: Resource$CloseFailException: Resource ID = 1
           at Resource.close(Resource.java:26)
           at Foo3.main(Foo3.java:5)
  Caused by: java.lang.Exception: I did it
   at Foo3.main(Foo3.java:8)
  
```
Likewise, a suppressed exception can have a cause: 

```kotlin
Exception in thread "main" java.lang.Exception: Main block
   at Foo4.main(Foo4.java:6)
   Suppressed: Resource2$CloseFailException: Resource ID = 1
           at Resource2.close(Resource2.java:20)
           at Foo4.main(Foo4.java:5)
   Caused by: java.lang.Exception: Rats, you caught me
           at Resource2$CloseFailException.<init>(Resource2.java:45)
           ... 2 more
  
```  

### printStackTrace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun printStackTrace(s: PrintStream): Unit
```

Prints this throwable and its backtrace to the specified print stream.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------|
| `s` | [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream.html#):`PrintStream`to use for output |

### printStackTrace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun printStackTrace(s: PrintWriter): Unit
```

Prints this throwable and its backtrace to the specified print writer.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------|
| `s` | [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#):`PrintWriter`to use for output |

### setStackTrace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStackTrace(stackTrace: Array<StackTraceElement!>): Unit
```

Sets the stack trace elements that will be returned by [getStackTrace()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getStackTrace())and printed by [printStackTrace()](https://developer.android.com/reference/kotlin/java/lang/Throwable#printStackTrace())and related methods. This method, which is designed for use by RPC frameworks and other advanced systems, allows the client to override the default stack trace that is either generated by [fillInStackTrace()](https://developer.android.com/reference/kotlin/java/lang/Throwable#fillInStackTrace())when a throwable is constructed or deserialized when a throwable is read from a serialization stream.

If the stack trace of this`Throwable` [writable](https://developer.android.com/reference/kotlin/java/lang/Throwable#Throwable(kotlin.String,%20kotlin.Throwable,%20kotlin.Boolean,%20kotlin.Boolean)), calling this method has no effect other than validating its argument.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stackTrace` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [StackTraceElement](https://developer.android.com/reference/kotlin/java/lang/StackTraceElement)!\>:the stack trace elements to be associated with this`Throwable`. The specified array is copied by this call; changes in the specified array after the method invocation returns will have no affect on this`Throwable`'s stack trace. |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`stackTrace`is`null`or if any of the elements of`stackTrace`are`null` |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a short description of this throwable. The result is the concatenation of:

- the [name](https://developer.android.com/reference/kotlin/java/lang/Class#getName())of the class of this object
- ": " (a colon and a space)
- the result of invoking this object's [getLocalizedMessage](https://developer.android.com/reference/kotlin/java/lang/Throwable#getLocalizedMessage())method

If`getLocalizedMessage`returns`null`, then just the class name is returned.

<br />

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this throwable. |
