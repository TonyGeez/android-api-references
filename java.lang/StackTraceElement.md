# StackTraceElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StackTraceElement

```
class StackTraceElement : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.StackTraceElement](StackTraceElement.md) |

An element in a stack trace, as returned by [java.lang.Throwable#getStackTrace()](Throwable.md)). Each element represents a single stack frame. All stack frames except for the one at the top of the stack represent a method invocation. The frame at the top of the stack represents the execution point at which the stack trace was generated. Typically, this is the point at which the throwable corresponding to the stack trace was created.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StackTraceElement](StackTraceElement.md))`(`declaringClass:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `methodName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `fileName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `lineNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a stack trace element representing the specified execution point. |

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](StackTraceElement.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Returns true if the specified object is another `StackTraceElement` instance representing the same execution point as this instance. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getClassName](StackTraceElement.md))`()` Returns the fully qualified name of the class containing the execution point represented by this stack trace element. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFileName](StackTraceElement.md))`()` Returns the name of the source file containing the execution point represented by this stack trace element. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineNumber](StackTraceElement.md))`()` Returns the line number of the source line containing the execution point represented by this stack trace element. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMethodName](StackTraceElement.md))`()` Returns the name of the method containing the execution point represented by this stack trace element. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](StackTraceElement.md))`()` Returns a hash code value for this stack trace element. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNativeMethod](StackTraceElement.md))`()` Returns true if the method containing the execution point represented by this stack trace element is a native method. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](StackTraceElement.md))`()` Returns a string representation of this stack trace element. |

## Public constructors

### StackTraceElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StackTraceElement(
    declaringClass: String!, 
    methodName: String!, 
    fileName: String!, 
    lineNumber: Int)
```

Creates a stack trace element representing the specified execution point.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `declaringClass` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the fully qualified name of the class containing the execution point represented by the stack trace element |
| `methodName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the method containing the execution point represented by the stack trace element |
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the file containing the execution point represented by the stack trace element, or `null` if this information is unavailable |
| --- | --- |
| `lineNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the line number of the source line containing the execution point represented by this stack trace element, or a negative number if this information is unavailable. A value of -2 indicates that the method containing the execution point is a native method |

| Exceptions ||
|----------------------------------|---------------------------------------------|
| `java.lang.NullPointerException` | if `declaringClass` or `methodName` is null |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Returns true if the specified object is another `StackTraceElement` instance representing the same execution point as this instance. Two stack trace elements `a` and `b` are equal if and only if: 

```kotlin
<code>equals(a.getFileName(), b.getFileName()) &amp;&amp;
      a.getLineNumber() == b.getLineNumber()) &amp;&amp;
      equals(a.getClassName(), b.getClassName()) &amp;&amp;
      equals(a.getMethodName(), b.getMethodName())
  </code>
```
where `equals` has the semantics of [Objects.equals](../java.util/Objects.md)).

<br />

| Parameters ||
|-------|----------------------------------------------------------|
| `obj` | the object to be compared with this stack trace element. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the specified object is another `StackTraceElement` instance representing the same execution point as this instance. |

### getClassName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClassName(): String!
```

Returns the fully qualified name of the class containing the execution point represented by this stack trace element.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the fully qualified name of the `Class` containing the execution point represented by this stack trace element. |

### getFileName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFileName(): String!
```

Returns the name of the source file containing the execution point represented by this stack trace element. Generally, this corresponds to the `SourceFile` attribute of the relevant `class` file (as per *The Java Virtual Machine Specification*, Section 4.7.7). In some systems, the name may refer to some source code unit other than a file, such as an entry in source repository.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the file containing the execution point represented by this stack trace element, or `null` if this information is unavailable. |

### getLineNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLineNumber(): Int
```

Returns the line number of the source line containing the execution point represented by this stack trace element. Generally, this is derived from the `LineNumberTable` attribute of the relevant `class` file (as per *The Java Virtual Machine Specification*, Section 4.7.8).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the line number of the source line containing the execution point represented by this stack trace element, or a negative number if this information is unavailable. |

### getMethodName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMethodName(): String!
```

Returns the name of the method containing the execution point represented by this stack trace element. If the execution point is contained in an instance or class initializer, this method will return the appropriate *special method name* , `<init>` or `<clinit>`, as per Section 3.9 of *The Java Virtual Machine Specification*.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the method containing the execution point represented by this stack trace element. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code value for this stack trace element.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isNativeMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isNativeMethod(): Boolean
```

Returns true if the method containing the execution point represented by this stack trace element is a native method.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if the method containing the execution point represented by this stack trace element is a native method. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of this stack trace element.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

**See Also**

- [java.lang.Throwable#printStackTrace()](Throwable.md))
