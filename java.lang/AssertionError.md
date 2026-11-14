# AssertionError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AssertionError

```
open class AssertionError : Error
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error) ||
| | | ↳ | [java.lang.AssertionError](https://developer.android.com/reference/kotlin/java/lang/AssertionError#) |
| --- | --- | --- | --- |

Thrown to indicate that an assertion has failed.

The seven one-argument public constructors provided by this class ensure that the assertion error returned by the invocation: 

```kotlin
new AssertionError(<i>expression</i>)
  
```
has as its detail message the*string conversion* of*expression* (as defined in section {@jls 5.1.11} of The Java Language Specification), regardless of the type of*expression* .

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AssertionError](https://developer.android.com/reference/kotlin/java/lang/AssertionError#AssertionError())`()` Constructs an AssertionError with no detail message. |
| [AssertionError](https://developer.android.com/reference/kotlin/java/lang/AssertionError#AssertionError(kotlin.Boolean))`(`detailMessage:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructs an AssertionError with its detail message derived from the specified`boolean`, which is converted to a string as defined in section {@jls 5. |
| [AssertionError](https://developer.android.com/reference/kotlin/java/lang/AssertionError#AssertionError(kotlin.Char))`(`detailMessage:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Constructs an AssertionError with its detail message derived from the specified`char`, which is converted to a string as defined in section {@jls 5. |
| [AssertionError](https://developer.android.com/reference/kotlin/java/lang/AssertionError#AssertionError(kotlin.Double))`(`detailMessage:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Constructs an AssertionError with its detail message derived from the specified`double`, which is converted to a string as defined in section {@jls 5. |
| [AssertionError](https://developer.android.com/reference/kotlin/java/lang/AssertionError#AssertionError(kotlin.Float))`(`detailMessage:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructs an AssertionError with its detail message derived from the specified`float`, which is converted to a string as defined in section {@jls 5. |
| [AssertionError](https://developer.android.com/reference/kotlin/java/lang/AssertionError#AssertionError(kotlin.Int))`(`detailMessage:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an AssertionError with its detail message derived from the specified`int`, which is converted to a string as defined in section {@jls 5. |
| [AssertionError](https://developer.android.com/reference/kotlin/java/lang/AssertionError#AssertionError(kotlin.Any))`(`detailMessage:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Constructs an AssertionError with its detail message derived from the specified object, which is converted to a string as defined in section {@jls 5. |
| [AssertionError](https://developer.android.com/reference/kotlin/java/lang/AssertionError#AssertionError(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new`AssertionError`with the specified detail message and cause. |
| [AssertionError](https://developer.android.com/reference/kotlin/java/lang/AssertionError#AssertionError(kotlin.Long))`(`detailMessage:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Constructs an AssertionError with its detail message derived from the specified`long`, which is converted to a string as defined in section {@jls 5. |

## Public constructors

### AssertionError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AssertionError()
```

Constructs an AssertionError with no detail message. 

### AssertionError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AssertionError(detailMessage: Boolean)
```

Constructs an AssertionError with its detail message derived from the specified`boolean`, which is converted to a string as defined in section {@jls 5.1.11} of The Java Language Specification.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------|
| `detailMessage` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):value to be used in constructing detail message |

### AssertionError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AssertionError(detailMessage: Char)
```

Constructs an AssertionError with its detail message derived from the specified`char`, which is converted to a string as defined in section {@jls 5.1.11} of The Java Language Specification.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------|
| `detailMessage` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):value to be used in constructing detail message |

### AssertionError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AssertionError(detailMessage: Double)
```

Constructs an AssertionError with its detail message derived from the specified`double`, which is converted to a string as defined in section {@jls 5.1.11} of The Java Language Specification.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------|
| `detailMessage` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):value to be used in constructing detail message |

### AssertionError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AssertionError(detailMessage: Float)
```

Constructs an AssertionError with its detail message derived from the specified`float`, which is converted to a string as defined in section {@jls 5.1.11} of The Java Language Specification.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| `detailMessage` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):value to be used in constructing detail message |

### AssertionError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AssertionError(detailMessage: Int)
```

Constructs an AssertionError with its detail message derived from the specified`int`, which is converted to a string as defined in section {@jls 5.1.11} of The Java Language Specification.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| `detailMessage` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):value to be used in constructing detail message |

### AssertionError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AssertionError(detailMessage: Any!)
```

Constructs an AssertionError with its detail message derived from the specified object, which is converted to a string as defined in section {@jls 5.1.11} of The Java Language Specification.

If the specified object is an instance of`Throwable`, it becomes the*cause*of the newly constructed assertion error.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------|
| `detailMessage` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:value to be used in constructing detail message |

**See Also**

- [java.lang.Throwable#getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause()) 

### AssertionError

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AssertionError(
    message: String!, 
    cause: Throwable!)
```

Constructs a new`AssertionError`with the specified detail message and cause.

Note that the detail message associated with`cause`is*not*automatically incorporated in this error's detail message.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message, may be`null` |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause, may be`null` |

### AssertionError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AssertionError(detailMessage: Long)
```

Constructs an AssertionError with its detail message derived from the specified`long`, which is converted to a string as defined in section {@jls 5.1.11} of The Java Language Specification.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------|
| `detailMessage` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):value to be used in constructing detail message |
