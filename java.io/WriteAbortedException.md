# WriteAbortedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WriteAbortedException

```
open class WriteAbortedException : ObjectStreamException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException) |||
| | | | ↳ | [java.io.ObjectStreamException](https://developer.android.com/reference/kotlin/java/io/ObjectStreamException) ||
| | | | | ↳ | [java.io.WriteAbortedException](https://developer.android.com/reference/kotlin/java/io/WriteAbortedException#) |

Signals that one of the ObjectStreamExceptions was thrown during a write operation. Thrown during a read operation when one of the ObjectStreamExceptions was thrown during a write operation. The exception that terminated the write can be found in the detail field. The stream is reset to it's initial state and all references to objects already deserialized are discarded.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WriteAbortedException](https://developer.android.com/reference/kotlin/java/io/WriteAbortedException#WriteAbortedException(kotlin.String,%20java.lang.Exception))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `ex:` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!`)` Constructs a WriteAbortedException with a string describing the exception and the exception causing the abort. |

| Properties ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | [cause](https://developer.android.com/reference/kotlin/java/io/WriteAbortedException#cause:kotlin.Throwable) Returns the exception that terminated the operation (the*cause*). |
| [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)! | [detail](https://developer.android.com/reference/kotlin/java/io/WriteAbortedException#detail:java.lang.Exception) Exception that was caught while writing the ObjectStream. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](https://developer.android.com/reference/kotlin/java/io/WriteAbortedException#message:kotlin.String) Produce the message and include the message from the nested exception, if there is one. |

## Public constructors

### WriteAbortedException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WriteAbortedException(
    s: String!, 
    ex: Exception!)
```

Constructs a WriteAbortedException with a string describing the exception and the exception causing the abort.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:String describing the exception. |
| `ex` | [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!:Exception causing the abort. |

## Properties

### cause

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val cause: Throwable?
```

Returns the exception that terminated the operation (the*cause*).

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | the exception that terminated the operation (the*cause*), which may be null. |

### detail

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var detail: Exception!
```

**Deprecated:** *This field predates the general-purpose exception chaining facility. The [Throwable.getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method is now the preferred means of obtaining this information.*

Exception that was caught while writing the ObjectStream. 

### message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String?
```

Produce the message and include the message from the nested exception, if there is one.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the detail message string of this`Throwable`instance (which may be`null`). |
